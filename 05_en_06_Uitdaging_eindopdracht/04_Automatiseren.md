
# 6. Ansible configureren

## Uitvoeren

- Ansible installeren
- Inventory maken
- SSH-toegang testen
- Pingtest uitvoeren

---

## Voorbeeld inventory

```ini
[raspberry]
pi-01 ansible_host=10.10.30.10
```

---

## Bewijs

```bash
ansible all -m ping
```

Maak screenshots van:

- Succesvolle pingtest
- Inventory bestand
- Ansible versie

---

# 7. Klantaccounts automatiseren

## Doel
Automatisch gebruikersaccounts aanmaken voor klanten met Ansible.

---

## Klanten

| Klant | Username | Wachtwoord |
|---|---|---|
| Stichting BCA | stichtingbca | acbgnithcits |
| Regenboog BV | regenboogbv | vbgoobneg |
| Vereniging Golf | vereniginggolf | floggnigineerev |

---

## Vereisten

- Gebruikers toevoegen aan groep `cloud_users`
- Wachtwoord instellen
- Geen shell toegang toestaan

---

## YAML voorbeeld

```yaml
users:
  - name: stichtingbca
    password: "acbgnithcits"

  - name: regenboogbv
    password: "vbgoobneger"

  - name: vereniginggolf
    password: "floggnigineerev"
```

---

## Bewijs

```bash
cat /etc/passwd
getent group cloud_users
```

Maak screenshots van:

- Aangemaakte gebruikers
- cloud_users groep
- Uitgevoerde playbook

---

# 8. YAML validatie

## Uitvoeren

Controleer YAML-bestanden op fouten.

---

## Commando

```bash
ansible-playbook site.yml --syntax-check
```

---

## Bewijs

Maak screenshots van:

- Syntax check
- Succesvolle uitvoering

---

# 9. Eindcontrole

## Controlepunten

| Onderdeel | Controle |
|---|---|
| SSH | Werkt met SSH keys |
| Docker | Containers draaien correct |
| osTicket | Webinterface bereikbaar |
| GitLab | Repository werkt |
| Ansible | Playbooks succesvol |
| Gebruikersbeheer | Accounts correct aangemaakt |
| Security | Geen shell-toegang voor klanten |

---

# Reflectie

Beantwoord de volgende vragen:

1. Wat ging goed tijdens de configuratie?
2. Welke problemen ben je tegengekomen?
3. Hoe heb je deze problemen opgelost?
4. Wat zou je de volgende keer anders doen?
5. Wat heb je geleerd over Linux, Docker en automatisering?
