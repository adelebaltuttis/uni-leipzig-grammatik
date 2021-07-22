---
header: Grammatik des Deutschen - Content Creation
footer: ${pageNo} / ${pageCount}
---



## Grammatik des Deutschen Content Creation

Folgende Inhalte können produziert und modifiziert werden:

| Inhalte         | web url           | source code location | Jekyll Typ |
| --------------- | ----------------- | -------------------- | ---------- |
| Posts           | /                 | _posts               | Post       |
| Team Mitglieder | /team             | _team                | Collection |
| Publikationen   | /publikationen    | _publicationen       | Collection |
| Lehraktivitäten | /lehraktivitaeten | _lehraktivitaeten    | Collection |
| Kontakt         | /kontakt          | _pages/kontakt.md    | Page       |



## Team Mitglieder

Einträge für Team Mitglieder werden hier publiziert:

```
https://home.uni-leipzig.de/grammatik-des-deutschen/team/
```

Im Source Code ist der Seiteneintrag hier zu finden:

```
_pages/team.md
```

Alle Einträge von Team Mitgliedern werden automatisch für die Team Seite von Jekyll generiert.

Es sind also keine Veränderungen an `team.md` vorzunehmen. 



### <img src="Grammatik des Deutschen Content Creation.assets/image-20210717180738907.png" alt="image-20210717180738907" style="zoom: 40%;" />

<div style="text-align:center">Bild: Beispiel von Team Mitgliedern</div>

### Wie füge ich neue Teammitglieder hinzu?

Um neue Teammitglieder zu erstellen müssen neue Markdowndateien in der Kollektion  `_team` angelegt werden.

Bei der Namensgebung von neuen Dateien bitte folgendes beachten:

- Es dürfen keine Umlaute benutzt werden.
- Es werden keine Großbuchstaben genutzt.
- Für Leerzeichen wird `Kebab Case` genutzt (zb Max Friedrich Mustermann → max-friedrich-mustermann.md)

<img src="Grammatik des Deutschen Content Creation.assets/image-20210717182035330.png" alt="image-20210717182035330" style="zoom:67%;" />

<div style="text-align:center">Bild: Anlegen neues Teammitglied im _team Ordner</div>

#### Basisinformationen

```yaml
---
title       : Max Mustermann
last_name   : Mustermann
excerpt     : Max Mustermann is a hard worker.
---
```

- Für title wird der volle Name des Teammitglieds angegeben
- Der Nachname muss separat unter `last_name` definiert werden (dies ist wichtig für die Darstellung der Publikationen)
- Der Eintrag  `excerpt` wird auf der Team Seite als Teaser Text angezeigt. Dieser Eintrag ist optional. Falls nicht definiert, nimmt Jekyll einen Auszug aus dem ersten Paragraphen der Markdown Datei. Falls es keinen Text gibt, bleibt das Feld leer.



<img src="Grammatik des Deutschen Content Creation.assets/image-20210717192045355.png" alt="image-20210717192045355" style="zoom:50%;" />

<div style="text-align:center">Bild: Neues Teammitglied in Seitenansich "Team"</div>

1. Entspricht dem Eintrag `title` 
2. Entspricht dem Eintrag `excerpt`
3. Ein Default Teaser wird angezeigt, wenn kein Bild definiert wurde.

#### Teaser Image

Für die Team Seite kann ein Teaser Bild definiert werden

```yaml
header:
  teaser: /assets/images/team/david-bowie-teaser.jpg
```

Es wird empfohlen das Bild im Projekt Ordner hier abzulegen:

```
assets/images/team
```

<img src="Grammatik des Deutschen Content Creation.assets/image-20210719104855505.png" alt="image-20210719104855505" style="zoom: 67%;" />

<div style="text-align:center">Bild: Max Mustermann Teaser Eintrag</div>

Achtung: Das Bild wird von Jekyll automatisch abgeschnitten, falls es nicht im Querformat angelegt ist.

