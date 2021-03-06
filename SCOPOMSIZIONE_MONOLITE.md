# Scopmosizione del monolite

- il punto di partenza e' non decidere tutto subito
- scopmorre il monolite
    - per performance
    - team di 4 persone su una tabella

- in tutti i casi : come si scompone? come ci muoviamo
    - Event storming big picture: per capire dove ci sono i casini
        - event sorming bla bla bla
        - cosa succede nel business? end to end.
        - eventi in riga, persona e come si relazionano tra di loro
        - osservando la gente si capisce che
            - si capisce perche *Questo e' un evento grosso/pubblico*
                - eventi duplicati
                - piu sottoscrittori
                - se c'e separazione tra competenze
                - se c'e separazione tra bounded context
            - dove fa male?
                - architettura
                - business
                - non e'e solo una cosa per sviluppatori
            - trovare dove sono i confini delle aree di interesse (diventatno bounded context)
                - mappare sulle persone che lo fanno (in org grandi)
                - e' piu' difficile vederli in realta' piccole, perche la gente ha molti cappelli (no separazione tra pianificazione ed esecuizione)
            - importante creare allinemanto, piu' facile in presenza, e con meno gente che deve decidere. (vedono il casino e vogliono risolverlo)
            - il goal del workshop e' trovare i problemi e decidere quali sono le cose da risolvere:

- Alberto: far emergere i problemi: uno capisce non solo "perche smontare il monolite" ma anche "la gente e' capace di fare quensta nuova cosa?"
    - ZB: c'e' anche la scelta: non ce la si fa e si /gquitta
    - aiuta anche far capire se e' una gabbia di matti
        - possono farcela : ZB da anche consulenza tecninca
        - non possono farcela/ la gente nono vuole venire / problemi personali ==?> ZB diche che e' meglio deistere
        - nella terra di mezzo: non c'e' tutto, ma sappiamo che cosa e' che rema conto, 
            - se ne parla dopo, e si legge la gente dopo, e si tenta di capire chi e' on board o no
            - si raccolgono tutte le informazioni e se ne parala dopo
                - non sul posto
        - (fattore grosso) se l'autore della roba vecchia e' andato via
        e' piu' facile migrare: la gente non si sente chiamata in discussione e si cambia facile
    - il successo avviene perche' si taglia col passato: se non si taglia, non si cambia.

- GPad: come viene chiamato lo ZioBrando? gpad lo chiamano come tecnico, come fa lui a fare change?
    - ZB fa consulenza e formazione: il motivo e' consulenza di alto livello:
    - ZB fare il risultato pubblico, cosi tutti si sentono chiamati in causa
    - ZB non lo chiamano per guardare 2 classi:
    - ES => va virale col rotolone sul muro, quindi lui consiglia
    di mettere il rotolone all'entrata. difficile farlo con miro, la genert si deeve loggare esplicitamente

- la terra di mezzo e' la norma: se il team e' cosi cosi, come si fa?
    - si beh senza problemi no li chiamano
    - tentiamo di capire di risolvere il problema giusto
    - quali sono le opzioni?
        - decisione!
    - Quale e' il guadagno del refactoring? e' alto? se si' si tenta, se no non ne vale la pena
    - problema di costruire il consenso su una mossa, il committment
    capire come valutare
    - mettere quelli bravi nelle condizioni di fare qualcosa di buono: difficile da remoto: non c'e' il "peso del consulente" ed il rispetto per l'evento.

- diciamo che hai vinto il consenso del middle management: e dopo? la srotoli all high management?
    - il meglio e' battere il ferro finche e' caldo:
        - 1 giorno disgnostica: capire il problema
        - 2 giorno fare il workshop: non li facciamo far uscire fino a che non si committano sulla soluzione.
    - aspetti il momento del "ma e' lei che tutto questo casino" 
    quando il rotolone e' visibile. per natura del risolvere il problema,  e' un problema dell'high management se non fanno niente col problem che fanno. e' importante che il punto di contatto sia abbastanza in alto.

- e' difficile trovare la porzione del sistema dove c'e un seam. che bisogna spaccare: la colonna Stato e' un chiaro indicatore di rottura
    

## Precisazioni dello Zio Brando

ZB =>
Grazie, ne approfitto per chiarire meglio la domanda (o la risposta) sulla Terra di mezzo:

ZB =>
Ed il concetto base è che siamo sempre nella terra di mezzo: se sono bravissimi magari fanno da soli, se non hanno idea di DDD non ti chiameranno neanche. Quindi in genere mi chiamano solo se c'è almeno qualcuno in azienda che ha qualche buona idea, ma non ha la leva politica per fare succedere le cose. (edited) 

ZB =>
EventStorming in questo senso è un ottimo sistema per fare succedere le cose, perché sbatte in faccia al business che sta perdendo soldi. Al business non interessa il refactoring, ed il debito tecnico. Al business interessa capire perché stiamo perdendo soldi o perché non ne stiamo guadagnando.

ZB =>
Io non guardo ai soldi perché sono avido. Ma guardo ai soldi, perché devo poter giustificare con il business un'operazione che vedono come un pugno in un occhio.

ZB =>
Agli occhi del business: Refactoring = mettere del budget per fare cose che non capisco e che non si vedono da fuori.

ZB =>
E pensano: ti concedo di farlo una settimana, ma poi basta.

ZB =>
L'unico modo per convincerli è portargli delle revenues.

ZB =>
Mentre il tipico dev commette due errori in questo campo:

ZB =>
Parte animato dal desiderio di pulire il codice (che è un problema suo, che non interessa necessariamente il business).
Non ha una chiara condizione di finito. Perché Rifare il monolite o... Rendere tutto più bello sono per il business "soldi bruciati senza sapere quando finirà"

ZB =>
Chiarito lo scope dell'intervento... chi ce la può fare in genere si auto-candida. Molto spesso perché semplicemente non vede l'ora.

ZB =>
Ma è fondamentale chiarire il perimetro dell'intervento. Perché molte volte lo stato di partenza è non va niente! e per quanto bravi possiamo essere, non abbiamo il tempo di sistemare TUTTO!.

ZB =>
Aggiungo:

ZB =>
Il cliente medio ti chiede di sistemare in 2 sessioni il casino ammucchiato di 50 developers in 15 anni.

ZB =>
Ed in genere riscrivere è più lento che scrivere.

ZB =>
Quindi essere circoscritti nelle promesse è un'ottima regola di sopravvivenza.

ZB =>
Anche se spesso si possono fare dei filotti: risolvi un problema e magicamente ne fai sparire 2 o 3 a valle.
