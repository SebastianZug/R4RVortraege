<!--
author:   Sebastian Zug; André Dietrich

email:    sebastian.zug@informatik.tu-freiberg.de

version:  1.0.2

language: en

narrator: UK English Female

icon:     https://media.aubi-plus.com/institution/thumbnail/3f3de48-technische-universitaet-bergakademie-freiberg-logo.jpg

link:     style.css

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/SebastianZug/R4RVortraege/main/2024_DigitaleWelten/presentation.md#1)


# Sind unsere Städte bereit für Roboter?

<h3>Konzepte für die Planung von autonomen Systemen auf Fuß und Gehwegen</h3>

![Szenarien](./images/Roboter_trifft_Menschen.jpg "Abb.: TUBAF Roboter im Stadtzentrum von Freiberg")

---

<div class="left">

Prof. Dr. Sebastian Zug, Institut für Informatik

TU Bergakademie Freiberg

</div>

<div class="right">

### Kongress für Geoinformatik und Geodäsie

### Digitale Welten - Dresden, 27.02.2024

</div>

  --{{0}}--
Dieser Vortrag gibt einen Überblick über die Herausforderungen und Chancen der Planung von autonomen Systemen, die auf Fuß- und Gehwegen operieren. Er fasst die in den Projekten "Ready for Smart City Robots" und "RoboTraces" mit verschiedenen Forschungspartnern entwickelten Konzepte zusammen.


## Chancen & Herausforderungen 

  --{{0}}--
Kompakte, nicht-automotive autonome Roboter lassen sich intuitiv für eine Vielzahl von Anwendungen nutzen. Der Fokus der gesellschaftlichen Diskussion liegt aktuell zwar auf  klassischen Lieferdiensten in urbanen Räumen. Die automatisierten Plattformen eröffnen aber auch eine Vielzahl von weiteren Anwendungsfeldern und Nutzungsmodelle. 

  --{{1}}--
Dabei können die Konzepte des Autonomen Fahrens von Straßenfahrzeugen aber nur bedingt auf die Fuß- und Radwege übertragen werden. Zum einen fehlt es schlicht und ergreifend an einem gemeinsamen Verständnis zum Betrieb der Roboter: Welche Größe und Gewicht dürfen sie haben? Welche Geschwindigkeiten sind zulässig? Welche Sicherheitsstandards müssen eingehalten werden? Ein autonomes Automobil kopiert einen menschlichen Fahrer, ein autonomer Roboter ist dagegen ein neuer Akteur im urbanen Raum, für den die spezifischen Regeln erst noch definiert werden müssen.


                          {{0-2}}
***********************************************************

> Anwendungsfelder für autonome Systeme reichen von Lieferdiensten, über die Wartungsaufgaben bis hin zu Begleitdiensten für Menschen ...

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Starships_at_Kingston_15.2.19.jpg/800px-Starships_at_Kingston_15.2.19.jpg?20190220172050 "_Starship' robot delivery vehicles a Kingston Shopping Centre, Milton Keynes. Awaiting a call to make a home delivery._ Quelle: Wikimedia Commons, [Link](https://commons.wikimedia.org/wiki/File:Starships_at_Kingston_15.2.19.jpg), Author: 'StevePotter49'")

***********************************************************

                          {{1-2}}
***********************************************************

ABER: _"... sie können aber nur eine Ergänzung zu bestehenden Prozessen und können keine vollständige Substitution darstellen."_ (Interview KEP Dienstleister)


***********************************************************

  --{{2}}--
Allerdings müssen auch ganz pragmatische Gründe betrachtet werden, die Fuß- und Radwege von den Straßen unterscheiden. Die Heterogenität des Operationsgebietes, die Dynamik der Umgebung, die nicht-maschinengerechten Infrastrukturen und Konfigurationen und der rechtliche Rahmen sind technische Herausforderungen, die es zu meistern gilt.

                          {{2-3}}
***********************************************************

> __Lieferroboter sind keine kleinen Autos! Warum ist das so?__

<details>
<summary>**Heterogenität der Umgebung**</summary>

<div class="left">

![](./images/Claudi_in_snow.jpg "Abb.: TUBAF Roboter im Stadtzentrum von Freiberg")

