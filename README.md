# CS-305 Software Security – Module Eight Journal

## Client Summary  
My client was **Artemis Financial**, a financial consulting company that creates personalized financial plans such as retirement, investments, savings, and insurance. They wanted to modernize their web application and make sure it was secure. Their main requirements were to add **secure communication (HTTPS/TLS)**, a **checksum verification step**, and to review and refactor the code for vulnerabilities.

## What I Did Well  
I did well identifying and fixing vulnerabilities using both **manual code review** and **OWASP Dependency-Check**. I recommended **AES-256 in CBC mode** for encryption, added **SHA-256 checksum verification**, and created a self-signed certificate with **Java Keytool** to test HTTPS in development.  
Coding securely is important because even small mistakes can expose sensitive data. Strong security builds client trust, keeps systems compliant, and protects a company’s reputation.

## Challenges and Growth Areas  
Not everything was perfect, but I learned a lot from the challenges:  
- In **static testing**, I found vulnerabilities and even spotted false positives, but I need to improve at refining suppression rules so reports are cleaner.  
- In **vulnerability reporting**, I realized scans only go so far — you have to carefully review reports so only actionable issues remain.  
- In **secure connection setup**, I generated certificates and changed the code for HTTPS, but didn’t fully establish a live secure connection. That reminded me that configuration and testing in real-world environments can take persistence.  
- **Maven setup was one of my biggest struggles.** At first, the Maven Dependency-Check plugin constantly failed due to API errors and configuration issues. I had to troubleshoot by checking my JAVA_HOME path, switching to the OWASP CLI tool with an API key, and running multiple scans to get reliable reports. Eventually, I did get Maven fully working, which gave me a stronger understanding of how builds and plugins connect to external vulnerability databases. This was frustrating, but also one of the most valuable lessons of the course.

## Layers of Security Added  
- **Cryptography** – SHA-256 checksum verification, AES-256 encryption recommendation.  
- **Secure Communication** – Converted HTTP to HTTPS with certificates.  
- **Input Validation & Error Handling** – Added validation and stopped stack trace leaks.  
- **Static Testing** – Used OWASP Dependency-Check to confirm no new vulnerabilities.  

In the future, I’d also use **SonarQube, Snyk, and GitHub Dependabot** to keep security testing automated in a CI/CD pipeline.

## Ensuring Functionality and Security  
After refactoring, I ran the application to confirm HTTPS worked in development and the checksum validated files. I re-ran OWASP Dependency-Check to make sure no new vulnerabilities were introduced and manually reviewed the code for errors.

## Tools and Practices Used  
- OWASP Dependency-Check (Maven + CLI)  
- Java Keytool (certificate generation)  
- SHA-256 checksum implementation  
- AES-256 encryption (recommended)  
- Secure coding practices (input validation, encapsulation, error handling)

## What I Can Show Employers  
From this work, I can show that I know how to:  
- Perform a **software vulnerability assessment**.  
- **Refactor insecure code** and apply modern security fixes.  
- Use **encryption, hashing, and HTTPS** in a Java application.  
- Apply **industry best practices** and use professional tools.  
- **Work through setbacks** — especially troubleshooting Maven until I got it working — which shows persistence and problem-solving.  

This project proves I can identify risks, implement secure solutions, and reflect on areas to grow, which is what real-world software security requires.
