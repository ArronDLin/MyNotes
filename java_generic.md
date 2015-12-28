# Java泛型

## Dec 24th, 2015

1. 泛型继承 直接看一个例子

    ```java
    public interface GenericDao<T, PK extends Serializable>
    ```
    
    这个例子实现类必须满足接口的泛型参数要求。T可以是任意类型，PK是实现了Serializable的类或者是继承了Serializable接口的接口。
    
    除了extends还可以用supper。例如如果是pk super ArrayList表示pk必须是Arraylist或其某父类。
    
## Dec 28th, 2015

1. joda-time的使用

    无疑，joda-time使时间的生成运算等更方便。
    
    ```java
    
    ```