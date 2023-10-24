tags: #zero-trust #principles #tenets #implementation #applying

# Applying Zero Trust Tenets

links: [[000 Index|Index]], [[100 Zero Trust MOC]]

---

### 1. Daten und Hardware sind Ressourcen
Dieser Grundsatz bedeutet, dass sowohl Daten wie auch ihre Quellen (Hardware, Sensoren, Speicher) gesichert werden müssen. Dies bedeutet, dass auch der physische Vektor bei der Implementation einer Zero Trust Umgebung massgebend ist. Alle auf den Daten und der Hardware aufbauende Sicherheitsmassnahmen bringen nichts, wenn die physische Sicherheit der Geräte nicht gewährleistet ist. Die Sicherheit kann erreicht werden, in dem bspw. alle Server in einem gesicherten Rechenzentrum mit entsprechenden Zugriffskontrollen betrieben werden und Geräte die eventuell draussen sind (Sensoren) über Systeme verfügen, physische Angriffe zu detektieren. Daten welche in einem permanenten Speicher liegen, müssen verschlüsselt abgelegt werden.

### 2. Alle Kanäle sind gesichert
Die Kanäle über welche kommuniziert wird, sind gesichert. Dies bedeutet dass für jede Verbindung ein [*Secure Channel*](https://janfuhrer.github.io/it-security-docs/themes/Secure%20Channels/#what-is-a-secure-channel) aufgebaut wird.

### 3. Zugriff auf Ressourcen wird pro Session vergeben
Dies bedeutet, dass sich Applikationen keine Zugriffe merken müssen, jedoch der Zugriff bei jedem Session-Beginn von neuem evaluiert werden muss.

### 4. Dynamische Regeln bestimmen über den Zugriff auf eine Ressource.
Die Regeln sollten über ein Interface festgelegt und gepflegt werden. Die Instanz welche die Regeln überprüft, sollte immer den neusten Stand haben.

### 5. Die Organisation misst und überwacht die Integrität und Sicherheit aller ihr angehörenden und angehängten Assets.
Dazu gehören scans aller devices und Sicherheitsaudits nicht zur Organisation gehörenden Komponenten, mit welchen kommuniziert wird.

### 6. Ressourcen werden alle dynamisch vor dem Zugriff authentisiert und authorisiert.


### 7. Die Organisation sammelt soviele Informationen über den aktuellen Zustand der Assets wie möglich und benutzt es zur Verbesserung der Sicherheit.

---
links: [[000 Index|Index]], [[100 Zero Trust MOC]]