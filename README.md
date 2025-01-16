# 🛰 ISS Tracker and Notifier

This Python script tracks the International Space Station (ISS) and sends an email notification when the ISS is overhead and it's nighttime at your location. By leveraging APIs and email automation, this script ensures you never miss the chance to spot the ISS.

---

## **Features:**
- **ISS Position Tracking:** Uses the [Open Notify ISS API](http://api.open-notify.org) to track the current latitude and longitude of the ISS.
- **Nighttime Detection:** Checks the sunrise and sunset times for your location using the [Sunrise-Sunset API](https://sunrise-sunset.org/api) to determine if it's dark.
- **Email Notification:** Sends an email when the ISS is overhead during nighttime.
- **Automated Checks:** Runs in a loop, checking the ISS position and local time every minute.

---

## **How It Works:**
- **Location Proximity Check:** Determines if the ISS is within 5 degrees of your latitude and longitude.
- **Nighttime Verification:** Confirms if the current time is after sunset or before sunrise.
- **Notification:** Sends an email alert when both conditions are met, indicating that the ISS is visible in the night sky.
- **Looping Execution:** Continuously checks conditions every 60 seconds.

---

## **Tech Stack:**
- **Requests Library:** For accessing the ISS position and sunrise-sunset APIs.
- **Datetime Module:** To handle and compare local times.
- **SMTP Library:** To send email notifications.
- **Time Module:** To add delay between checks and prevent overloading the APIs.

---

## **How to Run:**
1. Clone or download the repository containing the script.
2. Update the script with your email credentials and location:
   - Replace `MY_EMAIL` with your email address.
   - Replace `PASSWORD` with your email password.
   - Replace `MY_LAT` and `MY_LONG` with your latitude and longitude.
3. Install the required Python libraries:
   - Install the `requests` library if not already installed (`pip install requests`).
4. Run the script using Python (`python main.py`).
5. Ensure your email service allows SMTP access and has "Less Secure Apps" enabled or an app-specific password configured (if required).
6. Leave the script running to receive email notifications when the ISS is visible.

---

## **Dependencies:**
- `requests`: For API communication.
- `smtplib`: For sending emails.
- `datetime`: For time calculations.
- `time`: For adding delays in the loop.

---

This ISS Tracker and Notifier combines space exploration with automation to create an exciting, real-time experience. Look up and wave at the ISS when it passes overhead! 🌌🚀
