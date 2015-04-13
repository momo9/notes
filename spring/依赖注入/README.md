# 依赖注入

或者叫控制反转。在原本的过程中，如果 A 依赖 B，就必须得先定义好 B。现在是 A 依赖一个 B 的接口，具体什么是 B 是不清楚的。到 B 建立的时候，再把自己注入进去，实现了依赖的反转。

`ApplicationContext` 就是生成 bean 的工厂。

## constructor-based or setter-based

- mandatory: constructor-based
- optional: setter-based

## @Autowired

标注了 `@Autowired` 以后，可以省略一些配置，改为从已有的 bean 中寻找相应的对象（根据类型来匹配）

- 标注字段：不需要 setter 和 xml 中的 property
- 标注构造器：不需要 xml 中的 constructor-arg
- 标注 setter 与 getter：不需要 xml 中的 property

如果有多个匹配类型的 bean，会报错；这时可以通过 `@Qualifier` 来指定 bean

## 作用域

如果全局作用域的 bean 作为生存期较短的 bean 的依赖，则需要用到 aop-proxy

## web 应用中如何加载 spring 配置

- 在 `web.xml` 中加入相应的 `Listener`
- 配置文件为 `WEB-INF` 中的 `applicationContext.xml`

## @Component

- 标注了 `@Component` 的类将成为 bean
- 配置中需要有 `<context:component-scan/>`

## 获取 bean

通过 `WebApplicationContextUtils` 获取 context，再从 context 中获取 bean