</div>

<div class="right">

__Herausforderungen:__

+ Wegbreiten und -untergründe
+ variierende Bordsteinkanten
+ Hindernisse wie Treppen, Poller, Cafe-Tische etc.
+ Anstiege und Gefälle

</div>
</details>

<details>
<summary>**Dynamik der Umgebung**</summary>

<div class="left">

![](./images/Obstacle.jpg "Abb.: Plötzliche Hindernisse auf dem Gehweg")

</div>

<div class="right">

__Herausforderungen:__

+ Passanten, Radfahrerinnen, Tiere
+ Kinderwägen, Rollatoren, Rollstühle
+ Baustellen, Veranstaltungen, Märkte

</div>
</details>

<details>
<summary>**Nicht-Maschinengerechte Infrastrukturen / Konfigurationen**</summary>

<div class="left">

![](./images/Traffic_lights_from_robot.jpg "Abb.: Roboterperspektive auf eine Fußgängerampel")

</div>

<div class="right">

__Herausforderungen:__

+ Ampelanlagen
+ fehlende Einsehbarkeit von Situation wegen der geringen Bauhöhe
+ lokal schwierige Beleuchtungssituationen

</div>

</details>

<details>
<summary>**Rechtlicher Rahmen**</summary>

__Herausforderungen:__

+ Gesetz zum autonomen Fahren (2021)
+ Autonome-Fahrzeuge-Genehmigungs-und-Betriebs-Verordnung (2022)

> __§ 1 Straßenverkehrsgesetz (StVG)__
>
> (2) Als Kraftfahrzeuge im Sinne dieses Gesetzes gelten Landfahrzeuge, die durch Maschinenkraft bewegt werden, ohne an Bahngleise gebunden zu sein.
>
> (3) Keine Kraftfahrzeuge im Sinne dieses Gesetzes sind Landfahrzeuge, die durch Muskelkraft fortbewegt werden und mit einem elektromotorischen Hilfsantrieb mit einer Nenndauerleistung von höchstens 0,25 kW ausgestattet sind ...

</details>

***********************************************************

  --{{2}}--
Vor dem Hintergrund der Einschränkungen beim Betrieb - zu geringen Gehwegbreiten, einem ggf. hohen Passantenaufkommen oder einer schwer einsehbaren Wegekreuzung - ist die multimodale Planung des Einsatzes von autonomen Systemen die Schlüsselaufgabe für deren Einführung. Um zulässige Trajektorien zu identifizieren, müssen sowohl die Nutzbarkeit von einzelnen Streckensegmenten (_Radweg in der XYZ-Straße_) evaluiert als auch die konkrete Pfad unter sozialen und technischen Gesichtspunkten (_Fahrt entlang der Hauswand_) festgelegt werden. Im folgenden wird dies als makroskopische und mikroskopische Planung bezeichnet. 

{{3-4}}
***********************************************************

> __Ergebnis__: Die _multimodale_ Planung des Einsatzes von autonomen Systemen ist die Schlüsselaufgabe für deren Einführung.

![](./images/MakroskopischeSicht_Dresden.jpg "Abb.: Makroskopische Sicht auf Fuß- und Gehwege")
![](./images/MirkoskopischeSicht.jpg "Abb.: Mikroskopische Sicht auf konkrete Trajektorien")

Anmerkungen: 

1. Die makroskopische Planung arbeitet auf attributierten Graphen, die mikroskopische auf Gridstrukturen.
2. Beide Aspekte sind die Grundlage für die Einrichtung von "_Attributierten Roboter Korridoren_" notwendig.

***********************************************************

## Makroskopische Planung

  --{{0}}--
Bemerkenswert bei der Beantwortung der Frage ist die Tatsache, dass die Befahrbarkeit nicht nur von den Eigenschaften der Umgebung abhängt, sondern auch von der Konfiguration des Roboters selbst. Dessen Größe, die Fähigkeit Hindernisse zu überwinden und die Genauigkeit der individuellen Lokalisierungstechnik sind Faktoren, die eine roboterspezifische Untersuchung erforderlich machen. Wie können die Vereinbarkeit von Roboterkonfiguration und Umgebung in einer Metrik abgebildet werden? Neben der binären _ja/nein_ Entscheidung für die Befahrbarkeit, kann auch die Verlässlichkeit beschrieben werden. Im logistischen Kontext wäre das die Planbarkeit der Fahrtdauer und damit deren Determinismus. 

