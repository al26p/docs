---
title: MX-Eintrag konfigurieren
excerpt: Erfahren Sie hier, wie Sie mit OVHcloud MX-Einträge für Ihren Domainnamen konfigurieren 
updated: 2023-08-30
---

> [!primary]
> Diese Übersetzung wurde durch unseren Partner SYSTRAN automatisch erstellt. In manchen Fällen können ungenaue Formulierungen verwendet worden sein, z.B. bei der Beschriftung von Schaltflächen oder technischen Details. Bitte ziehen Sie im Zweifelsfall die englische oder französische Fassung der Anleitung zu Rate. Möchten Sie mithelfen, diese Übersetzung zu verbessern? Dann nutzen Sie dazu bitte den Button "Beitragen" auf dieser Seite.
>

## Ziel

Der Eintrag vom Typ MX legt den für die E-Mail-Adressen eines Domainnamens zuständigen E-Mail-Server fest. Damit wird Servern, die E-Mails an Ihre Adressen versenden, mitgeteilt, wohin diese versendet werden sollen. 

**Diese Anleitung erklärt, wie Sie bei OVHcloud MX-Einträge zur Konfiguration Ihres Domainnamens hinzufügen.**

## Voraussetzungen

- Sie haben Zugriff auf Ihr [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de) mit den erforderlichen Berechtigungen zum Verwalten des Domainnamens.
- Der Domainname verwendet die OVHcloud Konfiguration (die OVHcloud DNS-Server).
- Sie verfügen über einen MX Plan (enthalten in einem [Webhosting](https://www.ovhcloud.com/de/web-hosting/) oder [Kostenloses Hosting 100M](https://www.ovhcloud.com/de/domains/free-web-hosting/) oder separat bestellt), einen unserer [OVHcloud E-Mail-Dienste](https://www.ovhcloud.com/de/emails/) oder einen externen E-Mail-Dienst.

> [!primary]
>
> - Wenn Ihr Domainname **nicht** die DNS-Server von OVHcloud verwendet, muss die Änderung der MX-Einträge über das Interface des Anbieters vorgenommen werden, der die Konfiguration Ihres Domainnamens verwaltet.
>
> - Wenn Ihr Domainname bei OVHcloud registriert ist, können Sie überprüfen, ob er die OVHcloud Konfiguration verwendet: Gehen Sie in Ihrem [Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de) in den Tab `DNS-Server`{.action} und anschließend in den Tab `Allgemeine Informationen`{.action}. Wenn unter **DNS-Server** der Eintrag Aktiv angezeigt wird, verwenden Sie die OVHcloud DNS-Server.
>
> ![E-Mail](images/dns-servers-enabled.png){.thumbnail}

## In der praktischen Anwendung

### Grundlegendes zur Rolle von MX-Einträgen 

MX-Einträge (**M**ail e**X**change) werden verwendet, um einen Domainnamen mit den empfangenden E-Mail-Servern Ihres E-Mail-Dienstes zu verknüpfen.

Beispiel:

Von der Adresse **sender@otherdomain.ovh** wird eine E-Mail an **contact@mydomain.ovh** gesendet. Der Server, der die E-Mail sendet (**Outgoing mail server**) wird dazu:
- **(1)** Die DNS-Zone von **mydomain.ovh** auf deren **MX**-Einträge abfragen.
- **(2)** Die E-Mail an die URL des gelesenen **MX**-Eintrags weiterleiten.

![E-Mail](images/mx-dns-resolution.png){.thumbnail}

Die E-Mail wird an das Ziel **mx0.mail.ovh.net** gesendet, dem der Wert **0** vorangestellt ist. Dieser Wert wird als *Priorität* bezeichnet. Der niedrigste Wert wird zuerst abgefragt, der höchste zuletzt. Dies bedeutet, dass das Vorhandensein mehrerer Datensätze eine ausbleibende Antwort des MX-Datensatzes mit der niedrigsten Priorität ausgleicht.

Sie können mehrere MX-Einträge für denselben Domainnamen einrichten. In diesem Fall ist es notwendig, eine Prioritätsnummer für jede dieser Nummern zu definieren. MX-Einträge werden in aufsteigender Reihenfolge von der niedrigsten zur höchsten Nummer abgefragt, bis eine Antwort vom empfangenden Server erfolgt.

> [!warning]
>
> Generell ist bei der **Änderung der MX-Einträge in der DNS-Zone Ihres Domainnamens Vorsicht geboten**: Bei einer fehlerhaften Änderung können E-Mails an Ihre Adressen nicht mehr empfangen werden.
> Im Zweifelsfall empfehlen wir Ihnen, einen [spezialisierten Dienstleister](https://partner.ovhcloud.com/de/directory/) zu kontaktieren.

### Werte der OVHcloud MX-Konfiguration <a name="mxovhcloud"></a>

Nachfolgend finden Sie die Konfiguration für OVHcloud MX Plan (Standalone oder in einem [OVHcloud Webhosting](https://www.ovhcloud.com/de/web-hosting/) enthalten), [E-Mail Pro](https://www.ovhcloud.com/de/emails/email-pro/) und [Exchange](https://www.ovhcloud.com/de/emails/). Unsere E-Mail-Server verfügen über integrierte Antispam- und Antivirensoftware.

|Domain|TTL|Eintrag|Priorität|Ziel|
|---|---|---|---|---|
|*Leer lassen*|3600|MX|1|mx0.mail.ovh.net.|
|*Leer lassen*|3600|MX|5|mx1.mail.ovh.net.|
|*Leer lassen*|3600|MX|50|mx2.mail.ovh.net.|
|*Leer lassen*|3600|MX|100|mx3.mail.ovh.net.|
|*Leer lassen*|3600|MX|200|mx4.mail.ovh.net.|

Diese MX-Einträge müssen in der DNS-Zone Ihres Domainnamens konfiguriert werden, wenn Sie einen OVHcloud E-Mail-Dienst nutzen.

### MX-Eintrag in einer OVHcloud DNS-Zone konfigurieren

Um MX-Einträge in der OVHcloud Konfiguration Ihres Domainnamens zu erstellen oder zu bearbeiten, loggen Sie sich in Ihrem [OVHcloud Kundencenter](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.de/&ovhSubsidiary=de) ein. Gehen Sie in den Bereich `Domainnamen`{.action}, klicken Sie auf den Domainnamen und anschließend in den Tab `DNS-Zone`{.action}.

Die Tabelle zeigt die OVHcloud DNS-Konfiguration Ihres Domainnamens an. Jede Zeile entspricht einem DNS-Eintrag.

Überprüfen Sie zunächst mit der Filterfunktion über der Tabelle Ihrer DNS-Zone, ob bereits MX-Einträge vorhanden sind.<br>
Wählen Sie den Typ **MX** aus und bestätigen Sie, damit nur die MX DNS-Einträge Ihrer DNS-Zone angezeigt werden. Beachten Sie die Beispielanzeige unten.

![dnsmxrecord](images/mx-entries-research.png){.thumbnail}

- Wenn bereits MX-Einträge vorhanden sind und Sie diese bearbeiten möchten, klicken Sie rechts in der Zeile auf den Button `...`{.action}. und dann auf `Eintrag bearbeiten`{.action}.
- Wenn kein MX-Eintrag vorhanden ist, klicken Sie rechts neben der Tabelle auf `Eintrag hinzufügen`{.action} und wählen Sie `MX`{.action} aus. Geben Sie die angeforderten Daten für den E-Mail-Dienst ein:

**Wenn Sie über eine E-Mail-Lösung von OVHcloud verfügen**, verwenden Sie die Informationen unter [OVHcloud MX-Konfiguration ](#mxovhcloud).

![dnsmxrecord](images/modify-a-dns-zone-record-mx-step-1.png){.thumbnail}

Wenn Sie alle Daten eingegeben haben, schließen Sie die Schritte ab und klicken Sie dann auf `Weiter`{.action}.

**Wenn Sie eine andere E-Mail-Lösung nutzen**, befolgen Sie die Anweisungen Ihres E-Mail-Dienstanbieters.

> [!primary]
>
> Jede Änderung erfordert eine Propagationszeit zwischen 4 und 24 Stunden, bis sie voll wirksam ist.
>

## Weiterführende Informationen

[Allgemeine Informationen zu DNS-Servern](/pages/web_cloud/domains/dns_server_general_information)

[OVHcloud DNS-Zone bearbeiten](/pages/web_cloud/domains/dns_zone_edit)

[SPF-Eintrag konfigurieren](/pages/web_cloud/domains/dns_zone_spf)

[DKIM-Eintrag konfigurieren](/pages/web_cloud/domains/dns_zone_dkim)

Kontaktieren Sie für spezialisierte Dienstleistungen (SEO, Web-Entwicklung etc.) die [OVHcloud Partner](https://partner.ovhcloud.com/de/directory/).

Wenn Sie Hilfe bei der Nutzung und Konfiguration Ihrer OVHcloud Lösungen benötigen, beachten Sie unsere [Support-Angebote](https://www.ovhcloud.com/de/support-levels/).

Für den Austausch mit unserer User Community gehen Sie auf <https://community.ovh.com/en/>.