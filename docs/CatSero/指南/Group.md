# Group配置指南

## 新建Group

Group配置位于 `mirai-configs/group.yml`

首次打开，您应该会看到如下内容
```yaml
list:
  hello-group: 123456789
```
list下的hello-group即为GroupID
创建格式为`<id>: <群号>`

## 使用指南

打开`uses-config.yml`，您应该会发现每个功能下会有一个`var.group`:

```yaml
demo-use:
  var:
    group: hello-group
```

`var`内的`group`即为Group配置中的GroupID