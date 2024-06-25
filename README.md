# ESP32 Real Time Clock (RTC) with DS3231 Project

### Project Overview
The ESP32 Real Time Clock (RTC) with DS3231 project demonstrates how to use the DS3231 RTC module to keep track of real-time data with high accuracy using an ESP32 microcontroller. This project is ideal for applications that require precise timekeeping, such as data logging, scheduling tasks, and alarms.

### Components Needed
- **ESP32 Microcontroller**: The main controller that communicates with the RTC module.
- **DS3231 RTC Module**: A high-precision real-time clock module.
- **Jumper Wires**: Connect the RTC module to the ESP32.
- **Breadboard**: Optional, for organizing the circuit connections.

### Block diagram

### Circuit Setup
1. **Connecting the DS3231 RTC to ESP32:**
   - **I2C Communication**: Connect the SDA pin of the DS3231 to GPIO 21 on the ESP32 and the SCL pin to GPIO 22.
   - **Power Supply**: Connect the DS3231 to a suitable power supply (e.g., 3.3V or 5V and GND).

### Instructions
1. **Setup:**
   - Initialize serial communication for debugging purposes using `Serial.begin(9600)`.
   - Initialize I2C communication using `Wire.begin()`.
   - Create an RTC_DS3231 object to interact with the RTC module.
   - Check if the RTC is connected properly using `rtc.begin()`.
   - If the RTC lost power, set the time using `rtc.adjust(DateTime(F(__DATE__), F(__TIME__)))`.

2. **Operation:**
   - **Reading Current Time:**
     - Use `rtc.now()` to get the current date and time from the RTC.
     - Print the current date and time to the Serial Monitor using `Serial.print` and `Serial.println`.

3. **Considerations:**
   - **Battery Backup:** Ensure the DS3231 RTC module has a battery backup to maintain the timekeeping even when the main power is off.
   - **Time Zone and Daylight Saving:** Adjust the time based on the local time zone and consider daylight saving changes if necessary.

### Applications
- **Data Logging:** Timestamp data entries for accurate record-keeping.
- **Scheduling Tasks:** Automate tasks based on specific times and dates.
- **Alarms and Reminders:** Set up alarms or reminders for various applications.

### Useful Links
🌐 [ProjectsLearner - ESP32 RTC DS3231](https://projectslearner.com/learn/esp32-rtc-ds3231)  
📧 [Email](mailto:projectslearner@gmail.com)  
📸 [Instagram](https://www.instagram.com/projectslearner/)  
📘 [Facebook](https://www.facebook.com/projectslearner)  
▶️ [YouTube](https://www.youtube.com/@ProjectsLearner)  
📘 [LinkedIn](https://www.linkedin.com/in/projectslearner)

Created with ❤️ by ProjectsLearner
