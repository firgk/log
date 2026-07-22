## giffgaff apply and use




## 关于 giffgaff 的一些信息 

https://github.com/firgk/giffgaff


## 步骤

一台安卓手机，请先用 EasyEUICC 检测是否支持小白卡
一张小白卡（电商约 20 元，比如：某宝480k 22 元）可写入 esim 的卡片
一张国内单标 Visa / 万事达信用卡，卡上只标记 VISA 或 MasterCard ，无 银联 标记

1. giffgaff 创建账户

2. giffgaff 自己打补丁，或者是 用 魔改版 giffgaff（不安全），从而使这个软件可以检测到你后来插入的 esim

  giffgaff 自己打补丁
    使用 2026年5月01日 之前的 giffgaff 版本
    shizuku 配置好调试权限
    LSPatch 连接 shizuku
    安装 HOOKUICC 软件，打开之后选择第一个 ***hook*** 开关，其他不动
    LSPatch 管理-》模块，验证下  HOOKUICC 是否存在
    LSPatch 右下角加号，之后选择生成 修补后 apk 的文件夹， 之后再次加号，选择 giffgaff apk，之后 修补就可以了，修补完之后安装。长按 管理-》应用， 再次选一下 HOOKUICC
    之后正常 
    2026年7月22日 有时效性

3. giffgaff 手机端 购买 虚拟 esim
```
  打开`giffgaff APP`，登陆，
  1. 然后选择`eSIM`，
  2.  选择`choose your plan`，
  3.  选择`I don't want a plan`，
  4.  然后就是充值页面，最少充值`10英镑`，加上赠送的`5英镑`(不会立即到账)总共是`15英镑`,。
  5.  选择`add a payment method`
  6.  选择 `Card` （不要通过第三方去购买充值券）
  7.  然后要填写信息，不用写真实信息。地址信息可以在网上查找国外地址生成器自动生成。
  8.  然后就是要填写信用卡信息。包括 卡号 有效期 安全码 持卡人名字（全拼大写）。这些信息VISA卡上都有。照写就行。
  9.  如果出现按钮`Continue to install eSIM`，就代表成功了。
  10. 点击`Continue to install eSIM`，会给出一串字符。这串自负是不能直接在`EasyEUICC APP`中使用的。先保存起来。
```
4. EasyEUICC 写入
```
  1. 使用二维码生成工具，将这串字符粘贴到输入框，然后在前面加上`LPA:`（注意:是英文符号）。`[注意最后的字符串是这样的 LPA:1$****************这是马赛克*****************]`点击“`下载图片`”，将图片保存好。
  2. 打开`giffgaff APP`，点击**+**号，选择使用二维码添加，选择上一步保存的二维码。 等待写卡成功。
  3. 此时这张`小白卡`中已经写入`eSIM`信息。**可以在任何手机上使用了**。
  4. **注意** iOS手机关闭iMessage 和 Facetime ，国内安卓手机关闭网络短信。
```
  

refer:
  https://github.com/zzmy1917-svg/giffgaff-eSIM
  



英国地址生成器
https://www.meiguodizhi.com/uk-address

将文本转换为二维码
https://toolkit.xuehuayu.cn/dev/qrcode
