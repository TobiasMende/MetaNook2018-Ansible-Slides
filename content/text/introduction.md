# Ansible
## Configuration as Code
### MetaNook 2018
 Tobias Mende | [@tobias_mende](https://twitter.com/tobias_mende) | [tobias-men.de](https://tobias-men.de)

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

## Principals

* Configuration of the environment must be automated.
* **Everything** is under version control.
* Keep it as simple as possible
* Configuration is tested

--

## Many Advantages!

<div class='left-col'>
<ul>
  <li>no implicit knowledge</li>
  <li>version control</li>
  <li>reviews</li>
  <li>traceability</li>
  <li>repeatability</li>
  <li>rollbacks</li>
  <li>CI/CD</li>
  <li>...</li>
</ul>
</div>    
<div class='right-col'>
 <img src="content/images/infrastructureascode.png"/>
</div>

---

# About Ansible

--

## What is Ansible?

* <!-- .element: class="fragment" --> Human readable automation for
    * app deployments
    * configuration management
    * orchestration of workflows
* <!-- .element: class="fragment" --> agentless with standard tools (SSH, Python)
* <!-- .element: class="fragment" --> community powered and open source
* <!-- .element: class="fragment" --> _by Red Hat _

--

## What can Ansible do?

* <!-- .element: class="fragment" --> bring systems into a desired state
* <!-- .element: class="fragment" --> execute commands on many nodes
* <!-- .element: class="fragment" --> automation without code
* <!-- .element: class="fragment" --> delarative syntax _(what, not how)_
* <!-- .element: class="fragment" --> modules for different domains
  * databases, networks, cloud, file systems, Unix, Windows, ...

--

## My Ansible Projects

* <!-- .element: class="fragment" --> server configuration 
    * webhosting, mailserver, ...
* <!-- .element: class="fragment" --> RaspberryPi configuration 
    * OpenHab, Homegear, ...
* <!-- .element: class="fragment" --> „thing“ configuration in the IoT 
    * Azure Edge, Docker, ...