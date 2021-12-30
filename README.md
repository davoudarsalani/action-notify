# Notify by sending a Telegram message with Jalali date/time prepended
<div align='center'>
<img alt='last-commit' src='https://img.shields.io/github/last-commit/davoudarsalani/action-notify?&labelColor=black&color=grey&style=flat'>
<img alt='commit-activity' src='https://img.shields.io/github/commit-activity/m/davoudarsalani/action-notify?&labelColor=black&color=grey&style=flat'>
</div>
<br>

```yml
- name: Notifying
  uses: davoudarsalani/action-notify@master
  with:
    telegram_message: Corrected typos
    TELEGRAM_TOKEN: ${{ secrets.TELEGRAM_TOKEN }}
    TELEGRAM_TO: ${{ secrets.TELEGRAM_TO }}
```
