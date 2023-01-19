---
title: config.yml
---
```yaml
# CatSero Plugin Config
# Generate by CatSero v@plugin.version@

# 语言文件
locale: zh_CN

# bStats
bstats: true

# 检查更新
check-update:
  # 功能开关
  # true | false
  enable: true
  # 检查更新间隔
  # 单位: 秒
  interval: 3600
  # 版本模式
  mode: latest
  # 检查更新服务器API地址，一般情况请勿修改
  api-url: https://mcp.huahuo-cn.tk/api/CatSero/version

# JDBC
jdbc:
  # SQLite JDBC class名称
  sqlite-class-name: "org.sqlite.JDBC"
  # MySQL JDBC class名称
  mysql-class-name: "com.mysql.jdbc.Driver"
  # 数据储存方法
  # sqlite | mysql
  type: sqlite
  # MySQL设置
  mysql-config:
    # 地址
    host: localhost
    # 端口
    port: 3306
    # 用户名
    username: catsero
    # 密码
    password: 123456
    # 数据库名
    database: catsero
    # 时区
    timezone: "Asia/Shanghai"
    # 使用Unicode
    unicode: true
    # 数据库编码格式
    encoding: "UTF-8"
    # 使用SSL连接
    ssl: false

# 自定义QQ命令头
command-prefix:
  # 功能开关
  # true | false
  enable: false
  # 命令头
  prefix: ""
```