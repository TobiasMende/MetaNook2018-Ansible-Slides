# Ansible
## Configuration as Code
### MetaNook 2018
 Tobias Mende | [@tobias_mende](https://twitter.com/tobias_mende)

---

# Configuration as Code

--

<!-- .slide: data-background-image="content/images/ops-problem.jpg" data-background-size="contain" -->

--

> „Infrastructure as code is the approach to defining computing and network infrastructure through source code that can then be treated just like any software system.
>
> _Martin Fowler_

Notes:

* Unterschied Configuration / Infrastructure as Code:
  * CaC: Konfiguration bestehender Systeme
  * IaC: Erschaffung einer Infrastruktur
* Hier synonym verwendet
* Ansible kann beides

--

## Prinzipien

* Konfiguration der Umgebung muss automatisiert sein.
* **Alles** ist unter Versionskontrolle
* So einfach wie möglich halten!
* Konfiguration wird getestet

--

## Viele Vorteile!

<div class='left-col'>
<ul>
  <li>Kein implizites Wissen</li>
  <li>Versionskontrolle</li>
  <li>Reviews</li>
  <li>Nachvollziehbarkeit</li>
  <li>Wiederholbarkeit</li>
  <li>Rollbacks</li>
  <li>CI/CD</li>
  <li>...</li>
</ul>
</div>    
<div class='right-col'>
 <img src="content/images/infrastructureascode.png"/>
</div>

---

# Über Ansible

--

## Was ist Ansible?

* Menschenlesbare Automation
* App Deployment
* Konfigurationsmanagement
* Orchestration von Abläufen
* „Agentenlos“ mit Standard-Mitteln (SSH, Python)
* Community-Powered und Open Source

--

## Was kann Ansible?

* Systeme in einen gewünschten Zustand bringen
* Befehle auf mehreren Knoten ausführen
* Automatisierung ohne Code
* Deklarative Syntax _(Was, nicht wie)_
* Module für verschiedene Anwendungsgebiete
  * Datenbanken, Netzwerk, Cloud, Dateisysteme, Unix, Windows, ...

--

## Meine Ansible Projekte

* Server-Konfiguration 
    * Webhosting, Mailserver, ...
* RaspberryPi-Konfiguration 
    * OpenHab, Homegear, ...
* „Thing“-Konfiguration im IoT 
    * Azure Edge, Docker, ...