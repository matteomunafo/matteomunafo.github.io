# Sito accademico (Hugo + PaperMod)

Sito costruito con [Hugo](https://gohugo.io) e il tema
[PaperMod](https://github.com/adityatelange/hugo-PaperMod), ispirato nella
struttura (hero, sezione "Now", griglia "Paths", nota finale) al sito di
riferimento, con contenuti tuoi da compilare.

## Requisiti

- Hugo **extended** ≥ 0.146.0 (`hugo version` per controllare)
  - macOS: `brew install hugo`
  - Windows: `choco install hugo-extended` o `winget install Hugo.Hugo.Extended`
  - Linux: scarica il binario da https://github.com/gohugoio/hugo/releases
    (cerca `hugo_extended_..._linux-amd64.tar.gz`)

## Sviluppo locale

```bash
hugo server -D
```

Apri http://localhost:1313

## Struttura del contenuto

- `content/_index.md` — homepage (hero + sezioni "Now"/"Paths"/nota finale, in HTML dentro il markdown)
- `content/research/` — progetti/note di ricerca (una pagina per progetto)
- `content/publications/` — pubblicazioni (una pagina per paper)
- `content/notes/` — note di studio
- `content/about.md` — pagina "About"
- `content/archive.md` — archivio automatico di tutti i contenuti (layout integrato di PaperMod)

Per aggiungere un nuovo contenuto:

```bash
hugo new content research/nome-progetto.md
```

## Personalizzazione

- `hugo.toml` — titolo, menu, social icons (`params.socialIcons`), descrizione
- `assets/css/extended/custom.css` — stile della homepage (hero/paths grid)
- Sostituisci tutti i placeholder tra `[PARENTESI QUADRE]` nei file di contenuto

## Pubblicazione su GitHub Pages

1. Crea un repo `<tuo-username>.github.io`
2. Aggiungi un workflow GitHub Actions per Hugo (guida ufficiale:
   https://gohugo.io/host-and-deploy/host-on-github-pages/)
3. Push del branch `main`: la Action builda ed effettua il deploy

## Note

- Il tema PaperMod è incluso come git submodule in `themes/PaperMod`. Se
  scarichi lo zip senza history git, esegui:
  ```bash
  git init
  git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
  ```
  oppure clona semplicemente il tema nella cartella `themes/PaperMod` a mano.
