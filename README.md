# 国外服务器vps注册创建教程


很多时候我们需要使用 Google 查询第一手资料，比如官方的文档网站，或者一些文献，虽然市面上有一些 VPN 工具，但是它们不是很稳定，并且不是很安全，比较好的方式就是自己搭建一个属于自己的 VPN 服务，自己掌控。

## 优惠购买云服务器vultr

在搭建之前需要一台境外的云服务器，而 [vultr](https://www.vultr.com/?ref=8944093-8H) 服务商比较稳定，安全，相当于境内的阿里云。

值得说的一点是， [vultr](https://www.vultr.com/?ref=8944093-8H) 给新用户的福利相当给力，充值 10 美元就可以获取 100 美元，你可以点击 [vultr 专属赠送新用户 100 美元](https://www.vultr.com/?ref=8944093-8H) 进去抢先注册。

右上角有注册按钮，你也可以切换成中文界面：

<img width="1446" alt="vpn搭建教程" src="https://user-images.githubusercontent.com/84239400/119019442-be0cc500-b98c-11eb-895b-0d6300dce93d.png">

![](https://user-images.githubusercontent.com/84239400/119019760-0d52f580-b98d-11eb-9837-aba0990f1dfb.png)

接着使用邮箱和密码就可以注册了。

![](https://user-images.githubusercontent.com/84239400/119020042-4ee3a080-b98d-11eb-8341-bfc30f4b103c.png)

进去之后你可以看到这个页面，说明你已经通过 [vultr 专属优惠链接](https://www.vultr.com/?ref=8872890-6G) 获得了 100 美元赠送的资格：

![](https://user-images.githubusercontent.com/84239400/119020173-733f7d00-b98d-11eb-8ecc-a1afeb556fe6.png)

现在你只要选择支付宝充值 10 美元以上，就可以获得额外赠送的 100 美元。

![](https://user-images.githubusercontent.com/84239400/119020280-966a2c80-b98d-11eb-9113-8f5f0b75c5ea.png)

接下来就可以在这个平台选购云服务器了。

点击页面左边菜单栏的 「Products」进入服务器选购页面。

### Choose Server 选择服务器

选择 Cloud Compute 即可：

![](https://user-images.githubusercontent.com/84239400/119020373-af72dd80-b98d-11eb-8478-02d735b82709.png)

### Server Location

服务器的位置，可以选择美国地区，比如纽约：

![](https://user-images.githubusercontent.com/84239400/119020467-cadde880-b98d-11eb-8927-d3d837bbc20c.png)

选择服务器配置，看个人情况。$5适合个人搭梯子。

### Server Type

服务器类型，CentOS 8 x64 系统：

<img width="1297" alt="vpn搭建教程" src="https://user-images.githubusercontent.com/84239400/119020720-198b8280-b98e-11eb-9df3-19bf5a187a1e.png">

### Server Size

内存，个人使用10G完全够用，这里选择3.5美元一个月，性价比高，注意不要选择IPv6 ONLY的，要不然无法搭建使用。

<img width="1240" alt="vpn搭建教程" src="https://user-images.githubusercontent.com/84239400/119020895-4a6bb780-b98e-11eb-9ac8-3cdd4f4397de.png">

选择完了之后，下面的其它东西都不需要填，直接点击右下角 Deploy Now 就可以了：

![](https://user-images.githubusercontent.com/84239400/119020981-68391c80-b98e-11eb-9f16-00c75de88eeb.png)

这时候你就拥有了自己的一台云服务器了：

<img width="1261" alt="VPN搭建教程" src="https://user-images.githubusercontent.com/84239400/119021075-86068180-b98e-11eb-82a9-71edb9934f23.png">


点击 Cloud Instance ，可以看到你服务器的 IP 地址和密码：

<img width="1308" alt="vpn搭建教程" src="https://user-images.githubusercontent.com/84239400/119021183-a20a2300-b98e-11eb-8ff4-7f18d3e3bb80.png">


## 连接到你的服务器

### windows 系统连接到 vultr 服务器

windows 可以下载[PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)工具。

打开之后选择 session，将你在 vultr 网上得到的服务器 ip 复制过来，输入到这里：

![](https://user-images.githubusercontent.com/84239400/119023900-037fc100-b992-11eb-85ea-525a61a69657.png)

Port 默认 22，Connection Type 选择 SSH，接着点击 Open，连接进去之后输入你云服务器的密码。

### Linux 和 MacOS 连接到 vultr 服务器

Linux 和 MacOS 可以打开终端，使用如下命令连接：

```
ssh root@xx.xx.xxx.xx
```

`xx.xx.xxx.xx`就是你的服务器上的 IP 地址。

连接进去之后输入 yes 后按回车，接着输入你云服务器的密码，即可使用云服务器。

<img width="772" alt="vpn搭建教程" src="https://user-images.githubusercontent.com/84239400/119024049-32963280-b992-11eb-8c05-db6df1f7fbfa.png">

注意！有小概率情况是，如果你选日本机房，可能被自动分配到被墙的IP。如何判别呢？打开 http://ping.chinaz.com 输入你的服务器IP测试。如果Ping不通，说明IP被墙了。立即删掉这台服务器，重新创建一个。

Vultr全球机房测速地址
东京（日本）           https://hnd-jp-ping.vultr.com/vultr.com.1000MB.bin
洛杉矶（美国）         https://lax-ca-us-ping.vultr.com/vultr.com.1000MB.bin
西雅图（美国）         https://wa-us-ping.vultr.com/vultr.com.1000MB.bin
硅谷（美国）           https://sjo-ca-us-ping.vultr.com/vultr.com.1000MB.bin
法兰克福（德国）       https://fra-de-ping.vultr.com/vultr.com.1000MB.bin
巴黎（法国）           https://par-fr-ping.vultr.com/vultr.com.1000MB.bin
阿姆斯特丹（荷兰）     https://ams-nl-ping.vultr.com/vultr.com.1000MB.bin
伦敦（英国）           https://lon-gb-ping.vultr.com/vultr.com.1000MB.bin
纽约（美国）           https://nj-us-ping.vultr.com/vultr.com.1000MB.bin
芝加哥（美国）         https://il-us-ping.vultr.com/vultr.com.1000MB.bin
亚特兰大（美国）       https://ga-us-ping.vultr.com/vultr.com.1000MB.bin
迈阿密（美国）         https://fl-us-ping.vultr.com/vultr.com.1000MB.bin
达拉斯（美国）         https://tx-us-ping.vultr.com/vultr.com.1000MB.bin
新加坡                 https://sgp-ping.vultr.com/vultr.com.1000MB.bin
悉尼（澳大利亚）       https://syd-au-ping.vultr.com/vultr.com.1000MB.bin

# 延伸阅读
购买vps后，您就可以使用[ssr一键安装包](https://github.com/mku228/vpn-ss-ssr)，轻松科学上网。
