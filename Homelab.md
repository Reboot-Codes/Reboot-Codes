# Homelab Structure
This is probably not up to date as I make changes a lot. 
Yes, all of the device codenames are from norse mythology.

## Codename Keys:
```yaml
NetworkAndStuff:
  Asguard: Network
  Odin: PC(s)
  Thor: Laptop(s)
  Loki: Tablet(s)
  Mjonir: Phone(s)
  Valkyrie:
    "S#": "Server running software that isn't dependant on a lot of storage (usually running Rancher)."
    "N#": "Server running software that is dependant on a lot of storage (usually running TrueNAS)."
   allNetworkedVMs: "Virtual Machines I need access to all over my network, which aren't many."
   allNetworkCameras: "Wyze cam v3's and Wyze Doorbell Pro"
   allSmortHomeStuff: "Homepod Mini's, Light Bulbs, and other smart home stuff, all connected to HASS in some way or another."
ReadingTheNetworkGraph:
  domain: "Signifies my domain (e.g. reboothasstuff.co or something). Shown as: hostedThing (desc: hostedThing.domain)"
  HAndS: "H is a hardware thing, and S is software/user on that thing."
```

## At the moment:
```txt
H Cox/ISP (Modem/WAN Connection)
S   Reboot (My network user)
H     Laptop (thor.local)
H     iPad (loki.local)
H     iPhone (mjonir.local)
H     Rasperry Pi 3B+ (valkyire.local)
S       Gitlab ("I was going to use Gitea, but it didn't have builtin CI/CD" -me: git.domain)
S       Uptime Kuma (Like uptimerobot, but selfhosted: uptime.domain)
S       Guacamole (VNC + HTTPS: guacamole.domain)
S       Home Asistant (Smart Home Hub on Sterioids: hass.domain)
```

## What I hope to happen...
```txt
H Cox/ISP (Modem/WAN Connection)
*   ...[otherDevices]
H   pfSense (Firewal/Gateway, Asguard)
H     UniFi CloudKey Gen 2+ (Ui Network Controler)
H     UniFi Switch Lite 16 PoE (Main Switch with Active PoE)
H       PC (Custom build, pcpart picker link in Setup.md: odin.local)
H       XBox (Yes, I know, an xbox, *gasp*)
H       TV (Samsung 32" something, something)
H       UniFi AP Lite 6 (Provides WiFi 6)
H         Laptop (MacBook Pro 13 M1: thor.local)
H         Tablet (iPad: loki.local)
H         Phone (iPhone: mjonir.local)
H         OSSCM (OpenSourceSmartCoffeeMaker, coffee.local)
H         ...[allNetworkCameras]
H         ...[allSmortHomeStuff]
H       Valkyrie S1 (Local management-ish stuff only)
S         Home Asistant (Smart Home Hub on Sterioids: hass.domain)
S         Ansible (Stuff management that uses SSH: ansible.domain)
S         Guacamole (VNC + HTTPS: guacamole.domain)
S         Uptime Kuma (Like uptimerobot, but selfhosted: uptime.domain)
S         Sentry ("Oh Shnap" manager: sentry.domain)
S         PiHole (An adblocking DNS: dns.domain)
H       Valkyrie S2 (More public facing stuff)
S         Website (Blog + Portfolio + Selfhosted Domain: domain)
S         SearX (Privacy friendly search engine: search.domain)
S         MailU (Mail server: *@domain)
S         Matrix (Decentralized chat: matrix.domain)
S         0x0.st Instance (self hosted link shortener + pastebin replacement. I might make my own...: 0x0.domain)
S         Heimdall (Hass Dashboard, Might make my own: dash.domain)
H       Valkyire N1 (Storage Heavy stuff, local + public)
S         Plex (Media server: plex.domain)
S         Gitlab ("I was going to use Gitea, but it didn't have builtin CI/CD" -me: git.domain)
S         SyncThing (Sync stuff between computers: syncthing.domain)
S         BackupPC (Self-Hosted backup system: backup-pc.domain)
S         Motion Eye (DVR for local cameras: motion.domain)
S         MineOS (Yes, a minecraft server: mc.domain)
S         Graphana (All the data: graphana.domain)
S         ...[allNetworkedVMs]
```
