#  Progetto devops gestito da Aditinet per le componenti:
   
 F5-CIS
 F5-Mcgw
 NginxIngressController

Repository che contiene i sub chart helm  e i template di esempio per creare applicazioni Argo CD:
   f5-cis-subchart:
     contiene i file Chart.yaml, values.yaml .In questi file viene definita la dipendenza (repository helm da usare) e i parametri da passare al chart.
     per poter installare la componente F5-CIS.
   
   nginx-ingress-subchart
     contiene i file Chart.yaml, values.yaml .In questi file viene definita la dipendenza (repository helm da usare) e i parametri da passare al chart.
     per poter installare la componente NginxIngressController.
   
   nginx-mcgw-subchart
     contiene i file Chart.yaml, values.yaml .In questi file viene definita la dipendenza (repository helm da usare) e i parametri da passare al chart.
     per poter installare la componente NginxMCGW.
