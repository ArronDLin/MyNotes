# Java泛型

## Dec 24th, 2015

1. 泛型继承 直接看一个例子

    ```java
    public interface GenericDao<T, PK extends Serializable>
    ```
    
    这个例子实现类必须满足接口的泛型参数要求。T可以是任意类型，PK是实现了Serializable的类或者是继承了Serializable接口的接口。