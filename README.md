# 🔐 Secure Downloads - Chrome Extension + Spring Boot

A real-time file security solution combining a **Chrome Extension** and a **Spring Boot API** that scans downloaded files using the **VirusTotal API**. If any file is found malicious, it is **automatically deleted** from the user's system.

---

## 🚀 Features

- Monitors all completed downloads via Chrome Extension.
- Sends downloaded files to a local Spring Boot server for scanning.
- Uses the **VirusTotal Public API** to detect malware.
- **Deletes malicious files** automatically to protect users.
- **Batch processing** implemented to scan up to 4 files per minute (in line with VirusTotal rate limits).

---

## 🛠️ Technologies Used

- Java Spring Boot
- Chrome Extensions (JavaScript)
- VirusTotal Public API v3
- RESTful API
- JSON, HTTPClient
- Postman (for testing)

---

## 🔧 How It Works

1. **Download Monitoring**: Chrome Extension detects when a file download completes.
2. **API Call**: Sends the local file path to the Spring Boot API.
3. **File Scanning**: Spring Boot server uploads the file to VirusTotal and waits for the analysis.
4. **Malware Detection**:
   - If the file is **clean**: a success message is shown.
   - If the file is **malicious**: it is deleted from the system immediately.
5. **Batch Logic**: Up to 4 files are processed every minute to respect VirusTotal's rate limits.
