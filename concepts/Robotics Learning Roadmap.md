---
tags: [tools, research, llm-training]
sources: [tweet-2095189359037165674.md, tweet-2095333340153106905.md]
created: 2026-10-09
updated: 2026-10-09
---

# Robotics Learning Roadmap

## Ansatz (Stand 2026-09)

Der von hooeem zitierte Ronin-Artikel schlägt sechs Monate mit zwei bis drei Stunden täglich vor. Jede Stufe endet mit einem gebauten, getesteten und dokumentierten System; Lernziel ist praktische Arbeitsfähigkeit mit Hardware, keine Senior-Qualifikation nach sechs Monaten. Elektronik, Embedded, Mechanik, Software und Robot Learning werden als zusammenhängender Aufbau behandelt. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)

## Sechs Stufen (Stand 2026-09)

1. **Elektronik und Arbeitsmittel:** Ohmsches Gesetz, Spannungsteiler, Transistorschalter, Strombedarf, Schaltplan, Multimeter und Löten; zuerst Falstad/Tinkercad, danach reale Messungen. Python, Terminal und Git begleiten ab dem ersten Projekt die Arbeit. Aufgaben: Spannungsteiler simulieren, LED-Schalter aufbauen, Fehler elektrisch messen und Lötkontakte auf Durchgang prüfen. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)
2. **Mikrocontroller und Regelkreis:** Arduino, danach ESP32, PWM, Interrupts, I2C/SPI, nicht blockierendes Timing und Motoren mit Encoder. Aufgaben: Reaktionszeitspiel, Weboberfläche für Sensor/Servo, gezählte Radumdrehung und IMU-Komplementärfilter; als Monatsprojekte Linienfolger und Balancer mit dokumentierter Reglertuning-Iteration. Der Artikel bevorzugt TB6612FNG/DRV8833 gegenüber dem ineffizienteren L298N. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)
3. **Mechanik und Fertigung:** Ein CAD-Werkzeug vertiefen, Skizzen vollständig bestimmen, Parametrik, Baugruppen, Toleranzen und FDM-Materialwahl. Aufgaben: Servo-Halter nach Datenblatt, Toleranzlehre, Snap-fit-Gehäuse und ein Getriebe mit gemessenem Spiel. SO-101 als Leader/Follower-Arm aufbauen, kalibrieren, teleoperieren und eigene Greiferfinger testen. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)
4. **ROS 2 und Autonomie:** Nodes, Topics, Services, Actions, Parameters, Launch, colcon und ros2 bag; dann TF, xacro/URDF, Gazebo, ros2_control, SLAM Toolbox und Nav2. Aufgaben: eigene Multi-Node-Anwendung, eigener simulierter Roboter mit korrekten Trägheiten und Frames, Distanz-Action mit Feedback/Abbruch sowie Karte erstellen und navigieren. QoS-Mismatch, fehlende TF und schlechte Odometrie werden als wichtige Fehlerklassen genannt. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)
5. **Regelung, Kinematik und Wahrnehmung:** PID mit Windup/Filter/Feedforward, Zustandsraum, LQR/MPC, Vorwärts-/Inverse-Kinematik, Jacobian, Singularität, Kamerakalibrierung und 3D-Punktwolken. Aufgaben: Reglerantworten als CSV vergleichen, Cart-Pole mit LQR/PID, eigene Armkinematik prüfen, Objektposition aus kalibrierter Kamera schätzen und kollisionsfreien Pick-and-Place mit MoveIt 2 planen. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)
6. **Robot Learning und Portfolio:** LeRobot verbindet Teleoperation, synchronisierte Demonstrationen, Policy-Training und Deployment. Beispiel: 50 Demonstrationen auf SO-101 aufnehmen, ACT trainieren, Erfolg messen, weitere 50 gezielt für Fehlerfälle aufnehmen und erneut messen. Simulation mit MuJoCo Playground erlaubt einen Einstieg ohne eigenen Roboter. Portfolio-READMEs sollen Video, Diagramm, gemessene Werte und die behobenen Fehler zeigen. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)

## Ressourcen und Entscheidungen (Stand 2026-09)

Genannte Grundlagen sind All About Circuits, CS50P, Missing Semester, Arduino/Espressif-Dokumentation, Random Nerd Tutorials, Onshape/Fusion/FreeCAD, Articulated Robotics, offizielle ROS-2-/Gazebo-/Nav2-/MoveIt-Dokumentation, Brian Douglas, Steve Brunton, Modern Robotics, Peter Corke, Russ Tedrake, OpenCV, LeRobot und der Hugging-Face-Robotics-Kurs. Der gespeicherte Artikel enthält Namen und Beschreibungen, aber keine strukturierten Ressourcenlinks. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)

Zum Abschluss schlägt der Autor eine Spezialisierung vor: Robot Learning/Embodied AI, Autonomie/mobile Robotik oder Embedded/Mechatronik/Integration; die übrigen Bereiche bleiben Grundwissen. Theorie soll jeweils am eigenen System in Messung und Fehlersuche münden. Die Ros-Distro-Empfehlung Jazzy mit Gazebo Harmonic sowie Modell-/Lizenz-, Preis-, Hardware- und Gehaltsangaben sind der historische Artikelstand September 2026, keine aktuelle Kauf- oder Berufsempfehlung dieser Wiki. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)

## Grenzen (Stand 2026-09)

Der Zeitplan ist ein Vorschlag eines Autors ohne Ergebnisstudie; Hardwarezugang, Teilelieferung, Geld und Vorkenntnisse können ihn verändern. Zertifikate oder eine funktionierende Demo ersetzen in seiner Argumentation keine reale Zuverlässigkeit, dokumentierte Fehlerbehebung und Antworten auf Detailfragen zum eigenen Projekt. Arbeitsmarkt-, Finanzierungs- und Gehaltszahlen wurden hier nicht unabhängig verifiziert. [tweet-2095189359037165674](../sources/tweet-2095189359037165674.md)

## Zusätzliche Quadruped-Plattform (Stand 2026-09)

[Quaddle](../entities/Quaddle.md) bietet laut Petoi einen Browser-Simulator für ESP32-S3-Steuerlogik und Physik, ein veröffentlichtes URDF und OpenCat als Softwarebasis. Codeänderung, Bewegungssimulation und später UART-/ROS-Anbindung sind damit ein konkreter weiterer Werkzeugpfad für Quadruped-Experimente. Buddy/Scout beschreiben physisch geführtes Aufzeichnen und Wiedergeben von Bewegungen; das ist keine belegte ACT- oder LeRobot-Trainingsintegration. [tweet-2095333340153106905](../sources/tweet-2095333340153106905.md)
