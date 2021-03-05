# Session 1 in taverna: CQRS vs ES vs MS

- Lavornado su un progetto CQRS - DD Microservizi
- Raccontano le loro scelte e cosa hanno fatto
- Solito monolitone
 - Probelmi umani con la gente li
 - partiti da event sorming, tenatdo di capire l=event sotrming
    - MS di dimensione dell aggregato
    - CQRS -> si tutta la vita: quello funziona
    - ES -> no ma eventi emessi dagli aggregati, usati per comunicazione tra gli aggregati
    - definire aggregati ha messo ordine
    - no ES, perche sarebbe stato troppo per il cliente

- Acerbis: sembra l'architettura classica
    - cosa ci metti negli eventi?
    - cosa ti aspetti che succeda quando l'evento e' arrivato?

- Divisione tra gli eventi:
    - pubblici
        - esposti su rabbit
    - privati
        - eventi solo interni al microservizio
    - di default solo privato, e deve essere fatto pubblico
        - overengineering? no perche ti permette di separare la gestione dell'evento dal resto del sistema

- Come e' gestito l'eventual consitency?
    - all'interno dell'aggregato, quando viene persisito,
    gli eventi si eseguono sulMS o pubblicati su rabbit
    - verra' risolto che quando si salva il carrello, salvano gli eventi su una tabella secondaria (nella stessa transazione), e dopo pubblicano gli stessi eventi (pubblici o privati)
    (OUTBOX pattern)
    - I comandi (SU HTTP) hanno un risultato (no ,no ,no)
        - sono pochi
    - eventi su rabbit
        - struttura piatta
        - stesso exchange per tutti
        - anche workflow a microservizi

- Ancora su pubblici e privati
    - l'aggregato decide se e' pubblico o privato
    - 1 broker di rabbit
    - i privati servono per un discorso di refactoring, per salvaguardare il deploy singolo.
    - c'e' un event command: capisce che se l'evento e' pubblico o privato e decide se mandarlo in rabbit o eseguirlo localmente.

- Il process manager distribuite 'e un incubo da monitorare? lo 
avete gia' messo il monitoring o ci siete cascati?
    - si hanno il problema
    - comprensione:
        - event storming sul processo
        - event sorming sull'aggregato, e 
    - vengono aggiornato di continuo.
    - hanno usato correlation ID, e loggano e tenanto di capire che sudccede (con eventi che si sovrappongono nel tempo)

- come e' fatta la topologia delle code?
    - un unico exchange pubblico (events)
    - una routing key, che fa sditribuire a rabbit gli eventi come gli piace
    - ogni servizio si fa una coda, con prefetch, e sottoscrive
    - fun fact: un servizio non aveva prefetch, e quando andava su giu 
    moriva per il numero di eventi (fetchava tutto)
    - sottoscrizione solo all'event type
    - piacrebbe fare una cosa con dei namespace, con cose tipo
        - eventType : eventsubtype

- Il bounded context non ha una rappresentazione in architettura?
    - ora come ora e' composto da diversi servizi, con anche un monolitone

- Event bus interno: se hai piu' istanze dello stesso ms, la coda e' condivisa?
    - no e' interna all'istanza
    - perche interni all'istanza?
        - sono una cosa dove vogliono avere flessibilita' di refactoring e fare poco casino

- Come sono separati gli eventi?
    - sono classi diverse

- e quelli orchestrati e non orchestrati?
    - quando ci sono piu' istanze, e' difficile sapere quanti sono
    e quali sono e te li perdi se ti chiedono dati di sintesi: deve essere risolto da chi emette l'evento
    - Gpad mettono delle policy che sottoscrivono

- pubblici e privati: come fai a sapere che e' pubblico o privato?
    - loro hanno un solo repo che contiene una liberia con le versioni dei messaggi
    - anche loro tendono ad essere privati, minimizzando il numero di pubblici
