# HF_NWD_ITSE21a_Mylvaganam_Oehninger_Koenig

# Auftrag GNS3 Labor VPN:

## 1 Einleitung
Sie haben als Netzwerkingenieur den Auftrag erhalten in einem KMU einen zusätzlichen Geschäftsstandort per VPN zu erschliessen. Das KMU hat keinen eigenen Betriebsinformatiker. Jedes Mal, wenn eine Erweiterung des Netzwerkes benötigt wurde, hat das KMU eine andere IT-Firma beauftrag. Das hat zur Folge, dass überall unterschiedliche Geräte und VPN-Technologien eingesetzt wurden. Das ist eine optimale Gelegenheit, um neue VPN-Technologien kennenzulernen und zu vergleichen!
Die Wahl des Gerätes für Lausanne steht Ihnen frei. Alle anderen Standorte haben einen funktionierenden Internetanschluss und eine funktionierende VPN-Verbindung an den Hauptstandort in Zürich. In der Mitte finden Sie ein Netzwerk eines fiktiven ISP. Der verwendet OSPF als internes Routing-Protokoll (iBGP eignet sich für ISP besser). Über den ISP können sie auch auf das Internet zugreifen.

### Lernziele:
- Unterschiedliche VPN-Technologien kennenlernen
- VPN auf einem Router konfigurieren, testen und dokumentieren
Die messbaren Ziele sind direkt im GNS3 Projekt zu finden (siehe Screenshot oben).
Technische Berufsschule Zürich
Abteilung IT | HF | NWD
Philipp Albrecht, Stefan Kemper | NWD GNS3 Labor VPN V1.docx | 03.06.2023 2/3

## 2 Themengebiete
Diese Laborübung beinhaltet folgende Themengebiete:
- Kernthema: VPN Technologien OpenVPN, Wireguard, IPsec
- IP-Protokolle, namentlich IPv4 und IPv6
- Standardprotokolle wie HTTP, DHCP, DNS, ARP, ICMP, usw.
- Bedienung bzw. Konfiguration und Steuerung von Netzwerkgeräten und Server über die CLI
- Betriebssysteme: Cisco IOS, MikroTik RouterOS, pfsense
- Netzwerkdokumentation
 
## 3 Allgemeine Instruktionen
Bitte lesen Sie diese Instruktionen sorgfältig durch und fragen Sie bei Unklarheiten den Kursleiter.
In diesem Modul arbeiten Sie mit der Netzwerksimulationssoftware GNS3, mit der Sie per Drag-and-Drop Topologien in Sekundenschnelle aufbauen können. Im Hintergrund arbeitet GNS3 mit Qemu-KVM VMs für die Switche und Router und verbindet diese bezüglich Ihrer Topologie mit Linux-Bridges. Weitere Informationen zum Aufbau der TBZ Cloud Infrastruktur finden Sie im Repository https://gitlab.com/ch-tbz-it/Stud/allgemein/tbzcloud-gns3

Sie arbeiten jeweils in Zweier-Teams am selben Labor auf demselben Server bzw. derselben TBZ Cloud GNS3 Instanz. Wie Sie eine Verbindung zu Ihrer Instanz aufbauen können, erfahren Sie unter https://gitlab.com/ch-tbz-it/Stud/allgemein/tbzcloud-gns3/-/tree/main/02_Bedienungsanleitung . Den OpenVPN Key zu Ihrer Instanz erhalten Sie vom Kursleiter.

Damit Sie die Aufgaben lösen können, müssen Sie selbstständig im Internet recherchieren. Nicht alle notwendigen Informationen sind in diesem Dokument vorhanden.
Folgende Zugangsdaten sind bekannt:
- MikroTik: Benutzername: admin, Passwort: tbz1234
- Debian: Benutzername: debian, Passwort: debian
- Cisco: Passwort: tbz1234
- Standardpasswörter zum Ausprobieren: cisco, debian, admin1234, admin

