# Overview 

The folder contains a set of [github actions](https://github.com/features/actions) workflows that showcase how to integrate Dynatrace into software delivery workflows.

This was demonstrated in [this](https://www.youtube.com/watch?v=nBs2P7Idtz0) Monitor and modernize Azure operations with Dynatrace webinar starting at minute 25. 

[![Monitor and modernize Azure operations with Dynatrace webinar](https://img.youtube.com/vi/nBs2P7Idtz0/0.jpg)](https://www.youtube.com/watch?v=nBs2P7Idtz0)

# Demo Workflows

The set workflows are designed to show one step or the entire set of steps within this this representative pipeline diagram.

![app](./images/workflow.png)

| Step | Workflow Name | Comment |
| ---- | ------------------- | -------- |
| B | Keptn service onboarding | Demos this [image](https://github.com/keptn-sandbox/keptn-quality-gate-bash) that will onboard a demo service to [keptn](https://www.keptn.sh). All supporting files are in the `keptn` subfolder.|
| C | Monaco | Demos the [Dynatrace Monitoring as Code](https://github.com/dynatrace-oss/dynatrace-monitoring-as-code) framework (a.k.a. monaco).  All supporting files are in the `monaco` subfolder. |
| E | Keptn Automated SLO evaluation | Demos this [image](https://github.com/keptn-sandbox/keptn-quality-gate-bash) that will perform an automated SLO evaluation.   |
| F | Dynatrace GitHub Action | Demos this [GitHub Action](https://github.com/marketplace/actions/dynatraceaction) lets you send events [Dynatrace Custom metrics](https://www.dynatrace.com/news/blog/simplify-observability-for-all-your-custom-metrics-part-2-oneagent-metric-api/) about the GitHub workflow executions | 
| A,D | Deploy All | Demos the the deployment of the [Dynatrace Orders Demo Application](https://github.com/dt-orders/overview) to an Azure Kubernetes cluster.  Also calls the Dynatrace GitHub Action to send deployment events to Dynatrace. All supporting files are in the `manifests` subfolder. |
| A,D | Deploy Order | Same as "Deploy All" workflow, but just deploys the "order" service. |


# Demo Setup

1. [Dynatrace tenant](https://www.dynatrace.com/trial)
1. [Keptn](https://www.keptn.sh) installed with Dynatrace monitoring service
1. AKS Cluster installed with [Dynatrace Operator](https://www.dynatrace.com/support/help/technology-support/cloud-platforms/kubernetes/).  For my cluster I ran:
    ```
    az aks create --resource-group $RESOURCE_GROUP --name $RESOURCE_GROUP \
    --node-count 2 --enable-addons monitoring --generate-ssh-keys
    ```
1. github secrets were setup that are referenced in the workflows
    * `AZURE_CREDENTIALS` - JSON output from `az ad sp create-for-rbac` command
    * `DT_API_TOKEN` - API token with permission required by the Dynatrace action and Keptn onboard project container
    * `DT_BASE_URL` - Dynatrace URL such as `https://abc.live.dynatrace.com`
    * `KEPTN_API_TOKEN` - Keptn API Token
    * `KEPTN_BASE_URL` -  Keptn URL used by Keptn Bridge and API calls