> __Zielstellung:__ Auf welchen Wegen kann der Roboter überhaupt fahren?

<div class="left">

__Kriterien:__ 

1. Generelle Befahrbarkeit (z. B. Wegbreite, Bordsteinkanten, GNSS-Lokalisierungsgenauigkeit)
2. Determinismus der Ankunftszeiten (z. B. Passantenaufkommen, Länge von Umwegen im Fall von Hindernissen)

</div>

<div class="right">

__Herausforderungen:__

+ __Streckendaten__ (z. B. OpenStreetMap, amtliche Geodaten)
+ __Attribute__ (z. B. Wegbreiten, Hindernisse, Passantenaufkommen)
+ __dynamische Daten__ (z. B. Veranstaltungen, Baustellen)

</div>

### Herausforderung Datenlage 

  --{{0}}--
Die nachfolgende Tabelle illustriert die unzureichende Datenlage für die Planung von autonomen Systemen auf Fuß- und Radwegen am Beispiel von Open Street Map (OSM). Die Tabelle zeigt, dass die roboterrelevanten Attributen der Fuß- und Radwege, wie die Breite oder die Oberflächenbeschaffenheit bislang nur unvollständig hinterlegt sind. Zudem existieren aktuell keine übergreifenden Karten, die Fuß- und Radwege als eigenständige Infrastruktur in großem Maßstab abbilden.

                    {{0-1}}
***********************************************************

Open Street Map kann die Anfragen zu Attributen der Fuß- und Radwege nur unzureichend beantworten.

<!-- data-type="none" -->
| Attribute / Tags | intercity | local | cycleway | footway | sidewalk | bicycle |
| ---------------- | --------: | ----: | -------: | ------: | -------: | ------: |
| `surface`        |       100 |    85 |       98 |      85 |       88 |      86 |
| `width`          |         1 |     8 |       14 |       3 |        5 |       7 |
| `smoothness`     |        80 |    51 |       79 |      35 |       48 |      49 |
| `max_width`      |         0 |     0 |        0 |       0 |        0 |       0 |
| `est_width`      |         0 |     0 |        0 |       0 |        0 |       0 |

_Übersicht der hinterlegten Attribute für die Straßen und Wege der Stadt Dresden aus OSM (Feb. 2024)_

***********************************************************

                    {{1-2}}
***********************************************************

  --{{0}}--
Das Projekt "Ready for Smart City Robots" nutzt die Daten von Radfahrerinnen und Radfahrern, um diese Lücke zu schließen. Dabei werden zwei Konzepte verfolgt - ein community-basierter Ansatz, bei dem mit einer Mobiltelefonapp Daten zur aktuellen Wegbeschaffenheit gesammelt werden und mit den Nutzerinnen und Nutzer von Fahrradleihsystemen, wobei den Leihrädern eine hochintegrierte Sensorbox beigefügt wurde. Das Vorhaben stellt die Vor- und Nachteile der beiden Ansätze gegenüber und wertet deren Datenqualität und -quantität aus.

Das Projekt Ready for Smart City Robots zielt darauf ab diese Lücke zu füllen und aggregiert Daten aus 

+ Fahrradleihsystemen und 
+ anhand einer Mobilfunkapp.

<div class="left">

![](./images/Fahrrad_und_roboter.jpeg "Abb.: Leihlastenfahrräder für die roboterspezifische Datenerhebung")

</div>

<div class="right">

![](./images/Szenario_Schkeuditz.jpeg "Abb.: Erste Abdeckungsanalyse der App-basierten Datenerhebung am Versuchsstandort Schkeuditz")

</div>


***********************************************************

### Herausforderung Attribute 

> ... am Beispiel der Gewegsbreiten

  --{{0}}--
