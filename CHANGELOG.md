### 3. `CHANGELOG.md`
Aquest fitxer serveix per registrar històricament l'evolució del projecte. Hi he inclòs com a canvis recents les millores actuals que utilitza el teu script (com l'actualització del nou mòdul `google-genai` o el model `gemini-2.5-flash`).

```markdown
# Historial de Canvis (CHANGELOG)

Tots els canvis notables en aquest projecte estaran documentats en aquest fitxer.

## [1.1.0] - 2026-06-04

### 🚀 Afegit
- Creat el fitxer `README.md` amb instruccions d'ús, configuració de secrets i integració de JavaScript.
- Creat el fitxer `CONTRIBUTING.md` amb les directrius per a col·laboradors.
- Creat el fitxer `CHANGELOG.md` per fer el seguiment de versions del backend.

### 🔧 Modificat / Millorat
- S'ha actualitzat la llibreria clàssica de Google per fer servir el nou SDK unificat (`google-genai`).
- S'ha actualitzat el model a `gemini-2.5-flash` per a una major velocitat i millor comprensió del català.
- S'ha ampliat el límit del scraper recursiu a un màxim de **257 pàgines** per cobrir tota l'estructura de la web.
- S'ha afegit una línia de depuració en viu (`print`) que mostra el títol exacte llegit de cada pàgina extreta amb èxit.

### 🐛 Corregit
- Fixat el problema de dependències forçant la versió de `requests==2.32.4` per evitar conflictes de resolució en entorns virtuals recents.
- Corregit un problema potencial de bloqueig afegint un `timeout=10` a la funció de web scraping.

## [1.0.0] - Versió Inicial

### 🚀 Afegit
- Arquitectura bàsica basada en Flask i ngrok per a entorns Google Colab.
- Sistema de Web Scraping recursiu bàsic usant `BeautifulSoup`.
- Motor de cerca intern per paraules clau sobre l'arxiu JSON generat.
- Connexió bàsica amb la API de Google Gemini per respondre preguntes utilitzant el context de la web.
