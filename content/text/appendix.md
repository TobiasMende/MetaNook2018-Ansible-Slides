# Further Information

--

## Start now!

<ul>
  <li>install Python (2 or 3)</li> <!-- .element: class="fragment" -->
  <li>install Ansible (Package manager or `pip`)</li> <!-- .element: class="fragment" -->
  <li>transfer your pulbic SSH key to the target node</li> <!-- .element: class="fragment" -->
  <li>execute first commans with `ansible`</li> <!-- .element: class="fragment" -->
  <li>create your first playbook (i.e. with `ansible-generate`)</li> <!-- .element: class="fragment" -->
  <li>execute the playbook with `ansible-playbook`</li> <!-- .element: class="fragment" -->
</ul>

--

## Useful Tools

* VSCode with Ansible plugin
* ansible-generator
    * `pip install -U ansible-generator`

--

## Best Practices

### by [Ansible Doku](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html)

* one inventory file per environment (staging vs. production)
* separate top level playbooks by role
* unified folder structure

--

### Advantagses

* provide overview and structure
* enable fine granular executability
* avoid wrong targets (production instead of staging)

--

## Ansible Tower

* orchestration and monitoring
* credentials
* permissions
* visibility and compliance

see [Ansible Tower product page](https://www.ansible.com/products/tower)

--

## References

* [Quickstart Guide](https://docs.ansible.com/ansible/latest/user_guide/quickstart.html)
* [Szenario Guides](https://docs.ansible.com/ansible/latest/scenario_guides/guides.html)
* [Module Documentation](https://docs.ansible.com/ansible/latest/modules/modules_by_category.html)
* [Examples on Github](https://github.com/ansible/ansible-examples)

--

## Source Code ...

* [RevealJS Slides](https://github.com/TobiasMende/MetaNook2018-Ansible-Slides)
* [Ansible Playbook](https://github.com/TobiasMende/MetaNook2018-Ansible-Playbook)
* [Node JS Demo App](https://github.com/TobiasMende/MetaNook2018-Ansible-App)

[**View slides online!**](https://tobiasmende.github.io/MetaNook2018-Ansible-Slides/#/)

---
## Thank you for your attention!