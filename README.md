# minishift-addons
Incubator for addons to minishift

## Install
You need to clone this repository and locate yourself on the root directory of your clone

````
git clone https://github.com/jorgemoralespou/minishift-addons.git
cd minishift-addons
````

## kubernetes-dashboard
An addon to install [kubernetes-dashboard](https://github.com/kubernetes/dashboard)

If you want to install this addon once for your running minishift VM instance (if you have cloned this repo):

````
minishift addons apply kube-dashboard
````

or permantently:

````
minishift addons install kube-dashboard
````

This will install the dashboard everytime you create a new minishift VM instance.

