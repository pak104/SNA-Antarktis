Das Netzwerk hat nach dem Codebuch folgende Attribute:

*Vertex-Attribute* 

**id**

Eindeutige Identifikation der einzelnen Knotens (Expeditionen, Menschen, Sponsoren), der erfasst wird. Bei Menschen die ersten drei Buchstaben des Vor- und Nachnamens, bei Expeditionen ein zugeteilter Buchstabe in alphabetischer Reihenfolge, bei Sponsoren eine zugeteilte einzigartige ID.

**name**

Name oder Bezeichnung des Knotens.

**type**

Art des Knotens:
1 = Mensch, 2 = Expedition, 3 = Sponsor

**sex**

Bezeichnet das Geschlecht einer Person:
1 = männlich, 2 = weiblich, 3 = divers, 0 = NA

**country**

Bestimmt, aus welchem Land eine Person oder Expedition kommt. Nach ISO-3166 Alpha 2.

**year**

Bestimmt, in welchem Jahr die Expedition startete.
(0 = NA)

**success**
Beschreibt, ob das Ziel der Expedition erreicht wurde:
1 = ja, 2 = nein, 99 = NA

**duration**
Gibt die Dauer der Expedition in Monaten an.
(0 = NA)

Die Vertex-Attribute id, name, type und country treffen auf alle Knoten des Netzwerks zu. Dahingehen wird das Attribut sex nur für Knoten des type 1 ausgefüllt. Knoten der anderen types werden mit 0 markiert. Die Vertex-Attribute year, success und duration treffen nur auf Knoten des type 2 zu - also den Expeditionen. Um Fehler im Code zu vermeiden, werden NAs dieser drei Attribute mit 0 (year und duration) oder 99 (success) ersetzt.

*Edge-Attribute* 

**from**

Entspricht den IDs in der Nodelist.

**to**

Entspricht den IDs in der Nodelist.

**death**

Beschreibt, ob die jeweilige Expedition überlebt wurde: eins = überlebt, zwei = gestorben

**team_1**
Entspricht der jeweils wichtigsten Beschäftigung der Person:
eins = Expeditionsleiter (commander)
zwei = Stellvertretung (captain, executive commander, first mate, second mate, third mate, steward)
drei = Beruf außerhalb des Schiffes (scientist, artist, engineer, medic, cook, dogdriver, animal care, navigator)
vier = Beruf innerhalb des Schiffes (crewman und shipbuilder)

**team_2**
Entspricht der jeweils zweitwichtigsten Beschäftigung der Person (wenn vorhanden):
eins = Expeditionsleiter (commander)
zwei = Stellvertretung (captain, executive commander, first mate, second mate, third mate, steward)
drei = Beruf außerhalb des Schiffes (scientist, artist, engineer, medic, cook, dogdriver, animal care, navigator)
vier = Beruf innerhalb des Schiffes (crewman und shipbuilder)

**motivation**
Beschreibt die Motivation hinter dem Sponsoring einer Expedition:
eins = politisches Interesse,
zwei = wissenschaftliches Interesse,
drei = wirtschaftliches Interesse,
null = NA

**tn_uk**
Legt fest, ob Sponsor bzw. Mannschaftsmitglied Teil einer britischen Expedition war:
null = nein
eins = britische Expedition
