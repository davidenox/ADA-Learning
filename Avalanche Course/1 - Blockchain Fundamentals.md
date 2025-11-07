 # Blockchain

È importante introdurre il concetto di blockchain ad alto livello.
- Computer Decentralizzati;
- Applicazioni decentralizzate;
- Casi d'uso.

## Computer Decentralizzati

>[!important] Blockchain può essere pensato come un *nuovo* tipo di computer, il cui vantaggio chiave è la **decentralizzazione** - nessuna singola entità ha il controllo sull'intero sistema.

Il controllo viene distribuito tra molti partecipanti, favorendo trasparenza e sicurezza, poiché tutte le transazioni sono verificate dal consenso e registrate su un registro immutabile. 

Tuttavia, questa tecnica ammette dei compromessi: le blockchain sono *meno efficienti* rispetto ai sistemi tradizionali. Questo rende la blockchain ideale per determinati casi d'uso ( transazioni finanziarie sicure ) e meno adatta per attività che richiedono alta velocità ed efficienza.

## Applicazioni decentralizzate

>[!important] Le **dApp** sono programmi eseguiti su una blockchain. Un **contratto intelligente** è un programma di auto-esecuzione con i termini dell'accordo direttamente scritto nel codice, operando senza la necessità di un'autorità centrale di fiducia.

Le dApp sono più complesse e spesso costituite da più contratti intelligenti, che insieme offrono un'esperienza applicativa completa sulla blockchain. Questi programmi possono eseguire una vasta gamma di attività, dalla gestione delle risorse digitali all'esecuzione di protocolli di finanza decentralizzata (*DeFi*).

Questa *interoperabilità* consente agli utenti di beneficiare dei punti di forza di ogni piattaforma, combinando la facilità d'uso delle app mobile alla potenza di elaborazione dei server web e alla sicurezza e trasparenza della tecnologia blockchain.

## Casi d'uso

Le blockchain hanno proprietà uniche che le rendono eccellenti per determinati casi d'uso in cui la sicurezza, la trasparenza e la decentralizzazione sono fondamentali:

- **Finanza**: Le blockchain consentono transazioni trasparenti e sicure senza necessità di intermediari. Si tratta del fondamento delle criptovalute e delle piattaforme finanziarie decentralizzate. Le transazioni finanziarie sono a prova di manomissione e possono essere controllate in qualsiasi momento;
- **Gestione della supply chain**: La blockchain può fornire una registrazione immutabile del viaggio di un prodotto dall'origine al consumatore, aumentando la trasparenza e riducendo le frodi. Questo aiuta a garantire che ogni fase della catena di fornitura sia accuratamente monitorata e verificata;
- **Sistemi di voto**: Le caratteristiche della blockchain assicurano che i voti siano conteggiati con precisione e che non possano essere modificati, garantendo l'integrità democratica.

### Aspetti negativi

>[!warning] Le blockchain sono intrinsecamente meno efficienti rispetto ai database tradizionali, poiché richiedono consenso tra i nodi distribuiti, che possono rallentare la velocità delle transazioni e aumentare la complessità delle operazioni. 

Inoltre, la complessità di sviluppo e di mantenimento delle blockchain diventa una limitazione.
Blockchain è adatto per le applicazioni in cui la fiducia tra le parti è uno dei requisiti fondamentali e dove un record immutabile di transazioni è essenziale. Tuttavia, se la tua applicazione richiede un elevato throughput, un'elaborazione in tempo reale o la semplicità, un sistema centralizzato tradizionale potrebbe essere più appropriato. 

In breve, la blockchain è un *potente* strumento per le situazioni giuste, ma il suo utilizzo dovrebbe essere attentamente considerato rispetto alle esigenze specifiche della tua applicazione.

# Pagamenti

Questo capitolo approfondisce i saldi dei conti, le transazioni e le interazioni con gli utenti.

## Caso d'uso dei pagamenti

| Caso d'uso              | Strutture di dati | Interazioni utente               |
| ----------------------- | ----------------- | -------------------------------- |
| Pagamenti               | Saldi dei conti   | Fondi di trasferimento           |
| Finanza Decentralizzata | Prestiti,...      | Prendi in prestito, rimborsa, .. |
| Sistemi di voto         | Voti              | Voto                             |
| Supply Chain            | Spedizioni        | Consegna, Consegna               |
| Gestione dell'identità  | Certificati       | Problema, Prova                  |
## Saldi & trasferimenti del conto

### Saldi del conto

I **saldi del conto** si riferiscono alla *quantità corrente di denaro* o attività detenute in un conto specifico in un dato momento. Questo numero riflette il valore totale che tutti i crediti (+) e gli addebiti (-) sono stati contabilizzati, indicando quanto il titolare del conto ha a disposizione per uso o prelievo.

### Trasferimento

Un **trasferimento** è il processo di spostamento di denaro o beni da un conto all'altro. Questo tipo di operazione garantisce che il valore totale in tutti i conti rimanga costante, mantenendo l'integrità del sistema finanziario complessivo

#### Trasferimento non valido

Un **trasferimento non valido** si verifica quando una richiesta di transazione supera il saldo disponibile nel conto di invio. In questi casi, il trasferimento non può essere eseguito.
Questa salvaguardia garantisce che i conti non cadano inavvertitamente in saldi negativi e mantiene un monitoraggio finanziario accurato ed affidabile.

## Registro - Ledger

>[!important] Un **registro** è un sistema di registrazione completo che documenta *tutte* le transazioni. Mantiene un elenco dettagliato e cronologico delle transazioni, catturando ogni trasferimento tra account. 

Ciò garantisce che ogni azione sia tracciata e tracciabile con precisione, fornendo una visione chiara e completa dell'attività del sistema.

### Append-Only

Un **registro Solo Append** (Append-Only Ledger) opera aggingendo nuove transazioni alla fine del record senza modificare eventuali voci precedenti. Quindi, mentra il registro cresce con ogni nuova transazione, le transazioni passate rimangono invariate e preservate. 

Le transazioni non valide, che non riescono a eseguire a causa di problemi come fondi insufficienti, sono ancora registrate nel registro per mantenere una storia completa. Per invertire gli effetti di una transazione, è necessario aggiungere una nuova transazione che contrasti la precedente, garantendo l’integrità e la coerenza dello stato complessivo del Ledger.

# Firme

>[!important] Le firme digitali sono una componente fondamentale della tecnologia blockchain:  forniscono le basi crittografiche per transazioni sicure, autentiche e a prova di manomissione.

Come fanno le firme scritte a mano, le firme digitali consentono agli utenti di dimostrare la propria identità, autorizzare transazioni o attestare eventi.

## Firme digitali

Una **firma digitale** è un meccanismo crittografico che garantisce l'autenticità, l'integrità ed il non ripudio di messaggi o transazioni digitali.

****
work in progress
****