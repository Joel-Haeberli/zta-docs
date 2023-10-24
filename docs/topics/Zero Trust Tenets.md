tags: #zero-trust #principles #tenets

# Zero Trust Tenets

links: [[000 Index|Index]], [[100 Zero Trust MOC]]

---

Das offizielle NIST Dokument definiert 7 Grundsätze (Tenets), welche in Zero Trust Umgebungen beachtet werden sollten. Diese Seite fast diese kurz zusammen. Die Seite [[Applying Zero Trust Tenets]] diskutiert und listet Technologien, welche zum Erreichen der Grundsätze im Cloudumfeld eingesetzt werden können.
### 1. Daten und Hardware sind Ressourcen
Quellen von Daten (Sensoren bis hin zu Datenbanken) sind Ressourcen. Auch private Geräte von Arbeitnehmern können als Ressource betrachtet werden.

### 2. Alle Kanäle sind gesichert
Dies bedeutet, dass auch interne Kanäle gesichert kommunizieren müssen und nicht aufgrund der Lage (in welchem Netzwerk sich das Gerät befindet) eines Gerätes innerhalb eines Netzwerkes tiefere Sicherheitsanforderungen gelten.

### 3. Zugriff auf Ressourcen wird pro Session vergeben
Für jede Session, werden die Zugriffsrechte auf einen Ressource durch einen Konsumenten erneut geprüft. Die Zugriffsrechte sollten zudem möglichst minimal vergeben werden.

### 4. Dynamische Regeln bestimmen über den Zugriff auf eine Ressource.
Diese Regeln können auf Eigenschaften der Identität, der Applikation oder dem anfragenden Asset basieren. Es können auch Verhaltensmuster oder Signale aus der Umgebung für die Evaluierung benutzt werden.

### 5. Die Organisation misst und überwacht die Integrität und Sicherheit aller ihr angehörenden und angehängten Assets.
Vertrauen ist nicht erbbar. Es sollte ein *Continues Diagnostics and Mitigation (CDM)* System verwendet werden, um laufend die Integrität von Assets neu zu beurteilen und bei Bedarf Massnahmen zu ergreifen. Dazu gehören nicht nur die Assets welche der Organisation gehören, sondern auch Assets mit denen sie in Verbindung steht.

### 6. Ressourcen werden alle dynamisch vor dem Zugriff authentisiert und authorisiert.
Vor jedem Zugriff auf eine Ressource wird die anfragende Entität authentisiert und authorisiert. In einem ersten Schritt wird festgestellt, wer die Entität ist (Authentisierung). Danach wird geprüft, ob die betreffende Entität Zugriff auf die Ressource hat (Authorisierung).

### 7. Die Organisation sammelt soviele Informationen über den aktuellen Zustand der Assets wie möglich und benutzt es zur Verbesserung der Sicherheit.
Daten zu Clients, Requests, Responses, Assets und Ressourcen sollen gespeichert und laufend automatisiert werden. Die gewonnenen Einsichten werden benutzt um die Sicherheit des Systems laufend zu verbessern.

---
links: [[000 Index|Index]], [[100 Zero Trust MOC]]