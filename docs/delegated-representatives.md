# Delegated Representatives

## Introduction

This document describes a DAO structure in which community members may delegate their
voting power to representatives to vote on their behalf. Community members may delegate to
one or more representatives, and may also exercise their voting rights by voting directly on any
proposal.

Rationale: The primary motivation behind this is the need for more participation from the
average community member who does not have the experience or expertise to vote
meaningfully. Community members will still be encouraged to vote directly, but we can expect
that most of the time representatives will carry this out on behalf of the community members.

This DAO is being designed with the Nervos DAO treasury in mind as a source of funding, but
most of the concepts will work with any funding source.

The information in this document may overlap with [Mission & Values](./mission-and-values.md), which will be combined at a later date.

## Representatives

A representative is any community member who wishes to take a more active role in the
governance of the DAO. After declaring themselves as representatives, other community
members may delegate some or all of their voting power to the representative. This allows the
representative the ability to vote on proposals with the voting power of the community members
they represent.

A representative is not directly compensated simply for being a representative. Compensation
opportunities arise by completing tasks necessary for DAO operation, such as proposal review,
technical review, and milestone review.

Rationale: We do not want to attract those who will try to use their standing to seek
compensation without providing value. However, incentives are needed for those who
participate because of the time requirement to do proper diligence on DAO tasks.

There is no formal process for applying to be a representative. A representative is expected to
market themselves to the community to gain delegate votes. The voting platform will allow any
representative to manage a profile page for themselves where they can state their values and
describe what they want to do for the DAO and the greater ecosystem.

Rationale: A representative is a role that relies in part on altruism, and part on stakeholder
interest. There is a delicate balance that must be maintained to ensure that work performed for
the DAO has enough incentivization to be executed properly by those who have a vested
interest in the long-term, but not high enough that it gains the interest of short-term opportunists.

More information on voting weight as it relates to representatives is described later in this
document.
## Open Questions

1. Should representatives be required to perform KYC?
   a. Would a special DID+KYC give benefit for the identification of representatives?
2. Should representatives be required to lock a stake?
   a. How much CKB is required to lock in stake?
   b. Is the stake at risk of loss if the representative is found to have acted against the interests of the DAO?
   c. What is the process for adjusting the required stake amount when the value of CKB changes dramatically?
3. Should there be a fee for creating a profile page on the DAO?
   a. How much would the fee be?
   b. Should individuals be able to seek sponsorship to cover this fee if they are from disadvantaged regions of the world?

## DAO Roles

There are special roles that need to be filled to operate the DAO successfully. All roles should
be structured not as staff, but as compensation for work performed.
 
Rationale: The DAO is intended to be efficient. Processes should require minimal time and effort
and should not necessitate full-time staff. DAO roles are intended to require minimal training for
a qualified person, allowing the role to be taken over by others to avoid dependency on a single
individual.

DAO roles are related specifically to the facilitation of DAO processes. A separate document
has been created for **Community Roles** that are funded by the DAO.

### Role Definition
 
- **Auditor:** Responsible for ensuring that processes remain transparent and accurate. When meetings are taking place, the auditor ensures that the content of the discussion is made available to the public and is unadulterated. Also responsible for the first review of fraud reports to determine if they are frivolous or warrant additional attention by the community and representatives.
- **Proposal Screener:** Responsible for taking the first look at proposals that have been drafted and ensuring that they have followed procedure before the proposal is made public and representatives are called to review and vote on it.
- **Project Reviewer:** Responsible for reviewing projects periodically when they reach  milestones to ensure that the work meets expectations before payment. Also responsible  for reviewing project components completed in other ecosystems if they are requesting  an integration grant, to evaluate benefit to the Nervos community.
- **Technical Reviewer:** Responsible for doing deeper technical reviews on projects when necessary to accurately determine if grant expectations are met. A technical reviewer gives an opinion on whether the code is up to reasonable expectations, but they are not responsible for bugs or exploits, and this is not a replacement for audits.
- **Industry Experts:** Brought in as needed to review proposals or deliverables when their experience and insight are deemed beneficial to the process review process. Experts may also be brought in for forensic examination in the case of fraud investigation.
- **Moderator:** Responsible for removing spam from the DAO platform and helping to keep the peace between community members when disagreements occur.
- **Platform Maintainer:** Responsible for ensuring that the DAO platform itself is properly maintained and secured.
- **Communication Manager:** Responsible for ensuring that relevant issues regarding the DAO are communicated properly to the public and internally to the representatives in a  timely manner.
- **Treasurer:** Responsible for maintaining a small amount of funds in a multi-sig treasury "hot wallet" that is used to pay grant recipients quickly as they qualify for payments.
- **Vault Guardian:** A well-known and KYC-verified delegate that holds a voting key as part of the treasury vault smart contract which releases treasury funds to wallets controlled by Treasurers.

All processes for the screening and appointment of individuals to specific roles must be done in public view as much as possible. A single person may take on multiple different roles. Not all roles will be needed immediately, and these roles are expected to evolve.

## Platform

