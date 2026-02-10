# h4 Johnny Tables

**Student:** Suprim Karki


**Course Code:** ICI002AS2AE-3007

**Date:** Feb 10

*I have read and accepted the course rules. These exercises were performed on a safe, isolated lab environment for educational purposes only.*

## Read and Summarize

* **OWASP A01: Broken Access Control:** Users acting outside their permissions. It's like having a keycard that opens doors it shouldn't.
* **OWASP A05: Security Misconfiguration:** Insecure default settings or incomplete configurations, like leaving default admin passwords.
* **OWASP A06: Vulnerable and Outdated Components:** Using libraries or frameworks that have known security holes.
* **OWASP A03: Injection:** Sending untrusted data to an interpreter (like SQL) which tricks it into executing commands.
* **XKCD 327:** "Little Bobby Tables" - a mom names her son Robert; DROP TABLE Students;--. This exploits a database that doesn't sanitize inputs, deleting the student table.


## Goat (Install WebGoat)

I installed WebGoat 2023.4.

<img width="1440" height="900" alt="Screenshot 2026-02-10 at 23 26 17" src="https://github.com/user-attachments/assets/2d261384-4bc0-48c8-9953-13c5896dbc86" />

**Steps taken:**
1.  Verified Java was installed.
2.  Downloaded webgoat-2023.4.jar.
3.  Ran java -jar webgoat-2023.4.jar.
4.  Accessed at http://localhost:8080/WebGoat.



##  F12 (WebGoat Developer Tools)

I solved the "General: Developer Tools" assignment.

<img width="1440" height="900" alt="Screenshot 2026-02-11 at 0 40 12" src="https://github.com/user-attachments/assets/d4ad7588-3165-4a38-a428-fbeefe1594a0" />


**Solution:**
1.  Opened WebGoat and pressed **F12** for Developer Tools.
2.  Went to the **Network** tab.
3.  Clicked "Go!" and found the network request.
4.  Found the random number in the request/console.


<img width="1440" height="900" alt="Screenshot 2026-02-10 at 23 39 33" src="https://github.com/user-attachments/assets/e0746658-bd31-4608-935a-6ce6059a44ea" />


## Not Outdated (Linux Updates)

I updated my Linux OS.

**Commands:**
sudo apt-get update
sudo apt-get dist-upgrade

## Injected (WebGoat SQL Injection)
I solved the SQL Injection (intro) by breaking the query string.
<img width="1440" height="900" alt="Screenshot 2026-02-10 at 23 49 35" src="https://github.com/user-attachments/assets/6a7a3ffc-16df-4c9b-b7fe-e0d1923492de" />



## d) Sequel (SQLZoo)

I completed the SQL basics.

**0 SELECT Basics:**
Query: SELECT population FROM world WHERE name = 'Germany'

**2 SELECT from World:**
Query 1: SELECT name, continent, population FROM world
Query 2: SELECT name FROM world WHERE population >= 200000000

<img width="1436" height="783" alt="Screenshot 2026-02-11 at 0 48 19" src="https://github.com/user-attachments/assets/aaedcb94-2773-4061-8bd1-26b7633922ea" />
<img width="1432" height="811" alt="Screenshot 2026-02-11 at 0 51 18" src="https://github.com/user-attachments/assets/34fc3c3f-6c53-4912-9c57-65498f4a66c1" />


## PortSwigger Lab: SQL Injection

**Lab:** SQL injection vulnerability in WHERE clause allowing retrieval of hidden data.

**The Vulnerability:**
The app takes the category from the URL and puts it directly into the SQL query without checking it.

**The Exploit:**
I modified the URL to: filter?category=Gifts'+OR+1=1+--

*  closes the category string.
* OR 1=1 is always TRUE, so it returns everything.
* -- comments out the rest of the query.

**Result:**
Congratulated and The page displayed all products, including unreleased ones.

<img width="1437" height="802" alt="Screenshot 2026-02-11 at 0 57 07" src="https://github.com/user-attachments/assets/4712f7a7-7795-4395-a992-d8590e0656e5" />
