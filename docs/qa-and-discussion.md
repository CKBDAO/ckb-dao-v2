 # Q&A and Discussion

 A concise summary of key questions and answers regarding DAO design, voting, and governance.

 ## Voting User Experience

 **Q: How should users receive proposal notifications and participate?**  
 **A:** Use email notifications and social media for alerts. Wallets can embed a web view for proposal submission and voting, but core notifications rely on existing systems.

 **Q: Should the platform be fully decentralized and serverless?**  
 **A:** Fully serverless is unlikely in current timelines. Centralized services are acceptable if results are provably verifiable.

 **Q: Is mobile compatibility important?**  
 **A:** Yes, mobile support is crucial for wider adoption.

 ## Representative Requirements

 **Q: Should representatives undergo KYC or lock up stake?**  
 **A:** KYC can be strongly recommended using privacy-preserving services but not mandatory. Requiring a CKB stake adds complexity and may deter qualified candidates, so it is not required.

 **Q: How should abstentions and non-votes be handled?**  
 **A:** Maintain an “Abstain” option and add “Absent” for non-participation. Track vote rationale and publish representative voting statistics for accountability.

 ## Proposal Submission

 **Q: Is a 100k CKB fee too high? How to set a fair barrier?**  
 **A:** Implement a modest “waste-of-time” fee pegged to a USD equivalent, refundable under defined criteria. Provide waivers or sponsorship for applicants in disadvantaged regions.

 ## Voting Power and Token Types

 **Q: Should iCKB or unlocked CKB be recognized for voting?**  
 **A:** Yes. To prevent borrow-based attacks, new UTXOs start with zero voting weight and scale to full weight over 180 epochs (~30 days), aligning with Nervos DAO lockup logic.

 ## Governance and Incident Handling

 **Q: How to address problematic voting incidents?**  
 **A:** Enable community-triggered votes to remove (“fire”) representatives in misconduct cases, using procedures that cannot be blocked by delegates.

 **Q: Who audits and oversees DAO activities?**  
 **A:** Auditors review processes and fraud reports via a confidential ticketing system. Report status updates are public; details are published post-review or after a delay.

 ## Collaboration and Community Roles

 **Q: Can external teams (e.g., Magicbase Labs) be funded to build infrastructure?**  
 **A:** Yes, the DAO can grant funding to external teams aligned with its goals.

 **Q: Should DAO ambassadors or business development roles exist?**  
 **A:** Yes, as community-funded roles separate from core DAO operational roles, responsible for scouting and securing high-quality proposals.