
CKA is designed to test if the candidates have enough knowledge and skills to be K8s administrators. You need to know what skills and abilities the CKA expect the candidates to demonstrate in the exam so that you can align your daily practices with these requirements accordingly during preparation.

Be sure to read the CNCF CKA Exam Curriculum to understand what’s included in the CKA exam. The curriculum may change a little bit along with every K8s release; here is the outline when I take the exam:

-   25% — Cluster Architecture, Installation & Configuration
-   15% — Workloads & Scheduling
-   20% — Services & Networking
-   10% — Storage
-   30% — Troubleshooting

The CKA exam is two hours long. The examinee needs to solve 17 questions during the exam. In each question, there is a given scenario and a problem to solve. Most questions are not so straightforward, and the candidate often needs 3 or 4 steps to finish one question. So the time is quite tight. You need to use the time smartly and effectively without wasting time waiting, searching, or any things not directly related to problem-solving.

Perseverance leads to success. I strongly suggest you don’t skip a single day because if you skip one day and make an exception, there’s a good chance that it will be a second time, a third time…. You’ll fall into a spiral of missing practice and regret, and this kind of negative emotion does not help you pass the exam.

## Courses
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)
- How to prepare for the CKA Exam [Link](https://kube.academy/courses/how-to-prepare-for-the-cka-exam)
- 

## Links
- Training and Certification [Link](https://docs.linuxfoundation.org/tc-docs/)
- Kubernetes The Hard Way [Link](https://github.com/kelseyhightower/kubernetes-the-hard-way)
- How to Pass the Certified Kubernetes Administratos (CKA) Exam Without Any Stress? [Link](https://www.zhaohuabing.com/post/2022-02-08-how-to-prepare-cka-en/)
- CKA Exam Study Guide: A Complete Resource for CKA Aspirants [Link](https://devopscube.com/cka-exam-study-guide/)
- 
- https://github.com/alijahnas/CKA-practice-exercises 
- https://github.com/walidshaari/Kubernetes-Certified-Administrator
- https://github.com/StenlyTU/K8s-training-official
- https://github.com/ramitsurana/awesome-kubernetes

## Books
- The book _**Kubernetes in action**_ gives good general overview. The book can be [_downloaded_](https://github.com/indrabasak/Books/blob/master/Kubernetes%20in%20Action.pdf) from Internet.
- 

## Day 1
- Review Linux Foundation Certification Exam: Candidate Handbook. [Link](https://docs.linuxfoundation.org/tc-docs/certification/lf-handbook2)
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Core Concepts.


## Day 2

### RESOURCES
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Scheduling.
- https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/
- Kubernetes 101 - Kubernetes scheduler [Link](https://dominik-tornow.medium.com/the-kubernetes-scheduler-cd429abac02f)
- A Deep Dive into Kubernetes Scheduling. [Link](https://thenewstack.io/a-deep-dive-into-kubernetes-scheduling/)
- A Brief Analysis on the Implementation of the Kubernetes Scheduler. [Link](https://www.alibabacloud.com/blog/a-brief-analysis-on-the-implementation-of-the-kubernetes-scheduler_595083)
- 


> A scheduler watches for newly created Pods that have no Node assigned. For every Pod that the scheduler discovers, the scheduler becomes responsible for finding the best Node for that Pod to run on.

We can think of the Scheduler task as choosing the best place to allocate the required resources. A placement is a [partial](https://en.wikipedia.org/wiki/Partial_function), [non-injective](https://en.wikipedia.org/wiki/Injective_function) assignment of a set of Pods to a set of Nodes.

![[./images/kubernetes_cheduler.png]]


### Manual scheduling

### Labels and Selectors

### Taints and Tolerations

### Node Selectors

### Node Affinity

### Resource Limits

### Demonsets

### Static pods


### Multiple Schedulers


### Configuring Scheduler Profiles
- https://kubernetes.io/docs/reference/scheduling/config/ 


## Day 3
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Logging & Monitoring.

## Day 4
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Application Lifecycle Management.

## Day 5
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Cluster Maintenance.


## Day 6
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Security.

## Day 7
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Storage.

## Day 8
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Networking.

## Day 9
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Design and install Kubernetes.

## Day 10
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Install.

## Day 11
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Troubleshooting.

## Day 12
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Other Topics.

## Day 13
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Lightning Labs.

## Day 14
- CKA Certification Course - Certified Kubernetes Administrator. [Link](https://kodekloud.com/courses/certified-kubernetes-administrator-cka/)  Mock Exams.



## Some Tips for the exam

### Define aliases for the most frequently used kubectl commands
I use the following aliases in the exam:
```bash
alias k=kubectl 
alias kgp="k get pod" 
alias kgd="k get deploy" 
alias kgs="k get svc" 
alias kgn="k get nodes" 
alias kd="k describe" 
alias kge="k get events --sort-by='.metadata.creationTimestamp' |tail -8"
```

### Enable kubectl auto-completion
```bash 
source <(kubectl completion bash) 
echo "source <(kubectl completion bash)" >> ~/.bashrc
```

### Use the short name of K8s Resources instead of the full name.
| **Short name** | **Full name**          | **Short name** | **Full name**               |
| ---------- | ------------------ | ---------- | ----------------------- |
| cm         | configmaps         | ds         | daemonsets              |
| deploy     | deployment         | ep         | endpoints               |
| ev         | events             | hpa        | horizont pod autoscales |
| ing        | ingresses          | limits     | limitranges             |
| ns         | namespaces         | no         | nodes                   |
| pvc        | persistentvolumnes | po         | pods                    |
| rs         | replicasets        | rc         | replication controller  |
| sa         | serviceaccounts    | quota      | resource quotas         |
| svc        | services           |            |                         | 

### Use dry-run to generate yaml
During the exam, candidates will be asked to create some K8s resources such as pods, deployments, services, and so on. Writing yaml files for these resources from scratch is not only time consuming, but it is also difficult to remember the entire structure of a resource. You can use dry run to generate a basic yaml file, then make any necessary changes on that file, and then use the modified file to create the required resources.
```shell
k run ngix --image=nginx --dry-run=client -o yaml > nginx.yaml
```
To save time, we can define a shell variable:
```shell
export do="--dry-run=client -o yaml"
k run nginx --image=nginx $do > nginx.yaml
```

### Delete pods without waiting
Oftentimes we need to delete pods during CKA exams. k8s delete pods gracefully, which means that the kubectl command will wait until the relevant resources have been cleaned up, sometimes causing kubectl hang for a few minutes. So to minimize the wait time for deletion, we can force delete pods.
```shell
kubectl delete pod nginx --force --grace-period 0

export now="--force --grace-period o"
k delete pod nginx $now
```

### Use kubectl help to view examples of creating resources
The output of the `kubectl command --help` provides a number of common examples that can be copied and used in the exam with only minor modifications. Using this command saves you a great amount of time searching through the enormous k8s online documentation.

```shell
kubectl run --help
Create and run a particular image in a pod.

Examples:
  # Start a nginx pod
  kubectl run nginx --image=nginx

  # Start a hazelcast pod and let the container expose port 5701
  kubectl run hazelcast --image=hazelcast/hazelcast --port=5701

  # Start a hazelcast pod and set environment variables "DNS_DOMAIN=cluster" and "POD_NAMESPACE=default" in the
container
  kubectl run hazelcast --image=hazelcast/hazelcast --env="DNS_DOMAIN=cluster" --env="POD_NAMESPACE=default"

  # Start a hazelcast pod and set labels "app=hazelcast" and "env=prod" in the container
  kubectl run hazelcast --image=hazelcast/hazelcast --labels="app=hazelcast,env=prod"

  # Dry run; print the corresponding API objects without creating them
  kubectl run nginx --image=nginx --dry-run=client

  # Start a nginx pod, but overload the spec with a partial set of values parsed from JSON
  kubectl run nginx --image=nginx --overrides='{ "apiVersion": "v1", "spec": { ... } }'

  # Start a busybox pod and keep it in the foreground, don't restart it if it exits
  kubectl run -i -t busybox --image=busybox --restart=Never

  # Start the nginx pod using the default command, but use custom arguments (arg1 .. argN) for that command
  kubectl run nginx --image=nginx -- <arg1> <arg2> ... <argN>

  # Start the nginx pod using a different command and custom arguments
  kubectl run nginx --image=nginx --command -- <cmd> <arg1> ... <argN>
  ```

### Use kubectl explain to view the definition of a resource

The kubectl help command gives you examples of how to create a resource, but the help command only shows some common options and does not provide a complete structure for that resource. If we need to see the definition of a k8s resource, one way is to search in the k8s online documentation, but the search function in the K8s documentation is not very user-friendly and you may need to click multiple times, jump from pages to find the correct link. A more effecitve way is to use the kubectl explain command.

```shell
k explain pod.spec //View the pod spec definition 
k explain pod.spec.containers //View the containers definition 
k explain pod.spec.containers.resources //View the container resources definition k explain pod.spec.containers.resources.limits //View the containter resources limits definition
```
