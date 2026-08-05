# Unraid Community Application Templates

Official Unraid Community Application XML templates maintained by **hardly007** ([@JPetovello](https://github.com/JPetovello)).

---

## Available Templates

### 🔐 PasswordCheckerWeb
A self-hosted, lightweight Flask web application that evaluates password strength, checks for compromised credentials against Have I Been Pwned (HIBP) using k-Anonymity for privacy, and generates high-entropy passphrases based on the official 7,776-word EFF Large Wordlist.

* **Docker Image:** [`hardly007/password-checker-web:latest`](https://hub.docker.com/r/hardly007/password-checker-web)
* **Source Repository:** [JPetovello/password-checker-web](https://github.com/JPetovello/password-checker-web)

#### Configurable Environment Variables

| Variable | Default | Description |
| :--- | :--- | :--- |
| `REDIS_URL` | `memory://` | Optional Redis URI for distributed rate limiting (e.g., `redis://192.168.1.X:6379/0`). |
| `DISCORD_WEBHOOK_URL` | *(empty)* | Optional webhook URL for first-run/startup notifications. |
| `DISABLE_TELEMETRY` | `false` | Set to `true` to disable anonymous startup metrics. |
| `APP_SOURCE` | `unraid_ca` | Identifies deployment environment for container metrics. |

---

## How to Install on Unraid

### Option 1: Community Applications (Recommended)
Search for **PasswordCheckerWeb** directly inside the Unraid **Apps** tab and click **Install**.

### Option 2: Add Template Repository
1. In Unraid, navigate to **Docker** > **Template Repositories** (at the bottom of the page).
2. Paste the template repository URL:

    https://github.com/JPetovello/unraid-templates

3. Click **Save**. **PasswordCheckerWeb** will now appear under **Add Container** > **User Templates**.

---

## Support & Issues

If you encounter any issues or have feature requests, please open an issue on the main project repository:
* 🐛 **Report Bugs:** [PasswordCheckerWeb Issues](https://github.com/JPetovello/password-checker-web/issues)
