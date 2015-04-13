# Hibernate

- Hibernate 的同时也需要 JDBC
- 定义 `LocalSessionFactoryBean` ，通过这个 bean 设置 Hibernate
- *.hbm.xml
  - 定义 ORM 关系
  - `id` 对应主键， `generator` 选 `native`
  - DDL 语句支持得并不好
- 同时， `LocalSessionFactoryBean` 其实可以看作是 `SessionFactory` 的 bean，用于生成 `Session`
- `Session` 的操作
  - `save()` ，参数为 POJO
  - 建立 `Criteria` 确定查询的条件， `list()` 得到查询结果