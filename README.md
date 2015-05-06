gearman-plugin-client
=====================

A client to use with the [Jenkins Gearman plugin] (https://wiki.jenkins-ci.org/display/JENKINS/Gearman+Plugin).

Only works on Linux

Help
----
  python gear_client.py --help


Usage
-----

To run a build:

    python gear_client.py -s MyGearmanSever --function=build:myProject

To run the same job multiple times (with parameters):

    python gear_client.py -s MyGearmanSever --function=build:myProject --iterations=4 \
          --params='{"OFFLINE_NODE_WHEN_COMPLETE":"false","param1":"moon","param1":"sun"}'

To stop/abort a build:

    python gear_client.py -s MyGearmanSever --function=stop:MyGearmanSever \
          --params='{"name":"myProject","number":"130"}'

To update the build description:

    python gear_client.py -s MyGearmanSever --function=set_description:MyGearmanSever \
          --params='{"name":"myProject","number":"105","html_description":"<h1>My New Description</h1>"}'

To run a build and immediately set the slave offline:

    python gear_client.py -s MyGearmanSever --function=build:myProject \
          --params='{"OFFLINE_NODE_WHEN_COMPLETE":"true"}'
