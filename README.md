# Subspaces: working draft spec

## Core features of this design:

- **Fixed on-chain footprint**: 32-byte commitments regardless of batch size. Creating 1000 or a billion subspaces takes 32-bytes on-chain.

- **Minimal changes to the core client**: No SNARK/STARK logic into the core client itself. ZK is limited to the certificate verifier and can be easily updated/changed at any time without without consensus changes.

- **Off-chain by default**: Most users never need on-chain transactions. Cheap UTXO binding when interactive functionality is required (key rotation, transfers).

- **Zero on-chain metadata**: Names, certificates, zk proofs stay off-chain. The only visible on-chain data are the unique script_pubkeys when doing UTXO binding. 

-  **Post-Quantum ready**: If Bitcoin adopts PQ cryptography, we can switch to STARKs in the verifier logic - no consensus changes needed.

  
