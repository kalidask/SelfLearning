# Deployment.yml

Generic Application template for Deploying Images to Openshift

Use below command to deploy your application image:

oc process -f deployment.yml | oc create -f -


# AutoScaler.yml

This template is for enabling the autoscaling for applications deployed on OpenShift

it is based on the "Deployment" object and it scaled based on 2 metrics resource Memory & CPU.

Use below command to apply this template against your autoscale application:

oc process -f autoscaler.yml -p APPLICATION_NAME=helloworld -p NAMESPACE=core -p MINPOD=1 -p MAXPOD=4 | oc create -f -



