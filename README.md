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
- 🔒 **Secure** - Your API key never leaves your browser
- 🔗 **GMGN Integration** - Click any wallet to view on GMGN
- 📋 **One-Click Copy** - Copy wallet addresses instantly

## 🚀 Quick Start

### Option 1: Use Online (Recommended)
Visit: **[https://anupaminnit.github.io/solana-wallet-tracker/](https://anupaminnit.github.io/solana-wallet-tracker/)**

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/anupaminnit/solana-wallet-tracker.git

# Navigate to the folder
cd solana-wallet-tracker

# Start a local server
python -m http.server 8000

# Open browser
# Visit: http://localhost:8000
```

## 📋 Prerequisites

### Required:
- **BitQuery API Key** - [Get free key here](https://bitquery.io) (see setup below)
- **Web browser** (Chrome, Firefox, Safari, Edge)
- **Internet connection**

### Getting Your BitQuery API Key (Free):

1. **Sign up at BitQuery**
   - Visit [https://bitquery.io](https://bitquery.io)
   - Click "Sign Up" or "Get Started"
   - Create your free account

2. **Get Your API Key**
   - Log in to your BitQuery account
   - Go to your dashboard
   - Find your API key in the "API" section
   - Copy the key (starts with `ory_at_...`)

3. **Enter in the Tool**
   - Paste your API key in the "BitQuery API Key" field
   - The tool will remember it for your session
   - Your key is stored locally in your browser only

**💡 Note**: BitQuery's free tier includes enough requests for regular use!

## 🎮 How to Use

### Step 1: Enter Your API Key
Paste your BitQuery API key in the first field. This is required to fetch blockchain data.

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
The tool will show:
- **Total supply** of the token
- **Number of buyers** found in the window
- **Number of "diamond hands"** who met all criteria
- **Detailed table** with:
  - Full wallet addresses (clickable to GMGN)
  - Amount bought in USD
  - Current balance
  - Percentage of supply held

### Step 5: Analyze Wallets
- **Click any wallet address** → Opens GMGN analytics in new tab
- **Click 📋** → Copies wallet address to clipboard
- Cross-reference on [Solscan](https://solscan.io) or [Solana Explorer](https://explorer.solana.com)

## 📊 Example Use Cases

### 🎯 Find Early Whales
```
Buy Window: Token launch day (first 24 hours)
Min Buy: $1,000
Min Holding: 1% of supply
Check Time: 1 week later
```
**Result**: Find wallets that bought big on day 1 and still holding strong.

### 💎 Identify Conviction Holders
```
Buy Window: During a dip (2-3 days)
Min Buy: $500
Min Holding: 0.5% of supply
Check Time: 1 month later
```
**Result**: Discover who had the conviction to buy the dip and hold.

### 🔍 Track Insider Activity
```
Buy Window: Pre-announcement period
Min Buy: $100
Min Holding: 0.1% of supply
Check Time: Post-announcement
```
**Result**: Identify potential insiders who bought before news.

## 🛠️ Technical Details

### Built With
- **HTML5** - Structure
- **TailwindCSS** - Styling
- **Vanilla JavaScript** - Logic
- **BitQuery API** - Blockchain data
- **Solana RPC** - Token supply info

### How It Works
1. **Fetches total supply** from Solana RPC
2. **Queries BitQuery** for wallets that bought during the specified window
3. **Calculates historical balances** at the holding check time
4. **Filters results** based on your criteria
5. **Displays diamond hands** in a sortable table with GMGN links

### Data Sources
- **BitQuery Solana API** - For historical trades and balance snapshots
- **Solana RPC API** - For token supply information
- **GMGN.ai** - For wallet analytics (external link)

## 🔒 Security & Privacy

### Your Data is Safe
- ✅ **API key stored locally** in your browser only
- ✅ **No data sent to third-party servers** (except BitQuery & Solana)
- ✅ **All queries go directly** to BitQuery and Solana RPC
- ✅ **Open source** - inspect the code yourself
- ✅ **No tracking or analytics**

### Best Practices
- 🔐 Never share your API key publicly
- 🔐 Don't commit API keys to GitHub
- 🔐 Revoke and regenerate if exposed
- 🔐 Use BitQuery's free tier for testing

## 🐛 Troubleshooting

### "Failed to fetch" Error
**Cause**: CORS restrictions or network issues

**Solutions**:
1. ✅ Run on a local server (not by opening HTML directly)
2. ✅ Use GitHub Pages (recommended)
3. ✅ Check internet connection
4. ✅ Verify API key is valid

**How to run local server**:
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server
```

### "Cannot read properties of undefined"
**Cause**: Token doesn't exist or RPC issue

**Solutions**:
- ✅ Verify the token address is correct
- ✅ Check token exists on Solana mainnet
- ✅ Ensure dates are in correct format (YYYY-MM-DDTHH:MM)

### No Results Found
**Possible Reasons**:
- Token might not have had trades during that period
- Try widening the date range
- Lower the minimum buy amount threshold
- Check you're using the correct token address
- Verify dates are in the past (not future)

### API Rate Limits
**Free Tier Limits**:
- BitQuery free tier has rate limits
- If you hit limits, wait a few minutes
- Consider upgrading for higher limits
- Space out your queries

## 💡 Tips & Best Practices

### Getting Better Results
1. **Use realistic dates** - Set dates in the past, not the future
2. **Start broad** - Begin with lower thresholds and tighten gradually
3. **Check multiple periods** - Compare early buyers vs later buyers
4. **Cross-reference** - Verify wallet activities on multiple explorers
5. **Be patient** - Complex queries may take 10-15 seconds

### Avoiding False Positives
- High holdings don't always mean good investment
- Could be developer wallets
- Could be exchange wallets
- Could be locked/burned tokens
- Always do additional research (DYOR)

### Finding the Right Tokens
- Use recent launches (less than 30 days old)
- Look for tokens with actual trading activity
- Avoid tokens with suspicious patterns
- Check if liquidity is locked

## 📖 API Documentation

This tool uses:
- **[BitQuery Solana API](https://docs.bitquery.io/docs/examples/Solana/solana-balance-updates/)** - For DEX trades and balance history
- **[Solana RPC API](https://docs.solana.com/api/http)** - For token supply information

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions
- Add more filter options
- Export results to CSV/Excel
- Add wallet labeling feature
- Integrate more analytics platforms
- Add historical tracking charts
- Multi-token comparison

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 💬 Support

- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/anupaminnit/solana-wallet-tracker/issues)
- 💡 **Feature Requests**: [GitHub Discussions](https://github.com/anupaminnit/solana-wallet-tracker/discussions)
- 📧 **Email**: anupamsd2403@outlook.com

## 🙏 Acknowledgments

- **BitQuery** - For excellent blockchain data API
- **Solana** - For the fast, scalable blockchain
- **GMGN.ai** - For wallet analytics integration
- **The Community** - For feedback and support

## ⚠️ Disclaimer

**This tool is for research and educational purposes only.**

- This is NOT financial advice
- Cryptocurrency trading carries substantial risk
- Past performance does not indicate future results
- The developer is not liable for any financial losses
- Always verify information from multiple sources
- Only invest what you can afford to lose
- Do your own research (DYOR) before making investment decisions

**Use at your own risk. Trading cryptocurrencies can result in the loss of your entire investment.**

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/anupaminnit/solana-wallet-tracker?style=social)
![GitHub forks](https://img.shields.io/github/forks/anupaminnit/solana-wallet-tracker?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/anupaminnit/solana-wallet-tracker?style=social)

---

## 🔗 Related Projects

- [Solana Token Sniper](https://github.com/anupaminnit/solana-token-sniper) - Detect new token launches
- More coming soon...

---

**⭐ Star this repo if you find it useful!**

**Made with ❤️ by [Anupam](https://github.com/anupaminnit) for the Solana community**

---

*Last Updated: January 2026*
