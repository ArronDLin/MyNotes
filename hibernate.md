# Hibernate

## Dec 23rd, 2015

1. @javax.persistence.Entity vs @org.hibernate.annotations.Entity
    
    @org.hibernate.annotations.Entity是对@javax.persistence.Entity的补充，具有一些特有的属性，例如dynamicInsert， dynamicUpdate 

    ```
    @Entity
    @org.hibernate.annotations.Entity(dynamicInsert = true, dynamicUpdate = true)
    @Table(name = "MA_UIM_USER")
    public class JpaUIMUser extends AbstractAuditable<Long> implements User {
    ...
    ```