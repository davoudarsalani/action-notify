# Notify by sending a Telegram message with Jalali date/time prepended

```yml
- name: Notifying
  uses: davoudarsalani/action-notify@master
  with:
    telegram_message: |
      Typos corrected
    TELEGRAM_TOKEN: ${{ secrets.TELEGRAM_TOKEN }}
    TELEGRAM_TO: ${{ secrets.TELEGRAM_TO }}
```
