# Weitere Informationen

--

## Anfangen!

<ul>
  <li>Python installieren (2 oder 3)</li> <!-- .element: class="fragment" -->
  <li>Ansible installieren (Package Manager oder `pip`)</li> <!-- .element: class="fragment" -->
  <li>ggf. SSH-Key auf Zielrechnern hinterlegen</li> <!-- .element: class="fragment" -->
  <li>Erste Kommandos ausführen mit `ansible`</li> <!-- .element: class="fragment" -->
  <li>Erstes Playbook erstellen (z.B. mit `ansible-generate`)</li> <!-- .element: class="fragment" -->
  <li>Playbook ausführen mit `ansible-playbook`</li> <!-- .element: class="fragment" -->
</ul>

--

## Nützliche Tools

* VSCode mit Ansible Plugin
* ansible-generator
    * `pip install -U ansible-generator`

--

## Best Practices

### laut [Ansible Doku](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html)

* Ein Inventory-File pro Umgebung (staging vs. production)
* Top Level Playbooks nach Rollen aufteilen
* Einheitliche Ordnerstruktur

--

### Vorteile

* schafft Überblick
* ermöglicht feingranulare Ausführbarkeit
* vermeidet falsche Ziele (production statt staging)

--

## Ansible Tower

* Orchestration  and Monitoring
* Credentials
* Permissions
* Visibility/ Compliance

siehe [Ansible Tower Produktseite](https://www.ansible.com/products/tower)

--

## Referenzen

* [Quickstart Guide](https://docs.ansible.com/ansible/latest/user_guide/quickstart.html)
* [Szenario Guides](https://docs.ansible.com/ansible/latest/scenario_guides/guides.html)
* [Module Documentation](https://docs.ansible.com/ansible/latest/modules/modules_by_category.html)
* [Beispiele auf Github](https://github.com/ansible/ansible-examples)

--

## Quellecode & Co.

* [RevealJS Slides](https://github.com/TobiasMende/MetaNook2018-Ansible-Slides)
* [Ansible Playbook](https://github.com/TobiasMende/MetaNook2018-Ansible-Playbook)
* [Node JS Demo App](https://github.com/TobiasMende/MetaNook2018-Ansible-App)

[**Folien online anschauen**](https://tobiasmende.github.io/MetaNook2018-Ansible-Slides/#/)

---
## Vielen Dank für die Aufmerksamkeit!