## 4 Aufgaben
### 4.1 VPN Technologien per Packet Capture analysieren
Die drei verwendeten VPN-Technologien bauen auf unterschiedlichen Netzwerkstacks auf. Analysieren Sie die unterschiedlichen Protokolle mithilfe von Wireshark Captures und halten Sie Unterschiede in den Netzwerkstacks fest. Beantworten Sie mithilfe der Packet Caputes zusätzlich folgende Fragen in Ihrem Bericht: Weshalb kann IPSec und NAT ein Problem darstellen?

### 4.2 Neuen Standort Anbinden
1. Lesen Sie die Anforderungen an das Netzwerk und das Ziel. Entscheiden Sie sich für einen Router-Typ und richten das Gerät ein.
2. Richten Sie den Zugriff für Worker1 ein. Worker1 hat bereits via OpenVPN und Wireguard Zugriff auf zwei Standorte.
3. Testen und Konfigurieren Sie so lange bis alle Anforderungen erfüllt sind.
4. Dokumentieren Sie alle getätigten Konfigurationen so, dass eine andere Fachperson Ihre Konfiguration möglichst schnell nachbauen kann und versteht, was sie dabei tut (Dazu gehört unter anderen auch, dass sie z.B. alle Befehle per Copy-Paste einfügen kann)
Wenn Sie den Bericht abgeben, muss ihr Netzwerk in einem funktionsfähigen Zustand sein. Der Kursleiter wird nebst dem Bericht auch ihr GNS3 Labor überprüfen.
Technische Berufsschule Zürich
Abteilung IT | HF | NWD
Philipp Albrecht, Stefan Kemper | NWD GNS3 Labor VPN V1.docx | 03.06.2023 3/3
## 5 Hinweise zur Dokumentation
- Beschränken Sie sich auf das Wesentliche. Unterlassen Sie es leere Sätze oder persönliche Statements zu schreiben. Fokussieren Sie sich auf die Sachlage.
- Nachvollziehbarkeit: Anhand ihrer Dokumentation müssen Dritte in der Lage sein, alles exakt genau gleich nachbauen zu können.
- Erstellen Sie pro Gruppe ein eigenes privates Repository mit dem Namen HF_NWD und pushen Sie dieses auf GitLab (Alternativ GitHub). Gewähren Sie der Lehrperson den Zugriff auf das Repository.
- Machen Sie bei der Abgabe einen Export des aktuellen Repository-Standes und geben diesen als ZIP-File via Teams-Aufgabe ab.
- Die gesamte Dokumentation muss in Markdown erfolgen. Fügen Sie erstellte Netzwerktopologien als Grafiken ein.
- Alle Grafiken sind scharf und müssen gut zu lesen sein.
- Als Inspiration können Sie die Vorlagen von diesem Repository verwenden: https://gitlab.com/alptbz/beispiel-lernjournal-fuer-laboruebungen . Lassen Sie die Reflexion und das aufführen ihrer neuen Lerninhalte weg.
## 6 Regeln
- Es dürfen keine Geräte entfernt oder hinzugefügt werden – ausser am Standort Lausanne.
- Es ist erlaubt zu Testzwecken z.B. ein Ubuntu Desktop an einem Port anzuschliessen – wie wenn Sie ein Laptop an einem «echten» Router oder Switch einstecken.
- Alle Kabelverbindungen zwischen den Geräten sind fix. Erstellen Sie keine neuen (Ausser die für Lausanne – siehe Hinweis im GNS3 Projekt).
## 7 Bewertungskriterien und Abgabetermin
Informieren Sie sich bei der Kursleitung betreffend Abgabetermin und Bewertungskriterien. Zu spät abgegebene (bis 24h) Arbeiten erhalten Abzug nach Ermessen der Kursleitung. 24 Stunden nach dem Abgabetermin werden keine Arbeiten akzeptiert und die Aufgabe gilt als nicht erfüllt.

# Dokumentation Labor
## VPN Technologien per Packet Capture analysieren
Platzhalter für Antwort

