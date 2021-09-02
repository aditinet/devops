#  Progetto devops gestito da Aditinet per le componenti:
  
  - F5-CIS
  - F5-MCGW
  - F5-NginxIngressController
  
 Sotto la descrizione della cartella e il contenuto: 
 
  - f5-cis-subchart:
   
     contiene i file Chart.yaml, values.yaml.In questi file viene definita la dipendenza
     (repository helm da usare) e i parametri da passare al chart.per poter installare la componente F5-CIS.
   
  - nginx-ingress-subchart
   
     contiene i file Chart.yaml, values.yaml.In questi file viene definita la dipendenza (repository helm da usare) 
     e i parametri da passare al chart per poter installare la componente NginxIngressController.
   
   - nginx-mcgw-subchart
   
     contiene i file Chart.yaml, values.yaml.In questi file viene definita la dipendenza (repository helm da usare)
     e i parametri da passare al chart per poter installare la componente NginxMCGW.
   
   - argocd-apps
     Continene i file yaml usate da Argo CD per installare l'applicazione.
     
  
  Le istruzioni per l'installazione e i valori da modificare sono nei file README.md di ogni cartella chart.
