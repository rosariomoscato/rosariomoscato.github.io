---
title: Churn Modelling mediante Artificial Neural Network
published: false
---

Un problema tipico è prevedere se un dato cliente abbandonerà un servizio (per esempio chiudendo il suo conto-corrente presso una banca o cessando il suo abbonamento a un e-commerce) oppure, al contrario, continuerà a utilizzarlo.

Ci sono molti modi per eseguire il “Churn Modelling” ma uno dei più efficaci è quello di costruire una Rete Neurale Artificiale (ANN) da addestrare con i dati relativi a un determinato intervallo temporale, per esempio gli ultimi sei mesi, al fine di estrarre ed evidenziare le regolarità sottostanti i dati, utilizzandole per fare previsioni e classificazioni.

Partendo da un dataset contenente 10000 casi costruiremo una ANN dotata di uno strato di input, uno strato hidden e uno strato di output. La rete potrà essere addestrata mediante la tecnica della K-Fold Cross Validation e ottimizzata mediante un Grid Search. La Cross Validation e l’impiego di un eventuale Dropout permetterà di controllare e ridurre l’overfitting, mentre la Grid Search ci permetterà di ottenere il miglior set di iper-parametri al fine di garantire la migliore performance, calcolata in termini di accuracy.

![Il Dataset adoperato]({{site.baseurl}}/img/Churn1.png)

Il dataset utilizzato, riproduce perfettamente quelli che potrebbero essere i dati forniti da una banca per cui nelle sue colonne avremo:

- Customer ID (Identificativo Cliente)
- Surname (Cognome)
- Credit Score (Punteggio)
- Geography (Paese)
- Gender (Sesso)
- Age (Età)
- Tenure (Numero di anni con la banca)
- Balance (Saldo)
- NomOfProduct (Numero di Prodotti)
- HasCrCard (Carta di Credito)
- IsActiveMember (Cliente Attivo)
- EstimatedSalary (Stipendio Stimato)
- Exited (Rapporto Cessato)

![Numero di casi]({{site.baseurl}}/img/Churn2.png)

Dopo aver importato il dataset, creato i predittori (X) e la variabile dipendente (y), aver gestito le variabili categoriche, aver prodotto i set di Training e di Test e effettuato la standardizzazione dei dati, potremo finalmente procedere alla creazione delle nostra Rete Neurale Artificiale che avrà la struttura seguente: 

![La struttura della nostra ANN]({{site.baseurl}}/img/Churn3.png)

Il modello adottato, come si vede dalla Confusion Matrix, ha delle performance molto buone, oltre l’83% 

![onfusion Matrix]({{site.baseurl}}/img/Churn4.png)

A questo punto, immettendo dei valori nuovi, dunque non contenuti nel dataset iniziale, si potrà predire facilmente se il nuovo cliente rimarrà o lascerà la banca.Come accennato in precedenza la tecnica di K-Fold Cross Validation ci sarà utile per calcolare l’accuratezza media nel caso in cui, per esempio, K è uguale a 10.

Come si vede tale valore è 83.8%, quindi molto vicino a quello calcolato semplicemente poco fa, anche la sua deviazione standard è assolutamente accettabile valendo 1.88%.

Un’ analisi di tipo Grid Search ci permetterà, in ultimo, di determinare la migliore configurazione degli iper-parametri. Il risultato di tale ricerca ha portato a una best accuracy pari a 85.3% ottenuta con batch_size pari a 25, numero di epochs pari a 500 e Adam optimizer.

