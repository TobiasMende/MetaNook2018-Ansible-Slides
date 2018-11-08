# Ansible Grundlagen

--

## Playbooks

<div class='left-col'>
<ul>
  <li>enthalten „Tasks“, „Roles“, „Handlers“, …</li><!-- .element: class="fragment" -->
  <li>beschreiben den gewünschten Zustand eines "Inventars"</li><!-- .element: class="fragment" -->
  <li>sind yml-Files</li><!-- .element: class="fragment" -->
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
* bringe bestimmte Eigenschaften eines Systems in einen gewünschten Zustand <!-- .element: class="fragment" -->
* Ansible stellt über 450 verschiedene Module bereit <!-- .element: class="fragment" -->

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

## Inventories

* enthalten Gruppen, Hosts und ggf. Variablen <!-- .element: class="fragment" -->
* beschreiben, auf was ein Playbook angewendet wird <!-- .element: class="fragment" -->
* können statische oder dynamische sein <!-- .element: class="fragment" -->
  * Statisch: .ini oder .yml <!-- .element: class="fragment" -->
  * Dynamisch: z.B. Python-Skripte <!-- .element: class="fragment" -->

--

## Roles

<ul>
  <li>sind Sammlungen von Variablen, Tasks, Dateien, Templates, ...</li> <!-- .element: class="fragment" -->
  <li>bieten Strukturierung von Playbooks</li> <!-- .element: class="fragment" -->
  <li>sind wiederverwendbar und können geteilt werden</li> <!-- .element: class="fragment" -->
  <li>Docker Hub für Ansible Roles: https://galaxy.ansible.com</li> <!-- .element: class="fragment" -->
</ul>
