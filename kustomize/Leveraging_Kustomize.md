# Leveraging Kustomize for Kubernetes Manifests.

Source:   [Leveraging **Kustomize** for Kubernetes Manifests](https://learning.oreilly.com/library/view/leveraging-kustomize-for/9781098117078/)


- Kustomize provided a way to create custom versions of manifests via layering on additional changes and producing a separate version with the changes.

- Ideally, you would be able to keep using your existing files in their original format and make variations without making permanent changes or copies. And the differences between versions would be kept small and simple.

- Kustomize is an Apache License 2.0 tool that generates custom versions of manifests by overlaying declarative specifications on top of existing ones. Declarative refers to the standard way to describe resources in Kubernetes: declaring what you want a resource to be and how it should look and behave, in contrast to imperative, which defines the steps to create it.

- ***Overlaying*** describes the process where separate files are layered over (or stacked on top of) each other to create altered versions. Kustomize leverages specific kinds of overlays of the original manifest. The changes to be made in the rendered versions are declared in a separate, dedicated file named kustomization.yaml, while leaving the original files intact.

- Kustomize requires this special file, kustomization.yaml, to drive its behavior. One section of the kustomization.yaml file is dedicated to listing the resources. This section lists the names (and sometimes the paths) of the original manifests to base changes on. When you run a kustomize build command, after loading the resources, Kustomize applies the overlays and renders the result.