The DAO voting interface will primarily be web 2.0 based using open source software with applicable binding to web3 where necessary. All essential voting data will be publicly available so validity can be proven by anyone using freely available tools. Essential data required for proving will be published to one or more decentralized public locations, such as CKBFS, to ensure that permanent records will not be lost.

Rationale: Feasibility and accessibility are important considerations for a community DAO. True web 3.0 technology is not widespread enough to be ubiquitous. Barriers to adoption need to be avoided. Web 2.0 can fully meet the DAO’s present-day needs.
## Components

The following are the main sections of the DAO portal.

- Representative Portal
  - Representative Profiles
    - Information about beliefs and values.
    - Voting statistics and results. (Links to DAO Explorer.)
- Proposal Portal
  - Grant proposal management.
  - DAO rule change proposal management.
  - Proposal discussion.
- DAO Explorer
  - DAO Statistics
  - Real-time voting results.
- Communication Portal
  - Allows for notification of new proposals and proposal results.
    - Social media posts.
    - Email mailings.
  - Community member self-service subscribe/unsubscribe.
## Voting Method

Voting on the platform is collected and tallied primarily using off-chain systems that allow for robust programmability. This is similar to the existing Metaforo, but the process for binding must make user-friendliness a priority. Address binding must be accomplishable by an average user in 30 seconds or less.

Rationale: On-chain voting is complicated and inflexible while offering few benefits to the process at this stage. Future implementations should always consider full on-chain voting, but it should not be utilized unless it is deemed to have undeniable benefits that are realistically feasible both in timeline, budget, and usability. Remaining agile and flexible is of great benefit in the early stages of any new process. Community non-participation is the single greatest threat to decentralization.

Proposals will be voted on by representatives or by community members directly through the platform. When a community member delegates voting power, it does not exclude them from voting directly on a particular issue. When a user votes directly, their voting power is retained for their vote rather than being delegated on that particular proposal.

Rationale: Most voting will occur through delegates, but the community must retain the ability to vote directly on issues they feel strongly about. This is to avoid problematic situations inherent to governance systems where issue granularity is lost due to exclusive representative voting.
## Voting Power

Nervos DAO locked CKB allows for a voting power of 1 vote per Shannon. Unlocked CKB is also eligible, but subject to a lower voting power proportional to the age of the UTXO. A new UTXO will start at zero voting weight and gain additional voting weight each epoch until reaching full voting power at 180 epochs (30 days).

Rationale: A Shannon is used as a vote because it is the smallest natural divisor unit. The vote display will likely be similar to CKB, with a fractional representation of the Shannons. The purpose of aged UTXOs for voting is to recognize the fair-sized chunk of the community that will not use the Nervos DAO because of the 30-day lockup. This allows them access to vote while still offering some protection against a borrowed stake attack; where someone borrows a large sum of CKB for a short term specifically to manipulate the vote. Adjusting their vote weight by UTXO age effectively has the same cost effect as the Nervos DAO for mitigating this attack.
## Voting Types

Different types of voting will allow the community to vote more effectively on different issues.

### Primary

These types of voting will have immediate use cases and should be the focus of initial development efforts.

- Binary Voting: Simple two-option voting for yes or no. This is best suited for most proposals.
- Plurality Voting: Voters select one option they approve of, and the entirety of their vote weight is used for this vote. This is best suited for elections where there is only one seat available.
- Approval Voting: Voters select one or more options they approve of, and their vote weight is distributed equally among these options. This is best suited for elections where multiple seats are available.

### Future Consideration

These types of voting are designed to address more complex scenarios. While not immediately necessary, these could be implemented as the DAO evolves.

- Quadratic Voting: Vote power per individual has a vote cost, increasing quadratically so that no single individual gains too much voting power. This does not work well with direct voting due to the Sybil attack, but it would work fine with delegated voting if the representatives were required to KYC.
- Weighted Voting: Voters can assign different weight amounts to each vote option they choose. This offers superior granularity in voting preferences but is more complicated from a usability perspective.
- Ranked-Choice Voting: Voters rank their preferences, but are not allowed to adjust weights. Instead, weight is distributed using a fixed algorithm.
- Time-Weighted Voting: Voters gain additional weight from DAO-locked CKB that has been locked for longer. This rewards long-term holders who have sacrificed the opportunity cost of their assets.
## Voting Exclusion

Using a vote-weight system can result in too much centralization of power, which can then result in unjust influence and corruption. Examples of these are:

- Blockchain Foundations.
- Centralized exchanges.
- Mining pools (custodied rewards).
- Liquidity pools (DeFi).
- Staking pools (DeFi).

The most simplistic way to protect against this is to simply disallow voting by these organizations. While it does not mitigate the potential completely, it is a deterrent. Since voting is done publicly and auditable, large sums of CKB can be traced to an extent. In this case, fraud can be detected and handled by the community.
## Fraud Reporting

The ability for community members to report fraud for investigation is an essential part of maintaining an accountable system. The interface for such a system must balance simplicity and transparency with effectiveness in the face of adversity.

