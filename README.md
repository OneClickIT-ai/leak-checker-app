# 🛡️ Database Leak Checker

> Enterprise-grade database breach intelligence platform for security professionals

An advanced web application that leverages the LeakCheck.io API to search and analyze data breaches across 20+ billion leaked credentials from compromised databases worldwide.

![Platform Preview](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-blue)
![LeakCheck API](https://img.shields.io/badge/API-LeakCheck%20v2-cyan)

## 🚀 Features

- **Multi-Type Search** - Email, username, domain, phone number, password hash, and keyword lookups
- **Real-Time Analysis** - Instant breach detection with detailed exposure reports
- **Visual Intelligence** - Interactive dashboard with breach statistics and severity indicators
- **Search History** - Persistent tracking of all queries with localStorage
- **Advanced Filtering** - Auto-detection of query types with manual override options
- **Critical Alerts** - Automatic detection of password, SSN, and credit card exposures
- **Responsive Design** - Modern dark-themed UI optimized for Windows 11 and all devices
- **Zero Dependencies** - Pure vanilla JavaScript, no build tools required

## 🎯 Live Demo

**[Launch Application](https://ritacsolutionsllc.github.io/leak-checker-app)**

## 📋 Prerequisites

- Modern web browser (Chrome, Firefox, Edge, Safari)
- LeakCheck.io API key ([Get your key](https://leakcheck.io/api))
- Basic understanding of data breach concepts

## 🔧 Installation

### Option 1: Use Directly (No Installation)

Simply visit the [live application](https://ritacsolutionsllc.github.io/leak-checker-app) and enter your API key when prompted.

### Option 2: Run Locally

```bash
# Clone the repository
git clone https://github.com/ritacsolutionsllc/leak-checker-app.git

# Navigate to directory
cd leak-checker-app

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
