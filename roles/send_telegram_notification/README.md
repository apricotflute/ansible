# Ansible Role: send_telegram_notification

This Ansible role sends a notification message to a specified Telegram chat using the Telegram Bot API. It is designed to be simple and easy to use, allowing users to quickly integrate Telegram notifications into their Ansible workflows.

## Requirements

- A Telegram bot token. You can create a bot and obtain a token by talking to the [BotFather](https://core.telegram.org/bots#6-botfather).
- The chat ID of the user or group to which you want to send the notification.

## Role Variables

The following variables are required for the role to function properly:

- `telegram_token`: The token of your Telegram bot.
- `chat_id`: The chat ID of the user or group where the notification will be sent.
- `telegram_notification_text`: The text message that will be sent as a notification.

## Dependencies

No external dependencies are required for this role.

## Example Playbook

Here's a basic example of how to use this role in your Ansible playbook:

```yaml
- hosts: localhost
  gather_facts: no
  roles:
    - role: send_telegram_notification
      vars:
        telegram_token: "YOUR_TELEGRAM_BOT_TOKEN"
        chat_id: "YOUR_CHAT_ID"
        telegram_notification_text: "Hello! This is a test notification from Ansible."
