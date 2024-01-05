# Provisioning a KYMA instance on SAP BTP

## Enable SAP BTP, Kyma Runtime | SAP Tutorials

[Enable KYMA in BTP](https://developers.sap.com/tutorials/cp-kyma-getting-started.html)

[Sizing of the Trial Account](https://help.sap.com/docs/btp/sap-business-technology-platform/about-trial-account)

## Install local tools

[Install Ubuntu on WSL2 and get started with graphical applications ](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-11-with-gui-support#1-overview)
[Install kubectl](https://kubernetes.io/docs/tasks/tools/)

## Update your kube.config with the provided connection data

Installing prerequisite tools:

Postgres DB

``` kubectl
 kubectl apply -f /k8s/postgress 
```

Install Kafka, Zookeepr, AKQH

``` kubectl
 kubectl apply -f /k8s/postgress 
```



Code is available from Github Repository: [Github](https://github.com/mizmauz/heureso_kyma)
