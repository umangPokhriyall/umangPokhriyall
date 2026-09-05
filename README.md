### Umang Pokhriyal

Linux virtualization. Working on
[Cloud Hypervisor](https://github.com/cloud-hypervisor/cloud-hypervisor), in Rust.
B.Tech CSE 2026.

Long-form writeups: https://dev.to/umang_up

### Upstream

Cloud Hypervisor (Linux Foundation, Rust VMM) - virtio-net multiqueue, tap/tun, seccomp.

- [#8735](https://github.com/cloud-hypervisor/cloud-hypervisor/pull/8735) merged - document userfaultfd permissions for on-demand restore
- [#8755](https://github.com/cloud-hypervisor/cloud-hypervisor/pull/8755) merged - reject MQ pair counts above `max_virtqueue_pairs`
- [#8772](https://github.com/cloud-hypervisor/cloud-hypervisor/pull/8772) open, maintainer-approved - honour the negotiated queue pair count

### Projects

Every performance or security claim links to the benchmark, experiment, or test that produced it.

| Repo | The one result | Source |
|---|---|---|
| **[frost-ed25519-kit](https://github.com/umangPokhriyall/frost-ed25519-kit)** | Built an RFC 9591 FROST threshold signer after demonstrating a practical ROS forgery against the original implementation. Includes differential testing, fuzzing, and documented threat model. | `legacy/results/ros_forgery.txt` |
| **[low-latency-lob](https://github.com/umangPokhriyall/low-latency-lob)** | Explores data-structure tradeoffs in matching engines. A flat-array order book that excelled on synthetic workloads became 288× slower than a BTreeMap under real BTCUSDT traffic, with hardware counters explaining why. | `bench/results/throughput.csv` |
| **[Rust-Tcp-Server](https://github.com/umangPokhriyall/Rust-Tcp-Server)** | Compares 11 server architectures built on a shared sans-IO core. Shows that reducing syscall count alone does not guarantee higher throughput under C10K workloads. | `bench/results/c10k_summary.csv` |
| **[Coingate](https://github.com/umangPokhriyall/Coingate)** | Implements exactly-once withdrawal processing over an at-least-once event stream and validates it with exhaustive crash-injection testing. | `chaos/results/summary.md` |
| **[proctor](https://github.com/umangPokhriyall/proctor)** | Studies scheduler latency, verification cost, and distributed coordination, including a measured analysis of Redis round-trip overhead and accompanying security model. | `bench/results/metal-m4-large/sched/` |

Measured on rented AMD EPYC bare metal where the claim depends on hardware; the crypto and
exactly-once results are hardware-independent and reproduce anywhere. Each repo says which is which.

Open to remote systems and infrastructure roles.
