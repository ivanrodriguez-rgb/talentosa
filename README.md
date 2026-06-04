### 1. `README.md`
Aquesta és la guia principal del teu projecte. Inclou instruccions clares de com configurar els secrets de Google Colab (`GOOGLE_API_KEY` i `token_ngrok`), com funciona el teu codi i un exemple pràctic de codi en JavaScript per enllaçar el xat del teu Frontend amb la URL d'ngrok.

```markdown
# Assistent Virtual per al Portafolis d'Ivan Rodríguez

Aquest projecte és un backend complet desenvolupat en Python (Flask) dissenyat per a ser executat a Google Colab. Realitza una extracció massiva (web scraping) del portafolis d'en Ivan Rodríguez, processa la informació, indexa els continguts de forma intel·ligent i utilitza la IA de Google (**Gemini 2.5 Flash**) per respondre preguntes dels usuaris en temps real a través d'una API pública gestionada per **ngrok**.

## 🚀 Característiques

- **Extractor Total (Scraper):** Navega de forma recursiva per la web fins a un límit de 257 pàgines, evitant fitxers estàtics (.jpg, .pdf, .png) i rutes d'administració de WordPress.
- **Cercador Intel·ligent:** Filtra i puntua les pàgines més rellevants de la base de dades local segons les paraules clau de la consulta de l'usuari per optimitzar el context enviat a la IA.
- **Integració amb Gemini 2.5 Flash:** Genera respostes naturals, amables i contextualitzades en català, basant-se estrictament en els continguts extrets.
- **Túnel ngrok:** Exposa el servidor Flask local de Colab a una URL pública (`https://...ngrok-free.app/ask`) per connectar-lo fàcilment amb qualsevol frontend (JavaScript, aplicacions mòbils, etc.).
- **Seguretat amb Secrets:** Utilitza el sistema de `userdata` de Google Colab per gestionar les claus privades de l'API de Google i el token d'ngrok.

## 🛠️ Requisits i Arquitectura

El script depèn de les següents llibreries principals:
- `google-genai` (SDK oficial actualitzat de Google Gemini)
- `flask` i `flask-cors` (Per a la creació de l'API i gestió de peticions creuades)
- `pyngrok` (Per a la creació de la URL pública)
- `beautifulsoup4` i `requests` (Per a l'extracció i processament de l'HTML)

---

## 💻 Instal·lació i Ús a Google Colab

### 1. Configuració de Secrets a Colab
Abans d'executar el codi, has d'afegir les teves claus a la secció de **Secrets** (icona de la clau 🔑 al menú lateral esquerre de Google Colab):
1. Afefeix un secret anomenat `GOOGLE_API_KEY` amb la teva clau de Google AI Studio.
2. Afafeix un secret anomenat `token_ngrok` amb el teu token d'autenticació d'ngrok.
3. Activa l'accés del quadern a tots dos secrets.

### 2. Execució del Codi
Executa la cel·la del quadern. El procés farà el següent de manera automàtica:
1. Instalarà les llibreries necessàries.
2. Inicialitzarà el client de Gemini i ngrok.
3. **Fase de Scraper:** Començarà a descarregar i guardar els títols i continguts en un fitxer anomenat `dades_ivan_total.json`.
4. **Fase de Servidor:** Tancarà connexions antigues d'ngrok, n'obrirà una de nova i aixecarà el servidor Flask.

Al final de la consola veuràs una sortida similar a aquesta:
```text
🌍 URL PER AL TEU JAVASCRIPT:
[https://abcd-123-45-67-89.ngrok-free.app/ask](https://abcd-123-45-67-89.ngrok-free.app/ask)
