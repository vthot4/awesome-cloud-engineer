# Kustomize Problem Statement & Ideology (Notes)

We want to start off by going over what problems it tries to address and why it was ultimately created. Let's take a look at simple example:

In this case, we have this Nginx deployment YAML file:
```yaml
apiVersoion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 1
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        component: nginx
    spec:
      containers:
      - name: nginx
        image: nginx
```

Let's say that we have multiple environments. We're going to have one for development, wich is developing on our local machine, one for staging, and then ultimately one for our production environment.

![[./images/nginx_envs.png]]

Let's say that we want to customize our deployment so that it behaves a little bit differently in each one of our environments.

```Shell
		replicas: 1    # dev environment
		replicas: 2|3  # stg environment
		replicas: 5|10 # prod environment   
```

How do we actually go about modifying the different configurations on a per-environemnt basis.
One of the simplest solutions to this problem is to create three separate directories, one for each environment. 

🗂️  dev 

🗂️  stg

🗂️  prod


