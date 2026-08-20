Audit de cybersécurité Blue Team — Bordeaux Football Club (projet)
> Audit défensif complet d'une infrastructure d'entreprise fictive : état des lieux, remédiations, mise en place d'une chaîne de détection (SIEM/IDS) et d'une capacité de réponse à incident.
> Projet réalisé dans le cadre de ma certification à la **Guardia Cybersecurity School** (Analyste en cybersécurité).
📄 Lire le rapport d'audit complet (PDF) — 35 pages : méthodologie, analyse des vulnérabilités, remédiations et preuves de détection.
---
Contexte
Audit Blue Team d'une infrastructure segmentée (VLAN, DMZ, Active Directory) suite à un scénario d'incident (fraude au président par ingénierie sociale). L'objectif : évaluer la posture de sécurité, la renforcer, et mettre en place une supervision opérationnelle.
Compétences démontrées
Architecture réseau sécurisée : segmentation VLAN, DMZ, pare-feu OPNsense, principe Zero Trust (Deny All)
Durcissement Active Directory : Tiering Model, nettoyage des comptes à privilèges, GPO ANSSI, audit Purple Knight (score 94/100)
Authentification : politique de mots de passe conforme ANSSI, déploiement du MFA (TOTP)
Durcissement système Linux : SSH, fail2ban, UFW, audit Lynis
Supervision (SIEM / IDS) : déploiement de Wazuh (agents Windows + Linux), Suricata, tuning des règles et réduction des faux positifs (~70 % → < 15 %)
Détection & réponse : mapping MITRE ATT&CK, analyse CVE, procédure de réponse à incident, analyse forensique (Wireshark)
Facteur humain : campagne de phishing simulée (Gophish), programme de sensibilisation
Référentiels appliqués
ANSSI (Guide d'hygiène, recommandations mots de passe) · NIST Cybersecurity Framework · NIST SP 800-207 (Zero Trust) · MITRE ATT&CK · Benchmarks CIS
Stack technique
`Wazuh` · `Suricata` · `OPNsense` · `Active Directory (Windows Server 2022)` · `Ubuntu Server` · `Kali Linux` · `Purple Knight` · `Gophish` · `Hydra` · `Lynis` · `fail2ban` · `Wireshark`
Approche red + blue
Bien que défensif, cet audit intègre des tests offensifs pour valider la chaîne de détection : brute-force SSH (Hydra) détecté par fail2ban + Wazuh + Suricata, scan réseau (Nmap) capturé et analysé, campagne de phishing (Gophish). Cette démarche illustre ma capacité à penser attaque et défense.
---
Projet pédagogique réalisé sur une infrastructure de laboratoire fictive et isolée. Toutes les données (entité, IP, comptes, incident) sont fictives.
