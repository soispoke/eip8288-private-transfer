# Private, post-quantum secure transfer under EIP-8288

An interactive, step-by-step animation of a private transfer from a shielded pool under [EIP-8288](https://eips.ethereum.org/EIPS/eip-8288) proof dependencies and [EIP-8141](https://eips.ethereum.org/EIPS/eip-8141) frame transactions. It follows one transfer from the wallet's proof and frame transaction, through the pool's checks and the mempool, to the block, and shows how the program identity stays fixed while forks change the prover.

Open it at **https://soispoke.github.io/eip8288-private-transfer/**. Space plays or pauses, the arrow keys step through it, and each step has a spec note with the exact EIP rules it relies on.

The animation shows the program scheme proposed for EIP-8288's `0x11` in the ethresear.ch post "Post-quantum private transactions: Exposing an ISA". Today's EIP-8288 text names a verification key hash where that scheme names the program and its ISA version.

## PCS_open version

A second animation, *How PCS_open Works*, follows a transfer from the same pool under PCS_open: the pool's contract checks its own PIOP and records polynomial-commitment claims, and EIP-8288's aggregate checks the openings. It then shows how the commitment scheme can be upgraded. Open it at **https://soispoke.github.io/eip8288-private-transfer/pcs-open/**. It shows a design under discussion, and its sizes and gas figures are model estimates, as its spec notes say.

## Circuit-claim version

A third animation, *How circuit claims work*, follows the same transfer when the pool writes its rules in a constraint format Ethereum fixes, such as R1CS, and nodes check the whole proof natively. It mirrors the PCS_open version step by step and marks every step that differs from it. Open it at **https://soispoke.github.io/eip8288-private-transfer/circuit-claims/**. It shows an optional design under discussion, and its sizes and gas figures are draft prices or estimates, as its spec notes say.

## PCS_open vs circuit claims

A comparison, *PCS_open vs circuit claims* (about 4 minutes), explains the two jobs in a STARK proof and the boundary between app and protocol. It then weighs the tradeoffs: shared PIOP safety, fixed constraint formats, large-circuit availability and preparation, PCS upgrades, and the compatibility obligations when adding an ISA later. It uses diagrams without a mathematical derivation. Open it at **https://soispoke.github.io/eip8288-private-transfer/compare/**.

## Lean specifications as application identity

A fifth animation, *Lean Specifications as Application Identity* (about 3 minutes), explains from scratch how users of a private application can rely on short rules written in Lean rather than on its code, while Ethereum enshrines only its proving machine. It builds one picture: off chain, once per program, a Lean proof is checked by the Lean checker and the run is proven into a certificate; on chain, one transaction brings the certificate to the pool's contract, which compares three pinned hashes (rules, machine description, checker) and approves the program; every payment is then an ordinary proof from an approved program. Open it at **https://soispoke.github.io/eip8288-private-transfer/lean-spec/**. It shows a design sketch that is not built; technical details are in each step's spec notes.

`index.html`, `pcs-open/index.html`, `circuit-claims/index.html`, `compare/index.html` and `lean-spec/index.html` are single self-contained files. Their fonts are KaTeX's Computer Modern fonts, from [KaTeX](https://github.com/KaTeX/KaTeX) (MIT License).
