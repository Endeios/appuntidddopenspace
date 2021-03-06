# Monolite e strangler

- e' che quando ho capito il pezzo che voglio sparare, lo circondo di funzionalita'
event driven, e rubo una funzionalita' alla volta.
    - 1 essere sicuri che stiamo separando roba che ha senso dal punto di vista del business
        - non e' che il problam e' "il socio che disturba?"
    - cosa ci fa paura, e ci impedisce di cambiare?
        - questo gia' permette di creare lo spazio per l'esperimento

- *Partiti da dove faceva piu' male* 
    - 1 con affiancamanto (mirrorning)
    - feature flag (strangler facade)
        - switcha tra nuovo servizio e vecchi pezzo del monolite
            - qui il servizio dice al monolite cosa fare (prima era il contrario)
    - switch da UI

- Se i vincoli non sono tecnologici, ma emotivi e non VOGLIONO essere fixati, e' lecito quittare. 
    - bisogna definire un perimetro dove uno PUOI lavorare. 

- Occhio ad avere un accesso parziale ai decisori: altrimenti ci sono dei vincoli
che non possono essere risolti dalla posizione parziale
    - vedi: Avere coda di paglia
    - vedi: non voler pestare la coda di paglia di altri (<- Bauno)
- Red carpeting con un consulente: questo puo farti svoltare il lavoro.
