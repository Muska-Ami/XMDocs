# Bot配置指南

## 新建Bot

Bot配置位于 `mirai-configs/bot.yml`

首次打开，您应该会看到如下内容
```yaml
list:
  hello-bot: 123456789
```
list下的hello-bot即为BotID
创建格式为 `<id>: <Bot QQ号>`

## 使用

打开`uses-config.yml`，您应该会发现每个功能下会有一个`var.bot`:

```yaml
demo-use:
  var:
    bot: hello-bot
```

`var`内的`bot`即为Bot配置中的BotID