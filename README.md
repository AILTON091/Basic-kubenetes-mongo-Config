# Basic-kubenetes-mongo-Config


Lista dos principais comandos do kubectl com descrição:
Gerenciamento de Pods:

kubectl get pods: Lista todos os pods em execução no namespace atual.
kubectl describe pod <nome-pod>: Mostra informações detalhadas sobre um pod específico.
kubectl delete pod <nome-pod>: Exclui um pod específico.
kubectl logs <nome-pod>: Exibe os logs de um pod específico.
kubectl exec -it <nome-pod> -- <comando>: Executa um comando dentro de um container de um pod específico.
Gerenciamento de Deployments:

kubectl get deployments: Lista todos os deployments no namespace atual.
kubectl describe deployment <nome-deployment>: Mostra informações detalhadas sobre um deployment específico.
kubectl create deployment <nome-deployment> --image=<imagem>: Cria um novo deployment com a imagem especificada.
kubectl scale deployment <nome-deployment> --replicas=<numero>: Altera o número de réplicas de um deployment.
kubectl delete deployment <nome-deployment>: Exclui um deployment específico.
Gerenciamento de Serviços:

kubectl get services: Lista todos os serviços no namespace atual.
kubectl describe service <nome-serviço>: Mostra informações detalhadas sobre um serviço específico.
kubectl create service <nome-serviço> --port=<porta> --target-port=<porta-alvo> --selector=<rótulos>: Cria um novo serviço com as especificações fornecidas.
kubectl delete service <nome-serviço>: Exclui um serviço específico.
Gerenciamento de ConfigMaps:

kubectl get configmaps: Lista todos os ConfigMaps no namespace atual.
kubectl describe configmap <nome-configmap>: Mostra informações detalhadas sobre um ConfigMap específico.
kubectl create configmap <nome-configmap> --from-file=<arquivo>: Cria um novo ConfigMap a partir de um arquivo.
kubectl delete configmap <nome-configmap>: Exclui um ConfigMap específico.
Gerenciamento de Segredos:

kubectl get secrets: Lista todos os segredos no namespace atual.
kubectl describe secret <nome-segredo>: Mostra informações detalhadas sobre um segredo específico.
kubectl create secret generic <nome-segredo> --from-literal=<chave>=<valor>: Cria um novo segredo genérico com um par chave-valor.
kubectl delete secret <nome-segredo>: Exclui um segredo específico.
Outras operações:

kubectl get nodes:  Lista todos os nós no cluster.
kubectl cordon <nome-nó>: Corda um nó, impedindo que novos pods sejam agendados nele.
kubectl uncordon <nome-nó>: Descorda um nó, permitindo que novos pods sejam agendados nele.
kubectl get events: Lista todos os eventos no namespace atual.
kubectl describe events <nome-evento>: Mostra informações detalhadas sobre um evento específico.

# Executar os arquivos

kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml (deployment)


kubectl get node -o wide  --ver o ip externo 