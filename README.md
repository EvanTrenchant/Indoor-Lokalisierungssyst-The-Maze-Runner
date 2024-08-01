## Indoor-Lokalisierungssystem

Ziel dieses Projekts ist die Entwicklung eines Echtzeit-Lokalisierungssystems (RTLS) für Innenräume unter Verwendung der Ultra-Wideband-Technologie (UWB).

RTLS eröffnen eine Vielzahl von Möglichkeiten in verschiedenen Bereichen. Sie können das Warenmanagement in der Logistik optimieren, die Lokalisierung von Patienten und Geräten im Gesundheitswesen erleichtern, die Produktivität in Werkstätten steigern und eine präzise Navigation für autonome Roboter gewährleisten.

### Systemarchitektur

#### Hardware-Komponenten
- UWB-Module (BU01) : Werden verwendet, um die Distanz zwischen Tags und Ankern genau zu messen.
- ESP32: Mikrocontroller für die Verwaltung der UWB-Module und die Kommunikation mit dem WebSocket-Server.
- Computer: Beherbergt den WebSocket-Server und die Benutzeroberfläche. Spielt die Rolle des Wi-Fi-Routers und sorgt für die Netzwerkkommunikation.

#### Globale Funktionsweise

Die Geolokalisierung mit der UWB-Technologie beruht auf der Triangulation zwischen festen Ankern und den zu ortenden Tags.

**1. Datenerfassung:**

- Die ESP32 steuern und kommunizieren mit den UWB-Modulen.
- Diese UWB-Module senden und empfangen Signale in Form von elektromagnetischen Impulsen, um die Abstände zwischen ihnen zu messen.

**2. Verarbeitung und Übertragung:**

- Die ESP32 berechnen die Flugzeiten der Signale zwischen zwei UWB-Modulen, um die Entfernung zwischen ihnen zu bestimmen.
- Diese Entfernungen werden über Wi-Fi an den WebSocket-Server gesendet.

**3. Real Time Visualization:**.

- Der WebSocket-Server leitet die Daten an das Webinterface weiter.
- Das Webinterface ermöglicht die Konfiguration der Ankerpositionen und zeigt die Positionen der Tags in Echtzeit an, was eine dynamische Visualisierung der beweglichen Objekte ermöglicht.

### Ergebnisse und Analyse

Das entwickelte System zeigte eine hohe Präzision und Reaktionsfähigkeit bei der Positionsverfolgung in Echtzeit. Die von den UWB-Modulen gesendeten und vom ESP32 verarbeiteten Daten ermöglichten die Ortung eines beweglichen Objekts mit einer Fehlerquote von weniger als 20 cm.
<p align="center">
  <div style="display: flex; justify-content: center;">
    <img src="https://github.com/user-attachments/assets/92cf44eb-ecce-4f13-b941-4343075178d5" alt="Capture d'écran 2024-07-22 181003 - Copie" style="width: auto; height: 240px; margin-right: 10px;">
    <img src="https://github.com/user-attachments/assets/6bac45d7-c866-430e-99f8-74795ce5ec78" alt="IMG_20240722_181613 1" style="width: auto; height: 200px;">
  </div>
</p>

## The Maze Runner

Im Rahmen meines Studiums der Elektrotechnik habe ich an einem Wettbewerb für autonome Robotik teilgenommen. Die Aufgabe bestand darin, einen Roboter zu entwerfen, der in Rekordzeit aus einem Labyrinth herauskommt.

Wir hatten nur eine begrenzte Auswahl an Materialien zur Verfügung, was die Herausforderung umso interessanter machte:
- 1 Arduino UNO-Karte
- 1 Batterie
- 1 usb-Kabel
- 2 Servomotor mit kontinuierlicher Rotation
- 1 Servomotor 180°
- Blätter aus Hartpappe
- 2 Ultraschall-Distanzsensoren
- 1 PCB-Karten für Prototypen

Am Tag des Wettbewerbs navigierte der Roboter präzise und effizient durch das Labyrinth und gewann den ersten Platz.

![VID_20240219_182350(1) (online-video-cutter com) (1)](https://github.com/user-attachments/assets/517fcd24-457c-4e8b-ad78-b9be3997f2ef)
