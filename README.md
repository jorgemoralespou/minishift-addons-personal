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

## cors
An addon that will enable Cross-Origin resources from any source

## kubernetes-dashboard
An addon to install [kubernetes-dashboard](https://github.com/kubernetes/dashboard)

To access it:

````
minishift openshift service dashboard -n kube-dashboard
````

## cockpit
An addon to install [cockpit](http://cockpit-project.org/).

To access it:

````
minishift openshift service openshift-cockpit -n cockpit
````

## prometheus
An addon that will deploy Prometheus. 

NOTE: Requires Origin >= 3.6.0-rc.0

You should provide the namespace where it will be installed with the addon-env namespace, like this:

````
minishift addon apply prometheus --addon-env namespace=kube-system
````

To access it:

````
minishift openshift service prometheus -n <namespace>
````

# Install or enable
You need to install the addon:

````
minishift addons install <addon-name>
````

If you want to enable an addon once for your running minishift VM instance (if you have cloned this repo):

````
minishift addons apply <addon-name>
````

or permantently:

````
minishift addons enable <addon-name>
````

This will enable the addon everytime you create a new minishift VM instance.

