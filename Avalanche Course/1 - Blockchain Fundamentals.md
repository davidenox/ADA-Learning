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

Una **firma digitale** è un meccanismo crittografico che garantisce l'autenticità, l'integrità ed il non ripudio di messaggi o transazioni digitali. Essa lega in modo univoco una transazione al suo originatore; a differenza delle firme fisiche, le firme digitali sono generate matematicamente e sono praticamente impossibili da falsificare.

Nei sistemi Blockchain, ogni transazione deve essere firmata dal mittente per dimostrare di aver autorizzato il trasferimento di *asset*. Questa firma fornisce:

- **Autenticazione**: conferma l'identità del mittente della transazione;
- **Integrità**: assicura che i dati delle transazioni non siano stati modificati
- **Non ripudio**: impedisce al mittente di negare di aver effettuato la transazione

Le firme digitali si basano sulla **crittografia asimmetrica**, che utilizza una coppia di chiavi matematicamente correlate:

1. **Private Key**: Chiave segreta conosciuta solo dal proprietario. Viene utilizzata per firmare le transazioni e *deve* essere mantenuta sicura.
2. **Public Key**: Chiave condivisa pubblicamente derivata dalla chiave privata. Chiunque può utilizzarla per verificare le firme create dalla chiave privata corrispondente. Funge da indirizzo o "identità" sulla blockchain.

I dati firmati con la chiave privata possono essere verificati utilizzando la chiave pubblica, ma essa non può derivare la chiave privata.

### Il processo di firma

Quando un utente vuole effettuare una transazione su una blockchain:

1. **Create Transaction**: L'utente crea una transazione specificando dettagli come l'indirizzo del destinatario e l'importo da trasferire.
2. **Sign Transaction**: Il software del portafoglio dell'utente utilizza la propria chiave privata per creare una firma digitale unica per questa transazione specifica. La firma viene generata applicando un algoritmo crittografico (ECDSA - Elliptic Curve Digital Signature Algorithm) ai dati della transazione e alla chiave privata.
3. **Trasmissione**: La transazione, assieme alla firma digitale ed alla chiave pubblica dell'utente, viene trasmessa alla rete.
4. **Verifica**: I nodi di rete ricevono la transazione ed utilizzano la chiave pubblica fornita per verificarne la firma. Questo conferma che:
	- L'operazione è stata firmata dal titolare della chiave privata corrispondente alla chiave pubblica
	- I dati delle transazioni non sono stati modificati da quando sono stati firmati
- **Accettare** o rifiutare: Se la firma è valida, la transazione è accettata per l'inclusione in un blocco, altrimenti, viene respinta.

## Perché le firme digitali?

Le firme digitali risolvono diversi problemi critici nei sistemi decentralizzati:

- **Proprietà ed Autorizzazione**: Nei sistemi tradizionali, una banca verifica la tua identità quando effettui una transazione. In una blockchain decentralizzata non esiste autorità centrale che verifica l'identità. Le firme digitali forniscono una prova matematica che la persona che avvia una transazione possiede l'account ed autorizza il trasferimento.
- **Rilevamento di manomissioni**: Se qualcuno cerca di modificare una transazione firmata, anche cambiando un singolo carattere, la firma viene invalidata. Questo rende immediatamente evidente che la transazione è stata manomessa.
- **Privacy con Responsabilità**: Le firme digitali ti permettono di dimostrare di possedere un account senza rivelare la tua chiave privata.
- **Verifica della fiducia**: Chiunque può verificare una firma utilizzando la chiave pubblica senza bisogno di affidarsi a terzi. Ciò consente la natura peer-to-peer e senza fiducia delle reti blockchain, in cui i partecipanti non hanno bisogno di conoscersi o fidarsi l'uno dell'altro per effettuare transazioni in modo sicuro.

## Schemi comuni di firme

Diverse blockchain utilizzano diversi algoritmi crittografici per le firme digitali:

- **ECDSA** (*Elliptic Curve Digital Signature Algorithm*): offre un elevato livello di sicurezza con chiavi di dimensioni relativamente ridotte, rendendolo efficiente per le applicazioni blockchain.
- **EdDSA** (*Edwards-curve Digital Signature Algorithm*): alternativa all'ECDSA, offre prestazioni e proprietà di sicurezza migliorate.
- **Firme BLS** (*Boneh-Lynn-Shacham*): forniscono aggregazioni di firme di piccole dimensioni per mantenere la sicurezza e risparmiare spazio quando sono necessarie più firme.
- **Firme Schnorr**: consentono casi d'uso più complessi come le transazioni multi-firma in modo più efficiente.
## Considerazioni sulla sicurezza

La sicurezza di una firma digitale dipende interamente dal tenere in sicurezza la Private Key:

- **Non condividere mai la tua Private Key**
- **Utilizza un archivio sicuro**
- **Esegui backup accurati e sicuri**
- **Fai attenzione al phishing**

Le firme digitali sono la pietra angolare della sicurezza delle blockchain, consentendo transazioni verificabili senza bisogno di fiducia in un ambiente decentralizzato.

# Ordine di transazione attraverso il consenso

In una rete Blockchain, migliaia di partecipanti possono inviare transazioni simultaneamente sa qualsiasi parte del mondo. Affinché il sistema funzioni correttamente, tutti i partecipanti devono concordare un unico ordine coerente di transazioni. Queusto accordo si ottiene attraverso **meccanismi** di **consenso**: i protocolli che consentono alle reti distribuite di coordinare e mantenere una visione unificata dello stato della blockchain.

*Scenario*:  Due persone che cercano di spendere gli stessi soldi allo stesso tempo, questo è chiamato un **problema di doppia spesa**. Nel settore bancario tradizionale, un server centrale elabora le transazioni uno per uno e garantisce che non puoi spendere lo stesso dollaro due volte. Ma in una blockchain decentralizzata, non c'è alcuna autorità centrale per determinare quale transazione è arrivata prima.

Esempio:

- Alice ha 10 gettoni nel suo account
- Lei crea due transazioni quasi contemporaneamente:
    - Transazione A: Invia 10 token a Bob
    - Transazione B: Invia 10 token a Charlie
- Entrambe le transazioni sono valide da sole, ma Alice non ha abbastanza token per soddisfare entrambi

La rete deve decidere prima quale transazione elaborare. Qualsiasi transazione sia ordinata per prima avrà successo, e la seconda sarà respinta come non valida (saldo insufficiente). Senza un meccanismo di consenso per stabilire un ordine definitivo, diversi nodi potrebbero elaborare queste transazioni in ordini diversi, portando a stati di registro incoerenti in tutta la rete.

## Consenso

Il **consenso** è il processo attraverso il quale i partecipanti alla rete distribuita concordano su un'unica ed autorevole versione della verità: *l'ordine e la validità delle transazioni*. Un **meccanismo di consenso** è l'insieme di regole e procedure che abilitano questo accordo.

Gli obiettivi fondamentali dei meccanismi di consenso sono:

- **Accordo**;
- **Validità**;
- **Risoluzione**;
- **Integrità**.

Diversi meccanismi di consenso utilizzano approcci dievrsi, ma generalmente seguono una linea guida, ovvero il **Processo di base**:

1. **Transaction Submission**: Gli utenti creano e trasmettono transazioni alla rete.
2. **Transaction Pool**: Ogni nodo mantiene un *pool*  di transazioni non confermate che ha ricevuto.
3. **Block Proposal**: I nodi specifici (miner, validatori o leader) sono selezionati o competono per proporre il blocco successivo delle transazioni.
4. **Block Validation**: Altri nodi verificano che il blocco proposto contenga transazioni valide in un ordine valido.
5. **Block Acceptance**: Attraverso il meccanismo di consenso, la rete si impegna ad accettare o rifiutare il blocco proposto
6. **Blockchain Extension**: Una volta accettato, il blocco viene aggiunto alla blockchain ed il suo ordine di transazione diventa permanente.
7. **Aggiornamento di stato**: Tutti i nodi aggiornano la loro copia locale dello stato blockchain in base alle transazioni appena confermate.