Es bietet sich an, das Bild entsprechend zu formatieren. Wahlweise kann auch manuell ein weißer Hintergrund eingefügt werden, um das Abschneiden zu verhindern.

<img src="Grammatik des Deutschen Content Creation.assets/image-20210719105207998.png" alt="image-20210719105207998" style="zoom: 33%;" />

<div style="text-align:center">Bild: Teaser Bild mit weißem Hintergrund</div>

#### Markdowntext

Unterhalb der Front Matter Definitionen `---` kann nun Fließtext in Markdown gesetzt werden:

```markdown
## Beschreibung
Mustermann ist ein häufig verwendeter Familienname fiktiver Personen in Deutschland. Erika Mustermann und Max Mustermann stehen als Platzhalternamen für eine beliebige (reale) Frau und einen beliebigen (realen) Mann. Sie werden seit 1978 in Mustern, Vorlagen und Ausfüllhilfen, Formularen, Hinweisen und Datenbanken verwendet.

## Max Mustermann
Max Mustermann hat im deutschen Sprachgebrauch die Nachfolge von Otto Normalverbraucher als fiktive Person und Inbegriff des Durchschnittsdeutschen angetreten. 
Beachte
- Er ist ein Verwandter, nach üblicher Annahme der Ehemann der wesentlich bekannteren, ebenfalls fiktiven Erika Mustermann, die mit Foto und Lebensdaten viele Musterausweise und Dokumente ziert. 
- Ausweisdokumente auf den Namen Max Mustermann sind wesentlich weniger verbreitet
- Das Kraftfahrt-Bundesamt veröffentlichte ein Muster der 2006 eingeführten EG-Fahrerkarte mit dem Bild eines am 1. Februar 1976 geborenen Max Mustermann, ausgestellt von der Fahrerlaubnisbehörde Musterstadt.
```

Dieser wird automatisch ins Layout der Detail Seite des Teammitglieds eingebettet:

<img src="Grammatik des Deutschen Content Creation.assets/image-20210717194203921.png" alt="image-20210717194203921" style="zoom: 50%;" />

<div style="text-align:center">Bild: Max Mustermann Detail Seite</div>

#### Sidebar Inhalte

Für die Detailseite von Teammitgliedern können in der Front Matter Inhalte für eine Sidebar definiert werden.

Für den ersten Paragraphen ist ein Bild mit Position reserviert. Diese sind wie folgt definiert:

```yaml
---
sidebar:
- title		: Position
  image		: /assets/images/team/david-bowie.jpg
  text		: "Wissenschafterlicher Musterarbeiter"
---
```

Achtung: `sidebar:` darf nur einmal definiert werden! 

Alle Weiteren Einträge werden unter `sidebar: `entsprechend eingerückt.

Es wird empfohlen das Bild im Projekt Ordner hier abzulegen:

```
assets/images/team
```

<img src="Grammatik des Deutschen Content Creation.assets/image-20210719094421117.png" alt="image-20210719094421117" style="zoom: 67%;" />

<div style="text-align:center">Bild: Max Mustermann Bild und Position</div>

Weiterhin können Links für zb Email, Webseite und Social Sites definiert werden:

```yaml
- label	: "Email Kontakt"
  icon	: "fas fa-fw fa-envelope-square"
  url	: "mailto:maxmustermanns@gmail.com"
```

<img src="Grammatik des Deutschen Content Creation.assets/image-20210719094647573.png" alt="image-20210719094647573" style="zoom:67%;" />

<div style="text-align:center">Bild: Max Mustermann Bild und Position</div>

Es können beliebig viele Links definiert werden. Die folgenden Definitionen für `icon` stehen zur Verfügung:

```yaml
# Email Icon
icon	: "fas fa-fw fa-envelope-square"
# Instagram Icon
icon	: "fab fa-fw fa-instagram"
# Website Icon
icon	: "fas fa-fw fa-link"
# Github Icon
icon	: "fab fa-fw fa-github"
# Facebook Icon
icon	: "fab fa-fw fa-facebook-square"
# Twitter Icon
icon	: "fab fa-fw fa-twitter-square"
```



