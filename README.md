<div align="center">

# 🚀 CRYPTOSIGNAL PRO v5 BETA

**Read-only Technical Analysis Terminal for Binance Markets**

![Version](https://img.shields.io/badge/version-5.5.0--beta-blue)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-lightgrey)
![Status](https://img.shields.io/badge/status-public%20beta-orange)
![License](https://img.shields.io/badge/license-Proprietary-red)

**No account. No API keys. No access to your funds.**

[📥 Download](#-installation) • [💰 Pricing](#-pricing) • [✨ Features](#-features) • [❓ FAQ](#-faq) • [🔒 Security](#-security--privacy) • [💬 Support](#-support)

</div>

---

## 📸 Screenshot

<img width="1357" height="657" alt="image" src="https://github.com/user-attachments/assets/c9d8eee2-486e-43a7-827c-a8d6722cc5f7" />


---

## 🎯 What is CryptoSignal PRO?

CryptoSignal PRO is a Windows desktop terminal that scans the top cryptocurrency pairs on Binance Spot and Futures and produces a scored watchlist based on classical technical indicators and market microstructure data.

It uses **only public Binance market endpoints** — the same data visible on binance.com without logging in. It never asks for your account, API keys, or any credentials.

**It does:**
- Scan 20+ pairs in real time across Binance Spot and Futures
- Combine ADX, RSI, MACD, Volume Profile POC, and funding rate data into a confluence score
- Highlight conflicts between indicators instead of hiding them
- Warn about high-volatility events (CME expiry, FOMC, CPI) with Red Zone alerts
- Let you filter by session, liquidity tier, trend regime, and score

**It does not:**
- Place trades on your behalf
- Connect to your exchange account
- See your balance, positions, or history
- Promise returns or "signals that always work"
- Replace your own judgement

---

## 💰 Pricing

| Plan | Price | Notes |
|---|---|---|
| **Free Trial** | 150 hours of active use | No registration required. Full feature access. |
| **PRO** | $10 / month | Unlimited use. Cancel anytime. |

No credit card required for the trial. Payment for PRO is processed through a secure payment provider; the app itself never handles your payment data.

> Pricing is fixed during the public beta period. Early subscribers will be grandfathered at $10/month when the product exits beta.

---

## ✨ Features

### 📊 Technical Analysis
- **ADX** — trend strength and regime classification (trend ≥25 / flat <20)
- **RSI** — overbought/oversold with divergence detection
- **MACD** — signal line crosses and histogram divergences
- **Volume Profile POC** — point of control for session and daily ranges
- **ZigZag** — swing detection feeding divergence logic

### 🎯 Confluence Scoring
- 8-point checklist per pair, weighted score from −10 to +10
- Parameter calibration via walk-forward optimization on 90-day history
- Displayed Win Rate and Risk/Reward are **backtest results on historical data** — not live trading performance. See [important note](#about-backtest-numbers).

### 📈 Market Data
- Binance Spot and Futures (public REST + WebSocket endpoints)
- Funding rate history (last 7 days per symbol)
- Open interest snapshots
- Fear & Greed Index (alternative.me)
- Economic calendar (high-impact events only)

### 🔍 Filtering & Context
- Liquidity tiers: HIGH / MEDIUM / LOW / VERY LOW
- Session filter: Asia / Europe / US
- BTC correlation per pair
- **Conflict flags** — when indicators disagree, you see it
- **Red Zone warnings** — CME futures expiry, FOMC, CPI: auto-pause suggestions

### 📝 Trading Journal
- Manual trade logging (you enter trades; the app does not read them from any exchange)
- P&L and Win Rate calculation on your own entries
- CSV and JSON export for your own analysis
- Stored locally only — never uploaded

---

## 📥 Installation

### System Requirements
| | Minimum | Recommended |
|---|---|---|
| OS | Windows 10 (64-bit) | Windows 11 (64-bit) |
| RAM | 4 GB | 8 GB |
| Disk | 50 MB | 50 MB |
| Network | Stable connection | Wired / low-latency |

### Installing the Beta

1. Go to **[Releases](../../releases)**
2. Download `CryptoSignalPRO_Setup_v5.5.0.zip`
3. Run the installer and follow the wizard
4. Launch from Start Menu → CryptoSignal PRO
5. Your 150-hour free trial starts on first launch

> ⚠️ **SmartScreen warning:** This beta is not yet code-signed. Windows will show _"Windows protected your PC"_. Click **More info → Run anyway**. A signed release is planned for v5.6.
>
> If you prefer not to run unsigned binaries, wait for the signed release — that's a reasonable choice.

---

## 🔒 Security & Privacy

**Does CryptoSignal PRO need my Binance account or API keys?**

**No.** The app uses only public Binance market endpoints — the same ones any price chart website uses. You don't log in, you don't connect your account, you don't paste any keys.

**What this means in practice:**
- The app **cannot see your balance**
- The app **cannot place or cancel trades**
- The app **cannot withdraw funds**
- The app **does not know who you are on Binance**

It only reads public market data: prices, candles, order book depth, funding rates, open interest.

**Network activity:**
- Outbound connections only to: `api.binance.com`, `fapi.binance.com`, `alternative.me` (Fear & Greed Index), and the license/update endpoint
- The license endpoint sends only an anonymous machine ID and subscription status — no personal data, no browsing data, no trade data
- No user behaviour telemetry

**Trading journal:**
- Manual entry only — you type in your trades; the app does not fetch them from any exchange
- Stored locally in `%APPDATA%\CryptoSignalPRO\journal.db`
- Never uploaded anywhere

---

## ❓ FAQ

**Does this place trades for me?**  
No. CryptoSignal PRO is read-only. It shows signals; you place trades yourself on the exchange of your choice.

**Do I need to register or create an account?**  
No for the trial. A minimal account (email only) is needed for PRO subscription management.

**Do I need a Binance API key?**  
No. The app uses public Binance endpoints only.

**What exchanges are supported?**  
Binance Spot and Futures in v5. Bybit and OKX are on the roadmap.

**What happens after my 150 free hours?**  
The app switches to a limited view (top 3 pairs, no filters). You can subscribe to PRO to restore full access, or keep using the limited view for free.

**Can I cancel my subscription anytime?**  
Yes. Cancel from your account page; access continues until the end of the paid period.

**Why is Windows blocking the installer?**  
The beta isn't code-signed yet. A Sectigo certificate is planned for v5.6. Until then, SmartScreen will warn. This is normal for unsigned software.

**<a name="about-backtest-numbers"></a>Are the "Win Rate" numbers real trading results?**  
**No — they are results from 90-day backtests on historical data.** Past performance does not predict future results. There is no live, audited trading track record. Treat the scoring as a filtering aid, not a prediction.

**Is the source code available?**  
Currently closed-source. The GUI and indicator layers are planned to be open-sourced in v5.7 while the calibration engine remains proprietary.

**Where is the company based?**  
Czech Republic, European Union. Contact details below.

---

## ⚠️ Risk Disclaimer

**This software is an analysis tool, not financial advice.**

Cryptocurrency trading involves substantial risk, including:

- Extreme price volatility
- **Possible total loss** of invested capital
- Leverage amplifies losses as well as gains
- Exchange, counterparty, and custody risks

No indicator, including any produced by this software, predicts the future. Technical analysis describes probabilities, not certainties. Backtest results shown in the application are historical simulations — they are **not a promise of future performance**.

**Invest only what you can afford to lose. Do your own research. Consider consulting a licensed financial advisor.**

This software is provided "AS IS" without warranty of any kind. The author accepts no liability for any losses arising from its use.

---

## 🐞 Known Issues (v5.5.0 beta)

- SmartScreen warning on first launch (see [Installation](#-installation))
- Economic calendar may show events in UTC regardless of local timezone setting
- Rare WebSocket reconnect stall after network change — restart the app
- Multi-monitor DPI scaling imperfect on mixed-DPI setups
- Trial counter resets if system clock is changed (will be fixed in v5.6)

Please report new issues at [GitHub Issues](../../issues) with your Windows version and a log snippet from `%APPDATA%\CryptoSignalPRO\logs\`.

---

## 🗺️ Roadmap

- **v5.6** — Code signing, auto-updater, Bybit support, trial counter hardening
- **v5.7** — Open-source GUI and indicators layer, OKX support
- **v6.0** — TradingView webhook output, custom alert rules, mobile companion app

---

## 📜 License

Proprietary license — see [LICENSE.txt](LICENSE.txt).

- ✅ Personal use under free trial or active PRO subscription
- ❌ Redistribution, resale, or sublicensing
- ❌ Reverse engineering, decompilation, or circumvention of the trial mechanism
- ❌ Commercial use without written permission

---

## 💬 Support & Contact

- **Email:** cryptosignalc@gmail.com
- **Bug reports:** [GitHub Issues](../../issues) _(preferred)_
- **Feature requests:** [GitHub Discussions](../../discussions)
- **Telegram channel:** _(coming soon)_

Response time: typically within 48 hours on weekdays.

---

<div align="center">

**CryptoSignal PRO** — built in 🇨🇿 Czech Republic  
© 2024–2026 · All rights reserved

</div>
