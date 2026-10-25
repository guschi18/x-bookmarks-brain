---
tags: [tools, research, llm-training]
sources: [tweet-2095333340153106905.md]
created: 2026-10-09
updated: 2026-10-09
---

# Quaddle

## Plattform (Stand 2026-09)

Petoi beschreibt Quaddle als handtellergroßen, faltbaren Quadruped für Lernen, Tüfteln und Physical AI. Die Kampagne unterscheidet Builder, Buddy und Scout als ausbaubare Funktionsstufen. Der Tweet nennt einen Einstieg ab 99 Dollar; der gespeicherte Kampagnentext kündigt Auslieferungen ab Anfang Dezember 2026 mit möglichen Verzögerungen durch Zertifizierung, Werkzeugbau und Transport an. Diese Angaben sind Launchversprechen, keine Bestätigung heutiger Preise oder Verfügbarkeit. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

**Kampagne:** [Quaddle auf Kickstarter](https://www.kickstarter.com/projects/petoi/quaddle-open-source-desktop-robot-kit). Die beschriebene Plattform ergänzt die [Robotics Learning Roadmap](../concepts/Robotics%20Learning%20Roadmap.md) um einen kleinen Quadruped, während deren SO-101-Beispiel auf Manipulation mit einem Arm zielt. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

## Mechanik und Steuerung (Stand 2026-09)

Vier modifizierte PWM-Servos bewegen die Beine; eine MinDoF-Mechanik koppelt Schulter und Knie pro Bein, statt beide separat anzutreiben. Als offizielle Optionen nennt Petoi P1L mit Positionsfeedback und kontinuierlicher Rotation sowie P090; die Konstruktion soll auch Standard-9g-Servos aufnehmen. Lauf-, Dreh- und Seitwärtsbewegungen sind Anbieterbeschreibungen, keine hier reproduzierten Messungen. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

Ein ESP32-S3 dient als Motion Core; ein weiterer ESP32-S3 übernimmt in entsprechender Ausstattung AI-Anwendungen und Smart Home. Ein Schalter kann den AI Core abschalten; ein oben montierter Raspberry Pi Zero kann per UART als alternative höhere Steuerung dienen. Snap-fit-Bauteile, austauschbare Fußspitzen und 3D-gedruckte Erweiterungen sollen Umbauten erlauben. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

## Simulation und Softwarezugang (Stand 2026-09)

Der [Browser-Simulator](https://www.petoi.com/pages/quaddle-robot-simulator) soll ESP32-S3-Steuerlogik und physikalische Dynamik emulieren: Code ändern, kompilieren und Bewegungen ohne echten Roboter ausprobieren. Die Kampagne nennt eine mobile Nutzung ohne lokale Installation und ein [URDF auf Hugging Face](https://huggingface.co/petoi/quaddle) für andere Simulatoren. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

**Softwarebasis:** [PetoiCamp/OpenCat-Quadruped-Robot](https://github.com/PetoiCamp/OpenCat-Quadruped-Robot). Der Text kündigt eine ESP32-S3-Version des Arduino-Codes an und nennt Blockprogrammierung, Python/MicroPython und Arduino C++ als Lernstufen. [Serielles Protokoll](https://guide.petoi.com/apis/serial-protocol) sowie UART, Bluetooth und WLAN dienen der Anbindung weiterer Rechner. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

Für [ROS/ROS 2](https://guide.petoi.com/apis/ros-and-ros2) beschreibt Petoi zwei Wege: Raspberry Pi Zero auf dem Roboter mit UART-Steuerung oder ROS auf einem externen Computer, der per WLAN/Bluetooth kommuniziert. Das sind dokumentierte Integrationswege, keine hier getestete vollständige ROS-Konfiguration. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

## Bewegungsaufzeichnung und Erweiterung (Stand 2026-09)

Buddy/Scout sollen per Hand geführte Bewegungen über Feedback-Servos aufnehmen und wiedergeben können. Bewegungen lassen sich laut Kampagne in den [Skill Composer](https://guide.petoi.com/applications/skill-creation) importieren, feinbearbeiten und teilen; die Firmware-Skills werden als textbasierte Datenstruktur beschrieben. Diese Bewegungsaufnahme belegt keine automatische Policy-Optimierung. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

Scout wird mit Wahrnehmung von Menschen, Geräuschen, Licht, Distanz und Gesten beworben; Vision ist als Add-on beschrieben. TuyaOpen und Xiaozhi AI nennt die Kampagne als bereits integrierte Dienste mit geplanter Offenlegung vor Lieferung. Beispiele für Umbauten sind ein NanoDuck und Mecanum-Rover; dafür nötige Räder und Spezialfußspitzen gehören nicht zum Standardkit. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)

## Grenzen der Anbieterangaben (Stand 2026-09)

Petoi nennt bis zu zwei Stunden unbelastetes Gehen, wechselbaren Akku und USB-Betrieb mit Laden. Tatsächliche Laufzeit, Qualität der Simulation, Servo-Lebensdauer und Integrationsverhalten wurden hier nicht reproduziert. Quaddle ist laut Kampagne nicht wasserdicht; das Paddelbeispiel ist nur ein Proof of Concept. LLM-basierte Gespräche und Smart-Home-Funktionen nutzen im beschriebenen Beispiel externe AI-Dienste; der lokale Motion Core allein belegt keinen vollständig lokalen AI-Betrieb. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)
