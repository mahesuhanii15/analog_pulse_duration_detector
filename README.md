# analog_pulse_duration_detector
##  Project Description
I made this project for the analog domain in ELECTROTHON organised by ELECTRONICS club IITG.
# Pulse Duration Detector

## 📌 Objective
Design and simulate an analog circuit that detects whether an input pulse stays HIGH longer than a preset time and turns ON an LED only if the condition is met.

---

##  Working Principle
- RC network measures pulse duration  
- Capacitor charges while input is HIGH  
- Op-amp comparator checks if capacitor voltage crosses threshold  
- LED turns ON only for long pulses  
- Discharge transistor resets capacitor when pulse ends  

---

##  Transistor Roles
- **Qinv (NPN):** Input inverter and buffer  
- **Qcharge (PNP):** Charges timing capacitor  
- **Qdischarge (NPN):** Resets capacitor  
- **QLED (NPN):** Drives LED  

---

## Adjustable Threshold
Timing resistor parameterized in LTspice:
.param Rval = 200k
.step param Rval list 100k 200k 300k 400k

Higher resistance → slower charging → longer detection time.

---

##  Results
- Short pulses ignored  
- Long pulses detected correctly  
- LED turns OFF immediately after pulse  
- Auto-reset confirmed  
- Adjustable timing works as expected  

---

##  Tools Used
- LTspice  
- Op-amp comparator  
- BJTs  
- RC timing network  

---

