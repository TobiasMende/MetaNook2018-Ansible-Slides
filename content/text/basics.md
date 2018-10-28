# Ansible Grundlagen

--

## Playbooks

<div class='left-col'>
<ul>
  <li>Kollektion von „Tasks“, „Roles“, „Handlers“, …</li><!-- .element: class="fragment" -->
  <li>Beschreibung von Deployments, Konfiguration und Orchestrierung</li><!-- .element: class="fragment" -->
  <li>Beschreiben den gewünschten Zustand</li><!-- .element: class="fragment" -->
</ul>
</div>    
<div class='right-col'>
 <img src="content/images/playbook_structure.png" width="50%" /> <!-- .element: class="fragment" -->
</div>

--

## Tasks
* werden in der definierten Reihenfolge ausgeführt <!-- .element: class="fragment" -->
* werden auf alle Maschinen angewendet <!-- .element: class="fragment" -->
* führen Module mit spezifischen Argumenten aus <!-- .element: class="fragment" -->

```yaml
- name: Installing Packages
  package:
    name: "{{ item }}"
    state: present
  with_items:
    - ufw
    - fail2ban
```
<!-- .element: class="fragment" -->

--

## Modules
* sollten idempotent sein <!-- .element: class="fragment" -->
* Ansible stellt über 450 verschiedene Module bereit <!-- .element: class="fragment" -->
* Bringe bestimmte Eigenschaften eines Systems in einen gewünschten Zustand <!-- .element: class="fragment" -->

```yaml
- name: Installing Packages
  package:
    name: "{{ item }}"
    state: present
  with_items:
    - ufw
    - fail2ban
```
<!-- .element: class="fragment" -->

--

## Handler
werden am Ende ausgeführt, sofern notwendig. <!-- .element: class="fragment" -->

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

* Enthält Gruppen, Hosts und ggf. Variablen <!-- .element: class="fragment" -->
* Beschreibt, auf was das Playbook angewendet wird <!-- .element: class="fragment" -->
* Statische und dynamische Inventories <!-- .element: class="fragment" -->
* Statisch: .ini oder .yml <!-- .element: class="fragment" -->
* Dynamisch: z.B. Python-Skripte <!-- .element: class="fragment" -->

--

## Roles

<ul>
  <li>Sammlung von Variablen, Tasks, Dateien, Templates und Modulen</li> <!-- .element: class="fragment" -->
  <li>Unterstruktur für Playbooks</li> <!-- .element: class="fragment" -->
  <li>Wiederverwendbarkeit von Roles</li> <!-- .element: class="fragment" -->
  <li>Docker Hub für Ansible Roles: https://galaxy.ansible.com</li> <!-- .element: class="fragment" -->
</ul>

---

## Getting Started

<ul>
  <li>Python installieren (2 oder 3)</li> <!-- .element: class="fragment" -->
  <li>Ansible installieren (Package Manager oder `pip`)</li> <!-- .element: class="fragment" -->
  <li>ggf. SSH-Key auf Zielrechnern hinterlegen</li> <!-- .element: class="fragment" -->
  <li>Erste Kommandos abfeuern mit `ansible`</li> <!-- .element: class="fragment" -->
  <li>Erstes Playbook erstellen (z.B. mit `ansible-generate`)</li> <!-- .element: class="fragment" -->
  <li>Playbook ausführen mit `ansible-playbook`</li> <!-- .element: class="fragment" -->
</ul>