## Konfiguration Labor:
### Standort Lausanne:
Um den Standort Lausanne aufzubauen haben wir einen neuen MikroTik CHR 7.5 Router und einen Debian 11.4 PC erstellt.
Vom Router I-R1 ether6 eine Verbindung zum neuen Router ether1 und vom neuen Router ether2 zum Debian PC ens4 erstellt.
Beim neuen Router über die Console mit dem Default Login: admin PW:"blank" angemeldet und auch unser Passwort tbz1234 gesetzt.
Danbach den Router dann mit folgendem Befehl gemäss dem bestehenden Namenskonzept umbenannt:

    /system identity set name=LS-R1

Danach muss die IP-Adresse konfiguriert werden:
ether1:

    /ip address add address=203.0.113.70/30 interface=ether1 network=203.0.113.69

Nun muss eine "0-Route" definiert werden:

    /ip route add dst-address=0.0.0.0/0 gateway=203.0.113.69

Um auch DNS Requests bearbeiten zu können muss ein DNS Server definiert werden. Wir nutzen hierzu den öffentlichen DNS von Google mit der IP: 8.8.8.8

    /ip dns set allow-remote-requests=yes servers=8.8.8.8

Das "interne Netz" hinter dem Router LS-R1 muss auch konfiguriert werden, damit PC's über den Router gerouted werden können:

    /ip address add address=192.168.13.1/24 interface=ether2 network=192.168.13.0

Nun kann ein Server Netzwerk definiert werden. Dies mit einem DHCP damit die IP's dynamisch verteilt werden:

    /ip pool add name=dhcp_server ranges=192.168.13.20-192.168.13.50

    /ip dhcp-server network add address=192.168.13.0/24 dns-server=192.168.13.1 gateway=192.168.13.1

    /ip dhcp-server/add address-pool=dhcp_server interface=ether2 name=dhcp_server1

Nun muss noch eine Firewall NAT für den ausgehenden Verkehr erstellt werden

    /ip firewall nat add chain=srcnat action=masquerade out-interface=ether1

Dies erstellt eine einfache ausgehende NAT-Regel, die alle ausgehenden Verbindungen von den internen Geräten zur Internetverbindung des Routers übersetzt. 

Die Konfiguration muss dann manuell gespeichert werden:

    /system backup save name=LS-R1

Somit ist die Konfiguration für das Netzwerk in Lausanne soweit abgeschlossen.

### Wireguard Site-To-Site VPN Lausanne <-> Zürich
Auf beiden Routern, Lausanne LS-R1 und Zürich ZH-R1, muss das WireGuard Interface konfiguriert werden:
LS-R1:

    /interface/wireguard add listen-port=13234 name=LSZH

    /interface/wireguard print

    Keys von LS-R1 "LSZH":
    name="LSZH" mtu=1420 listen-port=13234
      private-key="MJtgEC/F8pfr847sMrdPViQlT03LEveGobsmFSZGlWY="
      public-key="hIyMi0/AA59z6bKV2zhEVhaK2QFjMtxZiEH5ET4xAG8="

ZH-R1:

    /interface/wireguard add listen-port=13234 name=ZHLS

    /interface/wireguard print

    Keys von ZH-R1 "ZHLS":
    name="ZHLS" mtu=1420 listen-port=13234
      private-key="6Axy3t2TcUKMFGVrF6Eoh2SUJJ6AKxdYOCdkInA6j3Q="
      public-key="bOMUgC3g1ec36LPZ+Hpvt8Mo50b1zuv6k7Wykk/LfEU="

Peer konfiguration:
LS-R1:

    /interface/wireguard/peers add allowed-address=192.168.9.0/24 endpoint-address=203.0.113.98 endpoint-port=13234 interface=LSZH \
    public-key="bOMUgC3g1ec36LPZ+Hpvt8Mo50b1zuv6k7Wykk/LfEU="

ZH-R1:

    /interface/wireguard/peers add allowed-address=192.168.13.0/24 endpoint-address=203.0.113.70 endpoint-port=13234 interface=ZHLS \
    public-key="hIyMi0/AA59z6bKV2zhEVhaK2QFjMtxZiEH5ET4xAG8="

VPN Routing:
LS-R1:

    /ip/address add address=192.168.250.1/30 interface=LSZH
    /ip/route add dst-address=192.168.9.0/24 gateway=LSZH

