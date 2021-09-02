# folder contenente i file per le applicazioni Argo Cd
Questa  helm sub chart directory contiene  i file Argo CD Application

Per ogni applicazione viene creato un file   applicazione.yaml, in questo file sono definiti i paramet
che Argo CD usa per creare l'applicazione, ci sono alcuni parametri da modificare per  personalizzare l'applicazione
 
  - metadata.name
  - metadata.namespace
  - spec.destination.namespace
  - spec.destination.server
  - spec.source.path                            (subchart directory del repository)
  - spec.source.repoURL                         (BaseURL del  repository)
  - spec.source.targetRevision:                 (versione del branch sul repository) 
  - spec.sync.comparedTo.destination.namespace  
  - spec.sync.comparedTo.destination.server
  - spec.sync.comparedTo.source.path
  - spec.sync.comparedTo.source.repoURL
  - spec.sync.comparedTo.source.targetRevision
