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
                - no aggregazioni o elaborazioni o edit
                - nell'evento ci deve essere lo stato (l'intero carrello, non solo aggiungo o tolgo un articolo)
                    - eventi con tutto (le informazioni vere) (vale la pena buttare tutto dentro che costa poco)
                    - eventi con ID (che il destinatario si recupera) (si puo fare bene)

- come si distingue quando l'evento e' dentro o fuori?
- facciamo che c'e' un' anagrafica.
    - bounded context con tutta l'anagrafica
        - quando aggiorno l'indirzzo di spedizione, e' facile pensare che gente e; interessata
    - Appendice A: come faccio sapere dire che quando dico cliente si intende lo stesso?
        - si parla di shared library comuni a tutti
        - si wrappano gli oggetti perche calistenics
    - un conto sono le entity e un conto e'e quello che scrivo nel db
    - nel DDD siamo sempre indipendenti dalla persistenza
    
- ( Naming evento )
    - no {X} cambi-indirizzo
    - si {/} cambi-indirzzo-per-nuova-sede

https://leanpub.com/agiletechnicalpracticesdistilled