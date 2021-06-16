# Overview 

The folder contains demo [github actions](https://github.com/features/actions) workflows that showcase how to integrate Dynatrace into software delivery workflows.

# Workflows

| Workflow Name | Comment |
| ------------------- | -------- |
| Deploy Order | Demos the the deployment of the [Dynatrace Orders Demo Application](https://github.com/dt-orders/overview) order service to an Azure Kubernetes cluster. Also calls the Dynatrace GitHub Action to send deployment events to Dynatrace. All supporting files are in the `manifests` subfolder. |
| Deploy All | Demos the the deployment of the [Dynatrace Orders Demo Application](https://github.com/dt-orders/overview) to an Azure Kubernetes cluster.  Also calls the Dynatrace GitHub Action to send deployment events to Dynatrace. All supporting files are in the `manifests` subfolder. |
| Monaco | Demos the [Dynatrace Monitoring as Code](https://github.com/dynatrace-oss/dynatrace-monitoring-as-code) framework (a.k.a. monaco).  All supporting files are in the `monaco` subfolder. |
| Dynatrace GitHub Action | Demos this [GitHub Action](https://github.com/marketplace/actions/dynatraceaction) lets you send events and metrics to a Dynatrace monitoring environment from a GitHub workflow. | 
| Keptn service onboarding | Demos this [image](https://github.com/keptn-sandbox/keptn-quality-gate-bash) that will onboard a demo service to [keptn](https://www.keptn.sh). All supporting files are in the `keptn` subfolder.|
| Keptn Automated SLO evaluation | Demos this [image](https://github.com/keptn-sandbox/keptn-quality-gate-bash) that will perform an automated SLO evaluation.   |

