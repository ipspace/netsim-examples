# Testing XML-to-JSON Conversion

Using structured data formatted as XML documents in Python-based automation solutions like Ansible is a fun exercise, more so when you have to deal with lists that might have a single element. Typical scenarios include:

* **show routes** executed on Junos with no IPv6 routing configuration. The **inet.6** routing table would have a single multicast route.
* **show vlan** executed on Nexus OS with no VLANs configured beyond VLAN 1.

The challenges are described in details in [Beware XML-to-JSON Information Loss](https://blog.ipspace.net/2021/01/beware-xml-json-information-loss.html) blog post and other blog posts in that series.

This directory contains test Ansible playbooks that interact with Junos and Nexus OS and correctly handle the cases of one-versus-many XML objects.

To test these examples on your own:

* Clone the repository.
* [Install *netsim-tools*](https://netsim-tools.readthedocs.io/en/latest/install.html)
* Within the `Ansible/XML` directory execute `netlab create`  to create *Vagrantfile*, Ansible inventory, and *ansible.cfg*
* Have fun

**Note:** The *Vagrantfile* created by the **netlab create** tool will be usable on a Linux system with *vagrant-libvirt* plugin. Please feel free to [add support for VirtualBox Vagrant boxes](https://netsim-tools.readthedocs.io/en/latest/contribute.html) to *[netsim-tools](https://github.com/ipspace/netsim-tools)* and submit a pull request.