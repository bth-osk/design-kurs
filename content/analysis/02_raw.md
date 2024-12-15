---
Title: 02 Appendix - Rådata
Description: This is our kmom05 load time raw data page.
Template: report
---

# Laddningstider - Rådata

**Författare:** osau24

## Sidor att analysera

- Sida A
    - A1 - https://ericschmidt.com/
    - A2 - https://ericschmidt.com/initiatives/
    - A3 - https://ericschmidt.com/bio/
- Sida B
    - B1 - https://pascalvangemert.nl/
    - B2 - //
    - B3 - //
- Sida C
    - C1 - https://bryantcodes.art/
    - C2 - //
    - C3 - //

## PageSpeed Insights

Analyser utförda 2024-12-14 - 2024-12-15.

|          | Sida A1 | Sida A2 | Sida A3 |
| :------: | :-----: | :-----: | :-----: |
| FCP (s)  | 0.3     | 0.5     | 0.3     |
| LCP (s)  | 3.2     | 0.5     | 2.0     |
| TBT (ms) | 0       | 0       | 0       |
| CLS      | 0       | 0.002   | 0.006   |
| SI (s)   | 0.3     | 0.6     | 0.3     |
| PS       | 83      | 100     | 91      |
| AS       | 93      | 94      | 100     |

