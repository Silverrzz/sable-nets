# sable-nets

| Net name | Arch | Schedule | Dataset | Tests | Notes |
| --- | --- | --- | --- | --- | --- |
| [sable-dev-net-1](nets/sable-dev-net-1.bin) | `((768 PSQT)x1hm -> 512)x2 -> ((SCOREx1))` | 1 stage, 240 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] | `-100 elo at 25K nodes` https://openbench.nocturn9x.space/test/7947/| Soft nnue reset back to 512hl with no extra features |
| [sable-dev-net-2](nets/sable-dev-net-2.bin) | `((768 PSQT)x1hm -> 1024)x2 -> ((SCOREx1))` | 1 stage, 480 SB; cosine LR decay from 0.001 to 0.00001; constant WDL of 0 | [Sable Goliath Data][goliath-data] | | Testing higher hl with no other changes |

[goliath-data]: https://openbench.nocturn9x.space/training/datasets/73a22972-7710-4e89-b90b-a9e70fa77ce7/

Dataset registered by Ellie: `EllieSilverrzz/sable-goliath-data`, revision/commit `7108685641ae60f29025ed5c597b7e15c13f4bf2` (2 files, 7.0 GB).
