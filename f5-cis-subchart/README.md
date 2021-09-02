# folder di installazione del CIS 
Questa  helm sub chart directory contiene i file per installare la componente F5 CIS (Container Nngress Service),  la cartella contiene due file Chart.yaml e values.yaml.

Il File Chart.yaml contiene:
	la versione che helm assegna all'installazione
    	la versione del chart helm
        la URL del repository helm

Il file values.yaml  contiene i parametri da sovrascrive rispetto al default.I piu comuni:
    big_ip_url                  - url che punta al BigIP dove saranno creati i servizi da esporre
    big_ip_partition            - partzione usata dal CIS per creare le risorse) 
    pool_member_type            - la modalita in qui raggiunge il servizio su kubernetes,
                                    NodePort  - apre una porta alta su master e node
                                    ClusterIP   -  espone direttamente l'IP del POD
									
per installare il CIS:

1.) Crea  la secret , questa secret contiene user e password per accedere al BigIP, deve essere creata
    nel namespace dove verra installato il CIS.Nella prossima release il secret verra creato in automatico via template helm.

  cubectl create secret generic bigip-login --namespace kube-system --from-literal=username=abcd --from-literal=password=abcd

2.) modifica valori dei file Chart.yaml, values.yaml

3.) modifica i valori del file f5-cis.yaml  nella cartella argocd-apps

4.) Installa l'applicazione
    cubectl create file f5-cis.yaml 
