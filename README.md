<h1 align="center">
  <br>
  <img src="https://github.com/ethereum-proxy/XBminer/blob/main/logo.png" width="500"/>
</h1>

<h4 align="center">基于GoLang的高性能多线程ETH/ETC矿池转发中继代理工具</h4>

<p align="center">
  <a>
    <img src="https://img.shields.io/badge/Release-V1.0.0-orgin.svg" alt="travis">
  </a>
  <a>
    <img src="https://img.shields.io/badge/Last_Update-2022_07_01-orgin.svg" alt="travis">
  </a>
  <a>
    <img src="https://img.shields.io/badge/Language-GoLang-green.svg" alt="travis">
  </a>
  <a>
    <img src="https://img.shields.io/badge/License-Apache-green.svg" alt="travis">
  </a>
</p>

<p align="center">
  <a href="https://ethereumproxy.gitbook.io/huan-ying/">文档(简体中文)</a> •
  <a href="https://t.me/ethereumproxy">Telegram 讨论群组</a> •
  <a href="https://t.me/ethereumproxy">Telegram 通知频道</a>
</p>

![Screenshot](https://github.com/ethereum-proxy/Minerproxy/blob/main/web.png)

## :sparkles: 特性

* :cloud: 矿池转发：支持ETH/ETC的中继代理，支持Stratum/NiceHash/Stratum2所有协议，方便统一管理(其他币种即将更新)
* :zap: 超高性能：採用高效率的GoLang语言编写，并对多线程进行优化
* 💻 自定义抽水：支持中继平台自定义抽水比例进行抽水，并支持在不关闭代理池的情况下进行动态修改
* 📚 多种抽水算法：用户可自选各种抽水算法，防止算力出现週期函数或心跳图的情况
* 💾 安全稳定：支持TCP、SSL等方式，并对CC攻击编写一定的策略进行防护
* :gear: 独家中转加密隧道模式：私有加密协议，安全性更高、更稳定，防嗅探、防扫描，矿厂必备
* :outbox_tray: 批量转发：一个软件即可开启对多个矿池的转发，无需开启多个进程
* :card_file_box: 热修改：配置均可网页后台上热修改，无需再修改繁琐配置文件再重启
* :art: 精美后台：后台网页功能全面、折线图、统计丰富、黑暗模式、多语言支持
* :eye_speech_bubble: 完善社区支持：Telegram 群组内可帮助处理解决遇到的各类问题，欢迎提出反馈建议
* :rocket: 开箱即用：All-In-One 打包，一键搭建运行，一键配置
* :family_woman_girl_boy: 多系统支持：Windows Linux 均可支持使用，无需额外环境等
* :gear: 专业团队：拥有丰富区块链开发的工作经验，多名开发人员来自香港科技大学名校
* :link: 快速响应：可选择开启，伪装低延迟(用户内核延迟处显示的延迟为矿机到中转服务器的延迟)、清理无效提交
* 🌈 ... ...

## :hammer_and_wrench: 部署

最新软件版本请见：<a href="https://github.com/ethereum-proxy/EthereumProxy/releases">Github Release</a></br>


### Linux一键管理脚本(自带崩溃重启，但无开机自启)
```shell
#海外服务器推荐
bash <(curl -s -L https://raw.githubusercontent.com/ethereum-proxy/EthereumProxy/main/scripts/manage.sh)

#国内服务器推荐
bash <(curl -s -L https://ddl.ink/ZuBZ)


```
```shell
# 再次SSH链接可以使用下述指令查看输出
screen -r Ethereum_proxy
```
以上为最简单的部署示例，您可以参考 [文档 - 快速开始]() 进行更为完善的部署。 

# Windows-使用方法
```bash
./EthereumProxy_V1.0.1.exe
```
或双击打开 启动.bat 运行成功后访问 IP:1997 (如：127.0.0.1:1997 注意开放端口) 进行配置即可。

## :alembic: 重要提示必看

*  1.Linux系统可以再次使用脚本突破连接限制，单机稳定2000台！！！
*  2.如果要用自己的域名证书，请直接替换server.key和server.pem文件，如果看不懂这句话就不要管，凤凰不用自己的域名证书无法使用SSL模式
*  3.本地算力跟矿池算力差距5%以内是正常情况，导致这个差额的因素有：
   挖矿软件手续费：0.65%-2%
   网络传输损失：2%-3%
   挖矿任务切换损失：0.5%-1%
   超频过度：＞1%
   如果差距过大，首先确认机器是否稳定跑满24小时，如果没跑满一天，先继续观察，稳定跑满一天后再看矿池的24小时平均算力，一般是接近矿机本地算力的；
如果已经跑满24小时，差距仍然大，通常都是超频过度


## :gear:  版本更新日志
```shell
                   
2022/07/01 v1.0.0  - 新增WEB暗黑模式。
                   - 纯转发不抽水，无开发费。
                   - 端口运行状态时可修改抽水用户。
                   - 支持本地加密客户端 MinerSec。
                   - 每端口最多可添加5个抽水账户。
                   - 提升稳定性，修复已知问题。
                   - 提升专业芯片机连接稳定性。
                   - 修复web控制台页面显示问题/提升矿机连接稳定性。
                   - 修复bug，提升内存使用效率。
                   - 优化抽水逻辑，提高逻辑切换性能。
```

## :family_woman_girl_boy: 联系我们

- Q Q 群: [暂无]()

- 电报组: [Minerproxy 交流](https://t.me/Minerproxy)
## :scroll: 开发抽水
* 纯转发模式不抽水，开启抽水转发模式则恒定0.3%
