# Grundlagen

---

## Playbooks
* Kollektion von „Tasks“, „Roles“, „Handlers“, …
* Beschreibung von Deployments, Configuration und Orchestrierung
* Beschreiben den gewünschten Zustand

Note: Add image

---

## Tasks
* werden in der definierten Reihenfolge ausgeführt
* für alle Maschinen
* führt ein Modul mit spezifischen Argumenten aus

```yaml
- name: Installing Packages
  package:
    name: "{{ item }}"
    state: present
  with_items:
    - ufw
    - fail2ban
```

---

## Modules
* sollten idempotent sein
* Ansible stellt über 450 verschiedene Module bereit
* Bringe bestimmte Eigenschaften eines Systems in einen gewünschten Zustand

```yaml
- name: Installing Packages
  package:
    name: "{{ item }}"
    state: present
  with_items:
    - ufw
    - fail2ban
```

---

## Handler
werden am Ende ausgeführt, sofern notwendig

```yaml
  - name: write some_random_foo configuration
    template: src=templates/foo.j2 dest=/etc/foo.conf
    notify:
    - restart apache
```

```yaml
- name: restart apache
  service: name=httpd state=restarted
```

---

## Inventory

* Enthält Gruppen, Hosts und ggf. Variablen
* Beschreibt, auf was das Playbook angewendet wird
* Statische und dynamische Inventories
* .ini oder .yml

```ini
[atlanta]
host1
host2

[raleigh]
host2
host3

[southeast:children]
atlanta
raleigh

[southeast:vars]
some_server=foo.southeast.example.com
halon_system_timeout=30
self_destruct_countdown=60
escape_pods=2

[usa:children]
southeast
northeast
southwest
northwest
```

---

## Roles

* Sammlung von Variablen, Tasks, Dateien, Templates und Modulen
* Unterstruktur für Playbooks
* Wiederverwendbarkeit von Roles
* Docker Hub für Ansible Roles: https://galaxy.ansible.com

---

## Getting Started

* Python installieren (2 oder 3)
* Ansible installieren (Package Manager oder pip)
* Erste Kommandos abfeuern
* Erstes Playbook erstellen (z.B. mit ansible-generate)
* ggf. SSH-Key auf Zielrechnern hinterlegen