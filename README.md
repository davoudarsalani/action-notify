# Notify by sending an SMS or a Telegram message

```yml
name: Notify

on: [push, pull_request, workflow_dispatch]

jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v2

      - name: Notifying
        uses: davoudarsalani/notify@master
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
