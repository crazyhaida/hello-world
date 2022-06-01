# Deploying deploymentConfig on openshift

## hello-world project using go languange

## Deploy the Hello World image on openshift
oc new-app https://github.com/crazyhaida/hello-world.git --name demo-app --as-deployment-config=true

## Follow build progress (Git only)
oc logs -f bc/hello-world

# Get more information about a DeploymentConfig

## Describe the DC to get its labels
oc describe dc/hello-world

## Get the full YAML definition
oc get -o yaml dc/hello-world


## Deleting all oc new-app resources

## Delete all application resources using labels (get them from oc describe)
oc delete all -l app=hello-world
