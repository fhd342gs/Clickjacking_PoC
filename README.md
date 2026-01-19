# Clickjacking PoC
A "Clickjacking" demonstration tool for security assessments.
- [CWE-1021: Improper Restriction of Rendered UI Layers or Frames](https://cwe.mitre.org/data/definitions/1021.html)
- [CAPEC-103: Clickjacking](https://capec.mitre.org/data/definitions/103.html)

<img width="1751" height="900" alt="image" src="https://github.com/user-attachments/assets/15dec245-571f-4449-a12b-780214c3f693" />

## Features
- **Multiple Attack Scenarios**: Click hijacking, credential harvesting, payment confirmation, OAuth permissions
- **Credential Harvesting Mode**: Overlay captures login credentials in real-time
- **Stealth Mode**: Invisible form borders with solid background to mask real placeholders
- **Full Positioning Controls**: Arrow pad, X/Y/W, field sizing, radius, padding, button offset
- **Attacker/Victim Views**: Toggle between setup and demonstration modes
- **Customizable Appearance**: Iframe size, field colors, border radius, text padding
- **Keyboard Shortcuts**: Arrow keys for positioning, Escape to exit victim view

## Quick Start
**Option 1: URL Parameters**
```
malicious_page.html?target=https://target.com/login&scenario=credential
```

**Option 2: Edit CONFIG**
```javascript
const CONFIG = {
    targetUrl: 'https://target.com/login',
    targetName: 'Target Corp',
    defaultScenario: 'credential'
};
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

## License
Mozilla Public License 2.0

## Disclaimer
For authorized security testing only. Use this project only on systems you own or where you have explicit written permission to test. You are solely responsible for how you use it; the author(s) assume no liability for any misuse, damage, or legal consequences resulting from use of this project or its contents.