Die nachfolgenden Grafiken illustrieren die Komplexität der dabei umzusetzenden Bildverarbeitung. Die linke Grafik zeigt das Ergebnis der Bewertung in einer einfachen Situation, der Fußweg grenzt sich deutlich von der Straße ab, die Wegbreite ist gut erkennbar. Die rechte Grafik zeigt dagegen eine Situation, in der die Wegbreite nur schwer zu bestimmen ist. Die Herausforderung besteht darin, die Wegbreite in einer Vielzahl von Situationen zuverlässig automatisiert zu bestimmen.

<div class="left">

![](./images/weg_erkannt.png "Abb.: Situativ gültige Erfassung der Wegbreite")

</div>

<div class="right">

![](./images/aufsteller.png "Abb.: Hindernisse auf dem Gehweg")

</div>

-----

_Quelle: Identifikation der minimalen Wegbreiten für Fuß- und Radwege anhand eines multimodalen Datensets (Bachelorarbeit, Lukas Neuber, 2024)_

## Mikroskopische Planung

  --{{0}}--
Die mikroskopische Planung untersucht nun, die konkrete Trajektorie des Roboters auf den Wegen. Dies schließt die Wahl der Fahrspur, die Geschwindigkeit und die Verhaltensregeln ein. Die Herausforderung besteht darin, die Sicherheit und Vorhersehbarkeit des Roboters zu gewährleisten.

> __Zielstellung:__ Wo sollte der Roboter (wie) auf den Wegen fahren? 

<div class="left">

__Kriterien:__ 

1. Sicherheitsgefühl, Vorhersehbarkeit (Sichtlinien, kritische Pfade)
2. Kontrollierbarkeit (Automatikmodus, manueller Modus)

</div>

<div class="right">

__Herausforderungen:__

+ __Datenlage__ (Sichtachsen, Passantenaufkommen)
+ __Modellierung Verhaltens anderer Verkehrsteilnehmer__ (z. B. Fußgängerdynamik)
+ __Kommunikationsmöglichkeiten__ 

</div>

### Herausforderung Sicherheitsgefühl

  --{{0}}--
Ein Aspekt einer defensiven Trajektorienplanung ist die Prüfung von Sichtlinien. Aus welcher Perspektive kann der Roboter aus seiner Umgebung überhaupt wahrgenommen werden? Diese Planung sollte im besten Fall anhand von Kartendaten vorgenommen werden, so dass eine aufwändige Erfassung vor Ort nicht notwendig ist. Die nachfolgende Grafik zeigt die Ergebnisse einer solchen Analyse auf der Basis von Open Street Map Daten, die nun mit realweltlichen Messungen verglichen werden. 

<section>
<div class="left">

![](./images/Kritische_Pfade_in_Freiberg.jpg "Abb.: Situativ gültige Erfassung der Wegbreite")

</div>

<div class="right">

![](./images/Sichtlinien_in_freiberg.jpg "Abb.: Hindernisse auf dem Gehweg")

</div>
</section>

_Vergleich der Sichtlinienanalysen auf der Basis von OSM Daten und realweltlichen Messungen (Bachelorarbeit, Vincent Junge, 2024)_

### Herausforderung Mensch

  --{{0}}--
Für die Interaktion von Robotern und Menschen exisiert eine Vielzahl von Laboruntersuchungen, es fehlen aber große Studien, die eine realweltliches Verhalten abbilden. Die nachfolgenden Grafiken zeigen die erste Ergebnisse einer solchen Studie, die im Rahmen des Projektes RoboTraces in Freiberg durchgeführt wurde. Die Grafik links zeigt die Verteilung der Abstände von Passanten zum Roboter. Die Grafik rechts zeigt beispielhafte Trajektorien von Personen auf der Burgstraße in Freiberg. Das Ziel der Untersuchung ist es, allgemeine kontextbasierte Verhaltensregeln zu identifizieren, die in die Planung der Trajektorien einfließen können.

Wie verhalten sich die Menschen in der Umgebung des Roboters?

{{0-1}}
![](./images/trau_dich.jpg "Abb.: Histogramm der Abstände von Passanten zum Roboter")

{{1-2}}
![](./images/Interaktions_schemas_HMI.jpg "Abb.: Beispielhafte Trajektorien von Personen auf der Burgstraße in Freiberg")


## Methodik

>Auf welchen Daten basieren die Arbeiten?

