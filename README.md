# RabbitMQ Ansible Role

## Version

Set `rabbitmq_version` to define the version of RabbitMQ to install.

```yaml
rabbitmq_version: 3.6.6-1
```

## Plugins

Set `rabbitmq_plugins` to define an array of plugins. Plugins will be enabled by default.

```yaml
rabbitmq_plugins:
  - rabbitmq_management
```

### Disable Plugins

Set `disabled` to disable plugins.

```yaml
rabbitmq_plugins:
  - name: rabbitmq_management
    disabled: True
```

### Install Plugins

Set `url` to install plugins.

```yaml
rabbitmq_plugins:
  - name: rabbitmq_delayed_message_exchange
    url: http://www.rabbitmq.com/community-plugins/v3.6.x/rabbitmq_delayed_message_exchange-0.0.1.ez
```

## License

MIT
