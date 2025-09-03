# 🔍 InstaRecon - Instagram OSINT Tool

![Python](https://img.shields.io/badge/python-v3.6+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Platform](https://img.shields.io/badge/platform-linux%20%7C%20windows%20%7C%20macos-lightgrey)

**InstaRecon** is a powerful Instagram Open Source Intelligence (OSINT) tool designed for cybersecurity professionals, penetration testers, and ethical hackers to gather publicly available information from Instagram profiles.

## ⚠️ **IMPORTANT LEGAL DISCLAIMER**

**This tool is intended for EDUCATIONAL and AUTHORIZED SECURITY TESTING purposes ONLY.**

- ✅ **Legal Use**: Authorized penetration testing, security research, educational purposes
- ❌ **Illegal Use**: Stalking, harassment, unauthorized surveillance, privacy violations
- 📋 **Your Responsibility**: Users must comply with all applicable laws and regulations
- 🏛️ **Legal Compliance**: Ensure you have proper authorization before testing any accounts
- 🔒 **Privacy Respect**: Only gather information that is publicly available

**The developers of this tool are NOT responsible for any misuse or illegal activities conducted with this software.**

## 🌟 Features

- 🔍 **User Intelligence Gathering**: Extract comprehensive public profile information
- 📊 **Engagement Analysis**: Calculate follower-to-following ratios and engagement metrics  
- 🌐 **Advanced Lookup**: Retrieve obfuscated contact information when available
- 📱 **Contact Information**: Extract public email addresses and phone numbers
- 🖼️ **Profile Media**: High-resolution profile picture URLs
- 📈 **Account Metrics**: Detailed statistics including posts, followers, and following counts
- 🏢 **Business Intelligence**: Identify business accounts and verification status
- 🔗 **External Links**: Extract website URLs and external connections
- 🚀 **Easy Setup**: Automatic dependency installation
- 💻 **Cross-Platform**: Works on Windows, macOS, and Linux

## 🛠️ Installation

### Prerequisites
- Python 3.6 or higher
- Valid Instagram account (for session ID)
- Internet connection

### Quick Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Faizee-Asad/InstaRecon.git
   cd instarecon
   ```

2. **Run the tool** (dependencies will auto-install)
   ```bash
   python instarecon.py -u target_username -s your_session_id
   ```

### Manual Installation

If you prefer to install dependencies manually:
```bash
pip install requests phonenumbers pycountry
```

## 🚀 Usage

### Basic Usage

**Search by Username:**
```bash
python instarecon.py -u username -s your_session_id
```

**Search by User ID:**
```bash
python instarecon.py -i 123456789 -s your_session_id
```

**Enable Debug Mode:**
```bash
python instarecon.py -u username -s your_session_id --debug
```

### Getting Your Instagram Session ID

1. Open Instagram in your web browser and log in
2. Open Developer Tools (`F12` or right-click → Inspect)
3. Navigate to **Application** tab → **Storage** → **Cookies** → `https://www.instagram.com`
4. Find the cookie named `sessionid`
5. Copy the **Value** field

![Session ID Guide](#)
<img width="1920" height="1080" alt="Session" src="https://github.com/user-attachments/assets/d975c2cb-07c7-42e0-8a8a-15203d00d687" />



### Command Line Options

```
Options:
  -h, --help            Show help message and exit
  -s, --sessionid       Instagram session ID (required)
  -u, --username        Instagram username to investigate
  -i, --id              Instagram user ID to investigate
  --debug               Show debug information and all available fields
  --no-banner          Skip the banner display
```

## 📊 Sample Output

```
╔══════════════════════════════════════════════════════════════╗
║                          InstaRecon                          ║
║                   Instagram OSINT Tool                       ║
║                                                              ║
║   For Penetration Testing & Ethical Hacking @Faizee-Asad     ║
╚══════════════════════════════════════════════════════════════╝

🔍 Starting reconnaissance for username: target_user
⏳ Gathering intelligence...

============================================================
INSTAGRAM RECONNAISSANCE RESULTS
============================================================

Username               : target_user
User ID                : 1234567890
Full Name              : John Doe
Verified Account       : ✓
Business Account       : ✗
Private Account        : ✗

Engagement Metrics:
Followers              : 15,432
Following              : 892
Posts                  : 156
Following/Follower Ratio: 0.06

External Links:
Website                : https://johndoe.com

Biography:
Photographer | Travel Enthusiast
📧 contact@johndoe.com
🌍 Based in New York

Public Contact Info:
Email                  : john@johndoe.com

Profile Picture        : https://instagram.com/profile_pic_url

────────────────────────────────────────────────────────────
ADVANCED RECONNAISSANCE
────────────────────────────────────────────────────────────
Obfuscated Email       : j***@g****.com
Obfuscated Phone       : +1 ***-***-1234

============================================================

🔒 Security Note: This information is publicly available
   Use responsibly and in accordance with applicable laws.
```

## 🔧 Technical Details

### Information Gathered

**Basic Profile Data:**
- Username and User ID
- Full name and biography
- Account verification status
- Business account status
- Privacy settings

**Engagement Metrics:**
- Follower count
- Following count
- Post count
- Engagement ratios

**Contact Information:**
- Public email addresses
- Public phone numbers (with country detection)
- External website links
- Obfuscated recovery information

**Media Information:**
- High-resolution profile pictures
- IGTV post counts

### Rate Limiting

Instagram implements rate limiting to prevent abuse. If you encounter rate limit errors:

- Wait 10-15 minutes between requests
- Use different session IDs if available
- Avoid making too many requests in a short time period

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Contribution Guidelines

- Follow PEP 8 coding standards
- Add comments for complex functions
- Test your changes thoroughly
- Update documentation as needed
- Respect the ethical guidelines

## 🐛 Common Issues & Troubleshooting

### "Rate limit reached"
**Solution**: Wait 10-15 minutes and try again. Consider using a different Instagram account.

### "User not found"
**Solution**: Verify the username spelling. The user might have changed their username or deleted their account.

### "Request timeout"
**Solution**: Check your internet connection and try again.

### "Invalid session ID"
**Solution**: 
1. Ensure you're logged into Instagram in your browser
2. Get a fresh session ID following the guide above
3. Make sure you copied the entire session ID value

### ModuleNotFoundError
**Solution**: The tool automatically installs dependencies. If this fails:
```bash
pip install requests phonenumbers pycountry
```

## 📚 Educational Use Cases

This tool is designed for legitimate security testing and educational purposes:

- **Penetration Testing**: Assess social media exposure during security audits
- **Security Research**: Study social engineering attack vectors
- **Digital Forensics**: Investigate public social media presence
- **Cybersecurity Training**: Demonstrate OSINT techniques
- **Privacy Awareness**: Show users what information is publicly available

## 🔒 Privacy & Ethics

**Respect Privacy**: Only gather information that is publicly available on Instagram.

**Get Authorization**: Always ensure you have proper authorization before investigating accounts.

**Follow Laws**: Comply with local laws and regulations regarding data collection and privacy.

**Use Responsibly**: Do not use this tool for harassment, stalking, or any malicious activities.

**Report Issues**: If you find vulnerabilities in Instagram's platform, report them responsibly to Meta's security team.

## ⚖️ Legal Notice

This tool accesses only publicly available information through Instagram's standard web interface. Users are responsible for ensuring their use complies with:

- Local and international privacy laws
- Instagram's Terms of Service
- Applicable cybersecurity and computer crime laws
- Ethical hacking guidelines and standards

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Instagram for providing public APIs
- The cybersecurity community for OSINT methodology
- Contributors and ethical hackers who improve the tool
- Open source libraries: `requests`, `phonenumbers`, `pycountry`

## 📞 Support & Contact

- **Issues**: Please use [GitHub Issues](https://github.com/yourusername/instarecon/issues)
- **Discussions**: Use [GitHub Discussions](https://github.com/yourusername/instarecon/discussions) for questions
- **Security**: Report security issues privately via email

---

**Remember: With great power comes great responsibility. Use this tool ethically and legally.**

⭐ If you find this tool useful for your security research, please give it a star!

---

*Developed by Asad faizee for the cybersecurity community*
