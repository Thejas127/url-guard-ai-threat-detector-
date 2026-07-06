# url-guard-ai-threat-detector-
URLGuard AI is a cyber-security threat intelligence interface and frontend application designed to detect malicious, suspicious, or phishing URLs in real time.

🔐 PassGuard Pro — Password Strength Analyzer
> A sleek, browser-based password security tool that analyzes strength, estimates crack time, and generates strong passphrases — all 100% locally, with zero data leaving your device.
>
> live demo[]
> 
✨ Features

🔍 Real-Time Password Analysis

Strength rating — Instant Weak / Fair / Good / Strong classification
4-bar visual meter — Color-coded strength indicator that updates as you type
Entropy score — Calculates bits of entropy based on character pool and length
Crack time estimate — Estimates resistance against a 10 billion guesses/sec GPU cluster
Show/hide toggle — Eye button to reveal or mask your password

✅ Security Criteria Checks
Six individual checks displayed in real time:
Criteria	Requirement
Length	12 or more characters
Uppercase	At least one A–Z
Lowercase	At least one a–z
Numbers	At least one 0–9
Symbols	At least one special character
Uniqueness	>65% unique characters ratio

📊 Stats Dashboard

Three at-a-glance stat cards:
Length — Character count with color-coded threshold feedback
Entropy — Bits score (80+ bits = green / secure)
Crack Time — Human-readable estimate (seconds → centuries)

🖥️ Terminal Feedback

A macOS-style terminal block shows contextual security advice for your current password level.
📖 Built-in Password Guide (4 tabs)
Tab	Content

✅ Do's	6 best practices (length, mixed types, passphrases, 2FA, etc.)
❌ Don'ts	6 common mistakes (dictionary words, reuse, leet speak, etc.)
Examples	4 real-world password examples rated from Instant Crack → Universe Lifetime
Formula	Step-by-step entropy math explained (pool → bits → crack time)
⚡ Passphrase Generator
Generates a strong, memorable passphrase using random words + symbols + numbers (e.g. `Cloud$Mango#Brick7!`), auto-loads it into the analyzer, and tests it live.


🧮 How Entropy Is Calculated
```
Character Pool:
  Lowercase only      →  26 chars
  + Uppercase         →  52 chars
  + Numbers           →  62 chars
  + Symbols (~32)     →  94 chars

Entropy (bits) = Length × log₂(Pool Size)

Example: 16-char password using all types
= 16 × log₂(94) ≈ 105 bits  →  STRONG ✅
```
Crack time targets (at 10¹⁰ guesses/sec):
```
< 60 bits   →  Crackable — hours to years
  80 bits   →  Everyday accounts (minimum recommended)
 100 bits   →  Banking, email, password managers
 128+ bits  →  Practically impossible
```
---
🛡️ Privacy
> **All analysis runs locally in your browser.**
> No password data is ever stored, transmitted, logged, or sent to any server.
This tool has zero backend. It is a single static HTML file with no external API calls.
---
🖼️ Preview

Weak Password	Strong Password
1-bar red meter, danger badge	4-bar green meter, strong badge
Entropy < 30 bits	Entropy 80+ bits
Crack time: Instant	Crack time: Centuries

🗂️ Project Structure
```
passguard-pro/
└── index.html      # Complete app — HTML + CSS + JS in one file
```
---
🛠️ Built With

Technology	Usage
HTML5	Structure & semantics
CSS3	Animations, grid layout, dark theme
Vanilla JavaScript	Real-time analysis logic
Share Tech Mono	Monospace terminal font
Syne	Display / heading font
No frameworks. No build tools. No npm. Zero dependencies.

📋 Strength Scoring Logic

Score	Label	Criteria
0	—	Empty input
1	Weak	Any input under 6 characters
2	Fair	8+ chars with some complexity
3	Good	12+ chars with multiple types
4	Strong	16+ chars, all types, high uniqueness

🤝 Contributing

Fork the repo
Create a feature branch: `git checkout -b feature/your-feature`
Commit your changes: `git commit -m "Add your feature"`
Push to the branch: `git push origin feature/your-feature`
Open a Pull Request

📄 License
This project is open source and available under the MIT License.

<p align="center">Made with 🔐 for a more secure web</p>
