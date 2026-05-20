# Mini Vulnerability Scanner

A lightweight web-based vulnerability scanner tool that performs basic security checks on websites.

## Overview

The Mini Vulnerability Scanner is a client-side HTML application that analyzes URLs for common security vulnerabilities and misconfigurations. It provides a quick assessment of website security posture.

## Features

- **HTTPS Detection**: Checks if a website uses secure HTTPS protocol
- **Port Status Monitoring**: Identifies open HTTP (Port 80) and HTTPS (Port 443) ports
- **Configuration Analysis**: Detects weak configuration indicators (e.g., "test" or "demo" in URLs)
- **Software Version Detection**: Identifies outdated or legacy software from URL patterns
- **Real-time Scanning**: Simulates scanning with visual feedback
- **Scan Reports**: Generates detailed vulnerability reports with timestamps
- **Print-Friendly Reports**: Export scan results as printable documents
- **Download Report**: Save or print the generated vulnerability report

## How to Use

1. Open `vulnerablility_scanner.html` in your web browser
2. Enter a website URL in the input field (e.g., `https://example.com`)
3. Click the **Scan** button
4. Wait for the scan to complete (2-second simulation)
5. Review the vulnerability report displayed below
6. Click the **Download Report** button to print or save the report (shows alert if no report is available)

## User Interface

- **Input Field**: Enter the target website URL
- **Scan Button**: Initiate the vulnerability scan
- **Download Report Button**: Export the scan results using the browser's print dialog
- **Report Container**: Displays scan results with status indicators:
  - ✔ Passed security check
  - ❌ Security issue detected
  - ⚠ Warning or potential vulnerability
  - 🕒 Scan timestamp

## Technical Details

### Architecture
- **Client-Side Processing**: All scanning logic runs in the browser
- **No Backend Required**: Pure HTML/CSS/JavaScript implementation
- **Responsive Design**: Mobile-friendly interface with dark theme

### Styling
- Dark purple theme for comfortable viewing
- Rounded borders and smooth transitions
- Centered layout optimized for desktop and mobile devices
- Media queries for print optimization

### Scanning Logic

The scanner checks for:
1. **HTTPS Protocol**: Validates secure connection
2. **Port Accessibility**: Reports common HTTP/HTTPS ports
3. **Weak Configuration**: Keywords like "test", "demo", "old", "legacy"
4. **Software Currency**: Detects potential outdated systems

### Report Download Functionality

The **Download Report** button uses the `downloadReport()` function which:
- Retrieves the generated vulnerability report from the report container
- Validates that a report has been generated (prevents download of empty reports)
- Triggers the browser's print dialog for saving or printing the report
- Displays an alert if no report is available to download

## Technologies Used

- **HTML5**: Semantic markup and structure
- **CSS3**: Styling with HSL color scheme and responsive design
- **JavaScript (Vanilla)**: Core scanning logic and DOM manipulation

## Limitations

- **Simulation-Based**: Current implementation uses pattern matching rather than actual network scanning
- **Client-Side Only**: Cannot perform deep vulnerability testing or access server information
- **Basic Checks**: Limited to URL pattern analysis and basic security headers
- **No Real Network Access**: Cannot actually scan ports or access server details

## File Structure

```
mini_projet/
├── README.md                          # Project documentation
└── vulnerablility_scanner.html        # Main application file
```

## Future Enhancements

- Integration with real vulnerability databases (e.g., CVE)
- Backend API for actual network scanning
- DNS record checking
- SSL/TLS certificate validation
- WHOIS information lookup
- Security header detection
- Email/contact information validation

## Browser Compatibility

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Installation

No installation required! Simply download the HTML file and open it in your browser.

## License

This project is provided as-is for educational and demonstration purposes.

## Author

Created by reesdsa13

---

**Note**: This is a demonstration tool meant for educational purposes. For comprehensive security assessments, use professional vulnerability scanning tools like OWASP ZAP, Burp Suite, or Nessus.
