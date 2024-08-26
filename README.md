
# 🚀 FXBacktestBoost - Forex Market Data Scraping & Analysis Script

## 📝 Overview

This script is designed to assist with backtesting by allowing you to analyze historical market data and news events as if they were live.
This can be especially useful when using replay functions on platforms like TradingView or FXReplay.com.

### ✨ Key Features:
- **Date Synchronization**: Automatically traverses dates within a specified range and fetches data for each day (and uses cache for multiple requests)
- **Data Filtering**: Filters events based on desired currencies and impact levels.
- **Comprehensive Output**: Presents filtered data in a table format, including date, time, currency, impact, event name, actual, forecast, and previous values.
- **Backtesting Enhancement**: Ideal for boosting your backtesting experience by providing historical context in sync with market data.

## 📦 Requirements

To run this script, you need the following Python packages:

```bash
pip install undetected-chromedriver
pip install selenium
pip install tabulate
pip install pandas
pip install matplotlib
pip install pickle
pip install redis
pip install seaborn
```

### 🗄️ Redis for Caching

Caching is implemented via Redis to enhance performance, especially for repeated data fetches.
To install Redis, follow the official installation guides:

- [Redis Installation Guide](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/)
- [Redis Windows Download](https://github.com/microsoftarchive/redis/releases)

Ensure Redis is running on your machine before running the script.

### 🛠️ ChromeDriver Path

The script uses Chrome via \`undetected-chromedriver\` for scraping. The path to Chrome may differ depending on your operating system. If you are not using Windows or if Chrome is installed in a different location, you may need to update the \`chrome_path\` variable in the script:

```python
chrome_path = "/path/to/your/chrome/executable"
```

## 🚀 Usage

To use this script, follow these steps:

1. **Set Date Range**: Manually set the `start_date` and `end_date` in the script
2. **Configure Filters**: Set the desired currencies and impact levels for scraping news data
3. **Define Forex Pairs**: Specify the forex pairs you want to analyze for correlation, ordered alphabetically
4. **Set Resampling Timeframe**: Define the timeframe for resampling the forex data. The `new_timeframe` variable can be set to different values, such as:
   
   - `'1min'`: Resample to 1-minute intervals
   - `'5min'`: Resample to 5-minute intervals
   - `'15min'`: Resample to 15-minute intervals
   - `'30min'`: Resample to 30-minute intervals
   - `'1h'`: Resample to 1-hour intervals
   - `'4h'`: Resample to 4-hour intervals (default)

5. **Run the Script**

### 💡 Contributing

New requests and functionality are always welcome! If you have ideas for improvements, feel free to open an issue or submit a pull request.

## ⚠️ Legal Disclaimer

- **ForexFactory.com**: This script is not affiliated with ForexFactory.com. Scraping data from ForexFactory.com is against their Terms of Service. By using this script, you agree to take full responsibility for any consequences arising from such use.
- **No Liability**: The author of this script assumes no liability for any outcomes related to the use of this script. Use it at your own risk.

## 📄 License

This script is released under the **MIT License**. This license is a permissive open-source license that is simple and easy to understand. It places very few restrictions on reuse and is generally accepted in the open-source community.
