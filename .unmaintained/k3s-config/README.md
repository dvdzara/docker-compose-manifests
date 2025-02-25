# k3s configuration

To install server or agent nodes copy all the files in the `var` and `etc`
directories to the system and then follow the instructions inside the
`server.yaml` or `agent.yaml` files.

If you want to restrict the load balacer creation only to certain nodes, set the
`svccontroller.k3s.cattle.io/enablelb=true` label on them.
