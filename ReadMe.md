# Autonomous Robot – Sensorik-Konzepte

Dieses Repository dokumentiert drei mögliche Sensorik-Konzepte für unseren autonomen Roboter.  
Wir haben **Konzept A („Front-Trio, starr“) ausgewählt**, da es am schnellsten und robustesten für die Teststrecke ist.  

---

## Überblick der Komponenten

- Chassis mit 4 DC-Motoren + Räder  
- Motortreiber (2 H-Brücken)  
- Arduino-Board  
- Batteriehalter (2× 18650) mit Schalter  
- 2× IR-Sensor (10–80 cm)  
- 1× IR-Sensor (20–150 cm)  
- 1× Ultraschallsensor  
- 1× Servo  

---

## Konzept A – „Front-Trio, starr“ ✅ *gewählt*

**Idee:** Alle Sensoren starr vorne montiert, schnelle Hinderniserkennung ohne Servo-Scan.  
**Einsatz:** Geschwindigkeit und einfache Logik → ideal für Bestzeiten.

### Vorteile
- Sehr einfache Montage & Programmierung  
- Keine Servo-Latenz → schnelle Reaktion  
- Robust und gut für **Teststrecke mit Hindernissen von vorn**  
- Eignet sich für **Bestzeit-Fahrten** (kontinuierlich rollend)

### Nachteile
- Keine Seiten- oder Rückabdeckung  
- IR unzuverlässig bei schwarz/matt oder spiegelnd  
- Schmale Stäbe/Schrägen können übersehen werden  

---

## Konzept B – „Scan-Kopf“ (Ultraschall auf Servo)

**Idee:** Ultraschallsensor wird mit Servo geschwenkt (±90°). IR-Sensoren bleiben starr für Nahbereich.

### Vorteile
- Große Abdeckung durch Servo-Scan  
- Roboter erhält mehr Kontext (2D-Frontkarte)  
- Flexibel für verschiedene Parcours  

### Nachteile
- Langsamer wegen Servo-Latenz (Stop-and-Scan)  
- Mechanisch/programmatisch komplexer  
- US-Mehrwege-Fehler bei Winkeln  

---

## Konzept C – „Wall-Follower“

**Idee:** Ein IR-kurz seitlich, um konstanten Abstand zu einer Wand zu halten. IR-lang und Ultraschall für Front-Hindernisse.

### Vorteile
- Sehr stabil fürs Fahren in Korridoren/Wandparcours  
- Konstante Regelung möglich  

### Nachteile
- Nur einseitige Abdeckung  
- Freistehende Hindernisse oder Abzweigungen kritisch  
- Weniger geeignet für offene Parcours  

---

## Entscheidung

Wir haben uns für **Konzept A („Front-Trio, starr“) entschieden**, da es:

- am **einfachsten** umzusetzen ist,  
- die **schnellsten Reaktionszeiten** ermöglicht (keine Servo-Latenz),  
- am besten für eine **schnelle Teststrecke mit Hindernissen** geeignet ist,  
- und somit die besten Chancen bietet, den aktuellen Rekord von **33 Sekunden** zu unterbieten 🚀.  

---
