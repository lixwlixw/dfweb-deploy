# OCDF页面部署
## 1. 登陆OCDF平台
```
oc login  https://10.1.234.34:443 -u username -p password
```
## 2. 创建项目
```
oc new-project datafoundryweb-test
```
## 3. 使用模版创建OCDFWeb应用
```
oc process -n openshift  datafoundry-web | oc create -f - 
```
## 4. 查看OCDFWeb pod状态
```
oc get pod
NAME                               READY     STATUS    RESTARTS   AGE
datafoundrypayment-1-5gs45         1/1       Running   0          5m
datafoundryservicevolume-1-cdwjl   1/1       Running   0          5m
gitter-1-4vw69                     1/1       Running   0          5m
web-console-1-3dm5v                2/2       Running   0          5m
```
## 5. 查看OCDFWeb URL并访问
```
oc get route|grep web-console|awk '{print $2}'
```
