# kubernetes-BogdanStashchuk
https://youtu.be/hNLQ3tCP8jQ?si=nDvq-UB0VRwXsR-v
https://youtu.be/It03Sjsl9s8?si=Pb8Wl1gLTa45kwXv

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
33. `k get deploy`
34. `k get services`
35. `k expose deploy my-nginx-deploy --port=8080 --target-port=80`
36. `k describe service my-nginx-deploy`
37. `k delete service my-nginx-deploy`
38. `k expose deploy my-nginx-deploy --type=NodePort --port=8888 --target-port=80`
39. `minikube service my-nginx-deploy --url`
40. `k expose deploy my-nginx-deploy --type=LoadBalancer --port=9999 --target-port=80`
41. `minikube tunnel`
42. `http://localhost:9999/`
43. `docker build . -t xmario/k8s-web-hello-ru:latest -t xmario/k8s-web-hello-ru:1.0.0`
44. `docker images | grep web-hello`
45. `docker login`
46. `$ docker push xmario/k8s-web-hello-ru --all-tags`
47. `k create deploy k8s-web-hello --image xmario/k8s-web-hello-ru:1.0.0`
48. `k expose deploy k8s-web-hello --type=LoadBalancer --port=3333 --target-port=3000`
49. `k describe service k8s-web-hello`
50. `k scale deploy k8s-web-hello --replicas=7`
51. `docker build . -t xmario/k8s-web-hello-ru:latest -t xmario/k8s-web-hello-ru:2.0.0`
52. `k rollout status deploy k8s-web-hello`
53. `docker ps | grep web-hello`
54. `k set image deploy k8s-web-hello k8s-web-hello-ru=xmario/k8s-web-hello-ru:2.0.0`
55. `k delete service k8s-web-hello`
56. `k detele deploy k8s-web-hello`
57. `k apply -f deployment.yaml`
58. `k apply -f service.yaml`
59. `minikube dashboard`
60. `k delete -f deployment.yaml -f service.yaml`
61. `docker build . -t xmario/k8s-web-to-nginx-ru`
62. `docker push xmario/k8s-web-to-nginx-ru`
63. `k apply -f k8s-web-to-nginx.yaml -f nginx.yaml`
64. `docker exec -it 5e8db015f48c sh`
65. `wget 10.105.243.186`
66. `cat index.html`
67. `rm index.html` - удаляет файл
68. `wget nginx` - обращение по имени сервиса, а не по IP. Работает изнутри контейнера
69. `nslookup nginx` - ответ от внутреннего DNS сервера
70. `docker tag xmario/k8s-web-to-nginx-ru:latest xmario/k8s-web-to-nginx-ru:1.0.0`
71. `docker images | grep k8s-web-to-nginx`
72. `xmario/k8s-web-to-nginx-ru`
73. `minikube status`
74. `minikube stop`
75. `minikube delete`
76. `export KUBECONFIG=clarice.yaml`
77. `k get pods --namespace=kube-system`
78. `k get namespaces`
79. `k get deploy`
80. `k get pods`
81. `k delete all --all`
82. `http://89.104.117.144:3333/`
83. `cd C:\Users\xpave\.kube && ls && cat config`
84. `k config set-cluster <CLUSTER_NAME> --server=<IP_SERVER:PORT_SERVER> --certificate-authrity=<PATH_TO_FILE>`
85. `k config set-credintails temp --username=<YOUR_NAME> --password=<YOUR_PASSWORD>`
86. `k config set-credentails temp --token=123456789`
87. `k config get-contexts`
88. `k config use-context minikube`
89. `k config get-clusters`
90. `k config get-users`
91. `k config delete-context k8s-cluster-2`
92. `k config delete-cluster k8s-cluster-2`
93. `k config delete-user k8s-cluster-2`