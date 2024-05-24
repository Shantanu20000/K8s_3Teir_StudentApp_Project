# K8S Three teir project
step 1

Clone dockerfile of frontend, backend and proxy and Build it. 

    git init
    git clone https://github.com/shantanu20000/k8s.git
    cd k8s/
    cd backend/
    docker build -t shan20000/k8s_3teir_project:backend .
    cd ../frontend
    docker build -t shan20000/k8s_3teir_project:frontend .
    cd ../proxy
    docker build -t shan20000/k8s_3teir_project:proxy .
    docker login

Give login and tocken of github

Push images to dockerhub

    docker push shan20000/k8s_3teir_project:backend
    docker push shan20000/k8s_3teir_project:frontend
    docker push shan20000/k8s_3teir_project:proxy

step 2

Apply deployment.yml and service.yaml file on Cloud Shell. go in every directory [backend, frontend, proxy] 

    kubectl apply -f deployment.yaml
    kubeclt apply -f service.yaml

step 3 

View all services copy proxy loadbalancer DNS and paste it on url bar of Crome

    kubeclt get svc

You will see Student form

fill up it and check data is store or not    

    

