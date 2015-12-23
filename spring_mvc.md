# Spring MVC

## Dec 23rd, 2015

1. Spring MVC可以支持以下的返回方式：ModelAndView，Model， ModelMap，Map，View，String， void。

    * ModelAndView 可以指定返回的页面，通过addObject()的方式设置返回值。addObject()将值设置到一个名为ModelMap的类中。
    
    ```
    @RequestMapping("/show1") 
public ModelAndView show1(HttpServletRequest request, 
           HttpServletResponse response) throws Exception { 
       ModelAndView mav = new ModelAndView("/demo2/show"); 
       mav.addObject("account", "account -1"); 
       return mav; 
   }  
    
    ```
    
    * Model 是一个借口，其实现类为ExtendedModelMap，继承了ModelMap类。
    
    * Map 
    
    ```
    
    @RequestMapping("/demo2/show") 
        public Map<String, String> getMap() { 
            Map<String, String> map = new HashMap<String, String>(); 
            map.put("key1", "value-1"); 
            map.put("key2", "value-2"); 
            return map; 
        }  
    ```
    在jsp页面中可直通过${key1}获得到值, map.put()相当于request.setAttribute方法。
    
    * View 可以返回pdf excel等
    
    * String 指定返回的视图页面名称
    
    *注意：如果方法声明了注解@ResponseBody ，则会直接将返回值输出到页面。*
    
    ```
    
    @RequestMapping(value = "/something", method = RequestMethod.GET) 
    @ResponseBody 
    public String helloWorld()  { 
    return "Hello World"; 
    }  
    ```
    
    