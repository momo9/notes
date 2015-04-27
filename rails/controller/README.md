# Controller

* `rails generate controller`
* `app/controllers` 下的类是 controller
* controller 类中的方法是 action，用 `controller#acttion` 来表示
* 可用 `rails generate controller` 生成
* controller 中定义的成员变量可以在 view 中使用
* controller 可以重定向到 `ActiveRecord` 对象，代表重定向至其 `show` action

## routes

* 在 `config/routes.rb` 中定义 routes
* 通过 `rake routes` 查看路径
