Zimbra MailServer installeren
=========

Deze rol installeert de Open Source Zimbra MailServer v9.0.0 op Rocky Linux 8.

Vereisten
------------

1. Een fresh install Rocky Linux 8
2. Minimum 8GB RAM
3. Minimum 15GB opslag
4. Vul de variabelen in

Rol variabelen
--------------

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
    - name: Installeer zimbra mailserver
      hosts: "{{ zimbra_server_IP }}"
      user: root
      roles:
        - zimbra
```


License
-------

Gebruik die maar, veel plezier.

Auteur informatie
------------------

Student aan AP Hogeschool Antwerpen, Bachelor Toegepaste informatica | Cyber Security & Cloud Computing
