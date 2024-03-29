---
title: uses-config.yml
---
# uses-config.yml

```yaml
# CatSero UsesConfig
# Generate by CatSero v@plugin.version@

# 所有的发送至QQ群的消息都支持mirai码
# 参见：
# https://docs.mirai.mamoe.net/Messages.html#mirai-%E7%A0%81
# https://docs.mirai.mamoe.net/Messages.html#%E6%B6%88%E6%81%AF%E5%85%83%E7%B4%A0
# https://docs.mirai.mamoe.net/Messages.html#%E6%B6%88%E6%81%AF%E9%93%BE%E7%9A%84-mirai-%E7%A0%81

# 聊天转发
chat-forward:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 自动清理样式代码
  clean-stylecode:
    to-mc: false
    to-qq: true
  # 消息头检测
  # 只有消息以这个字符串开头才会被转发
  header:
    # 功能开关
    # true | false
    enable: false
    # 消息头设置
    prefix:
      to-mc: "#"
      to-qq: "#"
  # 允许游戏内玩家使用mirai码
  allow-miraicode: false
  # 过滤器
  # 检测到消息内含有列表中的文本
  filter:
    # 功能开关
    # true | false
    enable: false
    # 自动更新列表
    auto-update:
      # 功能开关
      # true | false
      enable: true
      # 更新间隔
      # 单位: 秒
      interval: 300
    # 列表
    list:
      # 原生的列表
      via:
        to-mc: [ ]
        to-qq: [ ]
      # 从外部导入
      import:
        # 本地
        local: [ ]
        # 远程
        # 此处使用的是TrChat的默认远程源
        # 感谢南城提供的词库
        # CDN JsDelivr
        remote:
          - "https://cdn.jsdelivr.net/gh/Yurinann/Filter-Thesaurus-Cloud@main/database.json"
    # 替换成的字符
    replace: "**"
  # 使用MiraiMC内置绑定数据库查询QQ发言者名称
  use-bind: true
  # 格式
  format:
    # 内置占位符:
    # - %sender_permission%  发言者群权限(member，admin，owner)
    # - %name%  发言者名称
    # - %message%  消息
    to-mc: "&e[&aQQ&e]&e[&d%sender_permission%&e]&b%name%&r: %message%"
    # 内置占位符:
    # - %sender_permission%  发言者权限(player，admin)
    # - %name%  发言者名称
    # - %display_name%  发言者游戏中显示名称
    # - %message%  消息
    to-qq: "[MC][%sender_permission%]%name%: %message%"

# 发送玩家加入/退出消息
send-player-join-quit:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 格式
  # 内置占位符:
  # - %player% 加入玩家名称
  format:
    # 加入
    join: "%player%加入了游戏"
    # 退出
    quit: "%player%退出了游戏"
  # 需要拥有权限才会发送
  need-permission: false

# 发送玩家死亡消息
send-player-death:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 格式
  # 内置占位符:
  # - %player%  玩家名
  # - %message%  死亡消息
  format: "%player%死了,因为\n%message%"
  # 需要拥有权限才会发送
  need-permission: false

# 新人加入群欢迎
new-group-member-notification:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 格式
  # 内置占位符:
  # - %at%  @新成员
  # - %code%  新成员QQ号
  format: "欢迎%at%（%code%）加入本群!"

# 玩家解锁进度转发
send-advancement:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 格式
  # 内置占位符:
  # = %player%  玩家名
  # - %name%  进度名
  # - %description%  进度描述
  format: "%player%达成了进度: %name%\n描述: %description%"
  # 需要拥有权限才会发送
  need-permission: false

# TPS获取
get-tps:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group

# 在线玩家获取
get-online-list:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 格式
  format:
    # 无论是否有玩家在线都会发送
    # 内置占位符:
    # - %count%  当前在线玩家数
    # - %max%  最大在线玩家数
    0: |-
      当前在线: %count%
      最大在线: %max%
    # 当有玩家在线才发送
    # 内置占位符:
    # - %count%  当前在线玩家数
    # - %max%  最大在线玩家数
    # - %list%  当前在线玩家列表
    1: |-
      玩家列表: %list%
# QQ白名单
qwhitelist:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 检查是否在群内
  # 若存在白名单但不在群内则视为无
  check-if-on-group: true
  # 自助申请白名单
  self-application:
    # 功能开关
    # true | false
    enable: false
    # 申请格式
    # 内置占位符:
    # - %name%  玩家名（只能设置一个）
    format: "!申请白名单 %name%"
  # 限制每个QQ只能拥有一个白名单
  a-qq-only-an-account: true
  # 账户名称正则表达式
  regex: "^[A-Za-z0-9_]+$"

# 离群提示
group-member-leave-notification:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 格式
  # 内置占位符:
  # - %name%  名称
  # - %code%  QQ号
  format: "%name%（%code%）离开了本群"

# QQ命令执行
qcmd:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group

# QQ群占位符
info-placeholder:
  # 功能开关
  # true | false
  enable: false
  # Bot & Group设置
  var:
    # BotID
    bot: hello-bot
    # GroupID
    groups:
      - hello-group
  # 插件应该自动更新哪个内容的名称
  # (group|bot)
  should-updates:
    - group
    - bot
  # 更新间隔
  # 单位: 秒
  interval:
    # 群名称
    title: 30
    # Bot群名称
    bot-name: 60
  # 群名称格式
  format:
    titles:
      hello-group: '%origin% - 在线: %player_limit%/%player_max%'
    bot-name: "%origin% - TPS: %server_tps%"
```
