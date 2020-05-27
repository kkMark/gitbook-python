# 第二课 Linux远程管理命令

## 关机命令

| 关机/启动命令 |  |
| :--- | :--- |
| shutdown \[参数\] \[时间\] | 关机，不设置时间会在一分钟后自动关机 |
| 参数说明 | ===============  分隔号 =============== |
| -r | 重新启动 |
| -c | 取消关闭计算机 |
| 时间 | ===============  分隔号 =============== |
| now | 现在 |
| +分钟（如+10） | 多少分钟后 |
| 20:00 | 设置固定时间后 |

## 查看、配置网卡信息命令

| 查看、配置网卡信息命令 |  |
| :--- | :--- |
| ifconfig | 查看/配置网卡信息 |
| ping | 检测IP是否连接成功 |



## SSH（Secure Shell）

* SSH是Linux中非常重要的工具，通过SSH客户端访问到SSH服务器的远程机器上
* 数据传输数据进行加密，可以防止信息泄漏。并且数据传输是压缩的，可以提供传输的速度（重点）
* 在Mac/Ubuntu上，默认会安装`SSH服务器/SSH客户端`的软件。在win上需要安装 [PuTTY](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.73-installer.msi) 或者 [XShell](https://www.xshellcn.com/)
* 如果没有存在SSH服务，请输入 `sudo apt-get install ssh` 命令进行安装。之后在通过 `sudo service ssh start` 开启

```text
ssh [-p] user@remote
```

| ssh参数说明 |  |
| :--- | :--- |
| -p | 监听的端口\(默认22\) |
| user | 用户 |
| remote | 远程地址\(Ip｜用户｜别名\) |

## SCP （Secure Copy）

* 用于远程拷贝文件
* win需要使用FTP服务来传输文件，FTP的端口号是21而不是22。Win下可使用 `FileZilla`

```text
// 复制文件到ubuntu上面去
ssh [-P][-r] localFilename user@remote:remoteFileName
```

```text
// 复制文件到本地来
ssh [-P][-r] user@remote:remoteFileName localFilename
```

## SSH高级

```text
注：有关SSH配置信息都保存在 home 目录下的 .ssh 目录下
```

1. 免密码登陆
   * 执行 `ssh-keygen` 生成SSH钥匙
   * 执行 `ssh-copy-id -p user@remote` 上传到远程服务器上即可
2. 配置别名

   * 在 .ssh 目录下，创建一个config文件，然后输入以下内容

   ```text
   Host 别名

       HostName ip地址
       User 用户名
       Port 端口号
   ```

