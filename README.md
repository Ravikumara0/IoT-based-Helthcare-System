# 🏥 IoT-Based Healthcare System with Arduino Mega + ESP8266

A research-backed mini project focused on real-time health monitoring using IoT. The system continuously collects patient vitals, sends them to cloud servers (AWS), and provides two-way communication between doctors and patients—ideal for remote and portable healthcare support.

---

## 🧠 Abstract

The growing need for remote healthcare systems has accelerated the adoption of IoT in medicine. This project introduces an **IoT-based health monitoring system** using **Arduino Mega 2560 with a built-in ESP8266 Wi-Fi module**. The device continuously tracks vital parameters such as ECG, heart rate, and body temperature. It sends real-time data to the cloud, alerts medical personnel in case of critical changes, and allows direct communication between doctors and patients.

The system is **wearable**, **portable**, and can function in **rural or mobile health setups**—greatly reducing response time during emergencies and providing healthcare in inaccessible areas.

---

## ❓ Problem Statement

- Lack of continuous monitoring systems in rural and under-equipped areas.
- Delay in diagnosis due to absence of real-time communication.
- Inability to alert caregivers or doctors during chronic health variations.
- Non-portable health devices unsuitable for patients on the move or at home.

---

## ✅ Proposed System

- A **portable embedded system** with onboard sensors to monitor health metrics.
- **Wi-Fi-enabled data transmission** using the built-in ESP8266 module in Arduino Mega.
- Integration with **AWS IoT Core** for secure real-time data streaming and communication.
- **Alert-based notification** to doctors when patient parameters cross critical thresholds.
- **Two-way messaging** via MQTT for doctor-patient interaction.

---

## 🔧 Components Used

| Component                | Purpose                                      |
|-------------------------|----------------------------------------------|
| Arduino Mega 2560 + ESP8266 | Main microcontroller + Wi-Fi communication |
| AD8232 ECG Sensor        | To measure heart electrical activity         |
| Heartbeat Sensor         | For pulse monitoring                         |
| LM35 or DHT11            | Temperature sensing                          |
| 16x2 I2C LCD Display     | To display vitals locally                    |
| AWS IoT Core             | Cloud platform for communication             |
| Arduino IDE              | Development and code uploading               |
| MQTT Protocol            | For bidirectional data exchange              |
| USB Power / Battery Pack | For portability                              |

---

## 🧪 Working & Architecture

1. Sensors (ECG, Temp, Pulse) continuously collect data from the patient.
2. Arduino Mega processes this data and forwards it to the built-in ESP8266.
3. ESP8266 connects to Wi-Fi and pushes data to **AWS IoT Core** via MQTT.
4. Doctors access live vitals using a web dashboard or AWS MQTT client.
5. If the system detects anomalies (e.g., heartbeat > threshold), it immediately alerts the doctor.
6. Doctors can send real-time instructions or responses back to the patient (displayed on LCD).

📡 **System Architecture:**

![System Architecture](images/system_architecture.png)

```
[Patient Sensors] --> [Arduino Mega + ESP8266] --> [AWS IoT Core]
                                                   ↑         ↓
                                             [Doctor Dashboard] <--> [LCD Response]
```

---

## 📊 Results

- Vital data successfully streamed to AWS in real-time with low latency.
- Doctor-patient messaging functional through MQTT topic subscription.
- Alert system triggered correctly during test case simulations (high pulse rate).
- Portable prototype tested in a lab with consistent operation on battery.
- System demonstrated efficiency in remote monitoring without physical intervention.

![ECG Reading Output](images/ecg_output_lcd.jpg)
![MQTT Alert Screenshot](images/mqtt_alert.png)

---

## 🔮 Future Enhancements

- 🧠 Add AI to predict health emergencies before thresholds are breached.
- 🩸 Add more health sensors (BP, SPO2, glucose, etc.).
- 📱 Develop an Android/iOS app for better usability.
- ☁️ Store patient history and trends using AWS DynamoDB or Firebase.
- 🔋 Improve battery life using sleep modes or solar charging.
- 🏥 Connect with hospital management systems for full EHR integration.

![Mobile App UI Mockup](images/mobile_app_concept.png)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

- **Ravi Kumara S**  
  [LinkedIn Profile](https://www.linkedin.com/in/ravi-kumara-s)

---
