# sable-nets

| Net name | Arch | Schedule | Dataset | Tests | Notes |
| --- | --- | --- | --- | --- | --- |
| [sable-dev-net-1](nets/sable-dev-net-1.bin) | `((768 PSQT)x1hm -> 512)x2 -> ((SCOREx1))` | 1 stage, 240 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | -100 elo at 25K nodes | Soft nnue reset back to 512hl with no extra features |
| [sable-dev-net-2](nets/sable-dev-net-2.bin) | `((768 PSQT)x1hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | +58 elo at 25K nodes, +18 elo at STC, +28 elo at LTC | Testing higher hl with no other changes |
| [sable-dev-net-3](nets/sable-dev-net-3.bin) | `((768 PSQT)x2hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | +23 elo at 25K nodes, -10 at STC | Testing 2 input buckets |
| [sable-dev-net-4](nets/sable-dev-net-4.bin) | `((768 PSQT)x4hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | | Testing 4 input buckets |
| [sable-dev-net-5](nets/sable-dev-net-5.bin) | `((768 PSQT)x8hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | | Testing 8 input buckets |
| [sable-dev-net-6](nets/sable-dev-net-6.bin) | `((768 PSQT)x8hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; linear WDL from 0 to 0.4 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | | Testing linear WDL from 0 to 0.4 |
| [sable-dev-net-7](nets/sable-dev-net-7.bin) | `((768 PSQT)x8hm -> 1024)x2 -> ((SCOREx4))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; linear WDL from 0 to 0.4 | [Sable Goliath Data][goliath-data] (only the most recent 2.1B positions of 12ksn data) | | Testing 4 output buckets |
| [sable-dev-net-10](nets/sable-dev-net-10.bin) | `((768 PSQT)x1hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | All 12.17B positions ever generated | | Identical to net 2 except for the dataset |
| [sable-dev-net-11.1](nets/sable-dev-net-11.1.bin) | `((768 PSQT)x1hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 960 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | All 12.17B positions ever generated | | Identical to net 10 except trained on 960 SB instead of 480 |

[goliath-data]: https://openbench.nocturn9x.space/training/datasets/73a22972-7710-4e89-b90b-a9e70fa77ce7/

Dataset registered by Ellie: `EllieSilverrzz/sable-goliath-data`, revision/commit `7108685641ae60f29025ed5c597b7e15c13f4bf2` (2 files, 7.0 GB).
