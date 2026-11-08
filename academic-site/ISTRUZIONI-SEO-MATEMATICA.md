# SEO matematico — modifiche mirate

Copia i file nelle stesse posizioni della cartella locale `academic-site`.
Le modifiche non sostituiscono il tema PaperMod e non alterano l’impostazione grafica.

Modifiche:
- Nuova pagina HTML sulla tesi: `/research/strict-univalent-universes/`.
- Link alla pagina dalla homepage, dalla sezione Research e da Publications.
- Descrizioni più specifiche per Research e Publications.
- Parole chiave matematiche nella configurazione Hugo (solo come metadati ausiliari; Google non usa `meta keywords` per il ranking).

Per pubblicare:
```
git add .
git commit -m "Add mathematical research landing page"
git push origin main
```

Dopo la pubblicazione, invia l’URL della nuova pagina tramite Google Search Console.
Misura impressioni e query con la sezione Rendimento, senza aspettarti un risultato immediato o garantito.
I dati matematici della nuova pagina sono riassunti dai contenuti già presenti sul sito: controlla sempre che corrispondano alla formulazione della tua tesi.
