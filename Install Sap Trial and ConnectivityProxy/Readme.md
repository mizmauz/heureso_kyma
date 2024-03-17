# Install ECC Docker Image SAP ABAP Trail

https://community.sap.com/t5/application-development-blog-posts/now-available-abap-platform-trial/ba-p/13569137

https://hub.docker.com/r/sapse/abap-platform-trial

``` kubectl
docker pull sapse/abap-platform-trial:1909_SP01
```

``` startdocker image
docker run --stop-timeout 3600 -it --name a4h -h vhcala4hci sapse/abap-platform-trial:1909_SP01 -skip-limits-check -agree-to-sap-license 
```

## Systemparameter
sudo sysctl vm.max_map_count=2147483647
sudo sysctl fs.aio-max-nr=18446744073709551615

-agree-to-sap-license
-skip-limits-check


rm -f a4h

# Connecting SAP ECC To Kubernetes

## The Bigger Picture

[Connectivity Proxy](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/connectivity-proxy-for-kubernetes)

## Installing the Docker Image + Kubernetes
https://github.com/SAP-samples/kyma-runtime-extension-samples/tree/main/connectivity-proxy

## Configuration prerequisites
https://help.sap.com/docs/btp/sap-business-technology-platform/configure-sap-btp-connectivity-in-kyma-environment



