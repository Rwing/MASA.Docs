# 常见问题

### Q：MASA.DCC是什么？

A：[MASA.DCC产品介绍](stack/dcc/introduce)

### Q：我要怎么接入MASA.DCC?

A：请参考[MASA.DCC使用指南](stack/dcc/get-started)和[SDK接入示例](stack/dcc/sdk-instance)

### Q：团队页面为什么没有项目数据？

A：
1. 确保登录的账号有团队
2. 确保该项目已经分配给该团队
3. 如果团队不正确请在右上角切换对应的团队

### Q：修改完配置信息客户端为什么获取不到最新的数据？

A：在DCC中修改完配置是需要发布的，否则不会影响客户端正在使用的配置。

### Q：配置文件开启加密后为什么看不到配置内容了？

A：被加密的配置会对配置内容进行AES加密，而且只有管理员才能在系统中看到配置内容。通过SDK获取加密的配置时也需要先配置密钥才能对配置内容进行解密。

### Q：业务配置怎么创建?

A：业务配置无需你手动创建，它在你点击进入项目详情的时候会为你初始化一份业务配置，每个项目只有一份业务配置，业务配置所在的集群环境就是项目的所有集群环境，你可以自己去修改业务配置的名称。

### Q：公共配置怎么创建？

A：公共配置和业务配置一样，系统会为你初始化一份公共配置。公共配置所在的集群环境是MASA.PM创建的所有的集群环境。

### Q：撤销配置后配置内容为什么没有发生变化？

A：撤销配置只会撤销没有发布的配置，已经发布的配置不会被撤销，已经发布配置只能通过回滚才能回到上个版本。

### Q：回滚完为什么配置内容没有发生变化，但是会出现【已修改】的标签？

A：回滚是不影响当前正在修改的配置之的，当前的配置相较于上一个版本的配置是存在修改的所以会出现【已修改】的标签，如果想在界面上也看到上个版本的内容，回滚后在进行撤销即可。

我们会持续收集更多的 FAQ。