# AOP

OOP 通过对象间的关系来进行抽象，好比是树状结构。然而，有些行为是各个对象都具有的，好比标签一样，不便用 OOP 来描述，这时就需要 AOP。

Spring 的 AOP 是简单的 AOP，以方法作为切入点，在匹配的切入点上进行操作。

- 需要标注 `@Aspect` 的 bean 来定义 aspect
  - `@Pointcut` 用于定义切入点，包括匹配方法的表达式以及签名（切入点的标识）
  - `@Before` 、 `@AfterReturning` 等用于定义在切入点进行的行为
- 配置文件中需要加入 `<aop:aspectj-autoproxy>`