# Simple MacOS DuckDNS Updater

Automatically update your [DuckDNS](https://www.duckdns.org/) IP address. Only updates if Wi-Fi SSID is your home network [optional].

## Installation

Install plist to automatically run agent. Requires [`terminal-notifier`](https://github.com/julienXX/terminal-notifier).

```sh-session
$ brew install terminal-notifier
$ git clone https://github.com/jdxcode/duckdns
$ cd duckdns
$ ln -s $(pwd)/duckdns.plist ~/Library/LaunchAgents/duckdns.plist
$ echo > ~/.config/duckdns <<EOF
DUCKDNS_DOMAIN=xxx
DUCKDNS_TOKEN=xxx
DUCKDNS_SSID=xxx # optional to only run on single wifi ssid
EOF
$ launchctl load ~/Library/LaunchAgents/duckdns.plist
```