**Tabell 2.2:** *Resultat från PageSpeedInsights [[#1]][1] för sidorna **A1-A3 - Desktop**, för en enskild mätning för respektive sida. First Contentful Paint (FCP) [[#2]][2], Largest Contentful Paint (LCP) [[#3]][3], Total Blocking Time (TBT) [[#4]][4], Cumulative Layout Shift (CLS) [[#5]][5], Speed Index (SI) [[#6]][6], Performance Score (PS) [[#7]][7], Accessibility Score (AS) [[#8]][8]. Vid felrapportering och/eller annan avsaknad av resultat, anges "inte tillämpligt" (I/T).*

|          | Sida A1 | Sida A2 | Sida A3 |
| :------: | :-----: | :-----: | :-----: |
| FCP (s)  | 1.4     | 1.4     | 2.1     |
| LCP (s)  | 6.5     | 3.5     | 11.6    |
| TBT (ms) | 0       | 130     | 0       |
| CLS      | 0       | 0       | 0       |
| SI (s)   | 1.9     | 1.6     | 2.1     |
| PS       | 77      | 90      | 73      |
| AS       | 86      | 88      | 94      |

**Tabell 2.3:** *Resultat från PageSpeedInsights [[#1]][1] för sidorna **A1-A3 - Mobile**, för en enskild mätning för respektive sida. First Contentful Paint (FCP) [[#2]][2], Largest Contentful Paint (LCP) [[#3]][3], Total Blocking Time (TBT) [[#4]][4], Cumulative Layout Shift (CLS) [[#5]][5], Speed Index (SI) [[#6]][6], Performance Score (PS) [[#7]][7], Accessibility Score (AS) [[#8]][8]. Vid felrapportering och/eller annan avsaknad av resultat, anges "inte tillämpligt" (I/T).*

|          | Sida B1 | Sida C1 |
| :------: | :-----: | :-----: |
| FCP (s)  | 0.7     | 0.8     |
| LCP (s)  | 1.0     | I/T     |
| TBT (ms) | 60      | I/T     |
| CLS      | 0       | 0       |
| SI (s)   | 0.7     | 3.9     |
| PS       | 98      | I/T     |
| AS       | 95      | 95      |

**Tabell 2.4:** *Resultat från PageSpeedInsights [[#1]][1] för sidorna **B1-C1 - Desktop**, för en enskild mätning för respektive sida. First Contentful Paint (FCP) [[#2]][2], Largest Contentful Paint (LCP) [[#3]][3], Total Blocking Time (TBT) [[#4]][4], Cumulative Layout Shift (CLS) [[#5]][5], Speed Index (SI) [[#6]][6], Performance Score (PS) [[#7]][7], Accessibility Score (AS) [[#8]][8]. Vid felrapportering och/eller annan avsaknad av resultat, anges "inte tillämpligt" (I/T).*

|          | Sida B1 | Sida C1 |
| :------: | :-----: | :-----: |
| FCP (s)  | 2.8     | 2.8     |
| LCP (s)  | 4.9     | I/T     |
| TBT (ms) | 60      | I/T     |
| CLS      | 0       | 0       |
| SI (s)   | 4.5     | 9.0     |
| PS       | 75      | I/T     |
| AS       | 95      | 95      |

**Tabell 2.5:** *Resultat från PageSpeedInsights [[#1]][1] för sidorna **B1-C1 - Mobile**, för en enskild mätning för respektive sida. First Contentful Paint (FCP) [[#2]][2], Largest Contentful Paint (LCP) [[#3]][3], Total Blocking Time (TBT) [[#4]][4], Cumulative Layout Shift (CLS) [[#5]][5], Speed Index (SI) [[#6]][6], Performance Score (PS) [[#7]][7], Accessibility Score (AS) [[#8]][8]. Vid felrapportering och/eller annan avsaknad av resultat, anges "inte tillämpligt" (I/T).*

-------

## Firefox Network Monitor

Analyser utförda 2024-12-15.

|         | Sida A1 | Sida A2 | Sida A3 |
| :-----: | :-----: | :-----: | :-----: |
| ALR     | 12      | 12      | 5       |
| TS (MB) | 4.12    | 4.19    | 1.96    |
| LT1 (s) | 2.13    | 1.35    | 0.75    |
| LT2 (s) | 1.85    | 1.19    | 0.79    |
| LT3 (s) | 2.32    | 1.87    | 0.66    |
| LTM (s) | 2.10    | 1.47    | 0.73    |

**Tabell 2.6:** *Resultat från Firefox - Network Monitor [[#9]][9] för sidorna **A1-A3**. Antal laddade resurser (ALR), total storlek (TS) i MB, laddningstid (LT, försök 1-3), laddningstid medelvärde (LTM) för LT1/LT2/LT3.*

|         | Sida B1 | Sida C1 |
| :-----: | :-----: | :-----: |
| ALR     | 7       | 10      |
| TS (MB) | 4.01    | 1.43    |
| LT1 (s) | 1.71    | 0.86    |
| LT2 (s) | 1.34    | 1.09    |
| LT3 (s) | 1.68    | 1.08    |
| LTM (s) | 1.58    | 1.01    |

**Tabell 2.7:** *Resultat från Firefox - Network Monitor [[#9]][9] för sidorna **B1-C1**. Antal laddade resurser (ALR), total storlek (TS), laddningstid (LT, försök 1-3), laddningstid medelvärde (LTM) för LT1/LT2/LT3.*

## Referenser

1) https://pagespeed.web.dev/
2) https://web.dev/articles/fcp
3) https://web.dev/articles/lcp
4) https://web.dev/articles/tbt
5) https://web.dev/articles/cls
6) https://developer.chrome.com/docs/lighthouse/performance/speed-index
7) https://developer.chrome.com/docs/lighthouse/performance/performance-scoring
8) https://developer.chrome.com/docs/lighthouse/accessibility/scoring
9) https://firefox-source-docs.mozilla.org/devtools-user/network_monitor/

[1]: https://pagespeed.web.dev/
[2]: https://web.dev/articles/fcp
[3]: https://web.dev/articles/lcp
[4]: https://web.dev/articles/tbt
[5]: https://web.dev/articles/cls
[6]: https://developer.chrome.com/docs/lighthouse/performance/speed-index/
[7]: https://developer.chrome.com/docs/lighthouse/performance/performance-scoring
[8]: https://developer.chrome.com/docs/lighthouse/accessibility/scoring
[9]: https://firefox-source-docs.mozilla.org/devtools-user/network_monitor/
