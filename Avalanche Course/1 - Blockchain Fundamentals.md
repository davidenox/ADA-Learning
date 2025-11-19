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

### Consenso Vs Ordine di transazione

- **Meccanismo di consenso**: Protocollo complessiva che abilita l'accordo distribuito
- **Ordine di Transazione**: Risultato specifico ottenuto dal consenso, determina l'ordine in cui vengono eseguite le transazioni.
Il meccanismo di consenso è lo strumento, e l'ordine di transazione è uno degli obiettivi primari che esso raggiunge. 
I meccanismi di consenso riescono anche a:
- Determinare chi può aggiungere nuovi blocchi alla catena;
- Impedire ad attori maligni di riscrivere la storia;
- Assicurarsi che la rete rimanga operativa anche quando alcuni nodi falliscono o agiscono in modo errato;
- Distribuire il potere decisionale attraverso la rete.

#### Il consenso decentralizzato è impegnativo

Raggiungere il consenso in una rete decentralizzata è difficile poiché:

1. **Nessuna autorità centrale** fidato per prendere decisioni definitive;
2. **Ritardi di rete** derivati dal tempo tecnico di trasmettere informazioni, potrebbero far vedere ai nodi le transazioni in ordini diversi;
3. **Attori malevoli** possono essere dannosi e cercare di interrompere il consenso o manipolare l'ordine di transazione per il loro beneficio;
4. **Asincronia**, per la quale la rete non opera in perfetta sincronizzazione

## Consenso a catena lunga

La **Longest Chain Rule** (*regola*) è un principio fondamentale utilizzato in molte reti blockchain per risolvere i conflitti e mantenere un unico Ledger unificato. È il meccanismo che assicura che tutti i nodi alla fine siano d'accordo su quale versione della blockchain è quella "corretta", sia che la rete utilizzi PoW, PoS o altri meccanismi.

### Catene Concorrenti

In una rete distribuita in cui più produttori di blocchi lavorano contemporaneamente, è possibile per due validatori proporre blocchi validi quasi allo stesso tempo. Quando questo accade:

- Entrambi i validatori trasmettono i loro blocchi alla rete;
- Nodi diversi potrebbero ricevere prima blocchi diversi;
- La blockchain esegue una "fork" temporaneamente in due versioni concorrenti;
- Ogni versione è valida da sola, ma la rete deve sceglierne una.

Senza una regola chiara per risolvere la situazione, la rete potrebbe dividersi in modo permanente in diverse catene, distruggendo il consenso che rende la blockchain preziosa.

>[!important] Longest Chain Rule
>Quando esistono più versioni valide della blockchain, i nodi dovrebbero accettare la catena con il peso accumulato maggiore come catena autorevole.

"Più lungo" non significa necessariamente il maggior numero di blocchi, significa che la catena rappresenta il maggior peso cumulativo secondo le regole del protocollo. La metrica di peso specifica varia in base al meccanismo di consenso, ma il principio rimane lo stesso.

### Funzionamento

**Fase 1: La fork**

1. Il blocco 100 è l'ultimo blocco confermato
2. Validator A propone Block101A nello stesso momento in cui Validator B propone Block101B
3. Entrambi i blocchi sono validi e correttamente riferiti al blocco 100
4. A trasmette 101A, B trasmette 101B
5. I nodi più vicin ad A aggiungono 101A alla loro catena, i nodi più vicini a B aggiungono 101B
6. La rete ora ha *due catene concorrenti*.

**Fase 2: La gara**

Entrambe le catene continuano:

- Alcuni validatori si basano sulla parte superiore del blocco 101A, altri sul 101B
- Ogni catena cresce in modo indipendente
- Nessuna delle due è "sbagliata", secondo le regole del protocollo sono entrambe valide.

**Fase 3: Risoluzione**

Alla fine:

