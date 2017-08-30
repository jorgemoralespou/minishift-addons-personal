# Cloud Native Labs for OpenShift Roadshow Add-on
An addon to install [OpenShift's Roadshow Cloud Native Labs](https://github.com/openshift-roadshow/cloud-native-labs) and [guide](https://github.com/openshift-roadshow/cloud-native-guides).

Verify you have installed these addons, by following the [general readme](../../Readme.adoc#download-and-use-community-add-ons).

## Deploy cockpit
To deploy cockpit

```
$ minishift addon apply cockpit
```

## Use cockpit
Find cockpit console at the following URL:

```
$ minishift openshift service openshift-cockpit -n cockpit
```

You will need to log in with same user and creadentials as to OpenShift

## Delete cockpit
To delete cockpit, just do:

```
$ oc delete oauthclients/cockpit-oauth-client project/cockpit --as=system:admin
```
