# Installazione di NginxIngressController
Questa helm sub chart directory contiene i file per installare la componente F5 NginxIngressController
la cartella contiene due file Chart.yaml e values.yaml.

Il File Chart.yaml contiene:
 - la versione che helm assegna all'installazione
 - la versione del chart helm
 - la URL del repository helm

Il file values.yaml contiene i parametri da sovrascrive rispetto al default.I piu comuni:


  - controller.image.repository
  - controller.image.tag
  - controller.service
  
   
Passi necessari per installare NginxIngressController:


1.) modifica valori dei file Chart.yaml, values.yaml
2.) modifica i valori del file nginx-ingress-controller.yaml nella cartella argocd-apps
4.) Installa l'applicazione mediante il comando

   - kubectl create -f nginx-ingress-controller.yaml 
