# controller

- web.xml中，映射一个 `DispatcherServlet` ，假设名字为 `ctrl`
- 建一个 =ctrl-servlet.xml= ，对 =ctrl= 进行配置（就是一般应用中的 =applicationContext.xml= ）
- 配置好 `<mvc:annotation-driven/>` ，再开启 `<context: component-scan/>` ，就会自动去找 `@Controller` （可以有多个， `Controller` 其实是一种 `Component` ）
- controller 里再根据 url 等进行处理
	- 可以是服务，直接返回 POJO （简单的 Bean），被封装为 json、xml 等形式
    - 可以修改 model，传递给 view 显示（通过返回字符串确定具体的 view）
    
## DispatcherServlet 的处理过程

* `WebApplicationContext`
* locale resolver (optional)
* theme resolver (optional)
* multipart file resolver (about update, optional)
* search for **handler** (by `HandlerMapping`)
* if a *model* is returned, render the view
