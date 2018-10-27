# Was sonst noch?

---

## Best Practices

### laut [Ansible Doku](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html)

* Ein Inventory-File pro Umgebung (staging vs. production)
* Top Level Playbooks nach Rollen aufteilen
* Einheitliche Ordnerstruktur

### Vorteile

* schafft Überblick
* ermöglicht feingranulare Ausführbarkeit
* vermeidet falsche Ziele (production statt staging)

---

## Ansible Tower

* Orchestration  and Monitoring
* Credentials
* Permissions
* Visibility/ Compliance

siehe [Ansible Tower Produktseite](https://www.ansible.com/products/tower)

---

## Referenzen

* [Quickstart Guide](https://docs.ansible.com/ansible/latest/user_guide/quickstart.html)
* [Szenario Guides](https://docs.ansible.com/ansible/latest/scenario_guides/guides.html)
* [Module Documentation](https://docs.ansible.com/ansible/latest/modules/modules_by_category.html)
* [Beispiele auf Github](https://github.com/ansible/ansible-examples)

---

## Nützliche Tools

* VSCode mit Ansible Plugin
* ansible-generator
    * `pip install -U ansible-generator`