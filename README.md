# kvmalloc

## Getting Started
This script is intended to be utilized with KVM hypervisors to determine their current storage and memory allocations.

## Prerequisites

KVM hypervisor(s) set up with [Libvirt](https://libvirt.org)

Hypervisor(s) set up with a common domain and [Libvirt](https://libvirt.org) storage pool name.

## Usage

Download the script to a location from which your hypervisor(s) can be connected to through `virsh -c qemu+tls//$DOMAIN/system`. 

Modify the values at the top of the script under `MODIFY` to reflect your setup. 

Then run the following:

```bash
echo "LIST OF SPACE SEPERATED HOSTNAMES" | ./pathtoscript/kvmalloc
```

## Output Example

```bash
echo "LIST OF SPACE SEPERATED HOSTNAMES" | ./kvmalloc

HOST: FQDN PRINTED HERE
STORAGE:  Capacity:  797.22 GiB    Allocation:  630.03 GiB    Available:    167.18 GiB
MEMORY:   Total:     32674.30 MiB  Allocated:   29744.00 MiB  Unallocated:  2930.30 MiB

HOST: FQDN PRINTED HERE
STORAGE:  Capacity:  557.47 GiB    Allocation:  550.03 GiB    Available:    7.44 GiB
MEMORY:   Total:     65526.10 MiB  Allocated:   26456.00 MiB  Unallocated:  39070.10 MiB
```

## Authors

* **Megan Steeley** - [megdorkable](https://github.com/megdorkable)
