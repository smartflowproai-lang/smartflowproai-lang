# SmartFlow Observatory

Independent x402 settlement observatory on Base, run by one person. The instrument is a deliberately unfiltered micro-USDC ledger (66M+ rows, every transfer between $0.0005 and $5 at ingest, attribution downstream), an endpoint catalog (79K+ entries), and an open-source endpoint validator. Numbers are published with methodology and reproduce from queries; corrections are published too.

- Live decomposition: https://verify.smartflowproai.com/decomposed
- Weekly Intel: https://smartflowproai.substack.com
- Contact: info@smartflowproai.com

## Standards and spec work

- **x402-foundation #2814** (author): Bazaar settled-but-not-indexed. 9 (payTo, resource) tuples where verify+settle returned processing and no record ever materialised. Fixed and closed by the team; the tuples were later cited in the AIR receipt-spec discussion as the evidence case for explicit settlement status.
- **x402-foundation #2922** (AIR receipt spec): explicit `settlement_status` (settled / pending / failed), the re-derivation invariant, and the settle-response digest attachment design were adopted into the v0.2 drafts (tracking: agent-receipt-spec #1 and #2).
- **x402-foundation #2823** (payment-integrity verifier roadmap): payTo cross-check adopted into the design; contributed 12 anonymised test-vector files plus generator.
- **x402-foundation #2335** (facilitator attribution): three attribution rules accepted by the proposal author; reference implementation `x402-attribution-ref` with byte-level parity tests.
- **b20 AssetTransferMethod** (author): draft discussion of a settlement path for B20 on Base, where `exact` has none.
- **x402-endpoint-validator** (maintainer): open-source conformance validator with external contributors; strict-v2 mode and a fresh-probe response archive (sha256 of full raw payload plus decoded triage fields).
