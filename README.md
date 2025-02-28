# 🚀 FXBacktestBoost - Forex Market Data Scraping & Analysis Script

## 📝 Overview

FXBacktestBoost helps you analyze historical market data and news events in sync, enhancing your backtesting experience. It's perfect for platforms like TradingView or FXReplay.com, giving you a live market feel when replaying past market conditions.

### ✨ Key Features:
- **Automatic Date Sync**: Easily traverse through date ranges and automatically fetch market and news data for each day. Cached results speed up repeated requests.
- **Custom Filters**: Filter news events by specific currencies and impact levels.

## 📦 Requirements

You'll need the following Python packages:

```bash
pip install undetected-chromedriver selenium tabulate pandas matplotlib redis seaborn
```

### 🗄️ Redis for Caching

The script uses Redis to store and quickly retrieve data. You can install Redis by following these official guides:

- [Redis Installation Guide](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/)
- [Redis for Windows](https://github.com/microsoftarchive/redis/releases)

Ensure Redis is running on your machine before running the script.

### 🛠️ ChromeDriver Setup

The script uses Chrome via `undetected-chromedriver` for scraping. If Chrome is installed in a custom location, update the `chrome_path` in the script:

```python
chrome_path = "/path/to/your/chrome/executable"
```

## 🚀 How to Use

1. **Set Date Range**: Define `start_date` in the script. The script automatically pulls data for 7 days before the start date by default (correlation matrix).
2. **Customize Filters**: Specify the currencies and impact levels you want to analyze.
3. **Define Forex Pairs**: Add the forex pairs (in alphabetical order) for correlation analysis.
4. **Choose a Timeframe**: Set the resampling interval for the market data. Adjust the `new_timeframe` variable to one of the following:
   - `'1min'`: 1-minute intervals
   - `'5min'`: 5-minute intervals
   - `'15min'`: 15-minute intervals
   - `'30min'`: 30-minute intervals
   - `'1h'`: 1-hour intervals
   - `'4h'`: 4-hour intervals (default)

5. **Run the Script**

### 💡 Contributing

If you have ideas or want to add features, feel free to open an issue or submit a pull request!

## ⚠️ Legal Disclaimer

- **ForexFactory.com**: This script is not affiliated with ForexFactory.com, and scraping their data may violate their Terms of Service. Use at your own discretion and responsibility.

## 📄 License

This project is released under the **MIT License**, meaning it's open-source with very few restrictions on usage and modification.