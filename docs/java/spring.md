# Spring相关知识
## Spring Framework
- 包括了ioc依赖注入，Context上下文、bean管理、springmvc等众多功能模块，其它spring项目比如spring boot也会依赖spring框架。  
1. IOC框架
- 在spring中，对象的属性是由对象自己创建的，就是正向流程；如果属性不是对象创建，而是由spring来自动进行装配，就是控制反转。
2. context上下文和bean
- spring进行IOC实现时使用的有两个概念：context上下文和bean。
- 所有被spring管理的、由spring创建的、用于依赖注入的对象，就叫做一个bean。Spring创建并完成依赖注入后，所有bean统一放在一个叫做context的上下文中进行管理。
3. AOP
- AOP就是面向切面编程。如右面的图，一般程序执行流程是从controller层调用service层、然后service层调用DAO层访问数据，最后在逐层返回结果。
AOP以功能进行划分，对服务顺序执行流程中的不同位置进行横切，完成各服务共同需要实现的功能。