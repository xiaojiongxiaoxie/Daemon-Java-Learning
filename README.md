# Daemon-Java-Learning

`java学习心得体会，如发现有任何不对的地方，欢迎留言指正。`<br/>
`不定期更新中...`

## Spring
Spring 本身是一个非常流行的框架，但是由于涵盖的内容（概念、思想、设计模式等等）非常多，后面也会不断进行补充...

### 基于各种各样的 xml 的 spring 开发
... 

### 基于注解的 Spring 开发
#### 背景：
2018年暑假刚刚接触 springboot 的时候，觉得上手起来非常容易，能够很快速地写一个 HelloWorld，但是对其中的原理并不是非常清楚。后面初步接触了下 springboot 的源码，发现大部分原理都是 spring 中的。联想到自己刚刚接触 spring 的时候，也是对 spring 中的很多理念（譬如 IOC 和 AOP）非常懵，并且在后面用 spring 框架整合其它的框架（springmvc、mybatis等等）非常麻烦（因为需要各种配置），而且我隐约记得在进行框架整合时的版本设置也是个坑，等等。总之，一个不小心可能要三四天才能把各个框架搭建起来（原谅我快两年没写过ssm/ssh框架的整合了，有点忘记了）。<br/>
再后来，接触了 spring 基于注解的开发。哇，瞬间觉得很便捷（可能现在用 springboot 用习惯了吧，到处都是注解）。但是仔细想想，不论是基于注解的 spring 还是基于“传统”的 xxx.xml 这种形式的 spring 开发，最根本的运行流程都是一样的，而且可能是个人习惯问题吧，万一有人就是喜欢 beans.xml 呢。<br/>
悲催的是，在基于注解的 spring / springboot 的开发中，也因为注解出过各种各样的 bug，例如 @Autowired 注入组件失败了，@PropertySource 找不到配置文件了等等；而且，由于一个“小小”的注解帮我们自动完成了很多工作，我们对底层的工作原理更是知之甚少。所以，这里先对 spring 中的一些常用注解做简单梳理，并对涉及到的一些原理性的东西做一介绍。<br/>

#### 干货：
spring 中与组件注入相关的注解：
  * @Configuration <br/>
  * @Bean <br/>
  * @ComponentScan <br/>
  * @Component <br/> 
  * @Service <br/>
  * @Controller <br/>
  * @Repository <br/>
  * @Conditional* <br/>
  * @Primary <br/>
  * @Lazy <br/>
  * @Scope <br/>
  * @Import* <br/>
 
spring 中与属性赋值相关的注解：
  * @PropertySources  <br/>
    * @PropertySource  <br/>
  * @Value <br/>
  * @Autowired <br/>
    * @Qualifier <br/>
    * @Resources <br/>
    * @Inject <br/>
  * @Profile <br/>

spring 中与 AOP 相关的注解：
  * @EnableAspectJAutoProxy <br/>
  * @Before/@After/@AfterReturning/@AfterThrowing/@Around <br/>
  * @Pointcut <br/>

spring 中与声明式事务相关的注解：
  * @EnableTransactionManagement <br/>
  * @Transactional <br/>

