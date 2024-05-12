# Pandora Helper
![Static Badge](https://img.shields.io/badge/Next-8A2BE2?label=Pandora)
![Docker Pulls](https://img.shields.io/docker/pulls/q11391/pandora-next-helper?color=gold)
![Static Badge](https://img.shields.io/badge/%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9-green?label=doc)  
## 简单介绍
* **使用Web页面管理你Pandora的所有Token！**
* **你无需了解各种Token如何获取，Helper帮你处理了这一切！**
* 自动使用`Refresh Token`刷新`Access Token`，无需手动操作！
* 自动使用`Access Token`获取`Share Token`，无需手动操作！
* 管理账号下的所有`Share Token`。定时刷新、定时重置限额、吊销指定`Share Token`。

## 手动部署

* 在[Releases](https://github.com/nianhua99/PandoraHelper/releases)中下载对应操作系统和架构的包。
* 解压后修改同目录中的`config.json`至你需要的参数。
* 你必须设置一个8位以上的**admin_password**，它是你后台管理的登录密码！
* 各种Linux/Unix系统使用`./PandoraHelper`启动即可。
* Windows系统双击`PandoraHelper.exe`即可，当然需要在cmd中启动。

## Docker部署
待补充

## 配置文件
* **admin_password**：后台管理登录密码，必须设置。
* 有关Pandora.domain下的设置, 如果你反代了`new.oaifree.com`则需要修改为你反代后的域名。
* **title**：登录页的标题。

## 使用说明
* 管理员登录：访问`/admin`页面，输入`admin_password`即可登录。
* 普通用户登录：访问`首页`或`/login`页面，输入`Unique Name`和`密码`即可登录。
### 账号管理
* **账号管理**：在`账号管理`中可以查看所有账号的`Refresh Token`、`Access Token`、`Email`。
* **刷新Token**：在`账号管理`中点击`刷新`可以刷新`Access Token`。**只有你填入了`Refresh Token`才能使用此功能**。程序会在每日凌晨自动刷新。
* **添加账号**：在`账号管理`中点击`新建`，输入`Refresh Token`或`Access Token`，以及`Email`点击`保存`。请注意，这里的`密码`没有实际作用。
* **用量统计**：统计本账号下各个`Share Token`的用量情况。当前版本暂不可用。
* ![1.png](imgs/1.png)
### 生成共享账号
在`账号管理`中可以生成`Share Token`。点击`共享`列的 + 号，输入`Email`和`限额`等信息。点击`保存`即可生成`Share Token`。
- Unique Name / 密码: 你的伙伴将在本系统的 /login 页面使用Unique Name和这个密码登录。
- 有效期：到期后共享账号将被自动删除。
- 站点限制：共享账号只能在这些站点使用。
- GPT3.5/GPT4次数：这是共享账号的GPT3.5/GPT4次数限制（所有时间内）。
- **每天重置限额**：勾选后，每天凌晨将重置限额。这样你可以限制这个共享账号每天的使用次数。
- 显示用户信息：勾选后，共享账号会看到主账号的Email。
- 会话隔离：建议开启
- 临时聊天：开启后共享账号不会留下聊天记录。
![img_1.png](imgs/img_1.png)
### 分享管理
* **分享管理**：在`分享管理`中可以查看所有`Share Token`的各种信息。你可以在这里直接使用`Share Token`发起对话。

### 分享登录
本系统使用原生的Pandora登录页面，你可以在`/login`页面使用`Unique Name`和`密码`登录。
![img_2.png](imgs/img_2.png)
## 写在最后
- 特别鸣谢: [LinuxDo](https://linux.do/)
- 本项目前端基于 [Slash-Admin](https://github.com/d3george/slash-admin)
## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=nianhua99/PandoraNext-Helper&type=Date)](https://star-history.com/#nianhua99/PandoraNext-Helper&Date)
