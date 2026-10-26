---
tags: [security]
sources: [tweet-2114050517940990303.md]
created: 2026-10-26
updated: 2026-10-26
---

# Personal Cybersecurity Baseline

## Definition (Stand 2026-10)

Der von am.will empfohlene Leitfaden von Markets & Mayhem ordnet defensive Sicherheit nach dem Weg eines Angreifers: Zugangsdaten, Software, Netzwerk, Gerät und Menschen, die Zahlungen freigeben. Leitidee: Die meisten erfolgreichen Angriffe nutzen kein neues Exploit, sondern wiederverwendete Passwörter, ungepatchte Server oder hastige Menschen. Ziel ist, die Kosten eines Angriffs zu erhöhen, die unbemerkte Zeit des Eindringlings zu verkürzen und Wiederherstellung ohne Lösegeld zu ermöglichen. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)

## Lage laut Artikel (Autorenangaben)

Der Artikel zitiert den Verizon DBIR 2026: Ausnutzung von Schwachstellen (31 %) hat gestohlene Zugangsdaten (13 %) als häufigsten Einstieg überholt; nur 26 % der CISA-KEV-Einträge seien vollständig behoben, die mediane Behebungszeit steige von 32 auf 43 Tage; Ransomware in 48 % der Verstöße, 69 % der Opfer zahlten nicht. Der KEV-Katalog enthalte Stand 23.10.2026 1.756 Einträge. Diese Zahlen sind Zitate des Artikels und hier nicht geprüft. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)

## Maßnahmen

- Passwörter: Passwortmanager, einzigartige lange Passwörter; NIST: 15 Zeichen allein, 8 mit MFA, keine Kompositionsregeln, kein Pflichtwechsel nach Kalender; Wechsel nur bei Verdacht, Leak oder Personalwechsel; Have I Been Pwned für Alarme. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- MFA: Rangfolge Passkey/Hardware-Key vor TOTP, vor Push mit Number Matching, vor SMS, vor E-Mail-Code; zwei Security Keys registrieren, Recovery-Codes offline, SMS/Voice-Fallback entfernen, unerwartete MFA-Aufforderung als Warnsignal werten. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- Updates: automatisch inklusive Neustart, kurze Verzögerung; Organisationen mit Pilotring und Breitring; Geräte ohne Sicherheitsupdates nicht mehr für Banking und E-Mail nutzen. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- Software-Lieferkette: Install-Skripte blockieren (pnpm 10, ignore-scripts, allowScripts), Installation aus dem Lockfile (npm ci), Release-Cooldown (minimumReleaseAge, drei bis sieben Tage), Provenance, kurzlebige OIDC-Tokens statt Langzeit-Publish-Tokens, Build ohne Produktions-Secrets, Node.js LTS. Genannte Vorfälle: Shai-Hulud (2025), TanStack (Mai 2026, CVE-2026-45321). [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- Netzwerk: Router-Admin-Passwort, kein Remote-Admin, WPS und UPnP aus, Default-Deny eingehend, DNS-Filter (NextDNS, Quad9, Pi-hole), Gäste- und IoT-Netz getrennt, Segmentierung per Zugriff von Gast- oder IoT-Gerät testen. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- Geräte: Vollverschlüsselung (FileVault, BitLocker, LUKS) mit hinterlegtem Recovery-Key, App-Berechtigungen und OAuth-Freigaben prüfen, wöchentlicher Neustart (NSA-Hinweis), verschlüsselte Container oder Archive vor dem Cloud-Upload, Secrets nie in Notizen oder Repositories. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- Betrug und Deepfakes: Vertrauensphrase plus Rückruf auf bekannter Nummer, Zweitfreigabe und separate Prüfung bei Änderung von Bankdaten; Erkennen per Gehör ist keine Kontrolle. Der Arup-Fall (rund 25 Mio. USD) dient als Beispiel; die Umfragewerte von Gartner und Pindrop sind Autorenzitate, Pindrop hat ein kommerzielles Interesse. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- KI-Agenten für Sicherheitsarbeit: nur als unvertrauenswürdiger Analyst mit Nur-Lese-Kopien, Wegwerf-VM ohne Credentials, eingeschränktem Egress und Kostenlimit; Prompt Injection ist laut OWASP das Hauptrisiko. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
- Backups: 3-2-1 plus eine unveränderliche oder Offline-Kopie, getrennte Zugangsdaten, Verschlüsselung, Restore-Test mindestens vierteljährlich; ein Sync-Ordner ist kein Backup. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)

## 30-Tage-Plan für Einsteiger

Woche 1: Passwortmanager, E-Mail und Banking absichern, MFA, automatische Updates. Woche 2: Vollverschlüsselung, App-Berechtigungen, Breach-Alarme. Woche 3: Backups mit Offline-Kopie und Restore-Test, Gäste- und IoT-Netz, DNS-Filter. Woche 4: Verifikationsprotokoll mit Vertrauensphrase, Tabletop-Übung, verbundene Apps prüfen. [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)

## Grenzen

Die Quelle ist ein einzelner Leitfaden mit eigenen Statistiken; keine Zahl wurde unabhängig geprüft, und die Linkliste am Ende ist im Raw ohne URLs gespeichert. Die Empfehlungen zu Linux, Browsern und Mail-Verschlüsselung sind bewertende Aussagen des Autors. Für agentenspezifische Absicherung siehe [Claude Code Security Hardening](Claude%20Code%20Security%20Hardening.md). [tweet-2114050517940990303](../sources/tweet-2114050517940990303.md)
