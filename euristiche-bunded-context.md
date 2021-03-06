# Euristiche per spaccare i bounded context
- Follow behaviour, not data:
    - Il dato , la descrizione, e' dappertutto, quello che aiuta
    e' cosa stiamo facendo con questo dato: l'operazione
    prima dell'operando
    - come mi aiuta a capire che sono in un diverso bounded context?
        - lo ZB si immagina delle board di ES (does ZB dreams of ES?)
        - quando uno capisce che stai cambiano il linguaggio con cui operi sul dato
        allora sai che hai cambiato bounded context.
    - same name, different concept:
    - evitare il BillingCustomer, il DeliveryCustomer, se siamo in due contesti diversi

- Dipartimenti aziendali:
    - L'ultima cena: le persone, come in una cena, si dispongono tra colleghi, e si capisce
    anche chi e' giuda
    - E' un indicatore, ma puo essere che un ufficio si occupi di piu' cose
        - EG: planning / execution
        - EG: magari non tutto quello che il manager ha sotto e' un BC: 
            - esempio anagrafe/stato civile
    - David West: object thinking
    - Dipende da quanto e' grande un'azienda
        - aziede con dimensione malsana
        - aziede con dimensione sana

- Puo essere che i bounded context non sono "GIUSTI" ma sono, adatti o seguaono delle ottimizzazioni esplicitate.

- I Bounded context non sono spiegati benissimo nel libro blu. C'e' il pericolo che siano un po' base,
meglio chidere e andare in comunita ( esempio larghezza di banda)

- Spazio di applicabilita' di un modello.

- Mescolare e' piu' semplice di separare (costa meno) 