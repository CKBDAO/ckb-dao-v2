# Treasury Mechanisms

## Introduction

This document describes the challenges involved with the management of treasury-issued funds and potential directions that can be taken.

The solutions in this document are not mutually exclusive. Over the long term, different solutions may be used. Different iterations may be a realistic way to approach this endeavor.

## Challenges

Treasury funds are a target for bad actors. This makes anyone who is a key holder for the treasury a potential target.

Solutions: Risk is mitigated by having more key holders which requires a higher threshold of cooperation to unlock. Enacting mandatory time delays and withdrawal caps also serves as a deterrent. Key holders can also be hidden under company entities that serve as the public face.

Using a fully on-chain system that only processes on-chain proposals after community approval is another solution, but this in itself is a challenge because it is difficult, costly, and inflexible.

On-chain systems are more difficult, costly, and inflexible. On-chain systems also require a higher level of participation from the community to ward off bad actors, and it has a higher chance of failure if participation is too low. Development budgets have limits, and there are timelines that must be met.

Solutions: A fully on-chain solution is not fundamentally necessary for a functional DAO. This is a solution that can be stepped into after a meaningful technical design has been created and a sustainable governance community has been established.

## Implementations

A Treasury Mechanism is a framework for managing on-chain funds through security and governance structures that ensure controlled access, accountability, and adaptability within a decentralized system. Below are different potential implementations of treasury mechanisms.
  
### Treasury Multisig Wallet (Top Representitives)

The Treasury Multisig Wallet is a basic multisig wallet controlled by the top 10 (exact number TBD) representitives in the ecosystem by delegated voting power. It functions as a traditional multi-signature wallet requiring a fixed threshold of representitive signatures to authorize and execute treasury transactions.

The multisig wallet has the following properties:

1. Signer List – The authorized signers consist of the current top 10 representitives by delegated voting power. The list is defined off-chain and can be updated via the multisig process to reflect changes in rankings every 90 days (or as determined by the DAO).
2. Signature Threshold – A minimum of 7 out of 10 signatures is required to approve any transaction.
3. Transaction Process – Representitives prepare a transaction, collect off-chain signatures from peers, and submit the signed transaction on-chain once the threshold is met.
4. Signer Updates – To update the signer list the same 7-of-10 signature process is used to execute the contract upgrade.
5. No Additional Restrictions – There are no mandatory waiting periods, withdrawal caps, or specialized on-chain proposal cells.

If the deposit address must remain static to ensure a treasury hard fork is not required (TBD), then a custom multisig lock will need to be used which does not require a change of the args field, which forces an address change.

A representitive eligible for the multisig wallet must meet the following criteria:

1. Well-Known and KYC-Verified – Must be a publicly recognized individual who has completed KYC verification.
2. Active in the CKB Ecosystem - Must have a history of active participation in the CKB ecosystem, and in the DAO itself.
3. Demonstrated Strong Moral Character – Must have a proven track record of ethical behavior and responsibility.
4. Long-Term Commitment to the CKB Ecosystem – Must show dedication to the ecosystem’s growth and sustainability.
5. Technically Savvy – Must be capable of using DAO governance tools for vault management and proposal review.

A representitive who is on the Treasury List receives a small stipend for their participation and an additional stipend for each vote they participate in. This helps incentivize qualified individuals to take part in this process, and high turnover must be discouraged to mitigate revolving door risk. Incentives also help get a greater number of willing participants, which reduces individual risk.

Challenges to the qualifications of any individual can be resolved through a stakeholder vote using the DAO.

The wallet is designed to be a simple and secure way to manage treasury funds while maintaining a high-level transparency. It is a straightforward approach that can be implemented quickly and does not forbid a later move to more sophisticated treasury mechanism in the future.

### Treasury Vault and Treasury Guardian System (Vote-Based Proposals)

The Treasury Vault is the location where CKB funds are accrued from secondary issuance. It can be thought of as a single address with a custom vote-based lock known as the Treasury Vault Lock (TVL) which is controlled by a group of Vault Guardians.

The TVL is similar to a multi-sig, but it operates on proposals and has extra functionality and restrictions:

1. Proposals and votes are represented on-chain as cells.
2. Votes are cast in favor or in opposition to a proposal withdrawal.
3. A list of Vault Guardians is kept on-chain, each of which is allowed a single vote of equal power.
4. A list of Treasury Wallets is kept on-chain, and are the only valid withdrawal locations.
5. A majority vote from the Vault Guardians must be reached to begin a withdrawal.
6. The lock has a mandatory waiting period of 7 days for all withdrawals after a successful vote.
7. During the waiting period, Vault Guardians may change their vote stance to cancel the withdrawal.
8. A high majority vote by the Vault Guardians is required to change the list of Vault Guardians or Treasury Wallets.
9. A vote is also subject to a mandatory 7-day waiting period before the changes can be enacted.

Each proposal is placed in a specialized on-chain cell that contains only the minimal essential data:

- Payment Address – The designated recipient address for the funds requested.
- Payment Amount – The specific amount of CKB requested.
- Proposal Identifier – A reference code used to link the on-chain request to the complete proposal details stored in the DAO portal.

A Vault Guardian is a community member who is:

1. Well-Known and KYC-Verified – Must be a publicly recognized individual who has completed KYC verification.
2. Elected Through DAO Proposal – Must be selected and approved by the DAO community via a formal proposal process.
3. Demonstrated Strong Moral Character – Must have a proven track record of ethical behavior and responsibility.
4. Long-Term Commitment to the CKB Ecosystem – Must show dedication to the ecosystem’s growth and sustainability.
5. Technically Savvy – Must be capable of using DAO governance tools for vault management and proposal review.

A Vault Guardian receives a small stipend for their participation and an additional stipend for each vote they participate in. This helps incentivize qualified individuals to take part in this process, and high turnover must be discouraged to mitigate revolving door risk. Incentives also help get a greater number of participants, which reduces individual risk.

This method is designed to be simple to ensure that it is well-understood and realistically feasible in a short period of time. Voting relies on a small group of representatives instead of direct vote by CKB holders because this drastically simplifies the technical requirements, and bypasses certain fundamental challenges with UTXO-based chains, such as the aggregator problem, which directly affects the security of vote-based systems.

This model is not intended to replace direct community voting for DAO funds. The main motivation behind this is the secure management of funds created through treasury issuance. The funds available in the Treasury Vault can and should be withdrawn into smaller DAOs which can safely explore different methods of direct community voting.
