# FreqTrade Now

## Provision

Create a remote server on Digital Ocean that can constantly be running/trading. Cost is around \$5/mo.

1. Sign up for [Digital Ocean](https://cloud.digitalocean.com/registrations/new).
2. Create an [API Key](https://cloud.digitalocean.com/account/api) to get values `digitalocean_access_token` for `scripts/provision`.

After following the steps above and updating the `scripts/provision` file with your `digitalocean_access_token` you can run:

```bash
./ops provision
```

## Setup

Install freqtrade and configure it to work with Bittrex crypto exchange for trades and a bot on the messaging platform Telegram used to monitor and control freqtrade itself.

1. Signup for [Bittrex](https://bittrex.com/account/register).
2. Create a [Bittrex API Key](https://bittrex.com/Manage?view=api) to get values `exchange.key` and `exchange.secret` for `freqtrade/config.json`.
3. Signup for [Telegram](https://web.telegram.org).
4. Talk with [BotFather](https://telegram.me/BotFather) to create a new bot and get value `telegram.token` for `freqtrade/config.json`.
5. Talk with [userinfobot](https://telegram.me/userinfobot) to get `telegram.chat_id` value for `freqtrade/config.json`.

After you've completed the steps above to get all the credentials and you've updated `freqtrade/config.json` you can deploy freqtrade by running one of the following commands:

```bash
# fake trades (start with this)
./ops deploy dryrun

# real live trades
./ops deploy run

# backtest strategy
./ops deploy backtest
```

## Develop Locally

You can run these containers locally just like you would on Digital Ocean

```bash
# fake trades
./ops start dryrun

# real live trades
./ops start run

# backtest strategy
./ops start backtest
```

## Resources

- [Docker Installation](https://www.freqtrade.io/en/latest/installation/#automatic-installation-docker)
- [Back Testing](https://www.freqtrade.io/en/latest/backtesting/)