ZH-R1:

    /ip/address add address=192.168.250.1/30 interface=ZHLS
    /ip/route add dst-address=192.168.13.0/24 gateway=ZHLS

Dann müssen noch Firewall anpassungen gemacht werden, damit die Kommunikation nicht mehr blockiert wird von dem VPN:
LS-R1:

    /ip/firewall/filter
    add action=accept chain=input dst-port=13234 protocol=udp src-address=203.0.113.98
    add action=accept chain=input dst-port=13234 protocol=udp src-address=192.168.250.2
    add action=accept chain=forward dst-address=192.168.9.0/24 src-address=192.168.13.0/24
    add action=accept chain=forward dst-address=192.168.13.0/24 src-address=192.168.9.0/24

ZH-R1:

    /ip/firewall/filter
    add action=accept chain=input dst-port=13234 protocol=udp src-address=203.0.113.70
    add action=accept chain=input dst-port=13234 protocol=udp src-address=192.168.250.1
    add action=accept chain=forward dst-address=192.168.13.0/24 src-address=192.168.9.0/24
    add action=accept chain=forward dst-address=192.168.9.0/24 src-address=192.168.13.0/24

### Wireguard RoadWarrior VPN Worker1 <-> Lausanne
Auf dem Router in Lausanne muss hier auch zuerst ein Wireguard Interface erstellt werden:
LS-R1:

    /interface/wireguard add listen-port=13231 name=RWLS
    /ip address add address=192.168.14.1/24 interface=RWLS network=192.168.14.0

    Keys von LS-R1 "RWLS":
    name="RWLS" mtu=1420 listen-port=13231
      private-key="iAWpcqf7/q6dZcjxE6U3XUfVM50x6gtQ1Mev89xOaHU="
      public-key="nUAD6T4nqjWSl08cB9auIbyGkDTMXToQlewDmft67mc="

Danach muss ein peer konfiguriert werden zum remote Gerät, also dem Worker1. Dafür benötigen wir den Public Key des Worker1:

   /interface wireguard peers add allowed-address=192.168.14.2/32 interface=MTW_LS \
   public-key="public Key des Remote Devices"

Worker1:
Der Worker1 funktioniert bei uns im Labor aktuell nicht. Daher können wir den Public Key nicht herauslesen und auch den File-Share nicht Einbinden um dies zu testen...

Wir haben uns aufgrund der Probleme mit dem Worker1 und da wir nicht wussten, ob wir etwas falsch gemacht haben, bei einer anderen Gruppe um Hilfe gefragt und dies zusammen angeschaut. Leider konnten wir den Worker1 nicht zum laufen bringen. Gerne liefern wir dies noch nach, sollte der Worker1 wieder gefixt werden können.

#### File-Share
Auf dem erstellten Debian PC im Lausanne Netzwerk loggen wir uns mit dem Login: debian PW: debian ein.
Um auf dem PC einen File-Share installieren zu können, müssen wir diesen zuerst updaten:

    sudo su
    apt-get update
    apt update
    apt install samba

Somit ist Samba installiert. Danach können wir Samba konfigurieren:
User erstellen:

    sudo useradd worker1
    
    sudo passwd worker1 
    tbz1234

SMB User erstellen:

    smbpasswd -a worker1
    tbz1234

File-Share Ordner erstellen:

    mkdir /home/File-Share

Berechtigung des Ordners für den User anpassen:

    chown worker1 File-Share
    chgrp worker1 File-Share

Ordner Share in der Samba Konfiguration hinzufügen:

    sudo nano /etc/samba/smb.conf

    [File-Share]
    path = /home/File-Share
    readonly = no
    inherit permission = yes

Neustarten des Service, damit die Konfiguration aktiv wird:

    service smbd restart

Danach dürfte der File-Share vorhanden sein und funktionieren. Dieser sollte vom Worker1 im Café eingebunden werden können.

### IPSec Site-to-Site VPN Lausanne <-> Basel
LS-R1:

