# Live Demo

--

## Szenario
Automatischer Aufbau einer Infrastruktur und Deployment für eine Web-Anwendung.

* *Loadbalancer:* lb01.vagrant.test
* *App-Server:* app01.vagrant.test und app02.vagrant.test
* *Datenbankserver:* db01.vagrant.test

Note: Add image / diagram?

--

## Umsetzung

* Vagrant zum Aufbau der Demo-Infrastruktur
* Ansible Playbook
    * Nginx als LB
    * MySQL als Datenbank
    * NodeJS für die Anwendung

[App Source Code](https://github.com/TobiasMende/MetaNook2018-Ansible-App) – [Ansible Playbook](https://github.com/TobiasMende/MetaNook2018-Ansible)