# Fork Notes

Fork source doesn't forward packets because `net.ipv4.ip_forward=0` by default.

There is a PR that is closed that would have addressed this in the helm chart. 
https://github.com/helm/charts/pull/11852  


Modify your values.yaml to point to this docker repo instead of the original author.
https://github.com/helm/charts/blob/master/stable/openvpn/values.yaml#L12



# openvpn-docker

#### This is the docker image used by the kubernetes helm chart openvpn: [https://github.com/kubernetes/charts/tree/master/stable/openvpn](https://github.com/kubernetes/charts/tree/master/stable/openvpn).

#### There is not much here other than a base alpine image with packages needed to run openvpn: openssl, easy-rsa, openvpn, and iptables.  Much of the configuration is done through kubernetes and helm. Please refer to the scripts [here](https://github.com/kubernetes/charts/blob/master/stable/openvpn/templates/config-openvpn.yaml) for better understanding.

#### That chart originally used a base Alpine image, but the Alpine repositories worked inconsistently so this image was created to remove a point of failure.
