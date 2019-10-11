#### hibernate
######## 1.普通字段无法懒加载
可以使用hibernate-enhance-maven-plugin字节码增强器。
注：
1.自己单纯的实现PersistentAttributeInterceptable会对集合类的关联关系的懒加载产生影响，如没写好会无法保存多对多
2.使用字节码增强器后会导致json序列化失败，就算使用了Hibernate5Module也没用
3.针对这种情况，需要做特殊处理，我的方法是直接更改类，在对应set方法中使用PersistentAttributeInterceptor强转LazyAttributeLoadingInterceptor获取到session判断session是否已经存在
