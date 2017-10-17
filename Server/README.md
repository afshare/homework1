# 大作业-服务器综述


服务器采用了SpringMVC + Tomcat + MySQL 的形式。  

接口采用Url的形式，[接口文档点击查看]()  

服务器分层如下：  

![代码分层](https://github.com/afshare/homework1/blob/master/otherFiles/server-1.png?raw=true)  

1. __Android层：__ App应用层，需要调用服务器的接口，为了方便服务器可能遇到IP经常变换，所以使用了域名映射，用该域名[tclhw1.alish.wang](tclhw1.alish.wang)作为映射，访问接口：[tclhw1.alish.wang:8080/0/sign_in](tclhw1.alish.wang:8080/0/sign_in)  

2. __Presenter层：__ 接口层，用于展示处理从Android传回或者传出的数据，对接Android层和test.jsp（test.jsp用于自己测试接口）  

3. __Logic层：__ 业务逻辑层，处理业务逻辑，比如联系人的申请、接受，查找等。  

4. __Dao层：__ 结合JPA操作数据库，给Logic层提供便利的数据操作。  

5. __MySQL:__ 使用MySQL的原因在于本项目只是一个小型项目，并且MySQL开源，如果有必要，我们会选择更新为MariaDB。  

6. __Model模块：__ 将业务涉及到的实例抽象，方便Logic操作以及存储到数据库。  

7. __Json\_Model模块：__ 方便接口层调用，隔离Model模块以及运用到Model模块的操作。  

[SpringMVC请参考](https://my.oschina.net/gaussik/blog/385697?p=2&temp=1487223969103#blog-comments-list)  

[服务器环境的搭建以及相关配置可在这里查看](http://www.jianshu.com/p/744ef1595c43)  