- Un validatore basato sul blocco 101A propone il blocco 102A.
- Ora la catena che termina con il blocco 102A è più lunga (ha un peso cumulativo maggiore).
- I nodi che seguono la catena 101B vedono la catena più lunga
- In base alla regola della catena più lunga, passano alla catena più lunga
- Il blocco 101B è “orfano”: è valido ma non fa più parte della catena principale
- Le transazioni nel blocco 101B tornano al mempool per essere incluse nei blocchi futuri

**Fase 4: Convergenza**

- Tutti i nodi ora concordano sulla catena $100\rightarrow101A\rightarrow102A$.
- La rete si ri-converge su una singola versione
- L'operazione normale continua.

#### Perché funziona

- Presupposto di maggioranza **onesta**;
- Meccanismo di **auto-rinforzo**;
- **Incentivi economici**.

### Implicazioni per la finalità delle transazioni

#### Conferme

Il *conteggio* delle **conferme** di una transazione è il numero di blocchi aggiunti dopo il blocco contenente la transazione:

- **0 Conferme**: La transazione è nel `mempool` ma non ancora in un blocco ( *non confermata* )
- **1 Conferma**: La transazione è nell'ultimo blocco
- **2 Conferme**: Un blocco è stato aggiunto dopo il ramo contenente la transazione
- **Conferme multiple**: Più conferme si ottengono più è sicura la transazione

Più conferme ha una transazione, più è profonda nella blockchain:

- Per invertire una transazione con 1 conferma, un utente malintenzionato deve produrre 2 blocchi più velocemente della rete onesta
- Per invertire una transazione con 6 conferme, un utente malintenzionato deve produrre 7 blocchi più velocemente della rete onesta
- Questo diventa *esponenzialmente* più difficile con ogni conferma aggiuntiva

**Finalità** probabilistica: Nei sistemi che utilizzano la regola della catena più lunga, la finalità non è mai assoluta al 100%: c'è sempre una possibilità teorica di inversione. Tuttavia, questa probabilità diventa trascurabilmente piccola dopo diverse conferme.

### Quando la LCR può essere attaccata

Se un utente malintenzionato controlla più del 50% della potenza di convalida della rete:

1. **Possono creare una catena privata:** produrre blocchi in segreto senza trasmetterli
2. **Superare la** catena **onesta:** poiché controllano la maggioranza, la loro catena segreta cresce più velocemente
3. **Rilasciare la catena più** lunga: trasmettere improvvisamente la loro catena, che ora è più lunga
4. **Interruttori di rete** : i nodi seguono la regola della catena più lunga e passano alla versione dell'attaccante
5. **Transazioni invertite** : le transazioni nella catena onesta sono invertite

*Perché Questo Raramente Accade* :

- L'acquisizione del 51% della potenza di convalida è *estremamente costoso* (miliardi di dollari per le principali reti)
- L'attacco avrebbe sbalzato il valore della criptovaluta, *distruggendo l'investimento* dell'aggressore
- L'attacco è *rilevabile* e la comunità può rispondere (fork a una nuova catena, cambiare algoritmo di consenso).

### Reorgs profondi

Una **profonda riorganizzazione** (reorg) si verifica quando una catena lunga viene sostituita da una catena ancora più lunga:

- **Reorgs poco profonde** (1-2 blocchi): comune e atteso, avvengono naturalmente a causa dei ritardi della rete
- **Reorgs profondi** (6+ blocchi): estremamente raro e di solito indicano un attacco o un problema di rete principale
- **Protezione** : L'attesa di ulteriori conferme protegge da tutti gli aggressori tranne quelli più dotati di risorse

## Takeaway chiave

- La regola della catena più lunga risolve le fork temporanee facendo accettare ai nodi la catena con il peso più accumulato
- Assicura che la rete confluisca su un'unica versione coerente della cronologia delle transazioni
- La finalità delle transazioni è *probabilistica*: più conferme significano una sicurezza esponenzialmente più elevata
- La regola funziona perché i validatori onesti controllano la maggior parte del potere di convalida e hanno incentivi per seguirlo
- Gli attacchi del 51% sono teoricamente possibili ma economicamente impraticabili per le grandi reti decentralizzate

