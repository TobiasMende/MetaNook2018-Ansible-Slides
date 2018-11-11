# Ansible Basics

--

## Playbooks

<div class='left-col'>
<ul>
  <li>contain „tasks“, „roles“, „handlers“, …</li><!-- .element: class="fragment" -->
  <li>describe the desired state of an "inventory"</li><!-- .element: class="fragment" -->
  <li>are yml files</li><!-- .element: class="fragment" -->
</ul>
</div>    
<div class='right-col'>
 <img src="content/images/playbook_structure.png" width="50%" /> <!-- .element: class="fragment" -->
</div>

--

## Tasks
* are executed in the defined order <!-- .element: class="fragment" -->
* are executed on all nodes <!-- .element: class="fragment" -->
* execute a specific module with specific arguments <!-- .element: class="fragment" -->

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
* should be idempotent <!-- .element: class="fragment" -->
* bring a specific property of a system into the desired state <!-- .element: class="fragment" -->
* Ansible provides more than 450 different modules <!-- .element: class="fragment" -->

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
are executed at the end, if neccesary. <!-- .element: class="fragment" -->

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

* contain groups, hosts and (maybe) variables <!-- .element: class="fragment" -->
* describe, on what a playbook should be applied <!-- .element: class="fragment" -->
* can be static or dynamic <!-- .element: class="fragment" -->
  * static: .ini or .yml <!-- .element: class="fragment" -->
  * dynamic: i.e. Python scripts <!-- .element: class="fragment" -->

--

## Roles

<ul>
  <li>are collections of varibles, tasks, files, templates, ...</li> <!-- .element: class="fragment" -->
  <li>provide structure for playbooks</li> <!-- .element: class="fragment" -->
  <li>are reusable and can be shared</li> <!-- .element: class="fragment" -->
  <li>Docker Hub for Ansible Roles: https://galaxy.ansible.com</li> <!-- .element: class="fragment" -->
</ul>
