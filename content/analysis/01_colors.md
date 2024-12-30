---
Title: 01 Färger
Description: This is our kmom04 colors page.
Template: report
---

# Färger

**Författare:** osau24

Till kursmomentet KMOM4 skall färgval på utvalda webbsidor analyseras, inom uppgiften ["Utvärdera webbplatsers färgval och känslan de signalerar (v2)"](https://dbwebb.se/uppgift/utvardera-webbplatsers-fargval-och-kanslan-de-signalerar-v2). 

---
## Sidor att analysera
---

- Sida A - https://ericschmidt.com/
- Sida B - https://pascalvangemert.nl/
- Sida C - https://bryantcodes.art/

Urvalet av webbsidor för analys är separat beskrivet på sidan "Urval". Likaså finns skärmbilder för respektive sida (tagna 2024-11-28) utritade på den separata sidan "Sidvyer". 

---
## Metodik
---

Följande verktyg användes

- Firefox 132.0.1 (64-bit) [[#1]][1] för åtkomst, rendering, utläsning av CSS-formatering, och skärmbildstagning av sidorna.
- ColorZilla 3.4 (Firefox) [[#2]][2] webbläsartillägg för att identifiera färgkoder.

För att identifiera typsnitt användes "Inspector"-funktionen i Firefox. Typsnitt identifierades för den dominerande (bröd-) texten på respektive sida, därefter undersöktes ifall andra typsnitt fanns för olika rubriktyper (H1-H3). Ifall inte (p,h1,h2,h3)-HTML-taggar användes, tolkades texten på sidan utifrån vilka element som ansågs motsvara rubriker, underrubriker, och brödtext.

Färgscheman dokumenterades, via ColorZilla i Firefox, utifrån vad som ansågs vara den dominerande bakgrundsfärg på sidan i allmänhet, bakgrundsfärg för huvudsaklig brödtext, färg på huvudsaklig brödtext, bakgrundsfärg och textfärg på alternativa textblock, och annan typ av accentfärg. Två accentfärger valdes ut, utifrån att de subjektivt uppfattades förekomma frekvent på respektive sida. "Point sample"-funktionen i ColorZilla användes för att avläsa färgen på specifika punkter, istället för medelvärden över flera pixlar. Valet att använda "Point sample" var främst utifrån färgavläsningar på mindre detaljer, med korta avstånd till bakgrundsfärgen.

---
## Resultat
---

Nedan summeras resultat i separata tabeller för typsnitt och färgscheman.

*Typsnitt*

|          | Sida A  | Sida B           | Sida C (*)            |
| :------: | :-----: | :--------------: | :-------------------: |
| Brödtext | Graphik | Work Sans        | Roboto Mono           |
| H1       | Graphik | Permanent Marker | ?Bryant?              |
| H2       | Graphik | Permanent Marker | ?Roboto eller Bryant? |
| H3       | -       | Work Sans        | ?                     |

**Tabell 1.1:** *Typsnitt identifierade via CSS-avläsning för urvalda personsidor.*

(*): Viss svårighet fanns för att tolka typsnittförekomst på denna sida. Ett eget typsnitt, "Bryant", användes och länkades till. Dock kunde "Inspect"-funktionen i Firefox ibland inte mappa vissa objekt till HTML-block och CSS-regler. Eventuellt kan detta ha berott på att texten var integrerad i grafiska objekt. CSS-reglerna för olika HTML-element använde sig även av "inherit"-hänvsningar, och dessa länkningar undersöktes inte i full detalj. Utifrån dessa komplikationer är den tekniska typsnitt-utvärderingen av i synnerhet sida C bristande.

*Färgscheman - färgkoder*

|                    | Sida A  | Sida B  | Sida C (**) |
| :----------------: | :-----: | :-----: | :---------: |
| Allmän bakgrund    | #FFFFFF | #FFFFFF | #00FF00     |
| Bakgrund brödtext  | #FFFFFF | #FFFFFF | #00FFFF     |
| Brödtext           | #303030 | #616161 | #000000     |
| Bakgrund alt. text | #2B4169 | #E5E7EB | #BDFFBD     |
| Alt. text          | #E2E5EA | #535C69 | #000000     |
| Accent 1           | #0F1224 | #FED96F | #FFFF00     |
| Accent 2           | #88D0E8 | #7D838F | #FF00FF     |

**Tabell 1.2:** *Färgkoder identifierade, för urvalda personsidor, med ColorPicker webbläsartilläget. Utskrivna med hexadecimal kod.*

(**): Färgschemat var i detta fall mycket blandat. Då dominerande färger utvärderades subjektivt finns stora möjligheter till alternativa tolkningar. I synnerhet just för sida C, där starka (och ett större antal än för sida A eller B) färgkontraster använts.

*Färgscheman - färgrepresentation*

<table class="color-table" style="border-spacing: 10px; border-collapse: separate">
<tr>
<td> <b>Sida A</b> 
<td> <b>Sida B</b> 
<td> <b>Sida C</b> 
</tr>
<tr>
<td style="height: 100px; background-color: #FFFFFF; outline-style: solid">
<td style="height: 100px; background-color: #FFFFFF; outline-style: solid">
<td style="height: 100px; background-color: #00FF00; outline-style: solid">
</tr>
<tr>
<td style="height: 100px; background-color: #FFFFFF; outline-style: solid">
<td style="height: 100px; background-color: #FFFFFF; outline-style: solid">
<td style="height: 100px; background-color: #00FFFF; outline-style: solid">
</tr>
<tr>
<td style="height: 100px; background-color: #303030; outline-style: solid">
<td style="height: 100px; background-color: #616161; outline-style: solid">
<td style="height: 100px; background-color: #000000; outline-style: solid">
<tr>
<td style="height: 100px; background-color: #2B4169; outline-style: solid">
<td style="height: 100px; background-color: #E5E7EB; outline-style: solid">
<td style="height: 100px; background-color: #BDFFBD; outline-style: solid">
</tr>
<tr>
<td style="height: 100px; background-color: #E2E5EA; outline-style: solid">
<td style="height: 100px; background-color: #535C69; outline-style: solid">
<td style="height: 100px; background-color: #000000; outline-style: solid">
</tr>
<tr>
<td style="height: 100px; background-color: #0F1224; outline-style: solid">
<td style="height: 100px; background-color: #FED96F; outline-style: solid">
<td style="height: 100px; background-color: #FFFF00; outline-style: solid">
</tr>
<tr>
<td style="height: 100px; background-color: #88D0E8; outline-style: solid">
<td style="height: 100px; background-color: #7D838F; outline-style: solid">
<td style="height: 100px; background-color: #FF00FF; outline-style: solid">
</tr>
</table>

**Tabell 1.3:** *Utritade färger för materialet presenterat i tabell 1.2 (motsvarande placering av rader och kolumner).*

---
## Analys
---

Nedan följer en kort summering av mitt personliga intryck från respektive sida:

### Sida A

Är i grunden en ljus sida, men jobbar mycket med mörka kontraster i separata block - gärna med hjälp av bilder. Typsnitt, färgskala, och textformatering ger ett intryck av professionalism och lågmäldhet. Layouten eftersträvar inte en extrem minimalism utan olikfärgade bakgrundsblock förekommer, men det är tydligt att varje vy inte ska låtas domineras av varken grafisk- (e.g. bilder med mycket detaljer) eller text- (e.g. långa textstycken, text som upptar en stor del av skärmvyn) driven komplexitet.

### Sida B

En mycket ljus och lättläst sida där informationsblock generellt är väl avgränsade och färgvariation används mycket begränsat. Den största avvikelsen är öppningsvyn där grundfärgen till det (i princip) monokromatiska färgschemat direkt introduceras. Typsnittsvalet låts vara mer leksamt än i sida A, och här används istället det rubriksättande typsnittet till att anspela på det handgjorda och hantverksskicklighet. För mer informationsrika delar används ett enklare sans-serif typsnitt, med hög läsbarhet och kontrastrik färgsättning samt typsnittsvikt.

### Sida C

Här brukas färger med total mättnadsgrad och starka kontraster på ett nästintill provokativt sätt - 16-bitars färgdjup är inte direkt ett krav för större delen av sidan. Dels sker detta på ett kanske nostalgiskt sätt riktat mot äldre datorgrafik och tidig webbdesign. Sidan är långt från minimalismen i sida B, och kan snarare beskrivas som maximalistisk. Uppvisningen upplevs dock vara med glimten i ögat, och all denna primitiva formgivning och kanske ålderstigna färgpalett används med hög teknisk komplexitet, där interaktivitet och animationer är väntande för nästintill varje musklick. Detta kan eventuellt ses som en demonstration av att personen i fråga har ett starkt utvecklings- och teknikintresse, och jobbar gärna med profesionella designers för den grafiska aspekten. Typsnitten trycker likaså på det tekniska och kodnära, där brödtext gärna presenteras med fast breddsteg. Rubrikerna däremot visas ofta med mer komplexa i typsnittet och anspelar på det handgjorda.

### Återkoppling kring metodik och resultat

Jämförelserna gjorda här är starkt bristande i objektivitet och systematisk metodik. Dels beror detta på att färganalays och typsnittanalys, tolkats och avlästs manuellt och inte med något standardiserat verktyg/skript (e.g. att läsa av storlekar och färger på utritade element vid någon standardupplösning likt 1920x1080). Resultatinsamlingen försvårades även av att sidorna (främst gruppen A/B, i jämförelse med C) skiljde sig drastiskt i utformning, där sida C var väldigt animationsdrivet och inte på samma sätt uppstyckat i ett antal specifika HTML-sidor där texten är fast renderad.

Det hade varit intressant att prova att göra mer CSS-driven analys av färgskalor, då viss svårighet ibland fanns vid användning av "ColorZilla" för att selektera rätt åsyftad del för färgutläsning, eller för att tolka eventuella färggradienter. 

### Designprofil och eventuellt avvikelse från målsättning

Samtliga webbsidor skulle jag personligen anta har det utseende och profil som dess skapare eftersökt. Alla tre sidor framstår för mig att ha ett väldigt aktivt val av design, och jag har inte sett någonting antydande på en oönskad designutkomst.

---
### Avslutande ord
---

Trots att analysen av sidorna blev väldigt subjektiv, var det givande att påbörja denna process med att bekanta sig med ett begränsat urval av webbsidor för designanalys. Ifall sidorna hade valts om igen, hade troligtvis en webbsida valts för att vara en mer typisk "mörk-sida", då sida A-C är alla relativt ljusa sidor (även om startvyn på sida A ger intrycket av att vara med en relativt mörk grafisk profil). 

/osau24

---
## Referenser
---

1) https://www.mozilla.org/en-US/firefox/
2) https://www.colorzilla.com/firefox/


[1]: https://www.mozilla.org/en-US/firefox/
[2]: https://www.colorzilla.com/firefox/