>[!important] La regola della catena più lunga è una pietra angolare di molti meccanismi di consenso blockchain, trasformando un sistema distribuito caotico in un Ledger ordinato e sincronizzato di cui tutti i partecipanti possono fidarsi. 
>È una soluzione meravigliosamente semplice a un problema complesso: lasciare che la rete raggiunga un accordo attraverso una metrica chiara e oggettiva piuttosto che richiedere un coordinamento esplicito.

## Ciclo di vita delle transazioni

Comprendere il ciclo di vita completo di una transazione blockchain aiuta a capire come i sistemi decentralizzati elaborano i pagamenti e mantengono la sicurezza.

### Creazione

Una transazione inizia quando un utente decide di trasferire le risorse. Ciò comporta la specificazione di diverse info chiave:

- **Indirizzo del mittente** derivato dalla chiave pubblica del mittente
- **Indirizzo del destinatario** dove verranno inviati i beni
- **Importo** in criptovaluta o token
- **Commissione di transazione** offerto a miner/validator per includere la transazione in un blocco
- **Nonce** numero di sequenza che impedisce l'elaborazione multipla della stessa transazione
- **Dati aggiuntivi** quali campi opzionali per interazioni o note di smart contract

### Firma

Una volta creata la transazione, deve essere firmata crittograficamente per dimostrare l'autorizzazione:

**Il processo di firma** :

1. I dati della transazione vengono disattivati per creare un'impronta digitale unica della transazione
2. Questo hash è crittografato utilizzando la **chiave privata** del mittente, creando una firma digitale
3. La firma è allegata alla transazione insieme alla chiave pubblica del mittente
4. Il pacchetto combinato (transazione + firma + chiave pubblica) è ora pronto per la trasmissione

### Trasmissione

Dopo la firma, la transazione viene trasmessa alla rete peer-to-peer:

**Come funziona la radiodiffusione** :

1. Il portafoglio invia la transazione firmata a uno o più nodi a cui è collegato
2. Ogni nodo che riceve la transazione esegue la convalida di base
3. Se valido, il nodo inoltra la transazione ai suoi peer node
4. Questo processo continua fino a quando la transazione si propaga in tutta la rete
5. In pochi secondi, la maggior parte dei nodi ha ricevuto la transazione

**Topologia di rete** : Le reti blockchain utilizzano un protocollo di **gossip peer-to-peer** (*P2P*) in cui ogni nodo si collega a più altri nodi. Quando un nodo riceve una nuova transazione, la condivide con i suoi vicini, che la condividono con i loro vicini, creando una propagazione esponenziale.

**Cosa ottiene la trasmissione** :

- I dati completi delle transazioni
- La firma digitale
- La chiave pubblica del mittente

### Verifica

Prima di accettare una transazione, i nodi eseguono più controlli:

**Controlli di convalida** :

1. **Verifica della firma** :
	
    - Utilizzare la chiave pubblica fornita per verificare la firma
    - Conferma che la transazione è stata firmata dal proprietario dell'indirizzo del mittente
    - Rifiutare se la firma non è valida o non corrisponde alla chiave pubblica
	
2. **Controllo dell'equilibrio** :
    
    - Interroga lo stato blockchain attuale per controllare l'equilibrio del mittente
    - Assicurarsi che il mittente abbia abbastanza attività per coprire sia l'importo del trasferimento che la commissione di transazione
    - Rifiutare se insufficiente equilibrio
	
3. **Nonce Verification** (sistemi basati su account):
    
    - Verificare che la transazione nonce corrisponda al numero di sequenza previsto
    - Impedisce gli attacchi di replay e garantisce che le transazioni vengano elaborate in ordine
    - Rifiutare se nonce non è corretto
	
4. **Convalida del formato** :
    
    - Verificare la transazione segue la corretta struttura dei dati
    - Verifica che gli indirizzi siano validi
    - Assicurarsi che la transazione non sia malformata
	
