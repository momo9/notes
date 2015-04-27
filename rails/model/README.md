# Model

* 用 `rails generate model` 生成代码
* 用 `rake db:migrate` 来生成数据库
* 建立 model 对象时要求 *强类型* ，不能直接用 JSON 来反射，而需要指定各个字段

		params.require(:product).permit(:field1, :field2)

## 一对多关系

以一个 article 有多个 comment 为例。

* article 的 model 类中：`has_many`
	* 如果删除一个 article 要删除对应的 comment，需要加入 `dependent: :destroy`
* article 的 resource 中：增加 comment 的 resource
* resource 的 model 类中：`belongs_to`

## validation

* 在 model 中调用 `validates` 方法
* 将决定 `save` 与 `update` 是否成功
