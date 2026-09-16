# PnL Calendar

PnL Calendar is a read-only, local-first performance calendar for Interactive
Brokers users. It turns IBKR Flex reports into clear daily, monthly, and yearly
profit-and-loss views without sending account data through a developer-operated
server.


## Features

- Daily P&L calendar and 12-month yearly overview
- Net P&L, time-weighted return, win rate, and detailed period breakdowns
- Automatic synchronization when the app opens, plus manual synchronization
- Direct, read-only connection to the IBKR Flex Web Service
- Flex credentials protected by the iOS Keychain
- Financial report cache stored only in the app's private local storage
- English, Simplified Chinese, Spanish, and Japanese
- Light and dark themes, with configurable gain/loss colors
- Native layouts for iPhone and iPad
- Built-in demo data, so the interface can be explored without an IBKR account


## Using live IBKR data

Live synchronization requires your own Activity Flex Query ID and Flex Token.
In IBKR Client Portal:

1. Open **Reporting → Flex Queries**.
2. Create or edit an **Activity Flex Query** with XML output.
3. Enable **Change in NAV** and the fields needed for dates, starting/ending
   value, transfers, deposits/withdrawals, mark-to-market, and TWR.
4. Save the query and copy its Query ID.
5. Open **Flex Web Service Configuration**, enable the service, and create a
   token. Leave the IP restriction empty if the token will be used on a phone.
6. Enter the Query ID and token in PnL Calendar settings, then validate and save.


## Privacy

The iOS app connects directly from the device to Interactive Brokers over HTTPS.
It has no developer-operated backend, advertising, analytics SDK, or cross-app
tracking. Credentials are stored in the iOS Keychain and downloaded report data
is cached in the app sandbox.

Read the complete [Privacy Policy](PRIVACY.md).


## Support

For bugs or feature requests, open a [GitHub Issue](../../issues). Before opening
an issue, remove all tokens, Query IDs, account identifiers, balances, positions,
and report contents. Never publish credentials in an issue, screenshot, or log.


## Development

### iOS and iPadOS

Requirements:

- Xcode 16 or later
- iOS/iPadOS 18.0 or later

Open [`ios/PnLCalendar.xcodeproj`](ios/PnLCalendar.xcodeproj) in Xcode, select an
iPhone or iPad simulator, and run the `PnLCalendar` scheme. Simulator builds must
remain signed for Keychain access.

The deterministic App Store screenshot workflow is documented in
[`ios/AppStoreScreenshots`](ios/AppStoreScreenshots/README.md).



## Disclaimer

PnL Calendar is an independent third-party utility and is not affiliated with,
endorsed by, or sponsored by Interactive Brokers LLC or its affiliates.
Interactive Brokers and IBKR are trademarks of their respective owners.

The app is provided for informational record-keeping only. It does not execute
trades, manage funds, or provide financial, investment, tax, or legal advice.
