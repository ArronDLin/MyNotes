# Spring Session

## Dec 22th, 2015

1. 在spring中如何将变量放置在session中，

    利用Spring的SessionAttributes可以将ModelMap中的变量放到session中，前提是要将这个变量放到Modelmap中。
   
    1）在Controller中获取，在需要用到这个变量的Controller上加上@SessionAttributes(""),然后再用到的函数中加上参数@ModelAttributes("")。
    
    2）在jsp中获取，可以使用jstl的${sessionCope.变量名}获取。 
    
2.  接管Session

    利用SessionListener实现HttpSessionListener,然后在Initializer中通过servletContext.addListener(new SessionListener())注册。详情参考[Spring Java 配置之 Session 超时 ](http://www.oschina.net/translate/spring-java-configuration-session-timeout)
    
    
3. Spring security 2.0 session过期时自动转向登陆页面

    