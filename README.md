# PIRE Playbooks
This is a collection of playbooks for maintaining PIRE project.

## Prerequisites

The following system packages need to be installed on control machine.

* `python3`
* `python3-pip`
* `rpm-build` (rpm) if control machine runs Debian or Ubuntu)

The following python packages need to be installed on the control machine using `python3 -m pip`.

* `ansible`

## Run

Run `ansible-playbook` to execute playbooks.

```bash
ansible-playbook -i inventory/pire_webdav webdav/webdav.yml --ask-become-pass
```