# metallb-config

# Step 1 - Install MetalLB Operator
Using OCP console

# Step 2 - Advertise Address Range
```
apiVersion: metallb.io/v1beta1
kind: IPAddressPool
metadata:
  name: ip-addresspool
  namespace: metallb-system
spec:
  addresses:
    - 192.168.50.24/29
  autoAssign: true
  avoidBuggyIPs: false
```
In this example, I am delegating a /29 to MetalLB.  From 192.168.50.25 to 192.168.30