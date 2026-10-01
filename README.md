# Private, post-quantum secure transfer under EIP-8288

An interactive, step-by-step animation of a private transfer from a shielded pool under [EIP-8288](https://eips.ethereum.org/EIPS/eip-8288) proof dependencies and [EIP-8141](https://eips.ethereum.org/EIPS/eip-8141) frame transactions. It follows one transfer from the wallet's proof and frame transaction, through the pool's checks and the mempool, to the block, and shows how the program identity stays fixed while forks change the prover.

Open it at **https://soispoke.github.io/eip8288-private-transfer/**. Space plays or pauses, the arrow keys step through it, and each step has a spec note with the exact EIP rules it relies on.

The animation shows the program scheme proposed for EIP-8288's `0x11` in the ethresear.ch post "Post-quantum private transactions: Exposing an ISA". Today's EIP-8288 text names a verification key hash where that scheme names the program and its ISA version.

`index.html` is a single self-contained file. Its fonts are KaTeX's Computer Modern fonts, from [KaTeX](https://github.com/KaTeX/KaTeX) (MIT License).
