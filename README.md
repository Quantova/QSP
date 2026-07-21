# QSP

The Quantova Standards Process. QSP carries the proposal templates, the accepted standards, and the cryptographic transition track that is the only path to change the algorithm set.

Quantova is a sovereign post quantum Layer 1 whose one of one property is that every layer is post quantum with only NIST standardized schemes and no classical escape hatch anywhere. A property that strong needs a single guarded door for changing it. QSP is that door.

## What it is for

QSP is where a change to the protocol is written down, argued, and either accepted or rejected in the open. A proposal states the section of the specification it touches, the change it makes, and the reasoning behind it. Accepted proposals become standards that the implementation repositories then follow. It keeps protocol evolution deliberate and on the record rather than settled quietly in code.

## The crypto transition track

One track is set apart from all the others because of what it governs. The crypto transition track is the only path that can add or retire an approved cryptographic scheme or set a key rotation window. It carries two hard rules.

- A proposal on this track is invalid unless it includes an external cryptanalysis report. A scheme change without independent analysis does not even reach a vote.
- The track can never introduce a classical primitive. The post quantum only rule outranks the process itself, so there is no proposal, and no majority, that can put an elliptic curve scheme back into the stack.

This mirrors the crypto transition track in the QONCORD governance protocol, where the same constraints are enforced on chain. QSP is the human and documentary side of that same one way door.

## Status

This repository is early. It fixes the process, the templates, and the transition rules, and it grows as proposals are written. The frozen algorithm set and the crypto policy it defends live in POLICY-crypto in the Quantova-Specs repository, which is the source of truth QSP proposals are measured against.

## Cryptography

The approved set is ML-DSA-65 from FIPS 204 and SLH-DSA from FIPS 205 for signatures, ML-KEM from FIPS 203 for key establishment, and SHA-3 and SHAKE from FIPS 202 for hashing. There is no elliptic curve anywhere. The stack cryptography is a from scratch reference implementation validated against the NIST vectors. It has not been independently audited, and the chain is at testnet.

## Governance and license

Governed by the crypto policy, POLICY-crypto, in the Quantova-Specs repository. Commits are authored by the owner only. Dual licensed under Apache 2.0 and MIT.
