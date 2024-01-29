# Cloud-init configuration to install eBPF bcc tools

Build an Ubuntu VM using `Multipass` with `bcc` tools installed using:

```bash
multipass launch -n eBPF --cloud-init cloud-config-ebpf-bcc.yaml --timeout 3600 -c 2 -m 8G -d 10G
```

After the VM spins up, you can use `multipass shell eBPF` to login in to the VM. The `bcc` build folder is under `/root`.

## Teardown
To teardown the VM, run `multipass delete test && multipass purge`.
