# sable-nets

| Net name | Arch | Schedule | Dataset | Tests | Notes |
| --- | --- | --- | --- | --- | --- |
| [sable-dev-net-1](nets/sable-dev-net-1.bin) | `((768 PSQT)x1hm -> 512)x2 -> ((SCOREx1))` | 1 stage, 240 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] | -100 elo at 25K nodes | Soft nnue reset back to 512hl with no extra features |
| [sable-dev-net-2](nets/sable-dev-net-2.bin) | `((768 PSQT)x1hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] | +58 elo at 25K nodes, +18 elo at STC, +28 elo at LTC | Testing higher hl with no other changes |
| [sable-dev-net-3](nets/sable-dev-net-3.bin) | `((768 PSQT)x2hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] | +23 elo at 25K nodes, -10 at STC | Testing 2 input buckets |
| [sable-dev-net-4](nets/sable-dev-net-4.bin) | `((768 PSQT)x4hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] | | Testing 4 input buckets |

[goliath-data]: https://openbench.nocturn9x.space/training/datasets/73a22972-7710-4e89-b90b-a9e70fa77ce7/

Dataset registered by Ellie: `EllieSilverrzz/sable-goliath-data`, revision/commit `7108685641ae60f29025ed5c597b7e15c13f4bf2` (2 files, 7.0 GB).
