### 2. `CONTRIBUTING.md`
Aquest fitxer estableix les regles de col·laboració en el cas que algun company de classe, professor o programador vulgui ajudar-te a fer créixer o optimitzar l'aplicació.

```markdown
# Guia de Contribució (CONTRIBUTING)

Primer de tot, gràcies per voler millorar aquest assistent per al portafolis! Les contribucions fan que la comunitat de codi obert sigui un lloc increïble per aprendre, inspirar i crear.

## 👥 Com es pot contribuir?

### 1. Reportar errors (Bugs)
Si trobes un error en el codi de processament, caigudes del scraper o problemes de connexió:
- Obre una *Issue* detallant l'error.
- Inclou el missatge d'error de la consola de Google Colab.
- Explica quins passos vas seguir abans que fallés el programa.

### 2. Proposar millores
Estem oberts a noves funcionalitats! Idees interessants inclouen:
- Canviar el cercador bàsic de paraules clau per un sistema d'*Embeddings* semàntics (com `text-embedding-004`).
- Guardar el context de la conversa (memòria del xat) per permetre preguntes de seguiment.
- Millorar el filtratge d'HTML per eliminar elements repetitius (com menús de navegació o el peu de pàgina de WordPress).

## 🛠️ Procés de Desenvolupament i Submissió

1. **Fes un Fork** del repositori.
2. **Crea una branca de funcionalitat** per al teu codi:
   ```bash
   git checkout -b funcionalitat/NovaMillora