Label können hierbei beliebig erweitert werden. Zb so:

```yaml
- title: Ein neuer Sidebar Titel
  text: Ein neuer Sidebar Text <br> Mit mehr Inhalt
```

![image-20210718231722196](Grammatik des Deutschen Content Creation.assets/image-20210718231722196.png)

<div style="text-align:center">Bild: Max Mustermann Sidebar Erweiterung</div>

#### Akkordion Inhalte

Es können Akkordion Inhalte für die Detailseite von Teammitgliedern über die Front Matter definiert werden.

```yaml
accordion:
- title     : Berufliche Laufbahn
  subitems:
  - label   : "seit 10/2005"
    content : "Professor für Germanistische Linguistik an der Universität Leipzig"
  - label   : "10/1995 - 09/2005"
    content : "Professorin für Germanistische Linguistik an der Universität Berlin"
```

Hierbei gilt:

- Achtung: `accordion:` darf nur einmal definiert werden! 

  Alle Weiteren Einträge werden unter `accordion: `entsprechend eingerückt.

- Jedes Akkordion benötigt einen `title:` tag. Es können beliebig viele definiert werden.

- Für jedes Akkordion müssen `subitems:` definiert werden.

- Jedes subitem folgt immer der Syntax `label:` und `content:`

![image-20210719103224159](Grammatik des Deutschen Content Creation.assets/image-20210719103224159.png)

<div style="text-align:center">Bild: Akkordion Beispiel</div>

Weiterhin kann der Akkordion Typ "Publikationen" wie folgt definiert werden:

```yaml
- title: Publikationen
```

Hier müssen keine subitems definiert werden. Jekyll wird das Akkordion automatisch aus der Kollektion `publikationen` befüllen. 

Hierbei ist es wichtig, dass `last_name` für das Teammitglied definiert wurde (diese Definition wird als Suchterm für die Kollektion übernommen).



#### Beispiel Teammitglied

Hier ist eine fertige Front Matter Definition für ein Teammitglied:

```yaml
---
# Basics
title       : Max Mustermann
name        : Max Mustermann
last_name   : Mustermann
excerpt     : Max Mustermann is a hard worker.

# Teaser Image
header:
  teaser: /assets/images/team/david-bowie-teaser.jpg

# Accordion Content
accordion:
- title     : Berufliche Laufbahn
  subitems:
  - label   : "seit 10/2005"
    content : "Professor für Germanistische Linguistik an der Universität Leipzig"
  - label   : "10/1995 - 09/2005"
    content : "Professor für Germanistische Linguistik an der Universität Berlin"
- title     : Publikationen    

# Sidebar
sidebar:
- title     : "Position"
  image     : /assets/images/team/david-bowie.jpg
  text      : "Wissenschafterlicher Musterarbeiter"
- label     : "Email Kontakt"
  icon      : "fas fa-fw fa-envelope-square"
  url       : mailto:maxmustermanns@gmail.com
- label     : "Website besuchen"
  icon      : "fas fa-fw fa-link"
  url       : "https://your-website.com"
- label     : "Auf Twitter folgen"
  icon      : "fab fa-fw fa-twitter-square"
  url       : "https://twitter.com/mustermann"  
- title     : "Sprechzeiten"
  text      : "Dienstag 13:30 – 14:30 Uhr <br> Vereinbarung per E-Mail"
- title     : "Anschrift"
  text      : "Germanistische Linguistik <br> GWZ <br> Beethovenstraße 15, Raum 1412 <br> 04107 Leipzig"
---
```

Die obige Front Matter produziert die folgenden Inhalt für das Team Mitglied "Max Mustermann"

<img src="Grammatik des Deutschen Content Creation.assets/image-20210719105539605.png" alt="image-20210719105539605" style="zoom: 33%;" />

<div style="text-align:center">Bild: Max Mustermann Detail Seite</div>

