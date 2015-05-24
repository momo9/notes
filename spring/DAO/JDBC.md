# JDBC

- POJO
- DAO 接口
- DAO 实现
  - `JdbcTemplate` （依赖单例的 `DriverManagerDataSource` ，但 `JdbcTemplate` 本身不是单例）
  - 一个对应请求结果和 POJO 的 Mapper（实现 `RowMapper` )