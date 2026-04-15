# Web Application Security Testing – OWASP Juice Shop

## Overview

This project presents a comprehensive web application security assessment conducted on OWASP Juice Shop, an intentionally vulnerable application designed for security training and practice. The purpose of this project was to identify, analyze, and exploit common web application vulnerabilities within a controlled local environment, thereby gaining practical exposure to real-world security issues.

---

## Objectives

* To understand common web application vulnerabilities and their impact
* To perform structured security testing on a web application
* To exploit identified vulnerabilities in a controlled environment
* To analyze application behavior under malicious input conditions

---

## Tools and Technologies Used

* OWASP Juice Shop
* Docker (for local deployment)
* Web Browser Developer Tools

---

## Environment Setup

The application was deployed locally using Docker to ensure a secure and isolated testing environment. Running the application on localhost allowed for safe experimentation without interacting with external systems.

---

## Methodology

### 1. Application Reconnaissance

The application was initially explored to understand its structure and functionality. Key components such as the home page, authentication system, search functionality, and accessible endpoints were analyzed to identify potential input fields and attack surfaces.

---

### 2. Input Testing and Payload Injection

Various input points were tested using crafted payloads designed to identify vulnerabilities. These included login forms, search parameters, and URL-based inputs.

---

### 3. Request and Response Analysis

HTTP requests and responses were monitored using browser developer tools. The analysis focused on:

* HTTP status codes
* Response content and structure
* Error messages and system behavior

This helped in identifying abnormal responses and potential security weaknesses.

---

### 4. Vulnerability Exploitation

Identified vulnerabilities were exploited to assess their impact. This included bypassing authentication mechanisms, accessing restricted resources, and retrieving sensitive data.

---

## Vulnerabilities Identified

### Cross-Site Scripting (XSS)

Input fields were vulnerable to script injection due to insufficient input validation. Malicious scripts were successfully executed in the browser, demonstrating the risk of client-side attacks.

---

### SQL Injection

The authentication mechanism was susceptible to SQL Injection attacks. Improper handling of user input allowed bypassing of login controls, resulting in unauthorized access to privileged accounts.

---

### Broken Access Control

Restricted functionalities were accessed without proper authorization by manipulating URLs and API endpoints, indicating weaknesses in access control mechanisms.

---

### Sensitive Data Exposure

Certain directories and files were publicly accessible without authentication. These included backup files and internal documents, highlighting inadequate data protection.

---

### Information Disclosure

Application endpoints exposed sensitive user information, including email addresses and account details, due to insufficient access restrictions.

---

### Improper Error Handling

Malformed inputs triggered detailed server-side error messages, revealing internal application structure and behavior that could be leveraged by attackers.

---

## Results and Findings

The testing process revealed multiple critical vulnerabilities within the application. These findings demonstrate how improper input validation, weak access control, and inadequate error handling can significantly compromise application security.

---

## Key Learnings

* Practical understanding of common web application vulnerabilities
* Experience in exploiting vulnerabilities within a controlled environment
* Ability to analyze HTTP requests and responses effectively
* Awareness of the importance of secure coding practices and proper input validation

---

## Conclusion

This project provided hands-on experience in web application security testing and vulnerability exploitation. It reinforced foundational knowledge of web security principles and highlighted the importance of implementing secure development practices to prevent common vulnerabilities.

---


