# Ansible Role: install_tailscale

This Ansible role installs and configures Tailscale on Debian-based and other Unix-like distributions.

## Requirements

- Ansible 2.9 or later
- Target machines must have internet access to download Tailscale packages and files.

## Role Variables

| Variable Name           | Default Value                         | Description                                         |
|-------------------------|---------------------------------------|-----------------------------------------------------|
| `tailscale_pre_auth_key`| `None`                                | The pre-authentication key for Tailscale.           |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: install_tailscale
      vars:
        tailscale_pre_auth_key: your-pre-auth-key-here
