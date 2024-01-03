---
(시도1)   
gcloud container clusters get credentials in8minutes-cluster --zone us-centrall-a -project theta-style-403004   
gcloud auth login    

(시도2)
gcloud container clusters get-credentials in28minutes-cluster --zone us-centrall-a -project theta-style-403004   
> 에러발생1    
```
Fetching cluster endpoint and auth data.   
kubeconfig entry generated for in28minutes-cluster   
CRITICA ACTION REQUIRED gke-gcloud-auth-plugin, which is needed for continued use of kubectl, was not found or is not executable Install
gke-gcloud-auth-plugin for use with kubectl by following
https://cloud.google.com/blog/products/containers-kubernetes/kubectl-auth-changes-in-gke   
```
> 해결1(docs 참고) gke-gcloud-auth-plugin 설치   
yum install google-cloud-sdk-gke-gcloud-auth-plugin   

> 에러발생2   
```
Transaction check error   
file   
/usr/1ib64/google-cloud-sdk/platform/bundledpythonunix/lib/ite14.2.2/1ibitc14.2.2.a from install of google-cloud-sdk-458.0.1-1.x86 64 conflicts with file   
file   
/usr/lib64/google-cloud-sdk/platform/bundledpythonunix/lib/itcl4. 2.2/1ibitclstub4.2.2.a from install of google-cloud-sdk-458.0.1-1.x86 64 conflicts with   
file from package google-cloud-cli-458. 0.1-1.x86_64   
..(중략)...   
```
> 해결2   
yum shell   
> remove google-cloud-cli   
> install google-cloud-sdk   
> run   
---
## Step 12 구글 클라우드 콘솔의 GKE 복습   
ㅇ Google Cloud Platform   
Kubernetes Engine\Workloads 에서 작업이 가능하다   
---
## Stemp 13 쿠버네티스 아키텍처 이해하기 - Masger Node 와 Worker Node   


