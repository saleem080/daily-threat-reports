# Satori Threat Intelligence Alert: Scallywag Extensions Monetize Piracy

**WHAT:**  
The Scallywag campaign exploits digital piracy and URL-shortening services to orchestrate large-scale ad fraud through custom WordPress extensions. Threat actors use these tools to redirect users through multiple cashout sites filled with ads, employing tactics like forced wait times, CAPTCHA challenges, and deep linking to manipulate traffic and cloak the original referrer.

**WHEN:**  
Reported publicly on April 21, 2025.

**HOW:**  
- User entry points begin at piracy catalog or URL-shortening websites, where users click links promising pirated or shortened content.
- Deep linking is used to embed webform parameters that trigger ad-heavy versions of cashout sites upon arrival.
- Open redirectors (e.g., Google, X/Twitter) are exploited to mask the original referrer and make traffic appear organic to ad networks.
- Scallywag modules are installed on WordPress sites to easily deploy these redirect chains at scale.
- Users are funneled through multiple intermediary “cashout” pages packed with ads before reaching the promised content.
- Monetization is achieved by requiring users to:
  - Click buttons to proceed
  - Solve CAPTCHAs
  - Wait for hard-coded timers to expire
  - Scroll or navigate through multiple intermediary pages
- Custom WordPress extensions involved include Soralink, Yu Idea, WPSafeLink, and Droplink (the latter distributed exclusively via Scallywag cashout paths).
- Intermediate cashout websites fall under the "Undisclosed Use of Incentives" category in the Invalid Traffic (IVT) Taxonomy, as users only visit these pages to access pirated content.
- Fraud scale: 1.4 billion fake ad requests daily across 407 domains, prior to mitigation efforts that reduced volume by 95%.

**RECOMMENDATIONS:**  
Organizations and advertising platforms should implement robust ad fraud detection mechanisms that extend beyond static blocklists. Focus should be placed on behavioral analysis to detect cloaking, domain rotation, and anomalous traffic patterns.  
Platforms should:
- Monitor referrer data closely
- Block traffic routed through known open redirectors
- Audit partnerships and advertising channels regularly to ensure transparency and prevent revenue leakage to fraudulent intermediaries.

**Sources:**  
- Public Threat Intelligence Feeds (e.g., Human Security
