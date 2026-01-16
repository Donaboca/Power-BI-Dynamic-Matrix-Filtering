# Power BI Tricks
## Sisällysluettelo
- [Dynaaminen PBI matriisin rivien ja sarakkeiden suodatus](#dynaaminen-pbi-matriisin-rivien-ja-sarakkeiden-suodatus)
- [User Defined Functions, käyttäjän määrittelemät funktiot](#user-defined-functions-käyttäjän-määrittelemät-funktiot)
### Dynaaminen PBI matriisin rivien ja sarakkeiden suodatus
Esimerkki lopputuloksesta miten PBI matriisin rivejä ja sarakkeita voi raportin käyttäjän toimesta suodattaa dynaamisesti.

Esimerkissä oleva data on peräisin Microsoftin Contoso demo datasetista.

![GIF, joka näyttää miten raportin slicer muuttaa näkymää](Demotiedosto.gif)

<br>

### User Defined Functions, käyttäjän määrittelemät funktiot
Esimerkkinä numeron muotoilu. Perinteinen tapa vaatii muotoilumerkkijonon tai DAX-koodia jokaiseen mittariin, johon muotoilu halutaan kohdistaa. Käyttäjän määrittelemällä funktiolla toki vaatii saman toimenpiteen, mutta ylläpito helpottuu. Muutokset voidaan tehdä pelkästään funktioon.

Muotoile-kohtaan asetetaan esim. seuraava DAX-koodi.

![Measure Format](Format1.png)


UDF:n kohdalla vastaava koodi olisi seuraava, mutta muotoile-kohtaan asetetaan ainoastaan funktion nimi.

![Measure Format with UDF](Format2.png)

Käytetyn UDF-funktion koodi.

![UDF-esimerkkikoodi](Function.png)

M Sales Quantity -sarake tehty perinteisellä tavalla ja M Revenue UDF:n avulla - lopputuloksessa ei ole eroa, mutta mm. ylläpito voi helpottua UDF:n avulla reilusti.

![Numeron muotoilu - M Sales Quantity perinteisellä tavalla ja M Revenue UDF:n avulla](UDF.png)

