# Q&A and Discussion

A concise summary of key questions and answers regarding DAO design, voting, and governance. These questions are summarizations of the discussions and feedback from the community.

## Platform and User Experience

**Q: How should users receive proposal notifications and participate?**  
**A:** Use email notifications and social media for alerts. Wallets can embed a web view for proposal submission and voting, but core notifications rely on existing systems.

**Q: Should the platform be fully decentralized and serverless?**  
**A:** Fully on-chain decentralized solutions are unlikely in current timelines and introduce a lot of usability challenges. Hybrid Web5 services provide a more realistic solution as long as results remain provably verifiable.

**Q: Is mobile compatibility important?**  
**A:** Yes, mobile support is crucial for wider adoption.

## Voting Mechanics

**Q: How should abstentions and non-votes be handled?**  
**A:** Maintain an "Abstain" option and add "Absent" for non-participation. Representative voting statistics and history will be fully available for accountability.

**Q: How to mitigate delegate voting power concentration?**  
**A:** While saturation algorithms (diminishing returns on delegation) were considered, they introduce vulnerabilities to Sybil attacks without KYC and may over-empower anonymous large holders. The liquid democracy approach allows token holders to immediately withdraw delegation if representatives act against their interests. Transparency and active participation remain the primary mitigations.

**Q: What are the trade-offs of setting a maximum delegation limit on representatives?**  
**A:** Setting a hard cap on the voting power a single representative can receive helps prevent overcentralization. However, strict limits can dilute the influence of highly qualified delegates, especially in smaller or emerging ecosystems. This may incentivize Sybil attacks which can only be mitigated by requiring additional identity verification.

**Q: Should iCKB or unlocked CKB be recognized for voting?**  
**A:** Yes. To prevent borrow-based attacks, new UTXOs start with zero voting weight and scale to full weight over 180 epochs (~30 days), aligning with Nervos DAO lockup logic.

## Representatives and Governance

**Q: Should representatives undergo KYC or lock up stake?**  
**A:** KYC can be strongly recommended using privacy-preserving services but not mandatory. Requiring a CKB stake adds complexity with little to no benefit and may deter qualified candidates, so it is not required.

**Q: How to address problematic voting incidents?**  
**A:** Representatives involved in misconduct cases are still subject to local law and may face legal consequences, which is why KYC is recommended. Users can take direct action through liquid democracy; shifting their delegated power to another representative immediately.

**Q: Who audits and oversees DAO activities?**  
**A:** Auditors review processes and fraud reports via a confidential ticketing system. Report status updates are public; details are published post-review or after a delay.

## Proposals and Funding

**Q: Is a 100k CKB fee too high? How to set a fair barrier?**  
**A:** Implement a modest "waste-of-time" fee pegged to a USD equivalent, refundable under defined criteria. Provide waivers or sponsorship for applicants in disadvantaged regions.

**Q: Can external teams (e.g., Magicbase Labs) be funded to build infrastructure?**  
**A:** Yes, the DAO can provide funding to external teams aligned with its goals.

**Q: Should DAO ambassadors or business development roles exist?**  
**A:** Yes, as community-funded roles separate from core DAO operational roles, responsible for scouting and securing high-quality proposals.
