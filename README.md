# 🛡️ Database Leak Checker

> Enterprise-grade database breach intelligence platform for security professionals

An advanced web application that leverages the LeakCheck.io API to search and analyze data breaches across 20+ billion leaked credentials from compromised databases worldwide.

<<<<<<< HEAD
![Platform Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-blue)
![LeakCheck API](https://img.shields.io/badge/API-LeakCheck%20v2-cyan)
![Platform](https://img.shields.io/badge/platform-web-brightgreen)
=======
![Platform Preview](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-blue)
![LeakCheck API](https://img.shields.io/badge/API-LeakCheck%20v2-cyan)
>>>>>>> 08854d8a5dffdf7ad971964f4d7a9ebca63e3763

## 🚀 Features

- **Multi-Type Search** - Email, username, domain, phone number, password hash, and keyword lookups
- **Real-Time Analysis** - Instant breach detection with detailed exposure reports
- **Visual Intelligence** - Interactive dashboard with breach statistics and severity indicators
- **Search History** - Persistent tracking of all queries with localStorage
- **Advanced Filtering** - Auto-detection of query types with manual override options
- **Critical Alerts** - Automatic detection of password, SSN, and credit card exposures
- **Responsive Design** - Modern dark-themed UI optimized for Windows 11 and all devices
- **Zero Dependencies** - Pure vanilla JavaScript, no build tools required
<<<<<<< HEAD
- **Enterprise UI** - Glassmorphic design with smooth animations and transitions
=======
>>>>>>> 08854d8a5dffdf7ad971964f4d7a9ebca63e3763

## 🎯 Live Demo

**[Launch Application](https://ritacsolutionsllc.github.io/leak-checker-app)**

## 📋 Prerequisites

<<<<<<< HEAD
- Modern web browser (Chrome 100+, Firefox 100+, Edge 100+, Safari 15+)
- LeakCheck.io API key ([Get your key](https://leakcheck.io/api))
- Internet connection for API access

## 🔧 Installation

### Option 1: Use Directly (No Installation)

Simply visit the [live application](https://ritacsolutionsllc.github.io/leak-checker-app) and enter your API key when prompted.
=======
- Modern web browser (Chrome, Firefox, Edge, Safari)
- LeakCheck.io API key ([Get your key](https://leakcheck.io/api))
- Basic understanding of data breach concepts

## 🔧 Installation

USAGE EXAMPLES:
### Option 1: Use Directly (No Installation)

Simply visit the [live application](https://ritacsolutionsllc.github.io/leak-checker-app) and enter your API key when prompted.
## 📚 Detailed Usage Examples

### Basic Search Workflow

1. **Open the application** in your browser
2. **Enter your LeakCheck.io API key** when prompted (first search only per session)
3. **Select query type** from dropdown:
   - Auto-detect (default)
   - Email
   - Username
   - Domain
   - Phone
   - Hash
   - Keyword
4. **Enter search query** in the input field
5. **Click "Search Breaches"** to initiate lookup
6. **Review results** including breach sources, exposed fields, and dates

### Example Searches

#### Email Search
>>>>>>> 08854d8a5dffdf7ad971964f4d7a9ebca63e3763

### Option 2: Run Locally

```bash
# Clone the repository
git clone https://github.com/ritacsolutionsllc/leak-checker-app.git

# Navigate to directory
cd leak-checker-app

<<<<<<< HEAD
# Open in browser (Windows)
start index.html

# Open in browser (Mac)
open index.html

# Open in browser (Linux)
xdg-open index.html
```

## 🔑 API Setup

1. Sign up at [LeakCheck.io](https://leakcheck.io/) and obtain your API key
2. Open the application
3. Perform your first search - you'll be prompted for your API key
4. API key is stored only in your current browser session for security
5. Start investigating breaches!

**Security Note**: API keys are never stored in code or localStorage - you'll enter it per session for maximum security.

## 💻 Usage

### Search Types

| Type | Example | Description |
|------|---------|-------------|
| Email | `user@example.com` | Search by email address |
| Username | `johndoe123` | Search by username |
| Domain | `example.com` | Search all breaches from domain |
| Phone | `12063428631` | Search by phone number |
| Hash | `31c5543c1734d25c` | Search by SHA256 email hash |
| Keyword | `example` | General keyword search |

### Dashboard Overview

- **Total Searches** - Lifetime query count stored locally
- **Compromised Accounts** - Number of breaches detected
- **Clean Results** - Searches with no exposures found
- **Total Breaches** - Aggregate breach count across all searches

### Breach Details

Each breach result displays:
- Source database name and breach date
- Exposed data fields (email, password, name, address, etc.)
- Critical field indicators (🔴 passwords, 📧 emails)
- Severity badges for sensitive data

## 📚 Detailed Usage Examples

### Basic Search Workflow

1. Open the application in your browser
2. Enter your LeakCheck.io API key when prompted (first search only per session)
3. Select query type from dropdown (Auto-detect recommended)
4. Enter search query in the input field
5. Click "Search" to initiate lookup
6. Review results including breach sources, exposed fields, and dates

### Example Searches

#### Email Search
```
Query: john.doe@example.com
Type: Email (auto-detected)
Result: Shows all breaches containing this email address
```

#### Domain-Wide Search
```
Query: example.com
Type: Domain
Result: Shows all breaches from @example.com email addresses
```

#### Username Search
```
Query: johndoe123
Type: Username
Result: Shows breaches where this username appears
```

## 🛠️ Technology Stack

- **Frontend**: Pure Vanilla JavaScript (ES6+)
- **Styling**: Inline CSS with gradient effects and glassmorphism
- **Storage**: localStorage for search history
- **API**: LeakCheck.io REST API v2
- **Hosting**: GitHub Pages
- **Design**: Responsive, dark-themed UI

## 🔐 Security Features

- ✅ No API key storage in code or browser
- ✅ HTTPS-only API communication
- ✅ Client-side only processing (no backend)
- ✅ No sensitive data persistence beyond current session
- ✅ Automatic password exposure detection
- ✅ Rate limiting through LeakCheck API

## 🔧 API Integration Code

### Core Search Function

```javascript
async function performSearch(query, queryType) {
    const apiKey = prompt('Enter your LeakCheck.io API key:');
    
    try {
        const response = await fetch(
            `https://leakcheck.io/api/v2/query/${encodeURIComponent(query)}${
                queryType !== 'auto' ? `?type=${queryType}` : ''
            }`,
            {
                headers: {
                    'Accept': 'application/json',
                    'X-API-Key': apiKey
                }
            }
        );

        if (!response.ok) {
            throw new Error(`API Error: ${response.status}`);
        }

        const data = await response.json();
        displayResults(data);
        
    } catch (error) {
        console.error('Search failed:', error.message);
    }
}
```

### API Response Structure

```javascript
{
  "success": true,
  "found": 3,
  "quota": 9997,
  "result": [
    {
      "line": "user@example.com:password123:John Doe",
      "source": {
        "name": "Collection1",
        "date": "2019-01-07",
        "breach_date": "2019-01-07"
      },
      "fields": [
        "email",
        "password",
        "fullname"
      ]
    }
  ]
}
```

## 📊 Sample Output

### Clean Result
```
✅ No Breaches Found
"john.doe@secure-domain.com" appears to be safe - no data breaches found in our database
API Quota Remaining: 9,999
```

### Compromised Result
```
⚠️ 3 Breaches Detected
"test@example.com" has been compromised in 3 known data breaches

🔴 Critical: Password Exposure Detected
Passwords or authentication credentials were found in the breached data. Immediate action required!

Exposed Fields: 🔴 password, 📧 email, username, fullname, phone

Breach Sources:
├─ Collection1 (2019-01-07) - email, password, username
├─ LinkedIn (2016-05-18) - email, fullname, password
└─ Dropbox (2012-07-01) - email, password
```

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Development Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/enhancement`)
3. Commit changes following [Conventional Commits](https://www.conventionalcommits.org/)
4. Push to branch (`git push origin feature/enhancement`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This tool is intended for legitimate security research, breach notification, and personal data protection purposes only. Users are responsible for complying with applicable laws and regulations, including GDPR, CCPA, and CFAA. RITAC Solutions LLC is not responsible for misuse of this application.

## 🆘 Support & Reporting

- **GitHub Issues**: [Report bugs or suggest features](https://github.com/ritacsolutionsllc/leak-checker-app/issues)
- **Security Issues**: See [SECURITY.md](SECURITY.md) for vulnerability reporting
- **Email**: ritacsolutions@gmail.com
- **LeakCheck Documentation**: [LeakCheck API Docs](https://leakcheck.io/api)

## 🎖️ Credits

- **API Provider**: [LeakCheck.io](https://leakcheck.io/)
- **Developer**: RITAC Solutions LLC
- **Icons**: Unicode emoji characters

## 📈 Roadmap

- [ ] Export breach reports to PDF/CSV
- [ ] Multi-query batch processing
- [ ] Advanced filtering and sorting
- [ ] Email notification for new breaches
- [ ] Integration with Have I Been Pwned API
- [ ] Python CLI wrapper integration
- [ ] Dark/light theme toggle
- [ ] Browser extension version

---

**Built with 🔐 by [RITAC Solutions LLC](https://github.com/ritacsolutionsllc)**

*Protecting digital identities through breach intelligence*
=======
# Open in browser
start index.html

Detailed Info
🔑 API Setup
Sign up at LeakCheck.io and obtain your API key

Open the application

Enter your API key when prompted during search

Start investigating breaches

Security Note: API keys are never stored in code or localStorage - you'll enter it per session for security.

💻 Usage
Search Types
Type	Example	Description
Email	user@example.com	Search by email address
Username	johndoe123	Search by username
Domain	example.com	Search all breaches from domain
Phone	12063428631	Search by phone number
Hash	31c5543c1734d25c	Search by SHA256 email hash
Keyword	example	General keyword search
Dashboard Overview
Total Searches - Lifetime query count

Compromised Accounts - Number of breaches detected

Clean Results - Searches with no exposures

Total Breaches - Aggregate breach count across all searches

Breach Details
Each breach result displays:

Source database name and breach date

Exposed data fields (email, password, name, address, etc.)

Critical field indicators (🔴 passwords, 📧 emails)

Severity badges for sensitive data

🛠️ Technology Stack
Frontend: Pure Vanilla JavaScript (ES6+)

Styling: Inline CSS with gradient effects

Storage: localStorage for search history

API: LeakCheck.io REST API v2

Hosting: GitHub Pages

📊 API Integration
This application integrates with LeakCheck.io API v2 endpoints:

javascript
GET https://leakcheck.io/api/v2/query/{query}?type={type}
Headers: X-API-Key: your_api_key
Supported Query Types: auto, email, domain, username, phone, hash, keyword

🔐 Security Features
✅ No API key storage in code or browser

✅ HTTPS-only API communication

✅ Client-side only processing (no backend)

✅ No sensitive data persistence

✅ Automatic password exposure detection

✅ Rate limiting through LeakCheck API

🤝 Contributing
Contributions are welcome! This project is maintained by RITAC Solutions LLC.

Development Guidelines
Fork the repository

Create a feature branch (git checkout -b feature/enhancement)

Commit changes (git commit -m 'Add new feature')

Push to branch (git push origin feature/enhancement)

Open a Pull Request

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

⚠️ Disclaimer
This tool is intended for legitimate security research, breach notification, and personal data protection purposes only. Users are responsible for complying with applicable laws and regulations, including GDPR, CCPA, and CFAA. RITAC Solutions LLC is not responsible for misuse of this application.

🆘 Support
Issues: GitHub Issues

Email: ritacsolutions@gmail.com

Documentation: LeakCheck API Docs

🎖️ Credits
API Provider: LeakCheck.io

Developer: RITAC Solutions LLC

Icons: Unicode emoji characters

📈 Roadmap
 Export breach reports to PDF/CSV

 Multi-query batch processing

 Advanced filtering and sorting

 Email notification for new breaches

 Integration with HIBP API

 Python CLI wrapper integration

 Dark/light theme toggle

Built with 🔐 by RITAC Solutions LLC

Protecting digital identities through breach intelligence
>>>>>>> 08854d8a5dffdf7ad971964f4d7a9ebca63e3763
