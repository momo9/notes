# View

* 在 action 中 `render` ，得到 JSON 等格式
* 在 action 中不是 `render` 的话，处理完会转到 `app/view/controller/action.html.erb` 的 view 中
* 用 `link_to` 来指定超链接
* 删除时的确认是加在 view 上的，通过 JS 实现
* `_` 开头的 erb 文件是 partial 文件，可以在其它 erb 文件中 render
	* 单纯地被 include
	* 可迭代使用

## form_for

* `form_for` 的时候应该就会产生 JSON 一类的对象，传递给 controller

## render 与 redirect

* 正常的流程：有请求来，访问 controller，处理完转到对应的 view
* render：从 controller 跳到其它的 view
* redirect：发起一个新的请求