## 一、什么是Token

	token是用户身份的验证方式，我们通常叫它：令牌。
	最简单的token组成:uid(用户唯一的身份标识)、time(当前时间的时间戳)、sign(签名，由token的前几位+盐以哈希算法压缩成一定长的十六进制字符串，可以防止恶意第三方拼接token请求服务器)。还可以把不变的参数也放进token，避免多次查库。

## 二、Token验证流程

	1.客户端使用用户名跟密码请求登录
	2.服务端收到请求，去验证用户名与密码
	3.验证成功后，服务端会签发一个 Token，再把这个 Token 发送给客户端
	4.客户端收到 Token 以后可以把它存储起来，比如放在 Cookie 里或者 Local Storage 里
	5.客户端每次向服务端请求资源的时候需要带着服务端签发的 Token
	6.服务端收到请求，然后去验证客户端请求里面带着的 Token，如果验证成功，就向客户端返回请求的数据
	
## 三、简易时序图（基于IM）

![](https://github.com/ToyoBai/Network-programming/blob/master/IM/%E7%BD%91%E7%BB%9C%E7%BC%96%E7%A8%8B%E7%9B%B8%E5%85%B3%E7%9F%A5%E8%AF%86/Img/Token.png?raw=true) 

