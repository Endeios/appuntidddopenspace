# Errorri DDD

- non e' necessario mettere tutti a fare le stesse cose (avanzate) tutti assieme.
- Libro di vernon sul DDD: appendice A e' il valore: si parla di eventi:
    - ora come ora il sistema scalabile e' a evento
    - tipi di eventi
        - domain event (privato)
            - scatenato dall'aggregato
            - interno al bounded context (ha senso solo li)
        - integration event (pubblico)
            - gli altri aggregati devono essere comprensibili (sorta di lingua franca)
            - l'evento deve essere preso come e' (e' la legge) e buttato nel repo
                - no aggregazioni o elaborazioni
                - nell'evento ci deve essere lo stato (l'intero carrello, non solo aggiungo o tolgo un articolo)
                    - eventi con tutto (le informazioni vere) (vale la pena buttare tutto dentro che costa poco)
                    - eventi con ID (che il destinatario si recupera) (si puo fare bene)