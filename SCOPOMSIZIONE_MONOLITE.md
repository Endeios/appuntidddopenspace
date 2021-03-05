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

- la terra di mezzo e' la norma: team cosi cosi, come si fa cosi?
    - si beh senza problemi no li chiamano
    - tentiamo di capire di risolvere il problema giusto
    - quali sono le opzioni?
        - decisione!
    - Quale e' il guadagno del refactoring? e' alto? se si' si tenta, se no non ne vale la pena
    

