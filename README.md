### Umang Pokhriyal

Systems engineer focused on Rust, distributed systems, low-latency infrastructure, and applied cryptography.

I build projects to answer concrete engineering questions, measure the results, and publish both the successes and the failures. Every performance or security claim links to the benchmark, experiment, or test that produced it.

I'm self-taught, and this profile is my public engineering notebook. Everything here is intended to be cloned, reproduced, and inspected.

Website & long-form writeups: https://umangpokhriyall.github.io

| Repo | The one result | Source |
|---|---|---|
| **[frost-ed25519-kit](https://github.com/umangPokhriyall/frost-ed25519-kit)** | Built an RFC 9591 FROST threshold signer after demonstrating a practical ROS forgery against the original implementation. Includes differential testing, fuzzing, and documented threat model. | `legacy/results/ros_forgery.txt` |
| **[low-latency-lob](https://github.com/umangPokhriyall/low-latency-lob)** | Explores data-structure tradeoffs in matching engines. A flat-array order book that excelled on synthetic workloads became 288× slower than a BTreeMap under real BTCUSDT traffic, with hardware counters explaining why. | `bench/results/throughput.csv` |
| **[Rust-Tcp-Server](https://github.com/umangPokhriyall/Rust-Tcp-Server)** | Compares 11 server architectures built on a shared sans-IO core. Shows that reducing syscall count alone does not guarantee higher throughput under C10K workloads. | `bench/results/c10k_summary.csv` |
| **[Coingate](https://github.com/umangPokhriyall/Coingate)** | Implements exactly-once withdrawal processing over an at-least-once event stream and validates it with exhaustive crash-injection testing. | `chaos/results/summary.md` |
| **[proctor](https://github.com/umangPokhriyall/proctor)** | Studies scheduler latency, verification cost, and distributed coordination, including a measured analysis of Redis round-trip overhead and accompanying security model. | `bench/results/metal-m4-large/sched/` |

Measured on rented AMD EPYC bare metal where the claim depends on hardware; the crypto and
exactly-once results are hardware-independent and reproduce anywhere. Each repo says which is which.

Open to systems and infrastructure roles.
