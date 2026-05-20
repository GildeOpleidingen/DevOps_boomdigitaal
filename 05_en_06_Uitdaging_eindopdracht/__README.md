# 05 en 06 Uitdaging eindopdracht

> Deze eindopdracht vevangt de opdracht 5 en 6 van boom (deze hoef je niet te doen)
> Neem wel 2. uitrollen DevOps van 05 Uitollen DevOps door 

> Als je klaar bent met deze eindopdracht maak je een afspraak voor een cgi gesprek waar je het werk presenteert.

## Situatieschets
Je werkt als beginnende DevOps-engineer voor een snelgroeiende start-up. De organisatie levert diverse clouddiensten en verwacht binnen korte tijd op te schalen naar 100 medewerkers. Daarom moet de technische omgeving standaardiseerbaar, schaalbaar en volledig scriptbaar zijn.

---

## Wat moet er gebeuren?

### 1. Fysiek 10-inch rack
De opstelling bestaat uit:
- 1× MikroTik-router
- 2× Raspberry Pi 5
  - Pi #1: Linux-server
  - Pi #2: Ansible-server + Git server

### 2. MikroTik-router
Voor iedere klant wordt een loopback-interface aangemaakt:
- Omschrijving: customer <naam>
- IP-adres: beginnend bij 10.100.201.11, daarna oplopend

### 3. Linux-server (Raspberry Pi 5)
Voor elke klant moet automatisch (via Ansible) een gebruiker worden aangemaakt:
- Gebruikersnaam: <klantnaam>
- Groep: cloud_users
- Wachtwoord: klantnaam achterstevoren
- Geen shell-toegang

### 4. Automatiseren (Ansible)

Klanten:
- Stichting BCA
- Regenboog BV
- Vereniging Golf

### 5. Ticketsysteem (Docker)
Installeer osTicket via Docker op een van de Raspberry Pi’s.

### 6. Git server (Docker)

## DevOps-Werkwijze
1. YAML-bestanden worden aangepast
2. Commit naar Git
3. Ansible haalt veranderingen binnen
4. Configuraties worden uitgerold

---

## Voorbereiding – Plan van Aanpak

### Planning
Na het bestuderen van de opdracht maak je een planning hiervoor, gebruik ook een planningstool \
Zorg dat je de backlog vult met de stappen voor o.a. documentatie, rackopbouw, Pi-installaties, Ansible, Docker en testen.


### Documentatie oplevering

Beschrijf kort en duidelijk hoe jouw technische omgeving eruitziet.
Denk hierbij aan:

Linux-server(s)
Raspberry Pi
MikroTik-router
Docker containers
Git/ GitLab / versiebeheer
Ansible automatisering

Leg uit:

- Wat het systeem doet
- Waarom dit handig is voor een groeiend bedrijf
- Hoe alles met elkaar samenwerkt 

Welke DevOps-technieken ga je gebruiken?
Noem en beschrijf welke tools je gebruikt en waarom, zoals:
Git / GitLab (versiebeheer)
Ansible (automatisering)
Docker (containers)
YAML (configuratiebestanden)
SSH (beheer op afstand)

Leg per tool kort uit wat het doet in jouw project.

### Randvoorwaarden en risico’s

Beschrijf wat er nodig is om jouw systeem goed te laten werken, zoals:

netwerk (VLAN’s / IP-adressen)
servers of Raspberry Pi
Docker en Ansible installatie
GitLab toegang

Noem ook mogelijke risico’s, bijvoorbeeld:

verkeerde netwerkconfiguratie
firewall blokkeert toegang
SSH werkt niet goed
fouten in YAML of Ansible
verlies van configuraties

Schrijf het om in User Stories
Maak minimaal 3 user stories.
Gebruik dit format:
Als [rol] wil ik [doel] zodat [reden].
Bijvoorbeeld:
als systeembeheerder
als DevOps engineer
als support medewerker
Resultaat

## Uitvoering
Voer alles fysiek en technisch uit volgens het plan en documenteer dit in git.


## Terugkijken (Reflectie)
Schrijf over een moment waarop je iets anders of beter had kunnen doen en wat je ervan hebt geleerd.

