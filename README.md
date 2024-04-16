Ansible Role: Archlinux
=======================

An Ansible role that configures [Archlinux][] specifics.

Table of Contents
-----------------

<!-- toc -->

- [Requirements](#requirements)
- [Role Variables](#role-variables)
- [Dependencies](#dependencies)
- [Example Playbook](#example-playbook)
  * [Top-Level Playbook](#top-level-playbook)
  * [Role Dependency](#role-dependency)
- [License](#license)
- [Author Information](#author-information)

<!-- tocstop -->

Requirements
------------

- Ansible 2.9

Role Variables
--------------

For now, please check the templates. A more complete documentation will follow
later.

Dependencies
------------

```yml
---

# requirements.yml

roles:

  - name: idiv_biodiversity.archlinux
    src: https://github.com/idiv-biodiversity/ansible-role-archlinux
    version: vX.Y.Z

...
```

Example Playbook
----------------

### Top-Level Playbook

Write a top-level playbook:

```yml
---

- name: head server
  hosts: head

  roles:
    - role: idiv_biodiversity.archlinux
      tags:
        - archlinux

...
```

### Role Dependency

Define the role dependency in `meta/main.yml`:

```yml
---

dependencies:

  - role: idiv_biodiversity.archlinux
    tags:
      - archlinux

...
```

License
-------

MIT

Author Information
------------------

This role was created in 2024 by [Christian Krause][author] aka [wookietreiber at GitHub][wookietreiber], HPC cluster systems administrator at the [German Centre for Integrative Biodiversity Research (iDiv)][idiv].


[Archlinux]: https://archlinux.org/
[author]: https://www.idiv.de/en/groups_and_people/employees/details/61.html
[idiv]: https://www.idiv.de/
[wookietreiber]: https://github.com/wookietreiber
