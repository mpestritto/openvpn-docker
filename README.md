# Fork Notes

Fork source doesn't forward packets because `net.ipv4.ip_forward=0` by default.

There is a PR that is closed that would have addressed this in the helm chart. 
https://github.com/helm/charts/pull/11852  


Modify your values.yaml to point to this docker repo instead of the original author.
https://github.com/helm/charts/blob/master/stable/openvpn/values.yaml#L12



# openvpn-docker

#### This docker image is *NOT* used by the kubernetes helm chart openvpn: [https://github.com/kubernetes/charts/tree/master/stable/openvpn](https://github.com/kubernetes/charts/tree/master/stable/openvpn).

#### This is a fork to to update to alpine 3.9 and forward packets at the in the container by default.

