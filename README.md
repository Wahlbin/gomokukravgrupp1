# gomokukravgrupp1

Kravspecifikation för en digital version av Gomoku (fem i rad).

## Vad som finns i repot

| Sökväg | Innehåll |
|--------|----------|
| `docs/requirements/01-inledning.md` | Inledning, syfte och omfattning |
| `docs/requirements/02-funktionella-krav.md` | Funktionella krav — spelmekanik, spellägen, användarfunktioner |
| `docs/requirements/03-kompletterande-krav.md` | Kompletterande krav — användbarhet, felhantering, prestanda |
| `docs/requirements/04-icke-funktionella-krav.md` | Icke-funktionella krav |
| `docs/requirements/05-begreppsmodell.md` | Begreppsmodell — centrala begrepp och relationer |
| `docs/requirements/06-user-journey.md` | User journey — användarens väg genom systemet |
| `docs/requirements/07-use-case-overview.md` | Översikt av samtliga use cases |
| `docs/requirements/use-cases/` | Detaljerade use cases (UC-01 – UC-03) |

> Alla kravdokument ligger i `docs/requirements/`. Use cases ligger i `docs/requirements/use-cases/`.

## Spelet i korthet

Gomoku är ett strategispel för två spelare på ett **15×15**-rutnät. Spelarna turas om att placera pjäser på linjernas korsningar — den som först får **fem i rad** (horisontellt, vertikalt eller diagonalt) vinner.

## Kravsammanfattning

| Område | Krav |
|--------|------|
| Spelbräde | 15×15 linjer, pjäser på korsningar |
| Spelutgång | Vinst, förlust och oavgjort hanteras |
| Spellägen | Mot robot, online eller lokalt på samma enhet |
| Svårighetsgrad | Lätt, mellan och svår (mot datorn) |
| Anpassning | Spelaren kan byta färg på egna pjäser |
| Integritet | Anonymt spelande — ingen registrering, spårning eller statistik |

## Use cases

| ID | Namn | Beskrivning |
|----|------|-------------|
| [UC-01](docs/requirements/use-cases/UC-01-starta-nytt-parti.md) | Starta nytt parti | Spelaren startar ett nytt spel |
| [UC-02](docs/requirements/use-cases/UC-02-gor-ett-drag.md) | Göra ett drag | Spelaren placerar en pjäs på brädet |
| [UC-03](docs/requirements/use-cases/UC-03-bjuda-in-van.md) | Bjuda in vän | Spelaren bjuder in en vän till ett parti |

## Kompletterande krav (urval)

- Det ska tydligt framgå **vilken spelares tur** det är.
- Ett giltigt drag ska registreras **inom 1 sekund**.
- Spelplanen ska kunna navigeras **med tangentbord**.
- Systemet ska inte spara personuppgifter som inte behövs för spelets funktion.
- Systemet ska kunna starta ett nytt spel utan att tidigare drag påverkar matchen.

## Licens

[GPL-2.0](LICENSE)
