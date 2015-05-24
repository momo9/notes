# MyBatis

- POJO 必须实现 `Serializable`
- `SqlSessionFactoryBean` bean，用于配置 MyBatis
- Mapper
  - 开启 `<mybatis:scan />` ，自动扫描 Mapper 成为 bean
  - Mapper 是一个 `interface` ，类名与 xml 中的 `namespace` 对应，方法与查询的 `id` 对应
  - DAO 中通过调用 Mapper 的方法来执行相应 id 中的 SQL 语句