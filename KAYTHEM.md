# Kaythem maintained libp2p branch

Branch: kaythem/identity-v1. Base: 2fed78f074af91e0c7440eedd08b8f898ad4a3fe.
Owner: Kaythem-P2P. Upstream licenses and notices remain unchanged.

This initial commit backports SEC-PRUNE-01 from upstream
9c647828abea0dfc0b4e827dff1e176ec8b44752: nine inserted behavior lines,
GossipSub version 0.50.1 and matching manifest/lock/changelog metadata. The
newer base's existing 0.51.0 changelog section is preserved. No entire older
upstream lockfile is substituted.

The complete patched behavior file is upstream blob
639f1ff376ebb1129e3316b4694cc2e2290ddb0e.

Compiler-only library validation ran on installed stable Rust 1.97.1,
x86_64-unknown-linux-gnu. No upstream tests or key operations ran.
Detailed source/lock/build evidence lives in Kaythem/Kaythem-P2P reports.

Identity/provider feature integration is the next patch; this commit implements
no ML-DSA identity, PQ transport or consumer adoption. The compile control in
Kaythem-P2P remains independently pinned until its integration is qualified.
S-01-S-18 runtime/security acceptance and production budgets remain open.
This branch is not a production-ready or fully security-qualified release.

## Publication rules

Experimental Kaythem-specific integration is developed and reviewed in private
workspaces first. Publish only the reviewed, sanitized patch and evidence needed
to understand it. Private development is release discipline, not a security claim.
Do not publish private keys, seeds, secret-bearing signing fixtures, infrastructure
credentials, live node configuration or sensitive operational/deployment details.
Review the complete diff, commit history, branch/tag refs, logs and attachments
before publishing; ignoring files is not a substitute for this review.

Label proposed encodings, PQ Noise constructions and high-assurance profiles
experimental until the exact construction is approved and the implementation is
verified. Approval of a shared primitive or encoding does not verify an integrated
channel. A build, public fork or primitive audit is not a full security audit.
State which tests ran and which acceptance gates remain open; make no unsupported
interoperability, production-readiness or whole-channel security-level claims.

Preserve upstream MIT licensing, copyright headers and attribution. Review each
new dependency's actual license and required notices before public introduction,
including cryptographic dependencies. This branch currently adds no new
cryptographic dependency; its initial code change is the cited upstream backport.
Keep confidential reports in the private channel described in SECURITY.md.
