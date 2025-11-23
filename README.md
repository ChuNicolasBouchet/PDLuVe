# 🔌 Low-Voltage Smart PDU — Open Hardware / Open Firmware
**Version MVP – 4 à 6 canaux – 5 V – 6 A par canal**

Un PDU basse tension intelligent, modulaire, open source, conçu pour les clusters Raspberry Pi, serveurs SBC, dispositifs IoT et laboratoires personnels.

Le projet vise à proposer une alternative fiable et précise aux blocs de distribution 5 V maison, en combinant :
- sécurité électrique (switch high-side / disjoncteur électronique)
- mesure précise par canal (courant, tension, puissance)
- supervision (API REST, MQTT, Prometheus)
- contrôle (ON/OFF par canal)
- journaux et interface physique locale (OLED + boutons)
- extension future à 5–48 V et redondance d’alimentation

---

## 🎯 Objectifs du MVP

### ✔ 1. **Bus 5 V unique**
- Alimentation via une Mean Well LRS-150-5 (ou équivalent)
- Fusible physique d’entrée 25–30 A
- Monitoring global du bus (tension, puissance)

### ✔ 2. **4 à 6 canaux indépendants**
- Courant max : **6 A par canal**
- Protection électronique via **TI TPS4H160** (4 voies) ou **TPS1H200A**
- Filtrage LC par canal
- Connecteurs à vis robustes

### ✔ 3. **Mesure individuelle haute précision**
- **INA3221** (3 canaux) ×2 pour 6 sorties
- Shunt 0.01 Ω / 3 W par canal
- Tension, courant, puissance, énergie cumulée

### ✔ 4. **Supervision intelligente**
- MCU **ESP32-S3**
- Wi-Fi ou Ethernet
- API REST (JSON)
- MQTT
- Endpoint Prometheus
- Journaux internes (Flash)
- Protection FAULT / surintensité avec reset logiciel

### ✔ 5. **Interface locale**
- OLED 1.3" (SH1106)
- Boutons (navigation / ON-OFF)
- Affichage par canal ou global


--- 
	•	CERN Open Hardware License v2
	•	MIT pour le firmware
