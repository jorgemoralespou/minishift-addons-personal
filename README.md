
FOR THE SUPPORTED ADDONS, GO TO: https://github.com/minishift/minishift-addons

# minishift-addons
Incubator for addons to minishift

## Install
You need to clone this repository and locate yourself on the root directory of your clone

````
git clone https://github.com/jorgemoralespou/minishift-addons.git
cd minishift-addons
````

## helm
Installs helm tiller into minishift

To access it:

````
To use helm, provide the minishift host to your helm config

e.g.
   helm init --host #{ip}:8443 -c

And remember to have repositories configured, else add them:

e.g.
   helm repo add stable https://kubernetes-charts.storage.googleapis.com
   helm search
````

NOTE: You might need to have minishift admin context selected

