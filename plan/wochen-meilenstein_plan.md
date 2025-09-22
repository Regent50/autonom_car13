# Projektplan

## Woche 1 – Chassis & Power
**Aufgaben:**
- Chassis montieren
- Motoren & Treiber anschließen
- Stromversorgung (2×18650 + Schalter) sicherstellen

**Meilenstein:**  
Roboter fährt über Motor-Testskript

---

## Woche 2 – Basisfahrt
**Aufgaben:**
- Geradeausfahrt & Drehungen implementieren
- Motor-Kalibrierung (Geschwindigkeitsunterschiede kompensieren)

**Meilenstein:**  
Roboter fährt zuverlässig gerade & 90°-Kurven

---

## Woche 3 – Sensorik Kalibrierung
**Aufgaben:**
- IR- & Ultraschallsensor auslesen
- Reichweiten in cm kalibrieren (Fehlerkurven aufnehmen)
- Sensor-Montage finalisieren (Konzept A + ggf. Wallfollower-Test)

**Meilenstein:**  
Sensoren liefern reproduzierbare Distanzwerte

---

## Woche 4 – Erste Autonomie
**Aufgaben:**
- Hinderniserkennung + einfache Stop-Logik
- Erste autonome Geradeausfahrt mit Hindernis-Stopp

**Meilenstein:**  
Roboter erkennt Hindernis frontal und stoppt zuverlässig

---

## Woche 5 – Wallfollower (Training)
**Aufgaben:**
- Ein IR seitlich nutzen für Wandabstand
- PID-Regler entwickeln für konstante Spurführung

**Meilenstein:**  
Roboter folgt Wand in Testparcours stabil

---

## Woche 6 – Tuning & Bestzeit-Logik
**Aufgaben:**
- Geschwindigkeit hochsetzen
- Kombination aus Wand- und Hindernis-Logik
- Timeout-Handling, Not-Stop

**Meilenstein:**  
Roboter schafft komplette Strecke ohne Eingriff

---

## Woche 7 – Final-Demo
**Aufgaben:**
- Letzte Kalibrierung
- Demo-Run aufnehmen
- Doku im Git aktualisieren

**Meilenstein:**  
Finaler Parcours-Run <33 Sek.

---

# Meilensteinplan

- **Chassis & Power** – Basis-Hardware läuft
- **Basisfahrt** – Geradeaus & Kurven funktionieren
- **Sensorik kalibriert** – zuverlässige Distanzmessung
- **Erste Autonomie** – Roboter erkennt & stoppt vor Hindernis
- **Wallfollower** – stabile Fahrt an Wand entlang
- **Tuning** – Geschwindigkeit & Logik optimiert
- **Final-Demo** – kompletter Lauf <33 Sek.

# Mögliche Tests

| Test               | Beschreibung                           | Erwartetes Ergebnis/Metrik                       |
| ------------------ | -------------------------------------- | ------------------------------------------------ |
| Gerade             | 1 m Strecke ohne Hindernis             | Abweichung < 5 cm seitlich                       |
| 90°-Kurve          | Rechts/Links-Kurve                     | Erfolgreich < 2 Sek. Zeitverlust                 |
| Enge Passage       | 40 cm Breite, 1 m Länge                | Kein Kontakt, Wandabstand ≥ 5 cm                 |
| Hindernis auf Spur | Blockade nach 1 m Fahrt                | Stopp vor Hindernis (> 5 cm Abstand, 0 Kontakte) |
| Komplettlauf       | Ganzer Parcours mit allen Hindernissen | Zielzeit < 33 Sek., max. 0–1 Kontakte            |
