---
permalink   : /kontakt/
title       : Kontakt & Anfahrt
description : "Hier finden Sie die Kontakt und Anfahrtsmöglichkeiten für die Gruppe Grammatik des Deutschen kontaktieren. Es werden Telefonnummer, Adresse, Faxnummer Email und OpenStreetMap angezeigt."
email       : mkonrad@uni-leipzig.de
mail-icon   : fas fa-fw fa-envelope-square
mail-label  : E-Mail Schreiben
header      :
    image   : assets/images/banner/kontakt_default.jpg
---

## Anschrift
**Institut für Germanistik**

Geisteswissenschaftliches Zentrum <br>
Beethovenstraße 15, Raum 1409 <br>
04107 Leipzig

**Telefon**: +49 341 97-37354  <br>
**Telefax**: +49 341 97-37449

<a href="mailto:{{page.email}}" rel="nofollow noopener noreferrer"> 
    <i class="{{page.mail-icon}}" aria-hidden="true"></i> 
    <span class="label">{{ page.mail-label }}</span>
</a>

## Anfahrt

{% leaflet_map {"center" : [51.3406321, 12.3747329],
                "zoom" : 13,
                "providerBasemap": "OpenStreetMap.DE" }
%}
{% leaflet_marker { "latitude" : 51.33184919999999,
                    "longitude" : 12.368349059662645,
                    "popupContent" : "GWZ Uni Leipzig"} %}

{% endleaflet_map %}