Wir richten für das IPSec VPN ein Profil ein mit der Diffie-Hellmann Group 14	2048 bits MODP RFC 3526 ein. Dies definiert die Methode und den Algorithmus der Verschlüsselung:

    /ip ipsec profile add dh-group=modp2048 enc-algorithm=aes-128 name=LSBS

    /ip ipsec proposal add enc-algorithms=aes-128-cbc name=LSBS pfs-group=modp2048

Danach muss ein Peer zum Router, welcher erreicht werden muss, eingerichtet werden:

     /ip ipsec peer add address=203.0.113.82/32 name=LSBS profile=LSBS

Danach muss eine Identity mit einem "secret" erstellt werden:

    /ip ipsec identity add peer=LSBS secret=tbz1234

Nun braucht es auch hier wieder eine Richtlinie für die Verbindung:

    /ip ipsec policy add dst-address=192.168.11.0/24 peer=LSBS proposal=LSBS src-address=192.168.13.0/24 tunnel=yes

Damit auch Daten über die Verbindun gesendet werden können, benötigt es nun noch eine NAT Regel.

    /ip firewall nat add action=accept chain=srcnat dst-address=192.168.11.0/24 src-address=192.168.13.0/24

Es gibt nun noch Probleme, dass nicht alle Pakete ankommen. Grund ist z.B. IP Fasttrack. Somit müssen wir noch eine Firewall Regel hinzufügen, damit dies auch akzeptiert wird:

    /ip firewall filter add chain=forward action=accept place-before=0 src-address=192.168.11.0/24 dst-address=192.168.13.0/24 connection-state=established,related
    /ip firewall filter add chain=forward action=accept place-before=1 src-address=192.168.13.0/24 dst-address=192.168.11.0/24 connection-state=established,related

Nun muss die gleiche Konfiguration auf dem Router in Basel eingerichtet werden:
BS-R1:

    /ip ipsec profile add dh-group=modp2048 enc-algorithm=aes-128 name=BSLS

    /ip ipsec proposal add enc-algorithms=aes-128-cbc name=BSLS pfs-group=modp2048
    
    /ip ipsec peer add address=203.0.113.70/32 name=BSLS profile=BSLS
    
    /ip ipsec identity add peer=BSLS
    
    /ip ipsec policy add dst-address=192.168.13.0/24 peer=BSLS proposal=BSLS src-address=192.168.11.0/24 tunnel=yes
    
    /ip firewall nat add action=accept chain=srcnat dst-address=192.168.13.0/24 src-address=192.168.11.0/24
    
    /ip firewall filter add chain=forward action=accept src-address=192.168.11.0/24 dst-address=192.168.13.0/24 connection-state=established,related
    /ip firewall filter add chain=forward action=accept src-address=192.168.13.0/24 dst-address=192.168.11.0/24 connection-state=established,related

## Weshalb kann IPSec und NAT ein Problem darstellen?

Nat und IPSec VPN können sich aufgrund ihrer unterschiedlichen Herangehensweisen zur Behandlung von IP-Paketen gegenseitig stören, wenn sie gleichzeitig verwendet werden. Probleme können durch Adress- und Portübersetzung, Headermanipulation, Protokollkonflikte und erhöhte Routing-Komplexität entstehen. Um diese Probleme zu vermeiden, können Sie alternative VPN-Protokolle in Betracht ziehen, NAT Traversal verwenden oder Split Tunneling implementieren.

## GNS3 Labor Netzwerktopologie
![GNS3 Lab](https://github.com/Jinduujuun/HF_NWD_ITSE21a_Mylvaganam_Oehninger_Koenig/blob/main/2023-08-13%2021_01_31-NWD_VPN_Lab_V1%20-%20GNS3.png)

### Links und Hilfsmittel
[Wireguard](https://help.mikrotik.com/docs/display/ROS/WireGuard)

[ChatGPT](https://chat.openai.com/)

[Modul NW2 Lab Abgabe](https://github.com/Luxano-IT/NW2)

[MikroTik IPSec Wiki](https://wiki.mikrotik.com/wiki/Manual:IP/IPsec)

[MikriTik IPSec Dokumentation](https://mikrotrik.com/ipsec-site-to-site-vpn-configuration/)



