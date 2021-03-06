# e-appointment-checker

A simple crawler to check ICA's eAppointment page for SC application slot available.

The crawler will notify you via email once it has found a slot.

## Requirements:
### Browser driver for your OS
A browser driver is required as this script uses [selenium](http://www.seleniumhq.org/) to simulate normal user behavior and will open a real browser in background.

Follow the [instructions](https://github.com/SeleniumHQ/selenium/wiki/ChromeDriver#requirements) on Selenium wiki to get the webdriver for your OS installed. Note the webdriver must be included in your `PATH`.

**This script is tested with Chrome on Mac only.*

### Enable Gmail less secure app access
Please refer to the [instructions](https://support.google.com/accounts/answer/6010255?hl=en) by google. 

This is needed for the script to send you notification emails via `smtplib`.

### Python packages:
```
pip install -r requirements.txt
```

## Build and run:
Install requirement packages
```bash
make build
```

Run crawler
```bash
python sc_appointment_check.py your_nric no_of_applicant your_gmail gmail_password [retry_interval_in_seconds]
```

Monitor output file
```bash
tail -f sc_appointment_check.log

```

## Disclaimer
Use at your own risk. 

This script does NOT record your Gmail account or NRIC details.
The author should NOT be liable for any potential risk caused by using this script.