# RabbitMQ Ansible Role

## Version

Set `rabbitmq_version` to define the version of RabbitMQ to install.

```yaml
rabbitmq_version: 3.6.6-1
```

## Users

See [RabbitMQ user module](http://docs.ansible.com/ansible/rabbitmq_user_module.html).

Set `rabbitmq_users` to define an array of present users.

```yaml
rabbitmq_users:
- user: admin
  password: admin
  tags: administrator
```

| OPTION         | REQUIRED | DEFAULT |
|----------------|----------|---------|
| configure_priv | No       | .*      |
| password       | Yes      |         |
| read_priv      | No       | .*      |
| tags           | No       |         |
| user           | Yes      |         |
| vhost          | No       | /       |
| write_priv     | No       | .*      |

### Remove Users

Set `rabbitmq_users_absent` to define an array of absent users.

```yaml
rabbitmq_users_absent:
- guest
```

## Virtual Hosts

See [RabbitMQ virtual host module](http://docs.ansible.com/ansible/rabbitmq_vhost_module.html).

Set `rabbitmq_vhosts` to define an array of present virtual hosts.

```yaml
rabbitmq_vhosts:
- /one
- name: /two
  node: rabbit
  tracing: False
```

| OPTION  | REQUIRED | DEFAULT |
|---------|----------|---------|
| name    | Yes      |         |
| node    | No       | rabbit  |
| tracing | No       | False   |

### Remove Virtual Hosts

Set `rabbitmq_vhosts_absent` to define an array of absent virtual hosts.

```yaml
rabbitmq_vhosts_absent:
- /vhost
```

## Plugins

See [RabbitMQ plugin module](http://docs.ansible.com/ansible/rabbitmq_plugin_module.html).

Set `rabbitmq_plugins` to define an array of enabled plugins.

```yaml
rabbitmq_plugins:
- rabbitmq_management
- name: rabbitmq_delayed_message_exchange
  url: http://www.rabbitmq.com/community-plugins/v3.6.x/rabbitmq_delayed_message_exchange-0.0.1.ez
```

| OPTION | REQUIRED | DEFAULT | DESCRIPTION         |
|--------|----------|---------|---------------------|
| name   | Yes      |         |                     |
| url    | No       |         | Installs the plugin |

### Disable Plugins

Set `rabbitmq_plugins_disabled` to disable plugins.

```yaml
rabbitmq_plugins_disabled:
- rabbitmq_management
```

## License

MIT
