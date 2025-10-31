 Mini HTTP Server in C

Un piccolo server HTTP scritto in C per comprendere il funzionamento di base delle **socket TCP**, del **binding** e della gestione delle connessioni client-server.

 Funzionalità

- Creazione e configurazione di un socket TCP (`AF_INET`, `SOCK_STREAM`)
- Binding su porta 8081
- Accettazione delle connessioni in loop continuo
- Lettura delle richieste HTTP dal browser
- Invio di una risposta HTML statica
- Gestione base dell’header `Connection: keep-alive`

 Struttura

Il server:
1. Crea una socket
2. Imposta l’opzione `SO_REUSEADDR`
3. Esegue `bind()` e `listen()`
4. Resta in ascolto in un ciclo infinito (`while(1)`)
5. Accetta connessioni con `accept()`
6. Legge la richiesta con `read()`
7. Risponde con una pagina HTML base
