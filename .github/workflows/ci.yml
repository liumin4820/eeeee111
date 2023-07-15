name: ci

on:
  push:
    branches:
      - main
  schedule:
    - cron: "*/54 */6 * * *"

jobs:
  autogreen:
    runs-on: ubuntu-latest
    
    permissions:
      contents: write
  
    steps:
      - name: Clone repository
        uses: actions/checkout@v3

      - name: Auto green
        run: |
          git config --local user.email "liumin4820@outlook.com"
          git config --local user.name "liumin4820"
          git remote set-url origin https://${{ github.actor }}:${{ secrets.GITHUB_TOKEN }}@github.com/${{ github.repository }}
          git pull --rebase
          git commit --allow-empty -m "为了美好的明天！加油！努力！"
          git push
