---
title: "用户指南"
description: manual
draft: false
---


# 防火墙 

  通过策略配置，防火墙能极大地提高一个内部网络或主机的安全性，并过滤不安全的服务，从而降低内部网络或主机的风险。


## 创建

为了加强位于基础网络 vxnet-0 中的主机或路由器的安全性，可以在主机或路由器之前放置一个防火墙(Security Group)。QingCloud 系统为每个用户提供了一个缺省防火墙(ID 之后带有星标)，默认打开22端口。当然，您也可以创建更多的防火墙。初始状态下，每个防火墙都不包含任何规则，即，任何端口都是封闭的，您需要建立规则以打开相应的端口。另外，您可以借助 "IP/端口集合" 功能把具有相同特征的一组 IP 或者一组端口设置成为 "IP/端口集合"，并且在防火墙规则中进行添加，实现批量管理功能。

**第一步：创建防火墙**

点击 **安全** 中的 **防火墙** 进入如下界面

[![](../../../_images/create_sg_1.png)](../../../_images/create_sg_1.png)

> 注解：QingCloud 系统为每个用户提供了一个缺省防火墙(ID 之后带有星标)，默认打开22端口。也可以创建更多的防火墙

点击 **创建** 跳出如下界面

[![](../../../_images/create_sg_2.png)](../../../_images/create_sg_2.png)

在名称框里输入创建的防火墙名称，点击 **提交** ，进入如下界面

[![](../../../_images/create_sg_3.png)](../../../_images/create_sg_3.png)

左侧操作日志记录了防火墙ID、防火墙名称、标签、描述、资源以及创建时间。

选择防火墙点击 **更多操作** ，或右击防火墙条目，可进行应用防火墙规则、标签绑定/解绑、修改、复制以及添加到资源组的操作。

**第二步：配置服务**

**创建防火墙策略**

点击 **创建** ，跳出如下界面：

[![](../../../_images/create_sg_4.png)](../../../_images/create_sg_4.png)

填写规则名称、优先级(数字越小优先级越高，最多可添加100条规则)，选择方向、行为(支持)、协议(支持多协议设置)，填写起始端口(可点击右侧标志，选择IP/端口集合)、结束端口、源IP(不填表示所有IP地址，可点击右侧标志，选择IP/端口集合)。支持快捷方式，快速配置ping、ssh、http等规则。

配置上行、下行规则，点击 **应用修改** ，规则生效，界面如下

[![](../../../_images/create_sg_5.png)](../../../_images/create_sg_5.png)

点击每条规则的最右侧 **操作** 栏，可以禁止或启用该条规则。右键点击每条规则，跳出如下界面

[![](../../../_images/create_sg_6.png)](../../../_images/create_sg_6.png)

支持修改和删除该条规则。

**创建防火墙策略备份**

点击页面上侧的 **备份** 按钮，进入如下界面

[![](../../../_images/create_sg_7.png)](../../../_images/create_sg_7.png)

点击 **创建备份** ，跳出如下界面

[![](../../../_images/create_sg_8.png)](../../../_images/create_sg_8.png)

填写备份名称，点击 **提交**，进入如下界面

[![](../../../_images/create_sg_9.png)](../../../_images/create_sg_9.png)

选择备份策略再点击上侧 **回滚** 或鼠标右击备份策略选择 **回滚**，亦或鼠标左击备份策略，跳出如下界面

[![](../../../_images/create_sg_10.png)](../../../_images/create_sg_10.png)

点击页面中左侧 **开关** 按钮，“开”表示与当前防火墙对比，界面如下

[![](../../../_images/create_sg_11.png)](../../../_images/create_sg_11.png)

> 注解：页面下侧表示的不同颜色代表着不同的规则

“关”表示备份点规则，界面如下：

[![](../../../_images/create_sg_12.png)](../../../_images/create_sg_12.png)

点击 **回滚** ，跳出如下界面

[![](../../../_images/create_sg_13.png)](../../../_images/create_sg_13.png)

点击 **确认** ，备份规则会自动覆盖当前规则。

## FAQ