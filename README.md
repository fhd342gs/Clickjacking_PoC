# Clickjacking PoC

A professional clickjacking (CWE-1021) demonstration tool for security assessments.

## Features

- **Multiple Attack Scenarios**: Click hijacking, credential harvesting, payment confirmation, OAuth permissions
- **Credential Harvesting Mode**: Transparent overlay captures login credentials
- **Stealth Mode**: Invisible form fields with visible text input
- **Positioning Controls**: Arrow pad, X/Y/W inputs, field size adjustments
- **Attacker/Victim Views**: Toggle between setup and demonstration modes
- **URL Parameters**: Configure via query string for easy deployment

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

## URL Parameters

| Parameter | Description |
|-----------|-------------|
| `target` | Target URL to embed |
| `scenario` | `custom`, `social`, `payment`, `permissions`, `danger`, `credential` |
| `formX`, `formY`, `formW` | Overlay position and width |
| `fieldH`, `fieldFont`, `fieldGap` | Field height, font size, spacing |

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
