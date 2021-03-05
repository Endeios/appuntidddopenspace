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
            - importante creare allinemanto, piu' facile in presenza, e con meno gente che deve decidere. (vedono il casino e vogliono risoloverlo)