5. **Prevenzione a doppia spesa** :
    
    - Verificare che lo stesso input non sia già stato speso in un'altra transazione (sistemi UTXO come Bitcoin)
    - Confronta con le transazioni pendenti nel mempool

**Validazione a due fasi** :

- **Validazione rapida:** i nodi fanno controlli leggeri quando ricevono una transazione tramite trasmissione
- **Validazione completa** : i minatori/convalidatori effettuano controlli completi prima di includerlo in un blocco

**Cosa succede se la verifica Fallisce** :

- Il nodo rifiuta la transazione e non la inoltra ai pari
- La transazione muore e non entra nel mempool
- Il portafoglio del mittente potrebbe ricevere un messaggio di errore
- Il mittente deve risolvere il problema e creare una nuova transazione

### Mempool

Dopo la verifica, le transazioni valide attendono in un'area di detenzione temporanea:

**Che cosa è il Mempool** :

- Abbreviazione di *memory pool* - una raccolta di transazioni non confermate memorizzate nella RAM di ogni nodo
- Ogni nodo mantiene il proprio mempool (potrebbe differire leggermente a causa dei tempi di propagazione della rete)
- Le transazioni attendono qui fino a quando un minatore o un validatore le include in un blocco

**Ordine di transazione in Mempool** : Le transazioni sono tipicamente prioritarie:

- **Livello di commissione** : le tariffe più elevate hanno la priorità (particolarmente importante durante la congestione della rete)
- **Tempo ricevuto** : Le transazioni più vecchie possono ottenere la preferenza tra le transazioni con la stessa commissione
- **Dipendenze** : Alcune transazioni devono attendere che altre siano confermate prima

**Dinamica di Mempool** :

- Le dimensioni fluttuano in base all'attività di rete
- Durante l'alta congestione, i mempool crescono transazioni grandi e a basso costo possono attendere ore o giorni
- Le transazioni possono essere sfrattate se il mempool diventa troppo pieno (le transazioni a commissione più bassa vengono rimosse prima)
- Gli utenti possono spesso sostituire le transazioni in sospeso ripresentando commissioni più elevate (Sostituisci-per-Commissione)

## Finalizzazione

La fase finale è quando la transazione diventa permanentemente parte della blockchain:

**Conteggio di conferma** :

- **1 conferma** : la transazione è nel blocco più recente
- **2 conferme** : Un blocco aggiuntivo è stato aggiunto dopo il blocco contenente la transazione
- **6 conferme** : Sei blocchi di profondità (generalmente considerati sicuri in Bitcoin)
- **12+ conferme** : Molto sicuro, inversione estremamente improbabile

**Perché le conferme multiple** contano:

- Più una transazione è più profonda nella blockchain, più è difficile invertire
- Per invertire una transazione con 6 conferme, un utente malintenzionato dovrebbe ricordare 6 blocchi più velocemente della rete onesta
- Questo diventa esponenzialmente più difficile e costoso con ogni conferma

**Tipi di finalità** :

- **Finalità probabilistica** (PoW, sistemi a catena più lunga):
    
    - Mai 100% finale, ma probabilità di inversione si avvicina zero
    - Ogni blocco aggiuntivo rende più difficile l'inversione in modo esponenziale
    - Standard in Bitcoin, Ethereum (pre-merge) e sistemi simili
	
- **Finalità assoluta** (Alcuni sistemi PoS):
    
    - Una volta finalizzate, le transazioni sono matematicamente impossibili da invertire
    - Utilizzato in sistemi con gadget di finalità o consenso BFT
    - Fornisce una più rapida certezza economica, ma può sacrificare un certo decentramento

**Aggiornamento dello Stato** : Una volta confermati, gli effetti della transazione si riflettono nello stato blockchain:

