Zimbra MailServer installeren
=========

Deze rol installeert de Open Source Zimbra MailServer v9.0.0 op Rocky Linux 8.

Vereisten
------------

1. Een fresh install Rocky Linux 8
2. Minimum 8GB RAM (werkt ook op minder maar gaat moeizaam verlopen)
3. Minimum 15GB opslag
4. Vul de variabelen in

Rol variabelen
--------------

- Geef bij zimbra_server_IP de ip adress van server/machine waarop je zimbra wilt installeren.

```
zimbra_Domain_name: voorbeeld.be
zimbra_hostname: mail
zimbra_server_IP: 192.168.1.9
zimbra_fqdn: mail.voorbeeld.be
timezone: Europe/Brussels
zimbra_admin_password: uiopuiop
```

Voorbeeld Playbook
----------------

```
    - name: Installeer zimbra mailserver
      hosts: "{{ zimbra_server_IP }}"
      user: root
      roles:
        - zimbra
```

Voor het uit:

```
ansible-playbook playbook.yml
```

License
-------

MIT

Auteur informatie
------------------

Student aan AP Hogeschool Antwerpen, Bachelor Toegepaste informatica | Cyber Security & Cloud Computing

Special thanks
--------------

- Computingforgeeks.com voor de instructies om Zimbra 9 Mail Server te installeren op Rocky Linux.
- https://github.com/jmutai voor de prerequirements scripts. Deze scipts maken een A record en een MX record 
  aan. Ook passen deze scipts de firewall regels aan zodat enkel de poorten open staan die nodig zijn. 
  

Bronnen
-------

Instructies Zimbra 9 Mail Server installeren op Rocky Linux:
```
https://computingforgeeks.com/install-zimbra-mail-server-on-rocky-almalinux-rhel/
```

prerequirements scripts:
```
https://github.com/jmutai/scripts.git
```
