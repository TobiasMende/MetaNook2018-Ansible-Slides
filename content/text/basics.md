# Ansible Grundlagen

--

## Playbooks

<div class='left-col'>
<ul>
  <li>Kollektion von „Tasks“, „Roles“, „Handlers“, …</li>
  <li>Beschreibung von Deployments, Configuration und Orchestrierung</li>
  <li>Beschreiben den gewünschten Zustand</li>
</ul>
</div>    
<div class='right-col'>
 <img src="content/images/playbook_structure.png" width="50%" />
</div>

--

## Tasks
* werden in der definierten Reihenfolge ausgeführt
* werden auf alle Maschinen angewendet
* führen Module mit spezifischen Argumenten aus

```yaml
- name: Installing Packages
  package:
    name: "{{ item }}"
    state: present
  with_items:
    - ufw
    - fail2ban
```

--

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

--

## Handler
werden am Ende ausgeführt, sofern notwendig.

```yaml
- name: write some_random_foo configuration
  template: src=templates/foo.j2 dest=/etc/foo.conf
  notify: restart apache
``` 
<!-- .element: class="fragment" -->

```yaml
- name: restart apache
  service: name=httpd state=restarted
``` 
<!-- .element: class="fragment" -->

--

## Inventory

* Enthält Gruppen, Hosts und ggf. Variablen
* Beschreibt, auf was das Playbook angewendet wird
* Statische und dynamische Inventories
* Statisch: .ini oder .yml
* Dynamisch: z.B. Python-Skripte

--

## Roles

* Sammlung von Variablen, Tasks, Dateien, Templates und Modulen
* Unterstruktur für Playbooks
* Wiederverwendbarkeit von Roles
* Docker Hub für Ansible Roles: https://galaxy.ansible.com

---

## Getting Started

* Python installieren (2 oder 3)
* Ansible installieren (Package Manager oder `pip`)
* ggf. SSH-Key auf Zielrechnern hinterlegen
* Erste Kommandos abfeuern mit `ansible`
* Erstes Playbook erstellen (z.B. mit `ansible-generate`)
* Playbook ausführen mit `ansible-playbook`