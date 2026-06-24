# Azure-mini-project

# Azure Projekt – CloudStart GmbH

## A1 – Netzwerk

Es wurde die Resource Group **rg-cloudstart** erstellt. Anschließend wurde das Virtual Network **vnet-cloudstart** mit dem Adressraum **10.0.0.0/16** angelegt.

Folgende Subnetze wurden erstellt:

* snet-app (10.0.1.0/24)
* snet-mgmt (10.0.2.0/24)

Zusätzlich wurden die Network Security Groups **nsg-app** und **nsg-mgmt** erstellt und den jeweiligen Subnetzen zugewiesen. Für RDP wurde Port 3389 freigegeben, für SSH Port 22.

## A2 – Virtuelle Maschinen

Es wurde die Linux-VM **vm-mgmt01** erstellt und erfolgreich per SSH verbunden. Der Befehl „uname -a“ wurde erfolgreich ausgeführt.

Die VM wurde dem Subnetz **snet-mgmt** zugeordnet.

## A3 – Storage

Ein Storage Account wurde mit Standard Performance und LRS-Redundanz erstellt.

Der Blob Container **dokumente** wurde angelegt und eine Testdatei hochgeladen. Anschließend wurde eine SAS-URL erstellt und erfolgreich im Browser geöffnet.

## A4 – Entra ID und RBAC

Folgende Benutzer wurden erstellt:

* Anna Maier
* Ben Koller
* Clara Fuchs

Zusätzlich wurde die Sicherheitsgruppe **grp-entwickler** erstellt und Ben Koller hinzugefügt.

RBAC-Rollen:

* Anna Maier → Reader
* grp-entwickler → Virtual Machine Contributor

## A5 – Monitoring

Die CPU-Auslastung der VM wurde über Azure Monitor analysiert.

Zusätzlich wurde die Alert Rule **alert-cpu-hoch** erstellt:

* CPU-Auslastung > 80 %
* Severity 2
* E-Mail-Benachrichtigung aktiviert

## A6 – Defender for Cloud

Microsoft Defender for Cloud wurde geöffnet und der Secure Score überprüft.

Mehrere Sicherheitsempfehlungen wurden analysiert, darunter:

* MFA aktivieren
* Just-in-Time VM Access
* Management Ports einschränken

Die Sicherheitsrisiken wurden dokumentiert und bewertet.
