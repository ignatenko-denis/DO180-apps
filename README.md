# DO180-apps
DO180 Repository for Sample Applications

## DO180: Red Hat OpenShift I: Containers & Kubernetes

Download OpenShift CLI
```sh
https://docs.openshift.com/container-platform/4.8/cli_reference/openshift_cli/getting-started-cli.html
```

Login in web console
https://console-<YOUR_URL>

Open Menu item "Copy Login Command" like that 
```sh
oc login --token=<YOUR_TOKEN> --server=https://<YOUR_URL>
```

check OpenShift status
```sh
oc status
```

create new project
```sh
oc new-project myproject
```

create new app in 'myproject'
```sh
oc new-app mysql MYSQL''_USER=user MYSQL_PASSWORD=pass MYSQL_DATABASE=testdb -l db=mysql
```

create another new app
```sh
oc new-app https://github.com/openshift/ruby-hello-world --name=ruby-hello
```

view all cluster components (installed apps)
```sh
oc get all
```

view detail info about the component
```sh
oc describe <ANY_OPENSHIFT_NAME>
```

list of pods
```sh
oc get pods
```

view POD detail info
```sh
oc describe pod <POD_NAME>
```

list of services
```sh
oc get svc
```

detail info about service
```sh
oc describe service mysql
```
