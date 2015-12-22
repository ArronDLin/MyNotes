# Spring Security

## Dec 22th, 2015

1. Spring security RememberMe 

    登录后的定制，主要解决关闭浏览器后，session中变量丢失的问题。可以通过覆盖RememberMeService(如TokenBaseRememberMeService)中的processAutoLoginCookie()方法，在登录成功后，重新生成变量放到session中。 
    
    详情可参考[ Spring BlazeDS Integration之spring security(4)](http://blog.csdn.net/miqi770/article/details/44057969)
    
2.  接管Session,利用SessionListener实现HttpSessionListener,然后在Initializer中通过servletContext.addListener(new SessionListener())注册。详情参考[Spring Java 配置之 Session 超时 ](http://www.oschina.net/translate/spring-java-configuration-session-timeout)

