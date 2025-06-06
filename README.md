# 🔐 GitGuard: OSV Commit Scanner

A Java Spring Boot REST API that scans the last 100 commits of any public GitHub repository and checks for known vulnerabilities using the OSV (Open Source Vulnerabilities) database.

## 🚀 Features

- 🔍 Fetches last 100 commits from a GitHub repo
- 🛡️ Scans each commit using OSV API
- 📊 Returns vulnerability count per commit in JSON format

## 🛠️ Tech Stack

- Java 22  
- Spring Boot 3  
- GitHub REST API  
- OSV API  
- Maven

## 📦 API Endpoint

```http
GET http://localhost:8080/api/osv/scan?repo=OWNER/REPO
