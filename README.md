# NEXUS – Smart Barcode-Based Attendance System

**A smart, automated attendance management system integrating barcode scanning, cloud database technology, and IoT hardware.**

## About the Project

NEXUS is a barcode-based smart attendance system designed to simplify and automate the student attendance process in educational institutions.

Students scan the barcode printed on their college ID cards using a smartphone camera. The system validates the barcode, records attendance in a Supabase cloud database, and sends an event to an ESP32-based IoT device for real-time confirmation.

## Key Features

- **Barcode Scanning:** Scan student ID barcodes using a smartphone camera.
- **Student Management:** Add and manage student records.
- **Automated Attendance:** Record attendance directly in the cloud database.
- **Duplicate Prevention:** Prevent multiple attendance entries for the same student on the same day.
- **Real-Time IoT Feedback:** ESP32 receives attendance events through Wi-Fi.
- **OLED Display:** Displays attendance confirmation and student information.
- **LED Indicator:** Provides visual feedback.
- **Buzzer Alerts:** Provides audio confirmation.
- **Responsive Interface:** Accessible through desktop and mobile browsers.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Barcode Scanner | HTML5 QR Code Library |
| Database | Supabase PostgreSQL |
| Backend | Supabase Edge Functions |
| IoT Controller | ESP32 DevKit V1 |
| Display | 0.96-inch OLED |
| Communication | Wi-Fi, HTTPS |
| Development Tools | VS Code, Arduino IDE |

## System Architecture

1. Student presents their college ID card.
2. The smartphone camera scans the barcode.
3. The website sends the barcode value to a Supabase Edge Function.
4. The backend validates the student information.
5. Attendance is recorded in the Supabase database.
6. An attendance event is added to the device event queue.
7. ESP32 retrieves the event through Wi-Fi.
8. OLED, LED, and buzzer provide attendance confirmation.

## Hardware Requirements

- ESP32 DevKit V1
- 0.96-inch I2C OLED Display
- Active Buzzer Module
- LED
- 220Ω Resistors
- Breadboard
- Jumper Wires
- Smartphone with a camera

## Project Structure

```text
NEXUS/
│
├── index.html
│
├── css/
│   └── style.css
│
├── js/
│   └── script.js
│
│
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/NEXUS.git
```

### 2. Open the Project

Open the project folder in Visual Studio Code.

### 3. Run the Website

Use the VS Code Live Server extension to run the website locally.

For smartphone camera access, deploy the website using HTTPS.

### 4. Configure Supabase

Configure your Supabase project with:

- Supabase Project URL
- Supabase Publishable (Anon) Key
- Required database tables
- Edge Functions

Never expose your Supabase Service Role Key in frontend code.

### 5. Configure ESP32

Open `NEXUS_Main_Firmware.ino` in Arduino IDE.

Configure your Wi-Fi credentials, Supabase project URL, and device token before uploading the firmware to the ESP32.

## Database Tables

The project uses the following primary tables:

- `students` – Stores student details and barcode values.
- `attendance` – Stores attendance records and timestamps.
- `device_events` – Stores events for ESP32 notification.

## Future Enhancements

- Attendance analytics and reports.
- Export attendance records.
- Improved authentication and access control.
- Enhanced device communication security.
- Support for multiple IoT attendance devices.

## Project Information

**Project Name:** NEXUS – Smart Barcode-Based Attendance System

**Project Type:** Web Application + IoT Integration

**Purpose:** Academic Diploma Project

**Status:** Prototype Development

---

*Developed as an academic project to demonstrate the integration of web technologies, cloud databases, barcode scanning, and Internet of Things (IoT).* 
