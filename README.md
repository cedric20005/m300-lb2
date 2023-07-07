# Kubernetes - M300

## Einführung
Im **Modul 300** habe ich eine Kubernetes-Umgebung lokal auf meinem Notebook installiert. Für die Konfiguration habe ich die Dokuemntation unter folgendem Link verwendet: [Konfiguration Kuberentes](https://gitlab.com/mbe99/kubernetes/-/blob/master/README.md).
In dieser Dokumentation befasse ich mich nur mit den Arbeitsschritten, die bei zur oben verlinkten Dokumentation abweichen.

## Lokales Netzwerk in Virtualbox
Das Einrichten des Netzwerkes wurde meiner Meinung nach in der Dokumentation von Marco Berger nicht genug behandelt. Ich selber bin beim Netzwerk auf viele Probleme gestossen, weswegen ich ein paar Erfahrungen sammeln konnte.
In meiner Kubernetes Umgebung habe ich 4 virtuelle Maschinen mit der gleichen Konfiguration verwendet.

**Verwendete Adapter:**
- Host-only
- NAT

Die Host-only Adapter habe ich jeweils mit einer statischen IP gesetzt. Der Host-only Adapter ist für die interne Kommunikation des Clusters. Ich habe die folgenden IP-Adressen vergeben:
- master-node - 192.168.11.11
- worker1-node - 192.168.11.12
- worker2-node - 192.168.11.13
- nfs-server - 192.168.11.100
Der NAT Adapter ist für die Verbindung ins Internet, dabei wurde die VM auf DHCP gestellt.

  
## Probleme - Troubleshooting