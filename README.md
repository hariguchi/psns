# psns - ps for Linux namespaces

Regular **ps** command does not show the namespace to which
each process belongs to. This script shows it like as follows:

```
# psns
32365 ns1 /sbin/dhclient veth1
32375 ns2 /sbin/dhclient veth2
```

Both **ns1** and **ns2** are the names of Linux
namespaes. I.e., The commands above were invoked like as
follows:

```
# ip netns exec ns1 /sbin/dhclient veth1
# ip netns exec ns2 /sbin/dhclient veth2
```
