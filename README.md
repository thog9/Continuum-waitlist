# Continuum Waitlist Auto Bot 🚀

This Python script empowers you to interact seamlessly with the C8ntinuum platform, automating the email verification, embedded wallet creation, and referral redemption process.

🔗 Register: [C8ntinuum](https://app.c8ntinuum.com?ref=29QUG1TB)

## ✨ Features Overview

### General Features

- **Multi-Account Support**: Creates multiple accounts with automatic referral redemption.
- **Central Menu System**: Interactive menu for easy script selection via `main.py`.
- **Colorful CLI**: Uses `colorama` for visually appealing output with colored text and borders.
- **Asynchronous Execution**: Built with `asyncio` for efficient API interactions.
- **Error Handling**: Comprehensive error catching for API requests and OTP retrieval.
- **Vietnamese Interface**: Full Vietnamese language support with proper diacritics.
- **Proxy Support**: Supports HTTP, HTTPS, and SOCKS5 proxies for network requests.

### Included Features

✨ **Automated Email Verification** (`autoreff.py`)

- ✅ Temporary email generation using otpmail.vn
- ✅ Automatic domain selection from available domains
- ✅ Domain retry mechanism (3 attempts with fallback)
- ✅ Multi-threading support for multiple accounts (Semaphore 5)

✨ **OTP Retrieval & Verification**

- ✅ Automatic OTP code retrieval from email inbox
- ✅ Real-time inbox polling (120s timeout)
- ✅ OTP code extraction and verification
- ✅ Retry mechanism for failed OTP retrieval

✨ **Captcha Solving**

- ✅ Turnstile captcha solving via 2Captcha / Anti-Captcha / CapSolver / Yescaptcha / CapMonster
- ✅ Automatic API key detection from saved files

✨ **Privy Authentication Flow**

- ✅ Passwordless email OTP authentication
- ✅ Embedded wallet creation (SIWE signing)
- ✅ Session refresh for identity token with wallet
- ✅ 15s delay between retries (respect Privy 5 req/min rate limit)

✨ **Referral Code Redemption**

- ✅ Automatic referral code linking via C8 API
- ✅ Profile fetch with referral code display
- ✅ Account state tracking

✨ **Proxy Support**

- ✅ HTTP/HTTPS proxy support
- ✅ SOCKS4/SOCKS5 proxy support via `aiohttp_socks`
- ✅ Proxy authentication support
- ✅ IP address verification

## 🛠️ Prerequisites

Before running the scripts, ensure you have the following installed:

- Python 3.8+
- `pip` (Python package manager)
- **Dependencies**: Install via `pip install -r requirements.txt`
- **Captcha API Key**: Register at 2Captcha, Anti-Captcha, CapSolver, Yescaptcha, or CapMonster
- **proxies.txt** (optional): Add proxy addresses for network requests

## 📦 Installation

1. **Clone this repository:**
   ```sh
   git clone https://github.com/thog9/Continuum-waitlist.git
   cd Continuum-waitlist
   ```
2. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
3. **Prepare Proxy File (optional):**
   - Create `proxies.txt` for specific operations:
   ```
   ip:port:user:pass
   ```
   Format examples:
   ```
   http://username:password@proxy.com:8080
   socks5://username:password@proxy.com:1080
   192.168.1.1:8080:user:pass
   ```
4. **Run:**
   ```sh
   python autoreff.py
   ```
   - Enter your referral code
   - Enter the number of accounts to create
   - Select captcha service (first run only)

## 📁 Project Structure

```
Continuum-waitlist/
├── main.py              # Central menu launcher
├── proxies.txt          # Proxies file (optional)
├── accounts_c8.txt      # Generated accounts (auto-created)
├── 2captchakey.txt      # 2Captcha API key (auto-created)
├── anticaptchakey.txt   # Anti-Captcha API key (auto-created)
├── capsolverkey.txt     # CapSolver API key (auto-created)
├── requirements.txt     # Python dependencies
├── README.md            # This file
└── scripts/             # Other scripts (Continuum project)
    └── autoreff.py      # C8ntinuum auto referral bot

```

## 📊 Output Format

Generated accounts are saved in `accounts_c8.txt` with the following format:
```
Email: xxx@domain.com | Wallet: 0x... | PK: 0x... | Ref: XXXXXX | Token: xxxxxxxxxxxx
```

## 📨 Contact

Connect with us for support or updates:

- **Telegram**: [thog099](https://t.me/thog099)
- **Channel**: [CHANNEL](https://t.me/thogairdrops)
- **Group**: [GROUP CHAT](https://t.me/thogchats)
- **X**: [Thog](https://x.com/thog099)

---

## ☕ Support Us

Love these scripts? Fuel our work with a coffee!

🔗 BUYMECAFE: [BUY ME CAFE](https://buymecafe.vercel.app/)

🔗 WEBSITE: [BUY SCRIPTS](https://thogtoolhub.com/)
