#myproj1

#cd ~/Documents/GitHub/myGit/istioRoom/extproc/proj1

#Base kuberenetes setup with istio running

2. kubectl run nginx --image=nginx
3. kubectl label pod nginx app=default

#Run exproc service locally in the Laptop 

1. go run extproc-service.go 
    > Starting server on :5000
2. Check the Laptop ip  ( preferrably 192.xx ) and update the IP in the filter if the IP has changed
    > vim extproc-filter.yaml -> change the IP Address in the bottom section . 
3. curl http://laptopip:5000/extproc
4. kubectl apply -f extproc-filter.yaml



#Test Service 

1. kubectl run nginx -- curl http://nginx 



