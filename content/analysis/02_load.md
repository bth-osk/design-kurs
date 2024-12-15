---
Title: 02 Laddningstider
Description: This is our kmom05 load time page.
Template: report
---

# Laddningstider

**Författare:** osau24

Till kursmomentet KMOM5 skall laddningstid och användbarhet på utvalda webbsidor analyseras, inom uppgiften ["Utvärdera webbplatsers laddningstid och användbarhet (v2)"](https://dbwebb.se/uppgift/utvardera-webbplatsers-laddningstider-och-anvandbarhet-v2). 

## Sidor att analysera

- Sida A - https://ericschmidt.com/
- Sida B - https://pascalvangemert.nl/
- Sida C - https://bryantcodes.art/

Urvalet av webbsidor för analys är separat beskrivet på sidan "Urval". Likaså finns skärmbilder för respektive sida (tagna 2024-11-28) utritade på den separata sidan "Sidvyer". 

Utöver det allmäna urvalet av webbplatser att analysera, valdes (ifall möjligt) godtyckliga undersidor ut för hastighetsanalys.

## Metodik

Följande verktyg användes

- PageSpeed Insights [[#1]][1] för mer komplexa prestandamått och förslag för möjliga prestandaförbättringar.
- Firefox 133.0 (64-bit) [[#2]][2] för lokala mätningar av laddningstider och laddade resurser via Network Monitor verktyget [[#3]][3].

I PageSpeed Insights användes resultat från en enskild mätning, och inte värden från "(Core) Web Vitals" [[#4]][4] som anges på toppen av resultatsidan och kommer från CrUX/"Chrome User Experience Report" [[#5]][5]. Detta val gjordes främst då sida B inte fanns med sådana resultat listade, på grund av för få resultat via CrUX.

I Firefox Network Monitor räknades antalet laddade resurser som samtliga antal nätverksförfrågningar för resurser som skickades, även om någon resurs inte kunde laddas. Total (fil-) storlek angavs utifrån total storlek hos målfilerna. Laddningstid uppmättes utifrån egenskapen "load" och föregicks av en forcerad rensning av webbläsar-cache och omladdning av sidan. Sidladdningarna skedde i en desktop-miljö (1 854 px bred viewport), utan avvikande/icke-standard "user agent", och utan någon artificiell nätverksbegränsning. Nätverksanslutningen som användes uppmättes vid en enskild mätning via Bredbandskollen [[#6]][6], med standardinställningar (ipv4 / "närmaste mätserver" / "Websockets+HTTP").

Som mått för vilken sida som ansågs snabbast användes medelvärdena från mätningarna med Firefox Network Monitor.

## Resultat

Resultaten från mätningarna finns i huvudsak återgivna i sidan **"02 Appendix - Rådata"**.

Mätning via Bredbandskollen gav en nätverkshastighet på 34 Mbit/s i nedladdningshastighet och 13 ms svarstid.

I tabell 2.1 återges medelvärdena för lokala mätningar av laddningstid för respektive startsida. Sida C var snabbast och sida A långsammast. 

|         | Sida A | Sida B | Sida C |
| :-----: | :----: | :----: | :----: |
| LTM (s) | 2.10   | 1.58   | 1.01   |

**Tabell 2.1:** *Resultat från Firefox - Network Monitor [[#3]][3] för sidorna **A/B/C**. Laddningstid medelvärde (LTM) för tre enskilda mätningar.*

## Diskussion

Jämförelse mellan sidorna försvårades av att sida C gav felmeddelande för flera individuella mått PageSpeed Insights försökte utvärdera. Detta gjorde att viktad betygsättning för att ge ett "Performance Score" [[#7]][7] inte kunde beräknas för sida C. Därmed användes det enklare måttet med laddningstidmätningar via Firefox Network Monitor som jämförelse mått för att ranka sidorna. Måttet är dock inte talande utifrån användarinteraktionen, då den skripttunga sida C må vara snabbast på att ladda in alla resurser, men med startanimationer vid sidladdningen kan användaren inte interagera med sidan förrän flera sekunder senare.

Försvårande var även att sida B och C agerar som en huvudsida där allt innehåll återfinns. Detta gjorde att hastighetsmätningar på olika undersidor (A1/A2/A3) endast var möjligt för sida A. 

Nedan följer korta kommentarer om respektive sida och möjliga förbättringsförslag. Förbättringsförslagen är främst tagna från rekommendationer från resultatutvärderingen hos PageSpeed Insight, för respektive sida.

### Sida A

Representerar den textbaserade informationen och webbsidans huvudstruktur snabbt, även om högupplösta bilder används och agerar tidsbegränsande steg för sidan att vara färdigladdad. Den enklare biografi-sidan (A3) hade märkbart snabbare laddningstid, än de mer multimedia-komplexa A1/A2-sidorna.

#### A: Förbättringsförslag

Byte av filformat (nuläget PNG) för fullfärgsfotografierna som används i hög upplösning. Se över elementet som ger upphov till längst "Largest Contentful Paint" tid, vilket är ett högupplöst bildspel där en mp4-video spelas. 

```
<video loop="" playsinline="" preload="auto" autoplay="" muted="" src="https://ericschmidt.com/wp-content/uploads/Comp-2_2.mp4" style="position: absolute; max-width: none; top: 0px; left: 0px; width: 1854px;"></video>  <div class="container container--narrow"></div>
```

Kanske kan samma dynamiska bildvisningseffekt skapas "billigare", med enskilda bilder och javascript, istället för mp4-video.

### Sida B

Sidan domineras av en ladningssida med minimalt informationsinnehåll. Detta döljer eventuell fördröjning av att ladda in innehåll längre ner på sidan. Inladdning av speciellt typsnitt samt den högupplösta bilden till landningssidan är de mest begränsande elementen för att uppleva sidan som färdigladdad. Inladdningen av bilden till startsidan döljs relativt snyggt av att elementet snabbt målas upp med en bakgrundsfärg som matchar färgen på den kommande bilden.

#### B: Förbättringsförslag

Byte av filformat på bilderna med störst filstorlek (png och jpeg i nuläget). Inladdning av externa (Google Fonts) typsnitt verkar i nuläget fördröja laddningstiden (genom lång svarstid?), även om filstorleken i sig bara är någon enstaka KiB. Bilder som används till portfolio-sektionen tycks inte skalas i storlek utifrån webbläsarens viewport.

### Sida C

På grund av sin skripttunga natur är sidan svårare att jämföra utifrån inladdningshastighet, än sida A och B. Filstorlekarna som behöver laddas ner är små, men startanimationen gör att man inte når ett interagerande tillstånd med sidan förrån långt senare än resurserna är nedladdade (i testerna var skillnaden av storleksordningen 5x länge än laddningstiden - ej dokumenterat i resultatsektionen).

Även om flera betygsättningar och analyser från PageSpeed Insight inte var möjliga, var en observerad detalj att 5+ mp4-videor finns med bland (indirekt via JavaScript?) inlästa resurser. Dessa syntes inte under Firefox-analysen, men rapporterades från PageSpeed Index att uppgå till nästan 50 MB.

Det undersöktes inte systematiskt och är inte dokumenterat i metod/resultat-delen, men vid en ytlig inspektion under "Memory"-fliken i Firefox såg sida C ut att förbruka ca 10x så mycket arbetsminne som webbläsarflikarna med sida B eller C aktiva. 

#### C: Förbättringsförslag

Prestandautvärdera enskilda javascript-moduler utifrån CPU- och RAM-anvädning. Utvärdera alternativ till alla mp4-videos som läses in för portfolio-delen.

### Personligt mått av nödvändig laddningshastighet

Utan alltför omfattande funderingar i frågan, känner jag 5 sekunder som en "mjuk gräns" för en sida att laddas in utan att material finns i webbläsarens cache. Ingen av undersökta sidor kommer i närheten av detta gränsvärde. Jag värderar dock tid till "första pålitliga interaktion" högre än strikt laddningstid. Med tid till första pålitliga interaktion menar jag främst att det huvudsakliga skelettet av sidan är tillgängligt och interaktiva element är aktiva, samt att inga "Cumulative Layout Shift" sker som gör att interaktionen med sidan känns för tidig och opåltlig. Med det sagt enerveras jag betydligt mindre ifall vissa högupplösta bilder tar ytterligare tid att ladda in. Denna typ av beteende sker exempelvis på sida A, där textinnehåll och allmän layout är snabbt inladdat, men högupplösta bilder gradvis laddas in snyggt utan att några element flyttar på sig - utan att det upplevs som speciellt störande eller fördröjande för att ta del av sidan. 

### Avslutande ord

Jämförelsen blev tyvärr begränsad av mängden tekniska skillnader mellan sidorna (främst sida A/B i jämförelse med C, likt tidigare). Mest generellt gällande trender för att förbättra prestanda, är dock att det tycks finnas möjligheter att överväga andra filformat för bilder, samt alternativa sätt att förmedla samma bildinformation som relativt storlekstung mp4-video.

Fokus för analysen blev främst på desktop-miljön. Delvis på grund av att sida C ansågs vara mest lämpad som en desktop-upplevelsen. Även sida C är emellertid "mobilskärmskompatibel" och responsiv till den grad att man kan komma åt motsvarande information samt uppleva mycket av den interaktiva komplexitet som finns.

Alla sidor upplevdes av mig personligen (och under rådande tekniska förutsättningar) som rätt snabba, även om sida C kan få min webbläsare att jobba hårt och uppleva fördröjningar bortom rena laddningstider.

/osau24

## Referenser

1) https://pagespeed.web.dev/
2) https://www.mozilla.org/en-US/firefox/
3) https://firefox-source-docs.mozilla.org/devtools-user/network_monitor/
4) https://web.dev/articles/vitals
5) https://developer.chrome.com/docs/crux
6) https://www.bredbandskollen.se/
7) https://developer.chrome.com/docs/lighthouse/performance/performance-scoring

[1]: https://pagespeed.web.dev/
[2]: https://www.mozilla.org/en-US/firefox/
[3]: https://firefox-source-docs.mozilla.org/devtools-user/network_monitor/
[4]: https://web.dev/articles/vitals
[5]: https://developer.chrome.com/docs/crux
[6]: https://www.bredbandskollen.se/
[7]: https://developer.chrome.com/docs/lighthouse/performance/performance-scoring
