# Common Commands

### Connecting to localhost

{% code-tabs %}
{% code-tabs-item title="/etc/ansible/hosts" %}
```bash
[local]

    localhost ansible_connection=local

```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Execute a playbook on a specific host

```bash
ansible-playbook --limit <host from hosts file> someplaybook.yaml
```