The basis is a basic ticketing system. Reports are entered by community members and assigned a ticket number. Ticket visibility starts as limited to auditors only. This is to ensure that sensitive information is not leaked prematurely. The status of a report and its review state are public. The details of a report are not made visible to the public until approved by auditors. For sensitive topics, public viewing may be delayed temporarily, with a predefined hard upper threshold until automatic publication. For exceptions requiring more time, such as legal proceedings, a private vote by delegates is required.
### Open Questions

- What are the criteria for determining which assets can be used for DAO weight?
  - Should iCKB be recognized?
- Should fraud reporting allow anonymous submissions?
- What mitigations can prevent a DoS attack on the fraud reporting system?
- At what point does a fraud report become public without exception?
## Treasury

The treasury funds are managed in two levels, the Treasury Vault and Treasury Wallets.

More details about the implementation, as well as potential alternative models, can be found in the **Treasury Mechanisms** document.
### Treasury Vault

The Treasury Vault is the location where CKB funds are accrued from secondary issuance. It can be thought of as a single address with a custom vote-based multi-sig lock known as the Treasury Vault Lock (TVL) which is controlled by a group of Vault Guardians.

The TVL is similar to a multi-sig, but it has extra functionality and restrictions:

1. The lock maintains a list of Vault Guardians which are each allowed a single vote.
2. The lock relies on votes held in cells which are cast in favor or opposition to a withdrawal.
3. The lock maintains a list of Treasury Wallets which are the only valid withdrawal locations.
4. A majority vote from the Vault Guardians must be reached to begin a withdrawal.
5. The lock has a mandatory waiting period of 7 days for all withdrawals after a successful vote.
6. During the waiting period, Vault Guardians may change their vote stance to cancel the withdrawal.
7. A high majority vote by the Vault Guardians is required to change the list of Vault Guardians or Treasury Wallets.
8. A vote is also subject to a mandatory 7-day waiting period before the changes can be enacted.

Rationale: Because of the high amount of funds at stake, a more resilient system is needed. This system prevents bad actors from making withdrawals, even if some keys are compromised, and allows a period to rectify mistakes in the event of an error.
### Vault Guardians

Vault Guardian is a well-known and KYC-verified delegate who has been elected to the role through a DAO proposal. They are required to have demonstrated strong moral character, and a long-term commitment to the CKB ecosystem, and must be technically savvy enough to use DAO tools designed for the specific purpose of vault management.

Vault Guardian receives a small stipend for their participation and an additional stipend for each vote they participate in.

Rationale: This role is important and has risks associated since there are large sums of funds at stake. Extra care must be taken to ensure that only qualified individuals can take part in this process, and high turnover must be discouraged to mitigate revolving door risk.
### Treasury Wallets

A treasury wallet is a multi-sig wallet controlled by Treasurers. This is a normal wallet that uses standard locks and can make payments to anyone without waiting periods. A Treasury Wallet is a "hot wallet" that is used to pay grant proposals and any outstanding dues.

The ecosystem is not limited to a single Treasury Wallet. Many may exist for different purposes. These wallets have limited funds available for use and are expected to require refills from the Treasury Vault.

Examples of different Treasury Wallets:

1. DAO Proposals
2. DAO Roles
3. Community Roles
4. Core Development
5. Security Bounties
### Treasurer

Treasurer is responsible for managing a multi-sig Treasury Wallet and making approved payments.

Treasurer receives a small stipend for their participation and an additional stipend for payment activity.
### Open Questions

- Should Vault Guardians or Treasurers be required to lock a stake as an extra deterrent to fraud?
- What additional prerequisites should exist for Vault Guardians and Treasurers?
## Community Roles

Many roles in the community are currently being funded through centralized organizations, but it may make sense to move these to the DAO in time. These roles are typically related to community management and education, but may also encompass marketing and business development.

All roles should be subject to a policy of periodic reevaluation and renewal. This means that all roles expire by default and can only be renewed through new grants.

The details about the roles themselves are beyond the scope of this document and have been moved to **Nervos Community Fund DAO v2.0 - Community Roles**.

## Wallet Support and Binding Process

Both wide wallet support and superior user-friendliness are important, but their concerns are generally at odds with each other.

It is unrealistic for all wallets to make substantial modifications to support a single ecosystem. For example, Ledger hardware wallets are very popular, but the possibility of Ledger modifying their software to support the extended features of a Nervos ecosystem DAO is near zero.

Ledger wallets and other existing hardware and software wallets can and should have support extended to them. However, their binding process will likely be similar to that of Metaforo today.

User-friendliness can be addressed by extending features to better integrate wallets with the DAO. Using an aggregated message packet format could reduce the binding process to a single step regardless of how many addresses are used within the wallet. Using a custom API between wallets and the DAO would go one step further to ensure that the user can refresh bindings/balances with a single click in their wallet. This level of functionality is realistically attainable with proper cooperation between teams.

Pursuing both angles will give us the best compromise realistically attainable. Tier 1 ecosystem wallets will have seamless integration. Tier 2 ecosystem wallets will still be able to participate but their binding protocol will be more tedious.

More detailed information about the binding process can be found in [Address Binding Protocol](address-binding-protocol.md).