![](./images/Claudi_details.jpg "Abb.: Sensorische Konfiguration des Roboters")<!-- width="70%" -->

Datenlage:

+ 22 Fahrten im Jahresverlauf 2022/ 23 in Freiberg
+ wiederkehrender Rundkurs mit 2.5 km Länge
+ Abdeckung unterschiedlicher Kontexte (z. B. Wochenende, Feiertage, Veranstaltungen) und Situationen (Marktplatz, Fußgängerzone, schmale Gassen)

## Fazit und Resumee

  --{{0}}--
Um einen "Wildwuchs" bei der Etablierung von Roboteranwendungen zu vermeiden, ist eine klare und transparente Planung anhand entsprechender behördlicher Regularien notwendig. Dies setzt aber voraus, dass die Planungskonzepte und Kriterien für autonome Systeme auf Fuß- und Gehwegen verlässlich und nachvollziehbar sind. Die Herausforderungen liegen dabei in der Datenlage, der Abstraktion der Akzeptanzkriterien und der feingranularen Regularien. Gleichzeitig sind die Kommunen in diesen Entwicklungsprozess einzubinden, um entsprechend der lokalen Besonderheiten diese Festlegungen zu treffen.

<div class="left">

__Vision: Verlässliche Prognosen für die Bewegung von autonomen Systemen auf Fuß- und Gehwegen__

![](./images/isochronen_Dresden.jpg "Abb.: Abdeckungsareal eines Roboters mit 15min Fahrzeit (3.6km/h) startend vom Rathaus Dresden (rot Fußwege, blau Fuß- und Radwege)")

</div>

<div class="right">

__Hürden auf dem Weg dahin:__

+ Datenlage, Datenlage, Datenlage, ...
+ abstrakte Akzeptanzkriterien
+ feingranulare kommunale Regularien

... aber wir sind auf einem guten Weg!

{{1-2}}
!?[Robot_meets_barrier](./images/robot_meets_barrier.mp4 "In Freiberg ist auch schon die Infrastruktur _Ready for Robots_")<!--autoplay="true" muted="true"-->

</div>


## Referenzen

Publikationen:

<!-- class="reference" -->
> M. Plank, C. Lemardelé, T. Assmann, S. Zug, _"Ready for robots? Assessment of autonomous delivery robot operative accessibility in German cities,"_, Journal of Urban Mobility, Volume 2, 2022, [doi.org/10.1016/j.urbmob.2022.100036](https://www.sciencedirect.com/science/article/pii/S2667091722000243).

<!-- class="reference" -->
> S. Zug, N. Seyffer, M. Plank, B. Pfleging, F. Schrödel and F. W. Siebert, _"Identification of Potential Conflict Zones Between Pedestrians and Mobile Robots in Urban Situations,"_ 2023 IEEE 28th International Conference on Emerging Technologies and Factory Automation (ETFA), Sinaia, Romania, 2023, [10.1109/ETFA54631.2023.10275428](https://ieeexplore.ieee.org/document/10275428).


<!-- class="reference" -->
> M. Plank, G. Jäger, S. Zug, _"Delivery robots are not just small autonomous cars! How to close the gap in environmental data for planning their operation?"_, 2023 IEEE International Symposium on Robotic and Sensors Environments (ROSE), Tokyo, Japan, 2023, [10.1109/ROSE60297.2023.10410711](https://ieeexplore.ieee.org/document/10410711).

Relevante Projekte:

<!-- class="highlight" -->
> __Projekt:__
> [RoboTraces](https://bmdv.bund.de/SharedDocs/DE/Artikel/DG/mfund-projekte/robotraces.html), BMDV (2022 - 2023) - Hochschule Schmalkalden, TU Bergakademie Freiberg

<!-- class="highlight" -->
> __Projekt:__
> [Ready for Smart City Robots](https://bmdv.bund.de/SharedDocs/DE/Artikel/DG/mfund-projekte/r4r.html), BMDV (2022 - 2025) - TU Bergakademie Freiberg, Otto-von-Guericke Universität Magdeburg, Hochschule Anhalt, Hochschule Merseburg, TINK GmbH, DigiPL GmbH, CyFace GmbH, PTV AG, Landkreis Nordsachsen