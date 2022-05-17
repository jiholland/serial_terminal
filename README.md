Role Name
=========

Tcpdump from target. Fetch file.pcap from target to ansible-controller.

Requirements
------------

Tcpdump must be installed on target.

Role Variables
--------------

- capture\_time
- capture\_interface
- capture\_file
- capture\_src
- caputer\_dest

Dependencies
------------

None.

Example Playbook
----------------

    ---
    # ansible-playbook playbook_tcpdump.yml -e "target=localhost"
    - name: tcpdump from target and fetch .pcap to ansible-controller
      hosts: "{{ target }}"
      gather_facts: true
      gather_subset: network

      roles:
         - role: tcpdump
           tags: tcpdump

License
-------

BSD

Author Information
------------------

Jørn Ivar Holland
