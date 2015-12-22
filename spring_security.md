# Spring Security

## Dec 22th, 2015

1. Spring security RememberMe 登录后的定制，主要解决关闭浏览器后，session中变量丢失的问题。可以通过覆盖RememberMeService(如TokenBaseRememberMeService)中的processAutoLoginCookie()方法，在登录成功后，重新生成变量放到session中。 