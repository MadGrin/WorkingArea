.. csv-table:: **Tabella 28 - Componenti del parametro elencoAvvisiDigitali**
   :header: "**Dato**","**Liv**","**Genere**","**Occ**","**Len**","**Contenuto**"
   :widths: 15, 10, 30,10,10,10
   
   "identificativoDominio",2,"an","1..1","1..35","Campo alfanumerico contenente il codice fiscale dell'Ente Creditore che invia l'elenco degli avvisi Digitali."
   "elencoCompleto",2,"n","1..1",1,"Indica se l'elenco fornito contiene tutte le posizioni di debito per quel soggetto debitore presso l'Ente Creditore. Può assumere i seguenti valori:
   
   - 0 Elenco completo
   - 1 Elenco incompleto"
   "numeroAvvisi",2,"n","1..1",3,"Numero avvisi presenti nell'elenco."
   "avvisoDigitale",2,"s","0..n",,"Struttura facoltativa che contiene le informazioni dell'avviso digitale in modalità pull. La struttura è **obbligatoria** se l'elemento **numeroAvvisi e maggiore di 0**."
   "codiceAvviso",3,"an","1..1",18,"Codice dell’avviso di pagamento predisposto secondo quanto indicato al § 7.4.1 delle SANP. Contiene il codice IUV."
   "statoPagamento",3,"an","1..1","1.2","
   
   - 00 L’avviso è pagabile 
   - 01 L’avviso è già stato pagato
   - 02 L’avviso non è pagabile"
   "dataScadenzaAvviso",3,"an","0..1",10,"Indica la data, successiva alla data di scadenza sino alla quale si ritiene valido l'avviso, secondo il formato ISO 8601 **[YYYY]-[MM]-[DD]**"
   "importoAvviso",3,"an","1..1","3..12","Campo numerico (due cifre per la parte decimale, il separatore dei centesimi è il punto “.”), indicante l’importo relativo alla somma da versare. **Deve essere maggiore di “0.10”**."
   "descrizionePagamento",3,"an","1..1","1..249","Testo libero a disposizione dell’Ente per descrivere le motivazioni del pagamento."


.. csv-table:: **Tabella 27 - Componenti del parametro datiNotifica**
   :header: "**Dato**","**Liv**","**Genere**","**Occ**","**Len**","**Contenuto**"
   :widths: 15, 10, 30,10,10,10

   "dataOraRichiesta",2,"an","1..1","1..19","Indica la data e l’ora dell’evento di invio della richiesta secondo il formato ISO 8601, alla risoluzione del millisecondo e sempre riferito al GMT. Formato **[YYYY]-[MM]-[DD]T[hh]:[mm]:[ss]**"
   "identificativoMessaggioRichiesta",2,"an","1..1","1..20","Identificativo legato alla trasmissione della segnalazione digitale e consente di riconoscere la trasmissione duplicata. Deve essere univoco nell’ambito di 365 giorni consecutivi."
   "identificativoUnivocoSoggetto",2,"s","1..1",,"Aggregazione che riporta le informazioni concernenti l’identificazione fiscale del pagatore."
   "tipoIdentificativoUnivoco",3,"an","1..1",1,"Campo alfanumerico che indica la natura del pagatore, può assumere i seguenti valori:
   
   - **F** = Persona fisica
   - **G** = Persona Giuridica."
   "codiceIdentificativoUnivoco",3,"an","1..1","1..35","Campo alfanumerico che può contenere il codice fiscale o, in alternativa, la partita IVA del pagatore."
   "azioneDiAggiornamento",2,"an","1..1",1,"Indica il tipo di aggiornamento richiesto:
   
   - **A** = Attivazione
   - **D** = disattivazione"
   
.. csv-table:: **Tabella 26 - Componenti del parametro avvisoDigitale**
   :header: "**Dato**","**Liv**","**Genere**","**Occ**","**Len**","**Contenuto**"
   :widths: 15, 10, 30,10,10,10
   
   "avvisoDigitaleWS",2,"S","1..1","","Contiene le stesse informazioni definite per la struttura avvisoDigitale, specificata nella Tabella 19 al § 5.4.1."
   
.. csv-table:: **Tabella 25 - Componenti del parametro esitoAvvisoDigitaleWS**
   :header: "**Dato**","**Liv**","**Genere**","**Occ**","**Len**","**Contenuto**"
   :widths: 15, 10, 30,10,10,10
   
   "esitoAvvisoDigitaleWS",2,"S","1..1","","Contiene le stesse informazioni specificate per la struttura esitoAvvisoDigitale, definita nella Tabella 20 al § 5.4.1."
   
.. csv-table:: **Tabella 24 - Componenti del parametro avvisoDigitaleWS**
   :header: "**Dato**","**Liv**","**Genere**","**Occ**","**Len**","**Contenuto**"
   :widths: 15, 10, 30,10,10,10
   
   "avvisoDigitaleWS",2,"S","1..1","","Contiene le stesse informazioni definite per la struttura avvisoDigitale, specificata nella Tabella 19 al § 5.4.1."
