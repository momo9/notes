# handler

* `HandlerMethod` 是 Spring 3.1 新增加的（这是不是说明 handler 之前就是处理 `Controller` 用的？）

## Concepts

* spring mvc 的作用，就是将 HTTP request 映射为 handler
* handler 默认为 `@Controller` 和 `@RequestMapping`
* controller methods 是一系列注解了 `@RequestMapping` 的方法的集合

## 流程

### url 处理流程

* 根据 url 找到 class（Controller，也叫 handler）
* 根据 HandlerAdapter 来确定具体的 method

