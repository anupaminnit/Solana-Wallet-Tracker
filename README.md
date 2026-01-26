# 🕵️ Solana Wallet Tracker

Find "diamond hands" 💎 - wallets that bought early and held strong on Solana tokens.

![Solana Wallet Tracker](https://img.shields.io/badge/Solana-Blockchain-purple?style=for-the-badge&logo=solana)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 🎯 What Does This Do?

This tool helps you identify serious believers in a Solana token by finding wallets that:
1. **Bought during a specific time window** (e.g., opening weekend)
2. **Spent a minimum amount** (e.g., at least $100)
3. **Still held the tokens** weeks later (e.g., 0.1% of total supply)

Perfect for finding potential insiders, whales, or conviction holders!

## ✨ Features

- 🔍 **Track Any Solana Token** - Just paste the contract address
- ⏰ **Time-Based Analysis** - Set buy windows and holding check times
- 💰 **Filter by Amount** - Set minimum buy thresholds in USD
- 📊 **Beautiful UI** - Modern, gradient interface with real-time results
- 🚀 **No Installation** - Runs directly in your browser
- 🔒 **Secure** - API key stored locally in browser only

## 🚀 Quick Start

### Option 1: Use Online (Recommended)
Visit: `https://anupaminnit.github.io/Solana-Wallet-Tracker/`

### Option 2: Run Locally
1. Download `index.html`
2. Open Terminal/Command Prompt
3. Navigate to the folder:
   ```bash
   cd path/to/folder
   ```
4. Start a local server:
   ```bash
   python -m http.server 8000
   ```
5. Open browser: `http://localhost:8000`

## 📋 Prerequisites

- A **BitQuery API Key** (get free at [bitquery.io](https://bitquery.io))
- A web browser (Chrome, Firefox, Safari, Edge)
- Internet connection

## 🎮 How to Use

### Step 1: Enter Your API Key
Get your free API key from [BitQuery](https://bitquery.io) and paste it in the first field.

### Step 2: Configure Your Search

| Field | Description | Example |
|-------|-------------|---------|
| **Token Contract Address** | The Solana token you want to track | `8Jx8AAHj86wbQgUTjGuj6GTTL5Ps3cqxKRTvpaJApump` |
| **Buy Window Start** | When the buying period starts | `2024-01-18 05:00 AM` |
| **Buy Window End** | When the buying period ends | `2024-01-20 09:00 AM` |
| **Holding Check Time** | When to check if they still hold | `2024-01-22 11:00 PM` |
| **Minimum Buy Amount** | Minimum USD spent during buy window | `100` |
| **Minimum Holding %** | Minimum % of supply held at check time | `0.1` |

### Step 3: Run Analysis
Click the **"🔍 Run Analysis"** button and wait 5-15 seconds.

### Step 4: View Results
See:
- Total supply of the token
- Number of buyers found in the window
- Number of "diamond hands" who met all criteria
- Detailed table with wallet addresses, amounts, and holdings

## 📊 Example Use Cases

### Find Early Whales
```
Buy Window: Token launch day (first 24 hours)
Min Buy: $1,000
Min Holding: 1% of supply
Check Time: 1 week later
```

### Identify Conviction Holders
```
Buy Window: During a dip (2-3 days)
Min Buy: $500
Min Holding: 0.5% of supply
Check Time: 1 month later
```

### Track Insider Activity
```
Buy Window: Pre-announcement period
Min Buy: $100
Min Holding: 0.1% of supply
Check Time: Post-announcement
```

## 🛠️ Technical Details

### Built With
- **HTML5** - Structure
- **TailwindCSS** - Styling
- **Vanilla JavaScript** - Logic
- **BitQuery API** - Blockchain data
- **Solana RPC** - Token supply info

### How It Works
1. **Fetches total supply** from Solana RPC
2. **Queries BitQuery** for wallets that bought during the window
3. **Calculates historical balances** at the holding check time
4. **Filters results** based on your criteria
5. **Displays diamond hands** in a sortable table

## 🔒 Security & Privacy

- ✅ API key is stored **locally in your browser only**
- ✅ No data sent to any third-party servers
- ✅ All queries go directly to BitQuery and Solana RPC
- ✅ Safe to host publicly on GitHub Pages

**Note:** If sharing publicly, users must provide their own API key.

## 📝 GitHub Pages Deployment

### Step-by-Step:
1. Create a new GitHub repository
2. Upload `index.html` to the repository
3. Go to **Settings** → **Pages**
4. Select **main branch** as source
5. Save and wait 1-2 minutes
6. Access at: `https://anupaminnit.github.io/Solana-Wallet-Tracker/`

## 🐛 Troubleshooting

### "Failed to fetch" Error
- **Solution 1:** Run on a local server (not by opening HTML directly)
- **Solution 2:** Use GitHub Pages (no CORS issues)
- **Solution 3:** Install a CORS browser extension

### "Cannot read properties of undefined"
- Check if the token address is valid
- Verify dates are in the correct format
- Ensure the token exists on Solana mainnet

### No Results Found
- Token might not have had trades during that period
- Try widening the date range
- Lower the minimum buy amount threshold
- Check if you're using the correct token address

## 📖 API Documentation

This tool uses:
- **[BitQuery Solana API](https://docs.bitquery.io/docs/examples/Solana/solana-balance-updates/)** - For DEX trades and balance history
- **[Solana RPC API](https://docs.solana.com/api/http)** - For token supply information

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 💡 Tips & Best Practices

1. **Use realistic dates** - Set dates in the past, not the future
2. **Start broad** - Begin with lower thresholds and tighten gradually
3. **Check multiple periods** - Compare early buyers vs later buyers
4. **Cross-reference** - Verify wallet activities on Solscan or Solana Explorer
5. **Rate limits** - BitQuery has rate limits; don't spam requests

## 📞 Support

- 🐛 **Report Issues:** [GitHub Issues](https://github.com/anupaminnit/solana-wallet-tracker/issues)
- 💬 **Questions:** Open a discussion on GitHub
- 📧 **Email:** anupamsd2403@outlook.com

## 🎉 Acknowledgments

- Built with ❤️ for the Solana community
- Powered by BitQuery's awesome blockchain API
- Inspired by the need to find true believers in crypto projects

---

**⚠️ Disclaimer:** This tool is for research and educational purposes only. Always verify information independently and never make investment decisions based solely on this data. Past performance does not guarantee future results.

---

Made with 🚀 by Anupam Singh

**Star ⭐ this repo if you find it useful!**
