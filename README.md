# Overview 

The folder contains demo [github actions](https://github.com/features/actions) workflows that showcase how to integrate Dynatrace into software delivery workflows.

Here is a YouTube video demo:

[![YouTube Video](https://img.youtube.com/vi/sr_bKKfEKFA/0.jpg)](https://www.youtube.com/watch?v=sr_bKKfEKFA)

# Workflows

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
