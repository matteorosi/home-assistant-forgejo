# Home Assistant Add-on: Forgejo

![Supports aarch64 Architecture][aarch64-shield] ![Supports amd64 Architecture][amd64-shield] ![Supports armhf Architecture][armhf-shield] ![Supports armv7 Architecture][armv7-shield] ![Supports i386 Architecture][i386-shield]

Forgejo is a self-hosted lightweight software forge. Easy to install and run, it is a community fork of Gitea.

## About

Forgejo is a self-hosted Git service with a web interface, similar to GitHub, GitLab, or Gitea. This add-on allows you to run Forgejo directly on your Home Assistant instance.

## Features

- 🔒 **Secure**: Built-in user authentication and authorization
- 🌐 **Web Interface**: Modern and intuitive web UI
- 📝 **Git Repository Management**: Create, manage, and collaborate on Git repositories
- 🔄 **Built-in Git Server**: SSH and HTTP(S) access to your repositories
- 🎯 **Issue Tracking**: Built-in issue tracker and project management
- 🔗 **Webhooks**: Integrate with other services and CI/CD pipelines
- 📊 **Organizations**: Support for organizations and teams

## Installation

1. Add this repository to your Home Assistant Add-on Store:
   ```
   https://github.com/yourusername/forgejo-addon
   ```

2. Install the "Forgejo" add-on.

3. Configure the add-on (see configuration section below).

4. Start the add-on.

5. Access Forgejo at `http://your-home-assistant:3000`

## Configuration

Add-on configuration:

```yaml
domain: git.example.com
app_name: "My Forgejo"
admin_user: admin
admin_email: admin@example.com
admin_password: "your-secure-password"
root_url: "https://git.example.com"
ssh_domain: git.example.com
disable_registration: false
require_signin: false
secret_key: ""
internal_token: ""
lfs_start_server: true
offline_mode: false
```

### Option: `domain` (required)

The domain name for your Forgejo instance.

### Option: `app_name`

The name of your Forgejo instance (default: "Forgejo").

### Option: `admin_user`

The username for the initial admin user (default: "admin").

### Option: `admin_email`

The email address for the initial admin user.

### Option: `admin_password`

The password for the initial admin user. Leave empty to use the default password.

### Option: `root_url`

The full URL of your Forgejo instance. If empty, it will be generated automatically.

### Option: `ssh_domain`

The domain for SSH access. If empty, it will use the same as `domain`.

### Option: `disable_registration`

Whether to disable user registration (default: false).

### Option: `require_signin`

Whether to require sign-in to view repositories (default: false).

### Option: `secret_key`

Secret key for encryption. Leave empty to auto-generate.

### Option: `internal_token`

Internal token for API access. Leave empty to auto-generate.

### Option: `lfs_start_server`

Whether to enable Git LFS support (default: true).

### Option: `offline_mode`

Whether to run in offline mode (default: false).

## Ports

The add-on uses the following ports:

- `3000/tcp`: Web interface
- `2222/tcp`: SSH Git access

## Data Persistence

Your Git repositories and configuration are stored in the add-on's data directory and will persist across updates and restarts.

## Support

For support and questions, please visit:
- [Forgejo Documentation](https://forgejo.org/docs/)
- [Home Assistant Community](https://community.home-assistant.io/)

## Changelog & Releases

This repository keeps a change log using [GitHub's releases][releases] functionality.

## License

MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
[releases]: https://github.com/yourusername/forgejo-addon/releases
