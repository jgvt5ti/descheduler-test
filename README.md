# descheduler-test

Test descheduler for gke using manifests in [descheduler repository](https://github.com/kubernetes-sigs/descheduler)
We mainly tested RemovePodsViolatingTopologySpreadConstraint and confirmed that it worked.

## steps
We assume that there is 3 nodes in each of 3 regions 
1. Deploy nginx in 3 nodes
2. Cordon some node
3. Remove pod in cordoned node
4. Verify that topology constraints are broken
5. Uncordon the node
6. Run descheduler
