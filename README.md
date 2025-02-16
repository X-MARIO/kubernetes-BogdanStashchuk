# kubernetes-BogdanStashchuk

1. `choco install kubernetes-cli --force`
2. `choco install minikube --force`
3. `minukube status`
4. `minikube delete`
5. `minikube start --driver=docker`
6. `docker ps`
7. `kubectl version`
8. `kubectl cluster-info`
9. `minikube kubectl version`
10. `alias k=kubectl`
11. `k get nodes`
12. `k get pods`
13. `k get namespace`
14. `k get pods --namespace=kube-system`
15. `minikube ip`
16. `ping <IP>`
17. `ssh root@<TP>`
18. `minikube ssh`
19. `docker version`
20. `k run my-nginx-pod --image=nginx`
21. `k describe pod my-nginx-pod`
22. `curl <IP>`
23. `docker ps | grep nginx`
24. `docker exec -it 674444bbb732 sh`
25. `hostname`
26. `cat <FILE_PATH>`
27. `exit`
28. `k get pods -o wide`
29. `k delete pod my-nginx-pod`
30. `k describe deploy my-nginx-deploy`
31. `k scale deploy my-nginx-deploy --replicas=3`
32. `k get pod<POD_NAME>`