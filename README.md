# uptime_kuma – Ansible-Rolle für Uptime Kuma

Diese Ansible-Rolle installiert und verwaltet [Uptime Kuma](https://github.com/louislam/uptime-kuma) in einem Docker-Container.  
Zusätzlich unterstützt die Rolle **automatisiertes Backup** und **Wiederherstellung (Restore)** der Daten.

---

## 📦 Features

- Erstellt systemweiten Benutzer `kuma`
- Erstellt Verzeichnisstruktur unter `/opt/uptime-kuma`
- Deployt `docker-compose.yml` (gehärtet)
- Startet und verwaltet Uptime Kuma über Docker Compose
- Erstellt tar.gz-Backups von `/opt/uptime-kuma/data`
- Stellt Backups wieder her (inkl. optionalem Pre-Backup)
- Unterstützt `--tags` für gezielte Aktionen

---

## 🧾 Beispielverwendung

### 🔧 Inventory (`inventory/hosts.ini`)

Lokal:
```ini
[kuma_server]
188.245.242.150 ansible_user=admin ansible_port=2222
localhost ansible_connection=local
