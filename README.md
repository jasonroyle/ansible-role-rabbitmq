# RabbitMQ Ansible Role

## Version

Set `rabbitmq_version` to define the version of RabbitMQ to install.

```yaml
rabbitmq_version: 3.6.6-1
```

## Users

Set `rabbitmq_users` to define an array of present users.

```yaml
rabbitmq_users:
- user: admin
  password: admin
  vhost: /
  configure_priv: .*
  read_priv: .*
  write_priv: .*
  tags: administrator
```

### Remove Users

Set `rabbitmq_users_absent` to define an array of absent users.

```yaml
rabbitmq_users_absent:
- guest
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
