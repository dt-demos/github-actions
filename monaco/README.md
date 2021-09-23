# Overview

The scripts use a combination of [Dynatrace Monitoring as Code](https://github.com/dynatrace-oss/dynatrace-monitoring-as-code)

## set these before running monaco
export DT_BASE_URL=     # for example https://ABC.live.dynatrace.com
export DT_API_TOKEN=    # your API token with V2: SLO read/write & V1: read/write config & access problem/event feed
export NEW_CLI=1

## to run moanco
monaco deploy -v -e environments.yml ./projects

## To delete config

1. rename projects/delete.txt to projects/delete.yaml 
1. rerun monaco.  
1. Then rename file back to projects/delete.txt