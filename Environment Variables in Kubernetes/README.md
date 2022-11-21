### Question : There are a number of parameters that are used by applications. We need to define these as environment variables so that we can use them as needed within different configs. Below is a scenario which needs to be configured on Kubernetes cluster. Please find below more details about it.

* Create a namespace named as fieldref-namespace.

* Create a pod named envars-fieldref under the namespace fieldref-namespace.

* Configure spec as the container name should be fieldref-container, use image httpd preferable latest tag, use command 'sh', '-c' and args should be
'while true; do echo -en '/n'; printenv NODE_NAME POD_NAME POD_NAMESPACE; printenv POD_IP POD_SERVICE_ACCOUNT; sleep 10; done;'
**(Note: please take care of indentations)**

### Define four environment variables as mentioned below:

1. The first env should be named as NODE_NAME, set valueFrom fieldref and fieldPath should be spec.nodeName.

2. The second env should be named as POD_NAME, set valueFrom fieldref and fieldPath should be metadata.name.

3. The fourth env should be named as POD_IP, set valueFrom fieldref and fieldPath should be status.podIP.

4. The fifth env should be named as POD_SERVICE_ACCOUNT, set valueFrom fieldref and fieldPath shoulbe be spec.serviceAccountName.

Set restart policy to Never.

To check the output, exec the pod and use printenv command.

