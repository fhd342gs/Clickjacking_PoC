# Clickjacking PoC

A professional clickjacking (CWE-1021) demonstration tool for security assessments.

## Features

- **Multiple Attack Scenarios**: Click hijacking, credential harvesting, payment confirmation, OAuth permissions
- **Credential Harvesting Mode**: Overlay captures login credentials in real-time
- **Stealth Mode**: Invisible form borders with solid background to mask real placeholders
- **Full Positioning Controls**: Arrow pad, X/Y/W, field sizing, radius, padding, button offset
- **Attacker/Victim Views**: Toggle between setup and demonstration modes
- **Customizable Appearance**: Iframe size, field colors, border radius, text padding
- **Keyboard Shortcuts**: Arrow keys for positioning, Escape to exit victim view

## Quick Start

**Option 1: Edit CONFIG**
```javascript
const CONFIG = {
    targetUrl: 'https://target.com/login',
    targetName: 'Target Corp',
    defaultScenario: 'credential'
};
```

**Option 2: URL Parameters**
```
malicious_page.html?target=https://target.com/login&scenario=credential
```

## Controls

| Control | Description |
|---------|-------------|
| **Iframe Size** | Adjust iframe width × height to match target page |
| **Arrow Pad** | Move overlay position (or use keyboard arrows) |
| **X, Y, W** | Overlay position and width |
| **H, Font, Gap** | Field height, font size, spacing |
| **Rad, Pad** | Border radius and input padding |
| **Button Offset X/Y** | Position submit button independently |
| **Overlay Slider** | Overlay opacity for alignment |
| **Stealth Toggle** | Enable invisible fields mode |
| **Bg / Text Colors** | Match target form colors |

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `↑ ↓ ← →` | Move overlay (in credential mode) |
| `Escape` | Exit victim view |

## Defenses

Websites should implement:

```
X-Frame-Options: DENY
Content-Security-Policy: frame-ancestors 'none';
```

## Disclaimer

For **authorized security testing only**. Only test systems you own or have explicit permission to test.

## License

Mozilla Public License 2.0
