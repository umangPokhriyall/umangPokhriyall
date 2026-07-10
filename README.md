### Umang Pokhriyal

Self-taught systems engineer. Rust, low-latency, OS internals, applied cryptography.

I build falsifiable proof-of-work. Every performance claim below traces to a committed benchmark, and
I publish the results that underperformed as plainly as the ones that worked. The five repos aren't
unrelated projects. They're the disassembled parts of one system I'm building toward: a microVM-based
agent sandbox. Each part is built and measured on its own first.

**Site and writeups:** https://umangpokhriyall.github.io

| Repo | The one result | Source |
|---|---|---|
| **[frost-ed25519-kit](https://github.com/umangPokhriyall/frost-ed25519-kit)** | Shipped a threshold signer, audited it, then forged it on purpose: a valid signature on a message no honest session signed, ~50 ms. Rebuilt to RFC 9591 FROST, checked byte-for-byte. | `legacy/results/ros_forgery.txt` |
| **[low-latency-lob](https://github.com/umangPokhriyall/low-latency-lob)** | The "optimal" flat-array order book went from best on synthetic load to **288× slower than a BTreeMap on real BTCUSDT**. The CPU counters say why: one book is memory-bound, the other branch-mispredict-bound. | `bench/results/throughput.csv` |
| **[Rust-Tcp-Server](https://github.com/umangPokhriyall/Rust-Tcp-Server)** | 11 server models behind one sans-IO core, benchmarked to a true C10K. io_uring cuts syscalls/req in half (2.02 vs 4.03) and **still sheds load on a single ring**. 2× fewer syscalls isn't 2× throughput. | `bench/results/c10k_summary.csv` |
| **[Coingate](https://github.com/umangPokhriyall/Coingate)** | Exactly-once over an at-least-once stream. A chaos harness fires a crash at **every statement boundary × every redelivery schedule**: 0 conservation violations, 1 send per withdrawal, at READ COMMITTED. | `chaos/results/summary.md` |
| **[proctor](https://github.com/umangPokhriyall/proctor)** | A scheduler whose decision takes 400 ns but whose dispatch takes 890 µs, because it pays 2N+4 Redis round-trips. Measured on silicon, then explained. Plus verification math and a threat model that states what crypto can't do. | `bench/results/metal-m4-large/sched/` |

Measured on rented AMD EPYC bare metal where the claim depends on hardware; the crypto and
exactly-once results are hardware-independent and reproduce anywhere. Each repo says which is which.

Open to systems and infrastructure roles.
