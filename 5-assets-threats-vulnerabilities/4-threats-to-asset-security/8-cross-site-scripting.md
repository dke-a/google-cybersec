# Cross-Site Scripting (XSS)

Previously, we explored a few types of malware. All malicious software needs to be delivered to the target before it can work. Phishing and other social engineering techniques are common methods for malware delivery. Another way malware is spread is through web-based exploits.

## Web-Based Exploits

**Web-based exploits** are malicious code or behavior used to take advantage of coding flaws in web applications. These exploits are targeted to obtain sensitive personal information because web applications interact with multiple users across multiple networks. A common method for web-based exploits is **injection attacks**.

### Injection Attacks

An **injection attack** involves inserting malicious code into a vulnerable application. The application often appears to work normally because the injected code runs in the background, unknown to the user. Applications are vulnerable to injection attacks because they are programmed to receive data inputs, which can be something the user types, clicks, or data shared between programs. Properly coded applications should validate and handle user inputs correctly.

## Cross-Site Scripting (XSS)

**Cross-site scripting (XSS)** is an injection attack that inserts code into a vulnerable website or web application. These attacks are often delivered by exploiting HTML and JavaScript, which are used by most websites. XSS can give cybercriminals access to everything that loads on the infected web page, including session cookies, geolocation, webcams, and microphones.

### Types of XSS Attacks

There are three main types of cross-site scripting attacks: reflected, stored, and DOM-based.

#### Reflected XSS

In a **reflected XSS attack**, a malicious script is sent to the server and activated during the server's response. A common example is the search bar of a website. Criminals send their target a web link that appears to go to a trusted site. When clicked, it sends an HTTP request to the vulnerable site server, and the attacker’s script is reflected back to the user's browser, where it is executed.

#### Stored XSS

In a **stored XSS attack**, the malicious script is injected directly into the server. Attackers target elements of a site that are served to the user, such as images and buttons. The malicious code is activated when the user simply visits the site. Stored XSS attacks can be particularly damaging because the user has no way of knowing the site is infected beforehand.

#### DOM-Based XSS

**DOM-based XSS** refers to an attack where the malicious script exists in the web page a browser loads, without needing to be sent to the server to activate. In a DOM-based attack, a malicious script can be seen in the URL parameters, which reflect input from the user. For example, attackers might hide malicious JavaScript in HTML tags, which the browser processes and executes.

## Key Takeaways

Hackers use XSS methods to steal sensitive information. Security analysts should be familiar with these injection attacks. Understanding the different types of XSS attacks and how they work is crucial for defending web applications and protecting sensitive data.