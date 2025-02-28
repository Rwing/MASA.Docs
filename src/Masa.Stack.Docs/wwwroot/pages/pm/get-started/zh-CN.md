# 使用指南

1. 初始化

   1. 在使用 PM 时，第一步需要您初始化系统，默认会为您创建三个环境（Development、Staging、Production）一个集群（Default）并会初始化MASA.Stack的一些项目和应用。

2. 创建环境

   1. 点击左侧“新增环境“

      ![](http://cdn.masastack.com/stack/doc/pm/overview.jpg)

   2. 输入环境信息

      - 环境名称
      - 关联集群（多选）
      - 环境描述

      ![](http://cdn.masastack.com/stack/doc/pm/environment.jpg)

3. 创建集群

   1. 点击右上角的”新增集群“

   2. 输入集群信息

      - 集群名称
      - 关联环境（多选）
      - 集群描述

      ![](http://cdn.masastack.com/stack/doc/pm/cluster.jpg)

4. 创建项目

   1. 点击底部”新增项目“

   2. 输入项目信息

      - 项目名称
      - 所属项目团队（为项目分配团队，只有该团队的成员才能看到）
      - ID标识（唯一）
      - 项目类型
      - 环境/集群（多选）
      - 项目描述

      ![](http://cdn.masastack.com/stack/doc/pm/project.jpg)

5. 创建应用

   1. 站看某个项目点击”新增应用“
   2. 输入应用信息
      - 应用名称
      - 应用类型（Service、UI、Job）
      - 环境/集群（项目的中的环境/集群），多选
      
      ![](http://cdn.masastack.com/stack/doc/pm/app.jpg)