- Il saldo del mittente diminuisce dell'importo più la commissione
- Il saldo del destinatario aumenta dell'importo
- Il nonce viene incrementato
- Lo stato del contratto intelligente può essere aggiornato (se applicabile)

### Riepilogo

```pseudo
1. CREATION
   User creates transaction
   ↓
2. SIGNING
   Wallet signs with private key
   ↓
3. BROADCASTING
   Propagates across P2P network
   ↓
4. VERIFICATION
   Nodes validate signature, balance, format
   ↓
5. MEMPOOL
   Waits in memory pool
   ↓
6. CONSENSUS
   Included in block by validator
   ↓
7. FINALIZATION
   Gains confirmations, becomes irreversible
```

# Protezione dalla Sybil

>[!info] Attacco Sybil
>Come impedire ad un singolo attore malevolo di creare migliaia di identità false per manipolare un sistema?

Un attacco **Sybil** si verifica quando una singola entità crea molteplici identità false (nodi sybil) per ottenere un'influenza o un controllo sproporzionato su una rete.

In una rete decentralizata il potere decisionale dovrebbe essere distribuito tra molti partecipanti indipendenti. Ma se un'entità può impersonificare il maggior numero di partecipanti, può:

1. **Manipolare il consenso** : controllare quali transazioni sono incluse nei blocchi o influenzare l'ordine delle transazioni
2. **Lanciare 51% Attacchi** : Ottieni il controllo della maggioranza per riscrivere la storia
3. **Censurare le transazioni** : impedire l'elaborazione di utenti specifici o tipi di transazioni
4. **Corrompere i voti** : Nei sistemi di governance, votare più volte sulle modifiche del protocollo
5. **Drenare risorse** : Riempire di Spam la rete o monopolizzare le risorse scarse

Il problema fondamentale è che in una rete veramente aperta e senza permesso, la creazione di una nuova identità è essenzialmente gratuita: puoi generare una nuova coppia di chiavi pubbliche / private istantaneamente senza alcun costo.

## Meccanismi di difesa

Si tratta di strategie progettare per rendere estremamente costoso o impraticabile per un attaccante creare identità multiple.

### Costo di creazione di un'identità

L'approccio comune è quello di *attribuire un costo reale* a ciascuna identità o voto nel sistema, per il quale se creare ogni identità richiede una spesa, un attaccante non può creare identità illimitate senza disporre di risorse illimitate.

## Consenso vs. Sybil Defense

È fondamentale porre una distinzione di questi due obiettivi della blockchain, i quali sono spesso confusi perché gli stessi meccanismi servono ad entrambi gli scopi:

- La domanda a cui rispondono i meccanismi di consenso è : "*Qual è lo stato corretto della blockchain su cui siamo tutti d'accordo?*"
- La domanda a cui rispondono i meccanismi di difesa dalla Sybil è : "*Come facciamo a garantire che ogni identità nella rete rappresenti un'entità veramente indipendente?*"

## Esempio: Bitcoin

Bitcoin utilizza la Proof of Work (*PoW*):
**Ruolo del consenso**:

- I miner competono per trovare blocchi validi;
- La rete segue la catena più lunga valida;
- Questo assicura che tutti i nodi siano d'accordo sulla cronologia delle transazioni.

**Ruolo della Sybil Defense**:

- Creare 100 identità false di miner non ti avvantaggia;
- Ciò che conta è il potere computazionale, non il numero di identità;
- Per controllare la rete è necessario il 51% del tasso di hash totale (potenza di calcolo), che richiede un massiccio investimento in hardware ed elettricità;
- Questo rende gli attacchi Sybil proibitivamente costosi.

# Smart Contract

I **Contratti Intelligenti** sono programmi di autoesecuzione che funzionano con la blockchain, applicando automaticamente accordi senza intermediari.

Nello specifico, uno Smart Contract è un programma memorizzato su una blockchain che viene eseguito automaticamente qunado vengono soddisfatte delle condizioni predeterminate, come se fosse un accordo digitale scritto in codice, in cui la blockchain applica automaticamente i termini senza richiedere fiducia in nessuna persona o istituzione.

