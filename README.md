# Notify by sending a Telegram message or an SMS

```yml
- name: Notifying
  uses: davoudarsalani/action-notify@master
  with:
    send_telegram_message: true
    telegram_message: |
      Event: ${{ github.event_name }}
      Repo: ${{ github.repository }}
      Commit message: ${{ github.event.commits[0].message }}
      Diff: https://github.com/${{ github.repository }}/commit/${{ github.sha }}
    TELEGRAM_TOKEN: ${{ secrets.TELEGRAM_TOKEN }}
    TELEGRAM_TO: ${{ secrets.TELEGRAM_TO }}
```
