# Keylogger Script

This project is a Python-based keylogger that captures keystrokes and sends them to a specified email address at regular intervals.

---

## Disclaimer

This script is provided for **educational purposes only**. Unauthorized use of keyloggers to monitor or capture someone else's activities is illegal and unethical. Ensure you have explicit permission to use this tool in a controlled and authorized environment.

**Use responsibly and at your own risk.**

---

## Features

- Captures keystrokes in real time.
- Sends captured logs to a specified email address.
- Configurable time interval for email reporting.

---

## Requirements

- Python 3
- Required libraries:
  - `pynput`
  - `smtplib`

Install dependencies using pip:

```bash
pip install pynput
```

---

## How It Works

1. **Keystroke Logging:**
   - The script listens for keypress events using the `pynput` library.
   - It captures printable characters and handles special keys like space, enter, etc.

2. **Email Reporting:**
   - Logs are sent via email at user-specified intervals.
   - Uses the `smtplib` library to send emails through an SMTP server (e.g., Gmail).

3. **Configurable Parameters:**
   - Time interval for sending logs.
   - Email address and password for sending emails.

---

## Usage

### 1. Set Up Email Configuration

Edit the script to include your email credentials:

```python
my_keylogger = keylogger.Keylogger(120, "youremail@example.com", "yourpassword")
```

- Replace `"youremail@example.com"` with your email address.
- Replace `"yourpassword"` with your email account password.

### 2. Start the Keylogger

Run the script with Python:

```bash
python3 keylogger.py
```

The keylogger will start capturing keystrokes and send logs to the specified email address every 120 seconds (or the interval you set).

### 3. Stop the Keylogger

To stop the keylogger, use `CTRL + C` in the terminal.

---

## Security and Privacy

- **Email Passwords:** Use app-specific passwords or temporary credentials for security. Avoid using your primary email account password.
- **Testing Environment:** Run the script in a controlled environment where you have permission to capture keystrokes.
- **Legal Compliance:** Ensure compliance with applicable laws and regulations.

---

## Example Output

Captured logs will be sent to your email in the following format:

```
Keylogger started
Hello World !
[SPACE] This is a test [ENTER]
```

---

## Important Notes

- This script is designed for educational purposes and may not work in all environments.
- Sending emails requires an active internet connection and access to the configured SMTP server.
- Gmail users may need to enable "Less Secure App Access" or use an app-specific password.

---

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

