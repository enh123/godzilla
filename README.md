Godzilla 二开优化说明

本版本基于 Godzilla 进行二次开发与功能优化，主要优化内容如下：



1.移除回连 Gitee 校验逻辑

2.修复 random useragent 选项被自定义 User-Agent 覆盖的问题

3.去除 Host请求头不在请求包第二行的特征

4.去除Cookie末尾分号的特征

5.简单修改了 payload.dll，使其能够绕过 Windows Defender（Win11 以下系统）

由于修改了 payload.dll 内部类名，生成的 Webshell 中：

CreateInstance("LY")

需改为：

CreateInstance("MAIN")


6.修改了 BadPotato.dll 和 SweetPotato.dll 使其能够绕过wdf 正常加载并执行

7.对webshell进行了简单免杀并添加随机的返回流量


