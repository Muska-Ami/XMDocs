# SQL数据库配置指南

## SQLite

将 `jdbc.sqlite-class-name` 设置为正确的 JDBC 类名(一般保持默认即可)，并将 `jdbc.type` 设置为 `sqlite`
```yaml
# JDBC
jdbc:
  # SQLite JDBC class名称
  sqlite-class-name: "org.sqlite.JDBC"
  # 数据储存方法
  # sqlite | mysql
  type: sqlite
```

## MySQL
将 `jdbc.mysql-class-name` 设置为正确的 JDBC 类名(一般保持默认即可)，并将 `jdbc.type` 设置为 `mysql`

- 旧版 JDBC Class
  `com.mysql.jdbc.Driver`
- 新版 JDBC Class
  `com.mysql.cj.jdbc.Driver`
```yaml
# JDBC
jdbc:
  # SQLite JDBC class名称
  mysql-class-name: "com.mysql.jdbc.Driver"
  # 数据储存方法
  # sqlite | mysql
  type: mysql
```
