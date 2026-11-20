# Password Cracking Labs: Networkwalks Week 3
Password cracking labs with John the Ripper and Networkwalks tools, done in a controlled lab environment as part of a Cybersecurity &amp; Ethical Hacking program
> **Ethical use:** All work was done on files and hashes provided by the course, in a controlled lab environment. Passwords and flags are intentionally not shown.

## Overview
Weak passwords are one of the most common real-world attack vectors. Ethical password cracking helps organizations test how strong their password security really is. In these labs, I tested how well a password-protected PDF held up against different cracking approaches.

## Projects

### W3-PM1: Password Cracking with John the Ripper (JtR)
- **Goal:** Recover the password of a protected PDF using JtR on Windows
- **Tools:** John the Ripper, OnlineHashCrack (hash extraction), Notepad
- **Approach:**
  1. Uploaded the PDF to OnlineHashCrack to extract its hash
  2. Copied the hash into Notepad and saved it as a `.txt` file
  3. In JtR, used *Open password file*, browsed to the saved hash file and clicked *Start attack*
  4. Waited for the crack (time depends on computer speed and password complexity)
  5. Verified the recovered password by opening the PDF
- **Result:** [5 seconds + Simple Passwords like Password crack easily]

### W3-PM2: Password Cracking with Networkwalks Tools
- **Goal:** Same objective using the Networkwalks Hash Calculator and Password Cracker
- **Tools:** NW Hash Calculator, NW Password Cracker
- **Approach:**
  1. Opened the Networkwalks Hash Calculator in the browser
  2. Uploaded the locked PDF and got its hash value
  3. Copied the full hash
  4. Opened the Networkwalks Password Cracker in the browser
  5. Pasted the hash and started the attack. The tool tries different passwords until it finds a match. If it doesn't, that suggests the file has a strong password
  6. Verified the recovered password by opening the PDF
- **Result:** [Success + about 5 seconds to try various likely password]

## Challenges & Lessons

**Brute force vs. informed guessing**
On [W3-PM1 / W3-PM2], JtR's brute-force mode was taking too long. Instead of waiting it out, I switched to a targeted password-guess approach, trying likely passwords based on common patterns. This cracked the password quickly.

**Why it worked:** Brute force grows exponentially with password length, but people choose predictable passwords. A short list of smart guesses can beat billions of random attempts.

## Results

| Module | Method | Outcome | Flag captured |
|--------|--------|---------|---------------|
| W3-PM1 | John the Ripper | Cracked ✅ | ✅✅✅ |
| W3-PM2 | NW Password Cracker | Cracked ✅ | ✅✅✅ |

## Key Takeaways
- How password hashes are extracted and stored
- Dictionary vs. brute-force attacks, and the speed difference
- Why password length and complexity matter
- Defences: long passphrases, MFA, salting + slow hashing (bcrypt/Argon2)

## Author
**Shanil Bakili**
NETWORKWALKS-SHANIL-BAKILI-B084-WK3
