# 前后端数据加密传输 RSA非对称加密

#### 任务需求
要求登陆时将密码加密之后再进行传输到后端

#### 加密方式
RSA非对称加密

#### 实现
公钥加密，私钥解密

#### 研究进度
javascript与java端皆已实现

#### 个人方案
定时器，每天凌晨四五点跑，更换公钥私钥。
前端页面进入登录页，则请求后端获取公钥，当用户输入完登录表单点击提交时，将公钥与密码进行加密后传输。
如果后端解密失败，则返回指定状态码给前端，前端拿到此状态码，则再次请求后端，重新获取公钥。

#### 目录文件讲解
java为服务端代码

    Encrypt.java是一个controller控制器 演示了使用公钥将字符串进行加密 使用私钥将密文进行解密 
    encrypt目录下的RSACoder.java文件里有一个main方法 此方法演示了生成公钥私钥
html为客户端代码

    01.html演示了使用公钥将字符串进行加密