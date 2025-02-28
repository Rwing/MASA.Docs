## 介绍

基于[Mapster](https://github.com/MapsterMapper/Mapster)的一个对象到对象的映射器，在原来的基础上增加自动获取并使用最佳构造函数映射，支持嵌套映射，减轻映射的工作量。

## 入门

1. 安装`Masa.Contrib.Data.Mapping.Mapster`

``` powershell
dotnet add package Masa.Contrib.Data.Mapping.Mapster
```

2. 修改`Program.cs`，注册`Mapster`的映射器

```csharp
builder.Services.AddMapster();
```

3. 映射对象

```csharp
public void Main()
{
    var request = new
    {
        Name = "Teach you to learn Dapr ……",
        OrderItem = new OrderItem("Teach you to learn Dapr hand by hand", 49.9m)
    };
    IMapper mapper;// 通过DI获取
    var order = _mapper.Map<Order>(request);// 将request映射到新的对象
    Assert.IsNotNull(order);
    Assert.AreEqual(request.Name, order.Name);
    Assert.AreEqual(1, order.OrderItems.Count);
    Assert.AreEqual(49.9m, order.TotalPrice);
}
```

映射类`Order`:

``` Order.cs
public class Order
{
    public string Name { get; set; }
    public decimal TotalPrice { get; set; }
    public List<OrderItem> OrderItems { get; set; }

    public Order(string name)
    {
        Name = name;
    }
    
    public Order(string name, OrderItem orderItem) : this(name)
    {
        OrderItems = new List<OrderItem> { orderItem };
        TotalPrice = OrderItems.Sum(item => item.Price * item.Number);
    }
}

public class OrderItem
{
    public string Name { get; set; }
    public decimal Price { get; set; }
    public int Number { get; set; }
    
    public OrderItem(string name, decimal price) : this(name, price, 1)
    {
    }

    public OrderItem(string name, decimal price, int number)
    {
        Name = name;
        Price = price;
        Number = number;
    }
}
```

## 映射规则

* 目标对象没有构造函数时：使用空构造函数，映射到字段和属性。

* 目标对象存在多个构造函数：获取最佳构造函数映射

    > 最佳构造函数: 目标对象构造函数参数数量从大到小降序查找，参数名称一致（不区分大小写）且参数类型与源对象属性一致