gearman-plugin-client
=====================

A client to use with the Jenkins Gearman plugin


Usage
=====

get help:
  gear_client.py --help

send jobs to a gearman server:
  python gear_client.py -s MyGearmanHost --function=build:MyProject

run multiple jobs:
  python gear_client.py -s MyGearmanHost --function=build:MyProject --jobs=10
  
wait for last job to complete:
  python gear_client.py -s MyGearmanHost --wait --function=build:MyProject --jobs=10
  
pass in parameters:
  python gear_client.py -s MyGearmanHost --function=build:MyProject --params='{"OFFLINE_NODE_WHEN_COMPLETE":"false","param1":"moon","param1":"sun"}'

