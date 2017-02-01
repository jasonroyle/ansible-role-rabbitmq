# RabbitMQ Ansible Role

## Version

Set `rabbitmq_version` to define the version of RabbitMQ to install.

```yaml
rabbitmq_version: 3.6.6-1
```

## Plugins

Set `rabbitmq_plugins` to define an array of enabled plugins.

```yaml
rabbitmq_plugins:
- rabbitmq_management
```

### Install Plugins

Set `url` to install plugins.

```yaml
rabbitmq_plugins:
- name: rabbitmq_delayed_message_exchange
  url: http://www.rabbitmq.com/community-plugins/v3.6.x/rabbitmq_delayed_message_exchange-0.0.1.ez
```

### Disable Plugins

Set `rabbitmq_plugins_disabled` to define an array of disabled plugins.

```yaml
rabbitmq_plugins_disabled:
- rabbitmq_management
```

## License

MIT
