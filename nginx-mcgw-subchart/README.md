# Installazione NginxMCGW
Questa helm sub chart directory contiene i file per installare la componente F5 NginxMCGW
la cartella contiene due file Chart.yaml e values.yaml.

Il File Chart.yaml contiene:
 - la versione che helm assegna all'installazione
 - la versione del chart helm
 - la URL del repository helm

Il file values.yaml contiene i parametri da sovrascrive rispetto al default.I piu comuni:


  - image.repository
  - image.tag
  - replicaCount
  
   
Passi necessari per installare NginxMCGW:


1.) modifica valori dei file Chart.yaml, values.yaml

2.) modifica i valori del file mcgw.yaml nella cartella argocd-apps

4.) Installa l'applicazione mediante il comando

   - kubectl create -f mcgw.yaml 
