---
title: 外置登录指南
---
# 外置登录指南

> **SPCraftMC 的外置登录由 红石皮肤站 以及 StarSkin 提供，红石皮肤站的配置文档如下，StarSkin 的配置请移步到 <a href="https://docs.star-skin.cn">StarSkin Docs</a>**

## 一. 通用步骤
### 1. 登录<a href="https://mcskin.cn/"> 红石皮肤站</a>，地址为 https://mcskin.cn，注册并登录皮肤站，完成邮箱验证，否则无法正常使用相关功能。
![登录页面](https://pic-up.star-skin.cn/i/2023/06/28/951959f1-1d7c-c383-0196-427f1582ba13.png)

![登录页面](https://pic-up.star-skin.cn/i/2023/06/28/f8259419-9c78-db8c-27b4-b1107bdc473d.png
)

> **便于账号找回，一定要使用真实的邮箱。且注册后需要邮箱验证！**

### 2. 所需要的东西
①Yggdrasil API 认证服务器地址：https://mcskin.cn/api/yggdrasil <br>
②可以使用**外置登录**的Minecraft启动器。例如：HMCL，BakaXL，PCL2，以及其他的。

---

## 二. 配置启动器
### 1. HMCL（测试版-3.5.4.234）
法一：直接拖动皮肤站仪表盘页面中，“将此按钮拖动至启动器”字样的按钮，移动到HMCL启动器中，将会自动弹出登录页面，完成添加即可。<br>

法二: 点击账户，左下角“添加认证服务器”，输入https://mcskin.cn/api/yggdrasil，按照指示添加账户即可。

![启动器登录页面](https://pic-up.star-skin.cn/i/2023/06/28/4957b004-3aa7-8f6e-f9f7-0151d4ecbac0.png)

### 2. PCL2
法一：直接拖动皮肤站仪表盘页面中，“将此按钮拖动至启动器”字样的按钮，移动到PCL2启动器中，将会自动弹出登录页面，完成添加即可。<br>

法二: 选择游戏版本，依次点击“版本设置”，“设置”，选择登陆方式为“第三方登录Authlib Injector”，输入认证服务器：https://mcskin.cn/api/yggdrasil ，注册链接：https://mcskin.cn/auth/register ，其他选填。返回启动器主页，登录账号即可。

![启动器登录页面](https://pic-up.star-skin.cn/i/2023/06/28/c06628d0-b3d6-1953-8033-30a61f4bdd60.png)

### 3. BakaXL
进入“账户与档案”，“新增档案”，游戏模式选择“Authlib Injector”。验证服务器填写https://mcskin.cn/api/yggdrasil ,继续填写账户和密码，验证完毕即可。

![启动器登录页面](https://pic-up.star-skin.cn/i/2023/06/28/38f773d4-e7c1-0d63-608c-e57e88a48721.png)

### 4. 其他启动器
其他启动器的设置请自行查看相关文档，正确配置。

---

## 三.常见问题
### Q1:皮肤站无法登录
请检查您的网络情况，若正常，可能是皮肤站的服务器问题，可以添加他们的Q群咨询
### Q2:启动器无法正常登录账号
方法同上
### Q3:无法接受到邮箱验证
再三检查垃圾邮箱是否有，若真的无法收到，添加他们的Q群咨询。其次建议使用126邮箱。不要问可不可不验证，不行！！！！
### Q4：登录服务器提示“验证服务器”的字样
检查网络环境，可以尝试更换网络或者启动器，又或稍等片刻。切记：一定是**红石皮肤站**，别搞了半天是Little Skin.