I contratti intelligenti sono distribuiti su piattaforme blockchain che supportano la logica programmabile, con Ethereum (ETH) che è l'esempio più noto e Avalanche (AVAX) quello preso in esame.

## Processo di base

1. **Scrittura del Codice** : Uno sviluppatore scrive uno smart contract in un linguaggio di programmazione. Il contratto definisce:
    
    - Le condizioni che devono essere soddisfatte;
    - Le azioni da intraprendere quando le condizioni sono soddisfatte;
    - I dati che il contratto memorizza e gestisce.
	
2. **Distribuzione** sulla Blockchain: il contratto compilato viene distribuito alla blockchain inviando una transazione speciale. Una volta schierato:
    
    - Il contratto ottiene un indirizzo univoco sulla blockchain;
    - Il codice diventa permanente e immutabile;
    - Chiunque può interagire con il contratto al suo indirizzo.
	
3. **Interazione con il Contratto** : Gli utenti inviano transazioni all'indirizzo del contratto per:
    
    - Richiamare le funzioni definite nel contratto;
    - Inviare criptovaluta o token al contratto;
    - Leggere i dati memorizzati nel contratto;
    - Attivare i comportamenti automatici del contratto.
	
4. **Esecuzione automatica:** quando qualcuno interagisce con il contratto:
    
    - Ogni nodo della rete esegue il codice del contratto;
    - La logica del contratto determina ciò che accade (trasferimento di fondi, aggiornamento di dati, ecc.)
    - Tutti i nodi raggiungono il consenso sull'esito;
    - La blockchain registra i cambiamenti dello stato.

### Caratteristiche chiave

- **Deterministico**: Dati gli stessi input e lo stato blockchain, il contratto produce sempre gli stessi output. Non c'è casualità o influenza esterna.
- **Autonomo** : Una volta rilasciato, il contratto funziona esattamente come programmato senza l'intervento umano. Nessuno può fermarlo o cambiare il modo in cui si comporta.
- **Trasparente** : Il codice del contratto e il suo stato attuale sono visibili a tutti sulla blockchain. Chiunque può verificare ciò che fa e verificarne il comportamento.
- **Immutabile**: Dopo la distribuzione, il codice del contratto non può essere modificato. Questo assicura che le regole non possono essere alterate dopo che le persone iniziano a usarlo.
- **Trustless** : Gli utenti non hanno bisogno di fidarsi del creatore del contratto o di terze parti: devono solo fidarsi del fatto che il codice fa quello che dice (che possono verificare) e che la blockchain lo eseguirà correttamente.

## Applicazioni del mondo reale

I contratti intelligenti consentono un vasto ecosistema di applicazioni decentralizzate (dApp) in molti domini:

### Finanza Decentralizzata (DeFi)

DeFi utilizza contratti intelligenti per ricreare i servizi finanziari tradizionali senza banche o broker:

- **Protocolli di prestito** : prestare automaticamente criptovaluta e calcola l'interesse in tempo reale.
- **Scambi decentralizzati** : scambiare token direttamente con altri senza uno scambio centralizzato.
- **Stablecoin** : Mantenere valori di criptovaluta stabili attraverso algoritmi per contratti intelligenti.
- **Agricoltura di rendimento** : ottimizzare automaticamente i rendimenti su più piattaforme.

### Token non fungibili (NFT)

I contratti intelligenti alimentano la creazione, la proprietà e il trading di risorse digitali uniche:

- Dimostra la proprietà di arte digitale, oggetti da collezione o oggetti virtuali
- Paga automaticamente le royalties ai creatori sulle vendite secondarie
- Consente la proprietà frazionaria di attività di alto valore

### Gestione della supply chain

Tracciare le merci mentre si muovono attraverso catene di approvvigionamento complesse:

- Registrare automaticamente ogni passaggio del percorso di un prodotto
- Verificare l'autenticità e prevenire le contraffazioni
- Attivare automaticamente i pagamenti

