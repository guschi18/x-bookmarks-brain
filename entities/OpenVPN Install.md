---
tags: [tools, security]
sources: [tweet-2055579972039823438.md]
created: 2026-10-01
updated: 2026-10-01
---

# OpenVPN Install

## Rolle (Stand 2026-05)

[angristan/openvpn-install](https://github.com/angristan/openvpn-install) ist laut gespeicherter README ein Installer und Verwaltungswerkzeug für einen eigenen OpenVPN-Server auf Linux. Es erzeugt .ovpn-Clientprofile und verwaltet Zertifikate, Firewall und Forwarding; der Post bewirbt eine Einrichtung in Sekunden, ohne Messung. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

## Voraussetzungen und Bedienung

Die README verlangt Root-Rechte, aktiviertes TUN und systemd; die regelmäßigen Tests beziehen sich auf markierte Distributionen und amd64. Sie nennt Debian, Ubuntu, Fedora, openSUSE, Arch und mehrere Enterprise-Linux-Varianten mit Mindestversionen. Installation und Betrieb sind in dieser Quelle dokumentiert, nicht in diesem Ingest ausgeführt. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

Der interaktive Einstieg lautet ./openvpn-install.sh interactive. Die CLI nennt install, uninstall, client add/list/revoke/renew und server renew/status sowie JSON-Ausgaben für Automation. Da API-Kompatibilität nicht garantiert wird, empfiehlt der Projekttext für Automatisierung einen bestimmten Commit statt master. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

## Unabhängige Zugriffsregeln

Internetrouting ist standardmäßig aktiviert; Client-zu-Client-Zugriff und Zugriff auf serverseitige Netze sind deaktiviert. --local-network muss explizite CIDRs nennen; Netze dürfen die VPN-Pools nicht überschneiden. Für Heimnetzzugriff ohne Internetumleitung nennt die README --no-route-internet --local-network 192.168.1.0/24. Server-NAT lässt LAN-Geräte den VPN-Server als Absender sehen. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

## Sicherheitsoptionen im gespeicherten Stand

Als Defaults nennt der Installer AES-128-GCM, ECDSA/prime256v1, SHA256, TLS mindestens 1.2 und tls-crypt-v2. Kompression wird nicht mehr unterstützt; Client und Server sollen den Zertifikatstyp des Gegenübers über remote-cert-tls prüfen. Diese Angaben beschreiben das Projekt, keine Sicherheitsprüfung der Installation. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

PKI mit CA/CRL ist Standard; der alternative Fingerprint-Modus benötigt OpenVPN 2.6+ und selbstsignierte Peer-Zertifikate. Beim Entzug eines Fingerprints ist laut README ein Reload nötig, während eine CRL bei neuen Verbindungen automatisch gelesen wird; die Clientverwaltung beschreibt zusätzlich unmittelbare Trennung über die Management-Schnittstelle. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

## Versionen und Grenzen

Der Text nennt WireGuard für viele Anwendungsfälle einfacher und schneller, OpenVPN aber bei TCP-Bedarf, passwortgeschützten Schlüsseln oder Alt-Clients sinnvoll. DCO wird als optionale Kernelbeschleunigung unter versions-, Protokoll- und Cipher-Bedingungen beschrieben; UDP und AEAD gehören zu den genannten Voraussetzungen. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)

Die README vermischt aktuelle Optionen mit älteren FAQ-Empfehlungen, etwa für OpenVPN-2.4-Clients und CBC-Cipher; diese älteren Passagen sind keine einheitliche aktuelle Konfigurationsempfehlung. Anbieterpreise und die Datierung des Kernel-DCO-Eintrags wurden nicht geprüft. Der Autor warnt ausdrücklich davor, aus dem Einsatz des Skripts einen Schutz gegen die NSA abzuleiten. [tweet-2055579972039823438](../sources/tweet-2055579972039823438.md)
