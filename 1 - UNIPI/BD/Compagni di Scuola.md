## 0. Analisi del testo

* Compagni di scuola: nome della piattaforma digitale
* Utente: persona iscritta alla piattafforma. Può essere un ex alunno o un professore. Può creare gruppi classe. Un utente può cercare un gruppo classe e chiedere di unirsi. 
* Gruppo Classe: Insieme di utenti che facevano parte della stessa classe e che vogliono rimanere in contatto. Ogni utente che faccia parte del gruppo può accettare le richieste di unirsi di altri utenti. I gruppi prevedono due fasi: creazione e organizzazione cene.
* Classe: identificata da:
	* anno esame di maturità
	* sezione
	* scuola
	* città
* Amministratore: utente che gestisce un gruppo classe. Quando viene creata un nuovo gruppo classe l'utente che lo ha creato diventa amministratore. Ci deve sempre essere un amministratore per gruppo classe. Gli amministratori possono essere più di uno.
* ex compagno: alunno di una classe
* dossier digitale: accumulo di informazioni testuali tra cui nome, soprannome, data di nascita, fratelli, etc. e informazioni multimediali come foto, video, registrazioni, etc. Il dossier serve per aiutare a rintracciare l'ex alunno ma rimane anche dopo che l'alunno è stato ritrovato. È possibile commentare i dossier con aneddoti e ricordi
* Professori: utenti iscritti alla piattaforma che hanno insegnato in almeno una delle classi. Possono essere invitati nei gruppi classe e inclusi nei dossier.
* Sondaggi: creati per scegliere la data, il luogo e il tipo di cena

## 1. Descrizione del dominio

* **Utente**: rappresenta ogni persona registrata alla piattaforma. Ogni iscritto può partecipare a uno o più gruppi e può assumere diversi ruoli:
*secondo me la gerarchia è solo (utente ->prof o alunno) mentre amministra e partecipa sono relazioni tra utente e gruppo classe*
	a) **Creatore**: crea il gruppo ed è uno degli amministratori iniziali.
	*secondo me il creatore è inutile*
	b) **Amministratore**: gestisce il gruppo, crea sondaggi e organizza cene.
	c) **Partecipante**: membro del gruppo che può commentare e accedere ai dossier.
	d) **Professore**: partecipante che viene incluso al gruppo con delle limitazioni di visibilità sugli aneddoti che lo riguardano.

* **GruppoClasse**: ogni partecipante può creare un gruppo classe composto da ex compagni e professori specificando anno dell’esame di maturità, sezione, nome della scuola e città. Può essere creato solo una volta e da un solo utente ma può essere amministrato da massimo tre utenti contemporaneamente. *meglio scrivere che non ci può essere più di un gruppo della stessa classe. Non ho capito da dove salta fuori che non ci possono essere più di 3 amministratori*

**Dossier**: per ciascun utente viene creato un dossier personale che raccoglie informazioni personali, contenuti multimediali e commenti da parte di altri partecipanti. È visibile e modificabile da tutti gli utenti.

**Segnalazione**: ogni partecipante può suggerire collegamenti tra utenti per aiutare a  ritrovare ex compagni di classe o comunque per mandare messaggi utili per il gruppo.

Luogo: posizione geografica usata per localizzare cene e mappa interattiva dei partecipanti.

Cena: evento finale di ritrovo del gruppo. Può avere stato (proposta, confermata), tipo (informale, formale), luogo associato, e viene proposta solo quando il gruppo raggiunge almeno sei partecipanti.

Sondaggio: viene creato per decidere dettagli della cena come data, luogo e tipo di cena. Ogni cena può avere più sondaggi.

Votazioni: registra le preferenze di ciascun utente per ogni sondaggio, memorizzando le scelte effettuate.