---
title: Diagnosi Tumore del Seno mediante SVM
published: true
---
Il **tumore del seno** è una delle principali cause di morte per le donne affette da cancro [1]. Una diagnosi precoce e corretta è essenziale nel trattamento di questa patologia. La metodologia classica di diagnosi dipende fortemente dall’esperienza del medico e dalla sua capacità di ispezione visiva. Purtroppo, sebbene estremamente preparati e professionali, gli operatori umani possono incorrere in errori quando la correttezza di una valutazione dipende così profondamente dalle osservazioni [2]. Anche analizzando i risultati di numerosi test, una diagnosi precisa può essere difficile da ottenere persino per i professionisti più esperti. Tutte queste ragioni spiegano il motivo per cui la diagnosi automatica del tumore del seno sia un ambito di ricerca estremamente sensibile e delicato.

I tool di diagnosi computerizzata sono nati e pensati per **aiutare e supportare** i medici al fine di incrementare l’accuratezza delle diagnosi stesse [3-5].

Già nel 2001 una ricerca ha dimostrato come il Machine Learning e le Reti Neurali riescano ad accrescere sensibilmente l’accuratezza delle diagnosi. I risultati riportati nel lavoro di Brause [6] mostrano come il clinico con maggiore esperienza riesca a diagnosticare il tumore al seno con un’accuratezza del 79.97% mentre tale valore raggiunge il 91,1% quando la fase di diagnosi viene supportata dall’aiuto dell’Intelligenza Artificiale. I progressi raggiunti dal 2001 ad oggi hanno fatto salire ulteriormente tale percentuale portandola al 96%-97%.

I tumori del seno possono essere benigni o maligni e purtroppo, sebbene molti di essi siano diagnosticati durante la fase iniziale, circa il 20% di questi ultimi conduce le donne affette da tale patologia alla morte [7]. Un ausilio al lavoro dei medici che incrementa cosi tanto l’accuratezza  delle diagnosi può davvero fare la differenza.

Tecniche di classificazione come la Regressione Logistica o La Macchina a Vettori di Supporto (SVM) si rivelano estremamente utili.

In modo particolare, la **SVM**, basata sull’individuazione dell’iperpiano ottimale di separazione tra le classi (benigno o maligno) mediante la mappatura dei dati di ingresso in uno spazio delle caratteristiche (features) multidimensionale, ha il vantaggio di una fase di addestramento relativamente veloce anche in presenza di un ampio Data Set di dati di input [8-9].

Lo studio pubblicato dalla Hindawi Publishing Corporation nel settembre del 2014 [10] illustra dettagliatamente i risultati ottenuti dal Machine Learning applicato al Breast Cancer Wisconsin (Diagnostic) Data Set [https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)], un insieme di 569 casi di tumore distribuiti in 357 benigni e 212 maligni.

Ogni caso è costituito da un ID number, una diagnosi (B = benigno, M = maligno) e 30 caratteristiche (features). Le caratteristiche sono state estratte dalle immagini digitalizzate mediante tecnica FNA (Fine Needle Aspirate) applicata a una massa tumorale presente al seno.

Ebbene, un modello di Machine Learning basato su SVM e addestrato mediante tale Data Set riesce  a diagnosticare la classe del tumore con accuratezza che si attesta fino al **97.47**%.

![Tumore del seno (immagine)]({{site.baseurl}}/img/tumore_seno.png)

- [1] I. Christoyianni, E. Dermatas, and G. Kokkinakis, “Fast detection of masses in computer-aided mammography,” IEEE Signal Processing Magazine, vol. 17, no. 1, pp. 54–64, 2000.
- [2] N. Salim, Medical Diagnosis Using Neural Network, Faculty of Information Technology University, 2013.
- [3] A. Tartar, N. Kilic, and A. Akan, “Classification of pulmonary nodules by using hybrid features,” Computational and Mathematical Methods in Medicine, vol. 2013, Article ID 148363, 11 pages, 2013.
- [4] N. Kilic, O. N. Ucan, and O. Osman, “Colonic polyp detection in CT colonography with fuzzy rule based 3D template matching”, Journal of Medical Systems, vol. 33, no. 1, pp. 9–18, 2009.
- [5] A. Mert, N. Kiliç, and A. Akan, “Evaluation of bagging ensemble method with time-domain feature extraction for diagnosing of arrhythmia beats,” Neural Computing and Applications, vol. 24, no. 2, pp. 317–326, 2014.
- [6] R. W. Brause, “Medical analysis and diagnosis by neural networks,” in Proceedings of the 2nd International Symposium on Medical Data Analysis (ISMDA ’01), pp. 1–13, Madrid, Spain, October 2001.
- [7] T. S. Subashini, V. Ramalingam, and S. Palanivel, “Breast mass classification based on cytological patterns using RBFNN and SVM,” Expert Systems with Applications, vol. 36, no. 3, pp. 5284–5290, 2009.
- [8] M. F. Akay, “Support vector machines combined with feature selection for breast cancer diagnosis,” Expert Systems with Applications, vol. 36, no. 2, pp. 3240–3247, 2009.
- [9] B. Wang, H. Huang, and X. Wang, “A support vector machine based MSM model for financial short-term volatility forecasting,” Neural Computing and Applications, vol. 22, no. 1, pp. 21–28, 2013.
- [10] A. Mert, N. KjlJç, E. Bilgili, A. Akan, “Breast Cancer Detection with Reduced Feature Set”, 2014, Hindawi Publishing Corporation 