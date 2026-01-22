# 1. Informieren
## 1.1 Ausgangslage
Im Rahmen dieses Projektes soll für ein Informatik-KMU eine containerisierte Serverlösung mit mehreren Diensten umgesetzt werden. Ziel ist es, mit Docker und docker-compose einen Applikationsstack aufzubauen, welcher verschiedene firmeninterne Services bereitstellt. Die Lösung soll übersichtlich dokumentiert, getestet und versioniert werden.

Der Fokus liegt auf dem Einsatz von Microservices sowie auf der persistenten Speicherung der Daten, um einen realitätsnahen Betrieb sicherzustellen.

## 1.2 Analyse der Anforderungen
Der Auftraggeber hat die folgenden Anforderungen definiert:
- Bereitstellung eines Media-Wiki für firmeninterne Zwecke.
- Einsatz der Open-Source Plattform Nextcloud für Filesharing und Kollaboration.
- Verwaltung des Quellcodes über eine eigene GitLab oder Gogs Instanz.
- Persistente Speicherung aller Daten und eingesetzten Dienste.
- Überwachung und Verwaltung mittels Portainer
- Versionierung der notwendigen Dateien sowie der Systemdokumentation in einem privaten GitHub-Repository.


Funktionale Anforderungen in Tabellarischer Form
Tabelle 1.1
| Dienst     | Beschreibung                | Port |
| ---------- | --------------------------- | ---- |
| MediaWiki  | Internes Firmen-Wiki        | 8085 |
| Nextcloud  | Filesharing & Kollaboration | 8080 |
| Git-Server | GitLab                      | frei |
| Portainer  | Monitoring                  | 9000 |

---

# 2. Planen

---

# 3. Entscheiden

---

# 4. Realisieren

---

# 5. Kontrolle

---

# 6. Auswertung