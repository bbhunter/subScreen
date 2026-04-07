# SubScreen

Visual subdomain reconnaissance tool. Screenshot subdomains at scale directly in your browser - zero installation, zero dependencies.

![SubScreen](css/logo.png)

## Features

- **Multi-provider support** - thum.io (free, no API key), urlbox.io, or manual tab opening
- **Smart input parsing** - handles raw domains, subfinder, httpx, amass, nmap output formats
- **Automatic deduplication** - duplicate targets are removed automatically
- **Real-time progress** - live stats, progress bar, and per-screenshot status indicators
- **Interactive gallery** - responsive grid with hover actions, status filtering, and domain search
- **Lightbox viewer** - full-size screenshot viewing with keyboard navigation (arrow keys)
- **Export reports** - download standalone HTML reports with all screenshots
- **Drag & drop** - drop `.txt` or `.csv` files directly onto the input
- **Configurable** - screenshot size, render delay for JS-heavy sites, settings persistence
- **No installation** - just open `index.html` in any modern browser
- **No dependencies** - zero external libraries, pure vanilla JS + CSS

## Usage

1. Open `index.html` in your browser (or [use it online](https://momenbasel.github.io/subScreen/))
2. Paste your subdomain list into the targets field
3. Select a provider (thum.io works out of the box, no API key needed)
4. Click **Start Scan** or press `Ctrl+Enter`

### Supported Input Formats

```
# Raw domains
sub1.example.com
sub2.example.com

# With protocols
https://sub1.example.com
http://sub2.example.com:8080

# subfinder/amass output
sub1.example.com
sub2.example.com

# httpx output
https://sub1.example.com [200] [Apache]
https://sub2.example.com [301] [nginx]

# Comma-separated
sub1.example.com, sub2.example.com, sub3.example.com

# IP addresses
192.168.1.1
10.0.0.1:8443
```

### Providers

| Provider | API Key | Cost | Notes |
|----------|---------|------|-------|
| thum.io | Not required | Free | Default, works immediately |
| urlbox.io | Required | Paid | Higher quality, more options |
| Manual | N/A | Free | Opens each URL in a new browser tab |

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Ctrl+Enter` | Start scan |
| `Escape` | Close lightbox |
| `Left/Right` arrows | Navigate screenshots in lightbox |

## Deployment

No build step required. Host the files on any static file server or use GitHub Pages:

```bash
git clone https://github.com/momenbasel/subScreen.git
cd subScreen
# Open index.html or serve with any HTTP server
python3 -m http.server 8000
```

## License

MIT
