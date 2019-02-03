# Contributing

## Get Digital Ocean droplet types

```bash
# install jq if not already installed
brew install jq

# return list
curl -H "Authorization: Bearer <TOKEN>" https://api.digitalocean.com/v2/images | jq '.' | pbcopy
```

## Todo

- Create web interface
- 3 tabs Run, Backtest, Config
- Backtest, Run, and Dryrun should all be able to have multiple processes
- Run let's you select strategy file and run or dryrun it
- Backtest lets you edit preexisting strategy files A.py, B.py, C.py, D.py, etc with a nice Python editor
- Config let's you update the config.json
