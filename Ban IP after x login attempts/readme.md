
# Bad IP after x login attempts

This script automatically bans ip address after x login attempts.

Any banned ip will be stored in `ip_bans.yaml` file.

Make sure to use another device for testing and not your main device to avoid getting banned.

---

### ip_ban_enabled:

Set to true|false based on your needs

```yaml
ip_ban_enabled: true
```

---

### login_attempts_threshold:

The number of login attempts to ban the ip address

```yaml
login_attempts_threshold: 5
```
