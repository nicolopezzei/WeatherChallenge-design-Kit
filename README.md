# WeatherChallenge · Kit di design

Questo è un **laboratorio per sperimentare con HTML e CSS** sul design di WeatherChallenge, l'app di previsioni meteo del Liceo.

Qui non c'è niente di collegato al sito vero: nessun accesso, nessun database, nessun dato di persone reali. I nomi, i punteggi e le previsioni sono inventati. Puoi provare, rompere e ricominciare senza rischi.

## Come si usa

1. Scarica la cartella (o clonala da GitHub).
2. Apri `index.html` con un doppio clic: si apre nel browser, senza installare niente.
3. Apri la cartella con un editor di testo (per esempio Visual Studio Code) e modifica i file in `assets/css/`.
4. Salva e **ricarica la pagina** nel browser (tasto F5): vedi subito l'effetto.

**Per vedere la versione da telefono:** nel browser premi F12 e poi clicca l'icona del telefono. In alternativa, stringi la finestra sotto i 768 px.

## Cosa c'è dentro

```
index.html              l'elenco di tutte le pagine
login.html              accesso (più 3 varianti: errore, uscita, senza numeri)
dashboard.html          calendario (computer) e lista risultati (telefono)
insert-forecast.html    modulo per inserire una previsione
history.html            storico delle previsioni
ranking.html            classifica con podio
public-forecasts.html   previsioni pubbliche dei migliori
resources.html          strumenti meteo
weather-sources.html    elenco dei siti meteo
menu.html               le voci del menu

assets/css/
  tema.css              <- PARTI DA QUI: colori, forme e font in poche righe
  style_*.css           i fogli di stile veri del sito, uno per pagina
  kit_statico.css       parti che nel sito vero sono create dal JavaScript
  style_menu.css        stile del menu
assets/img/             nuvola e logo segnaposto
```

## Regole del gioco

- **Puoi cambiare:** colori, font, dimensioni, spaziature, bordi, ombre, animazioni, allineamenti.
- **Meglio non cambiare:** i nomi delle classi e la struttura dell'HTML (i tag `<div>`, `<section>`...). Il sito vero usa gli stessi nomi: se li lasci uguali, il tuo CSS potrà essere riportato nel sito senza fatica.
- **Un cambiamento alla volta:** prova, guarda, poi passa al successivo. Se qualcosa si rompe, annulla l'ultima modifica (Ctrl+Z).
- **Annota cosa cambi:** scrivi in un file di testo il nome del file, la riga e perché hai fatto quella scelta. Serve a spiegare le tue idee agli altri.

## Esercizi

### Livello 1: colori (file `tema.css`)
1. **Cambia il cielo.** Modifica `--wc-cielo-alto` e `--wc-cielo-basso`. Prova un tramonto, una notte, un cielo di tempesta. Controlla dashboard, storico e strumenti.
2. **Cambia i colori dei punteggi.** Modifica `--green`, `--orange`, `--red`. Guarda come cambiano classifica, previsioni pubbliche e le etichette nello storico.
3. **Cambia il font dei titoli.** Scegli un font su [Google Fonts](https://fonts.google.com), copia il link `<link>` nell'`<head>` di una pagina e scrivi il nome in `--wc-font-titoli`.

### Livello 2: forme e atmosfera
4. **Arrotonda o spigola.** Cambia `--wc-raggio-contenitore` e `--wc-raggio-card`: da 0 (spigoli vivi) a 30px (molto morbido).
5. **Ridisegna il login.** In cima a `style_login.css` ci sono le variabili `--wcl-*` con i colori della pagina. Cambia l'intestazione blu: che effetto fa un'altra tinta? E se la rendessi più chiara?
6. **Le nuvole.** In `style_dashboard.css` trova `.cloud`: cambia la velocità (`animation`) o la dimensione. Prova a rendere le nuvole più numerose.

### Livello 3: leggibilità
7. **Contrasto.** Con il [Contrast Checker di WebAIM](https://webaim.org/resources/contrastchecker/) controlla le coppie di colori: testo bianco sul giallo "In corso" del calendario, testo grigio chiaro nelle card, i badge verdi e rossi. Il rapporto deve essere almeno 4.5:1. Quali non lo rispettano? Proponi un'alternativa.
8. **Telefono.** Ridimensiona la finestra a 360 px. C'è qualcosa troppo piccolo da toccare con un dito (meno di 44 px)? Qualcosa che esce dallo schermo?

### Sfide
9. **Un tema nuovo.** Inventa un tema intero (per esempio "Tramonto", "Neve", "Notte") modificando soltanto `tema.css`.
10. **Il sondaggio.** Fai due varianti della stessa pagina e chiedi a 5 compagni, senza dire nulla, quale preferiscono e perché. Annota le risposte.

## Cose da sapere

- **Il calendario, il menu e l'intestazione sono "finti".** Nel sito vero sono creati dal JavaScript o da `header.php`. Qui sono scritti a mano in HTML (stili in `kit_statico.css`) e non reagiscono ai clic: il menu non si apre e i mesi non cambiano.
- **Su telefono la dashboard mostra la lista dei risultati**, non la griglia del mese. I pulsanti "Griglia" e "Lista" non funzionano in questo kit.
- **Il bottone "Entra con Google" apre la dashboard.** Nel sito vero fa l'accesso.
- **Serve internet** per caricare Bootstrap e i font da Google. Senza connessione le pagine si vedono ma con uno stile semplificato.
- Il logo della scuola è sostituito da un segnaposto: puoi usare un'altra immagine mettendola in `assets/img/`.
