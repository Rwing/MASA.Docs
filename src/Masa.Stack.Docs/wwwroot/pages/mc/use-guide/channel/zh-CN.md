---
title: 使用指南-渠道管理
date: 2022/12/09 11:46
---

渠道用于消息推送通道的账号配置,支持短信、邮箱、站内信、app等渠道类型

### 列表
渠道列表以卡片形式展现，支持糊搜索、分页等功能
![channels](http://cdn.masastack.com/stack/doc/mc/channels.png)

### 新增渠道

1. 选择渠道类型
   
   ![channel-add-type](http://cdn.masastack.com/stack/doc/mc/channel-add-type.png)

2. 渠道配置信息
   - 渠道ID用于调用sdk发送消息的参数“ChannelCode”

   1. 短信渠道配置
      - 目前短信发送使用阿里云，AccessKeyId和AccessKeySecret请填写对应阿里云的参数
      - 短信渠道创建后，会同步阿里云的短信模板到本地短信模板池子，创建短信模板时可以直接选择

      ![channel-add-sms](http://cdn.masastack.com/stack/doc/mc/channel-add-sms.png)

   1. 邮箱渠道配置

      ![channel-add-email](http://cdn.masastack.com/stack/doc/mc/channel-add-email.png)

   3. 站内信渠道配置

      ![channel-add-websiteMessage](http://cdn.masastack.com/stack/doc/mc/channel-add-websiteMessage.png)