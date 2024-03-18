# karolina.adamicki

Aufgabe 5:

5.1. Der Pod in Kubernetes ist kurzlebig und nicht dauerhaft, d. h. wenn er ausfällt, ist er weg. Das Deployment ermöglicht bei ausgefallenen Pods, dass ein neuer Pod gestartet wird. Außerdem können mit Deployments mehrere Replikas gestartet werden, das Deployment stellt dabei sicher dass immer die gewünschte Zahl an Replikas verfügbar ist. Deployments können auch Rollbacks auf vorherige Versionen machen, das können alles Pods nicht.

5.2. Das Service ist ein Zugriffspunkt auf die Pods. Wenn also Anfragen an den Service kommen, leitet dieser die Anfragen direkt an die Pods weiter. Dabei dient der auch als Lastverteiler, weil er die Anfragen (im Round Robin Prinzip?) an die Pods weiterleitet. 

5.3. Man kann eine Kubernetes Anwendung nach außen erreichen über einen Nodeport Service, einen Loadbalancer oder Ingress. NodePorts öffnen einen Port auf jedem Node des Clusters, über den die Anwendung dann erreichbar ist. Loadbalancer weißen bei Cloud-Providern automatisch eine öffentliche IP-Adresse zu, um den Traffic auf die Pods zu verteilen. Ingress-Controllers leitet die Anfragen von außen an die entsprechenden Services innerhalb des Clusters, basierend auf Hostname oder Pfad, weiter. 
