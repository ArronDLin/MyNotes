# Spring Session

## Dec 22th, 2015

1. 在spring中如何将变量放置在session中，利用Spring的SessionAttributes可以将ModelMap中的变量放到session中，前提是要将这个变量放到Modelmap中。
   
    1）在Controller中获取，在需要用到这个变量的Controller上加上@SessionAttributes(""),然后再用到的函数中加上参数@ModelAttributes("")。
    
    2）在jsp中获取，可以使用jstl的${sessionCope.变量名}获取。 

