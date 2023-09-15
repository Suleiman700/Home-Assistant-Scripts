
# Failed login notification

This script sends a notification to the mobile app when detects wrong login attempt.

Basically it detects new notification and check ofr condition.

---

### condition:

This condition checks if `login attempt` exists in notification data

```yaml
condition:
    - condition: template
      value_template: "{{ 'Login attempt' in trigger.notification.title }}"
```

---

### action:

Action gets the message and send it to the mobile app.

```yaml
action:
    - service: notify.notify
      data_template:
        title: Failed login
        message: "{{ trigger.notification.message }}"
```

demo of message:

> Login attempt or request with invalid authentication from <DEVICE_NAME> (<IP_ADDRESS>). See the log for details.
