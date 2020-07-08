---
title: Fashion Assistant
published: false
---
Il valore dell’industria mondiale della moda è elevatissimo, qualcosa come il 2% dell’intero PIL del globo. Negli ultimi anni, a causa dell’affermarsi di nuove tecnologie come la Computer Vision, il Machine Learning e il Deep Learning, il modo  di fare moda e di pianificarne e prevederne gli sviluppi e le tendenze sta cambiando drasticamente.

Prendendo spunto dall’[Echo Look](https://www.youtube.com/watch?v=9X_fP4pPWPw) di Amazon e a puro scopo di ricerca, immaginiamo l’ipotetica situazione in cui un retailer (di fantasia) o uno stilista (sempre di fantasia) decida di farsi sviluppare un assistente virtuale che spulciando tra le immagini Instagram o Facebook dei clienti riesca a classificare il loro stile di abbigliamento oppure i capi e gli accessori di maggiore popolarità come pantaloni, borse, abiti.

![Fashion-Assistant-1.png]({{site.baseurl}}/img/Fashion-Assistant-1.png)

Tale assistente potrebbe essere utilissimo per determinare stili e tendenze e aiutare a scegliere le campagne e attività di marketing da lanciare. 

Le Reti Neurali Artificiali (ANN), in modo particolare le reti di tipo Convoluzionale (CNN), sono particolarmente indicate per la trattazione e gestione delle immagini. In tale senso ci viene in aiuto il Data Set chiamato Fashion-MNIST, pubblicato recentemente da [Zalando](https://research.zalando.com/welcome/mission/research-projects/fashion-mnist/). Esso contiene ben 70000 immagini in formato 28×28 pixels associate a 10 classi (categorie) di articoli di abbigliamento (t-shirt, pantaloni, vestiti, cappotti, sandali, ecc.). Tali immagini sono ulteriormente suddivide in un gruppo di training costituito da 60000 elementi e uno di test composto dai 10000 campioni restanti.

L’idea di fondo della nostra ricerca è quella di dare in pasto a una rete neurale convoluzionale le immagini del Fashion-MNIST Data Set al fine di verificarne la capacità di classificazione e la relativa accuratezza.

![Fashion-Assistant-2.png]({{site.baseurl}}/img/Fashion-Assistant-2.png)

Adottando un layout classico del tipo Convoluzione-Pooling-Flatten-Dense si evidenzia che i risultati migliori si ottengono con uno strato di Convoluzione composto da 64 nodi con Dropout del 25%, MaxPooling, Flatten e poi due strati Densi di cui uno da 32 nodi e l’ultimo, di Output, ovviamente costituito da 10 nodi. In questo modo si raggiunge un’accuratezza a livello di test del 91.9%. I risultati sono illustrati brevemente nelle figure seguenti

![Confronto tra Classe Predetta e Classe Reale]({{site.baseurl}}/img/Fashion-Assistant-3.png)

![Matrice di Confusione del modello adoperato]({{site.baseurl}}/img/Fashion-Assistant-4.png)

![Report Riassuntivo Metriche]({{site.baseurl}}/img/Fashion-Assistant-5.png)



