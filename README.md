# OtusHomeWork2 - Kubernetes base
1. Response on port 8000
2. Has http-method
   GET /healsh/
   RESPONSE: {"status": "OK"}
3. Configure k8s with Deployment, Service and Ingress
4. REQUESTS: http://arch.homework/health
             http://arch.homework/otusapp/roman/health
   RESPONSE {"status", "OK"}

commands to apply:
git clone https://github.com/RomashkoRomanV/otus_home_work_2.git
cd otus_home_work_2
minikube addons enable ingress
kubectl apply -f deployment.yaml -f service.yaml -f ingress.yaml
kubectl get ing
curl -H 'Host: arch.homework' http://<IP_ADDRESS>/health
curl -H 'Host: arch.homework' http://<IP_ADDRESS>/otusapp/roman/health
