# Trade Now

## Provision

Create a remote server on Digital Ocean that can constantly be running/trading. Cost is around \$5/mo.

1. Sign up for [Digital Ocean](https://cloud.digitalocean.com/registrations/new).
2. Create an [API Key](https://cloud.digitalocean.com/account/api) to get values `digitalocean_access_token` for `provision`.

```bash
./provision
```

## Setup

Install freqtrade and configure it to work with Bittrex crypto exchange for trades and a bot on the messaging platform Telegram used to monitor and control freqtrade itself.

1. Signup for [Bittrex](https://bittrex.com/account/register).
2. Create a [Bittrex API Key](https://bittrex.com/Manage?view=api) to get values `exchange.key` and `exchange.secret` for `config.json`.
3. Signup for [Telegram](https://web.telegram.org).
4. Talk with [BotFather](https://telegram.me/BotFather) to create a new bot and get value `telegram.token` for `config.json`.
5. Talk with [userinfobot](https://telegram.me/userinfobot) to get `telegram.chat_id` value for `config.json`.

```bash
./setup
```

## Run

Start running the freshly configured freqtrade on the server we just created. Use `run-dryrun` to complete fake trades just to make sure everything is working correctly. After all looks good you can manually transfer some BTC into Bittrex account and use `run` to start real live trades.

```bash
# fake trades
./run-dryrun

# real live trades
./run
```

## Helpful commands for managing droplet

```bash
# Log into droplet
ssh root@68.183.167.29 # Replace with actual IP

# Docker commands
docker logs freqtrade
docker logs -f freqtrade
docker restart freqtrade
docker stop freqtrade
docker start freqtrade
docker rm freqtrade
```

## Resources

- [Docker Installation](https://www.freqtrade.io/en/latest/installation/#automatic-installation-docker)
