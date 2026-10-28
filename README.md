# tss-nano: CPU sparse MoE pretraining

Transfer and continuation package for the existing 497M-parameter byte language model.

- 2048-byte sequences; TreeSSM backbone and sparse FFF experts.
- Original training equations and checkpoint layout are preserved.
- Native AVX-512/VNNI build, followed by measured CPU thread/affinity tuning.
- Cosmopedia-v2 is streamed into a bounded prefetch cache.
- Checkpoints contain slow weights, not optimizer moments: continuation starts fresh moments.

Release assets include the source/setup archive and the two-file checkpoint.
No credentials, private SSH keys, or cloud account configuration are included.

Training has not started on Vultr at package creation.
