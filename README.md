<h1>Scanner Prodotti</h1>

Questo sistema consente ai commercianti di aggiornare in modo semplice la giacenza del magazzino utilizzando uno scanner per codici a barre. Il gestionale, che integra anche funzionalità di e-commerce, sarà gestito tramite WordPress.


La nostra applicazione comunicherà con le API di OpenAI per cercare informazioni sul prodotto tramite il codice a barre. Una volta individuato il prodotto, l'applicazione genererà un file JSON che verrà inviato a WordPress tramite API.
<br>
<br>
<b>Procedura Operativa:</b>
1) Collegando lo scanner, sarà possibile scansionare l'etichetta del prodotto.
2) Dopo aver acquisito il codice numerico dall'etichetta, il commerciante potrà:
- Aggiungere una quantità specifica del prodotto al magazzino.
- Verificare la disponibilità del prodotto in magazzino.
- Rimuovere una quantità specifica dal magazzino.
3) Esito dell'operaziome
<br>
<br>

<b>Procedura pratica</b>
![Screenshot 2024-10-12 220757](https://github.com/user-attachments/assets/0fba9d12-3cf0-4df9-9bc2-b4ed94ea5ed9)

La nostra webapp sarà fatta in Python e PHP, Oltre a Html, CSS, Javascript e Bootstrapp.
1) In un form viene mandato tramite Api a OpenAI il codice del prodotto.
2) L'Api di OpenAI si occupa di mandare a sua volta una richiesta alla SERP di Google per analizzare i risultati. In particolare prenderemo i risultati di Ebay e Amazon.
3) Una volta fatta la ricerca, i risultati vengono elaborati.
4) Una volta elaborata, la risposta, ci verrà inviata sulla nostra app.
-- La risposta ritornata dall'api può essere TRUE(Abbiamo i dati del prodotto) o FALSE(Not found)--
5) In caso di true il gestore del negozio può eseguire delle operazioni e salvare il JSON su wordpress tramite API.
6) Come ultimo step Wordpress ci comunica se il salvataggio è andato a buon fine!
