# Proof of Stake Simulator

An interactive, browser-based Proof of Stake simulator for **COMP1830 Blockchain for Fintech** (University of Greenwich), Lab 2.

**Live:** https://apogiatzis.github.io/comp1830-proof-of-stake/

Students can explore:

- **Proposer selection** – each slot a validator is chosen with probability proportional to its stake.
- **Attestations and finality** – epochs are justified when validators holding ⅔ of the stake attest; two justified epochs in a row finalise the earlier one.
- **Rewards and stake concentration** – with rewards re-staked, does a large validator's share grow?
- **Missed slots and the inactivity leak** – offline validators miss proposals and, if finality stalls, slowly lose stake until the online validators hold ⅔ again.
- **Slashing** – a validator caught double-signing is penalised and ejected; the penalty grows with the total stake slashed together.

## Scenarios

Link straight to a scenario with `?scenario=<name>`:

| Scenario | Link |
|---|---|
| Equal stakes | `?scenario=equal` |
| One large validator (40 %) | `?scenario=whale` |
| A large validator goes offline (35 %) | `?scenario=blocker` |
| Half the network offline | `?scenario=outage` |
| Slashing: alone vs together | `?scenario=slash` |

## Notes

It is a simplified teaching model (8 slots per epoch, a flat 5 % inactivity leak, slashing correlation penalty applied immediately). See *About this model* on the page for how it differs from Ethereum.

Single static page: `index.html` plus the University of Greenwich brand fonts (Cooper Hewitt and Public Sans, SIL Open Font Licence). [three.js](https://threejs.org) 0.170.0 is loaded from jsDelivr.
