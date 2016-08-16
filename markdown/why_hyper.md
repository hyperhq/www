
# _The Best from Both Worlds: VM and Container_

-----------

## Performance

When VMs take tenths of seconds to boot, Hyper is able to launch instances in ***sub-second***. Also, Hyper requires the ***minimal resource footprint***: ~12MB mem, which means higher density: run hundreds of Hyper instances on a server, where a dozens of VMs would overload.

## Secure

Hyper is immune from the "*shared kernel*" problem in containers, because virtualization offers an excellent ***Hardware-enforced Isolation***. The attack surface of a VM instance is quite small, because it lacks of the variety of functions (and, therefore, the potential flaws to be exploited) provided by standard operating systems.

## Portable

Hyper is ***hypervisor agnostic***. [The current implementation](http://gnep.gitbooks.io/hyper/content/release_notes/index.html) supports KVM, with Xen, and more in the roadmap. Combined with [the portability of App Container Image](https://github.com/appc), Hyper allows you to build, ship, and run apps anywhere, without worrying about the infrastructure technology stack.

## Immutable

Hyper eliminates the need for Guest OS. There is no moving part inside of a HyperVM instance to be configured or managed. ***The entire stack is Immutable***.

## BYOK - bring your own kernel

In a multi-tenant environment, the platform must allow developers to pick different kernel and modules. This is an easy job in Hyper, but very hard to do with containers, due to the fact of ”sharing the host kernel".

## Production Ready

Virtualization is mature. Features like LiveMigration, SDN, SDS have been battle-tested for years. With Hyper, you can just ***Plug & Play***. No need to wait another two years for the container-version SDN.

## Better ROI

Virtualization is widely implemented among enterprises. Instead of rebuilding everything with containers, Hyper provides a ***Seamless Integration*** path to your existing virtual infrastructure.

-------

# Summary
The following table gives a more detailed comparision between Container, (traditional) VM and Hyper:

| -  | Container| VM | Hyper |
|---|---|---|---|
| Isolation | Weak, shared kernel | Strong, HW-enforced  | Strong, HW-enforced  |
| Portable  | Yes | No, hypervisor dependent | Yes, hypervisor agnostic and portable image |
| Boot  | Fast, sub-second  | Slow, tenths of seconds  | Fast, sub-second  |
| Performance  | Great | OK| Good, minimal resource footprint and overhead |
| Immutable | Yes  | No, configuration management required | Yes, guest os is gone  |
| Image Size| Small, MBs  | Big, GBs  | Small, MBs  |
| Backward Compatibility | No, brand new world | Great, everything still works  | Good, still a "Machine", much less changes  |
| Maturity   | No  | Yes, production ready, SDN, SDS, LiveMigration, etc.  | Yes, just plug-&-play |
| ROI| Low, rebuild everything with container  | N/A | High, seamless integration with your virtual infrastructure  |

### Find out more in [Hyper docs](http://docs.hypercontainer.io).
