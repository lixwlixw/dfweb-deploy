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
## 4. 查看OCDFWeb访问URl 并访问
```
oc get route
```
