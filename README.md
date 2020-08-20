# ansible-role-alert-logic-agent

Install the Alert Logic threat manager / log manager agent to your EC2 app nodes running in an Amazon VPC.

## Requirements

- OS: Ubuntu
- Alert Logic IDS appliance running in your VPC
- Your playbook must gather facts

## Role Variables

- `alert_logic_agent_deb_source`: See defaults/main.yml

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  gather_facts: true
  become: true
  roles:
    - name: Install the alert logic agent
      role: acromedia.alert-logic-agent
```

## License

GPLv3

## Author Information

[Acro Media Inc](https://www.acromedia.com/)