### Organizzazioni Autonome Decentralizzate (DAO)

Organizzazioni governate interamente da smart contract:

- I membri votano le proposte utilizzando i token
- Le proposte approvate vengono eseguite automaticamente
- I fondi del Tesoro sono gestiti in modo trasparente per codice

### Giochi e mondi virtuali

Abilita la vera proprietà e l'interoperabilità degli elementi digitali:

- I giocatori possiedono veramente i loro oggetti di gioco come gettoni
- Gli oggetti possono essere scambiati o utilizzati in diversi giochi
- Le economie di gioco funzionano con contratti intelligenti trasparenti e automatizzati

### Assicurazione

Automatizza l'elaborazione dei reclami e i pagamenti:

- Assicurazione parametrica che paga automaticamente in base ai dati (ad esempio, i dati meteo per l'assicurazione delle colture)
- Nessun operatore di reclami necessari per i casi semplici
- Pagamenti più veloci con spese generali più basse

## Esempio: Token Swap

**Scenario** : Alice ha 100 AVAX e vuole scambiarlo per i 2.000 USDC di Bob. Nessuna delle due parti si fida dell'altra.

**Soluzione tradizionale** : utilizzare uno scambio centralizzato per facilitare il commercio. Entrambe le parti devono fidarsi dello scambio per gestire i loro fondi onestamente e non congelare i conti.

**Soluzione Smart Contract** :

``` solidity
contract TokenSwap {
    address public alice;
    address public bob;
    uint256 public avaxAmount;
    uint256 public usdcAmount;
    bool public aliceDeposited;
    bool public bobDeposited;
    uint256 public deadline;
    
    IERC20 public usdcToken;
    
    // Alice creates the swap offer
    constructor(address _bob, uint256 _usdcAmount, address _usdcToken) payable {
        alice = msg.sender;
        bob = _bob;
        avaxAmount = msg.value;  // Alice deposits AVAX
        usdcAmount = _usdcAmount;
        usdcToken = IERC20(_usdcToken);
        aliceDeposited = true;
        deadline = block.timestamp + 1 hours;  // 1 hour to complete
    }
    
    // Bob deposits his USDC to complete the swap
    function depositUSDC() public {
        require(msg.sender == bob, "Only Bob can deposit");
        require(block.timestamp < deadline, "Swap expired");
        
        usdcToken.transferFrom(bob, address(this), usdcAmount);
        bobDeposited = true;
        
        // Automatically execute the swap
        executeSwap();
    }
    
    // Execute the swap once both have deposited
    function executeSwap() private {
        require(aliceDeposited && bobDeposited, "Both must deposit");
        
        // Send AVAX to Bob
        payable(bob).transfer(avaxAmount);
        
        // Send USDC to Alice
        usdcToken.transfer(alice, usdcAmount);
    }
    
    // If Bob doesn't deposit before deadline, Alice gets her AVAX back
    function refund() public {
        require(block.timestamp >= deadline, "Deadline not reached");
        require(!bobDeposited, "Swap already completed");
        
        payable(alice).transfer(avaxAmount);
    }
}
```

**Come Funziona** :

1. Alice crea il contratto di swap, specificando l'indirizzo di Bob e la quantità di USDC che vuole
2. Alice invia 100 AVAX al contratto quando lo crea
3. Bob ha 1 ora per depositare 2.000 USDC nel contratto
4. **Se Bob deposita** : Il contratto scambia automaticamente—Bob ottiene l'AVAX, Alice ottiene l'USDC
5. **Se Bob non deposita** : dopo la scadenza, Alice può chiamare `refund()`per riavere il suo AVAX

Questo è veramente senza fiducia! Né Alice né Bob possono imbrogliare perché:

- Alice non può riprendersi il suo AVAX una volta che Bob deposita (lo swap viene eseguito automaticamente)
- Bob non può prendere l'AVAX senza depositare il suo USDC
- Se Bob non partecipa, Alice riave indietro i suoi fondi
- Nessun scambio centralizzato può congelare, confiscare o abusare dei fondi, sono solo messi su un contratto che non può fare altro che eseguire lo swap con loro.
- Lo scambio è atomico: o entrambe le parti si verificano, o non accade

## Sfide e limitazioni

Sebbene potenti, gli smart contract devono affrontare diverse sfide.
### Vulnerabilità di sicurezza

**Il problema**: i bug nel codice degli smart contract possono essere sfruttati. Poiché i contratti sono immutabili, i bug non possono essere corretti dopo l'implementazione.

*Esempio famoso*: l'hacking di DAO nel 2016 ha portato al furto di 50 milioni di dollari a causa di una vulnerabilità di rientranza.

**Soluzione**: test rigorosi, audit professionali, verifiche formali e modelli di codifica sicuri.

### Problema Oracoli

**Il problema**: gli smart contract non possono accedere autonomamente a dati esterni (meteo, quotazioni di borsa, risultati sportivi). Hanno bisogno di “oracoli” che forniscano loro informazioni sul mondo reale.

*Sfida*: gli oracoli reintroducono nel sistema la fiducia e potenziali punti di fallimento.

**Soluzione**: reti Oracle decentralizzate che aggregano dati provenienti da più fonti.

### Incertezza giuridica

**Il problema**: lo status giuridico degli smart contract non è chiaro in molte giurisdizioni. Cosa succede quando il codice è in conflitto con la legge?

*Sfida*: la risoluzione delle controversie e la responsabilità non sono sempre chiare.

**Evoluzione**: i quadri giuridici si stanno gradualmente adattando per riconoscere gli smart contract.

### Immutabilità: un'arma a doppio taglio

**Vantaggio**: nessuno può modificare le regole

*Rischio*: impossibilità di correggere bug o aggiornare le funzionalità.

**Soluzioni**: modelli di contratto aggiornabili o progettazione di percorsi di migrazione verso nuovi contratti.

## Il futuro degli smart contract

Gli smart contract sono ancora in evoluzione, con sviluppi entusiasmanti all'orizzonte:

 - Nuovi linguaggi: consentono una logica più complessa e una programmazione più sicura.
 - Contratti cross-chain: contratti che operano su più blockchain.
 - Verifica formale: prove matematiche che dimostrano il corretto funzionamento dei contratti. 
 - Contratti che preservano la privacy: utilizzo di prove a conoscenza zero per eseguire i contratti in modo privato.

>[!important] Gli smart contract rappresentano un cambiamento fondamentale nel modo in cui creiamo e applichiamo gli accordi. Eliminando gli intermediari e automatizzando l'esecuzione, consentono nuove forme di fiducia, coordinamento e attività economica che prima erano impossibili. 

Con la maturazione della tecnologia, gli smart contract sono destinati a ridefinire settori che vanno dalla finanza alla governance all'intrattenimento, creando un'economia digitale più automatizzata, trasparente e accessibile.

# Token

## Token Nativi

Un **token nativo** è la valuta digitale primaria o la criptovaluta nativa di una determinata blockchain. I token nativi agiscono come base per il trasferimento di valore ed il funzionamento della rete all'interno dei rispettivi ambienti.

- **Ethereum**: ETH;
- **Avalanche C-Chain**: AVAX;
- **Dexalot**: ALOT:
- ...

I token nativi svolgono più ruoli chiave allinterno delle reti blockchain basate su EVM, come:

- **Trasferimento di valore**: I token nativi agiscono come valuta primaria per le transazioni P2P all'interno della rete, consentendo lo scambio di valuta tra i partecipanti;
- **Commissioni**: I token nativi vengono usati come "carburante" per pagare le commissioni di transazione, le implementazioni dei contratti ed altre operazioni di rete. Ciò garantisce che le risorse siano allocate in modo efficiente all'interno della rete;
- **Sicurezza**:
---- 



