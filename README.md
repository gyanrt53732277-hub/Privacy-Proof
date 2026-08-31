# ProofFolio: Privacy-Preserving Academic Credential Verification
   
> **Tagline:** Verify qualifications, not personal data. Built on the Midnight Network. 
 
[![CI](https://github.com/gyanrt53732277-hub/ProofFolio/actions/workflows/ci.yml/badge.svg)](https://github.com/gyanrt53732277-hub/ProofFolio/actions/workflows/ci.yml)

## Links

- **Live app:** [Open ProofFolio](https://proof-folio.rajivdubey.dev/)
- **Demo video:** [Watch the demo](https://drive.google.com/file/d/1odZ8Ty0ZkfOIBKg_FxeahA8IwssD2sjN/view?usp=sharing)
- **X link:** [Checkout on X](https://x.com/ProofFolio)
- **Feedback form:** [Submit ProofFolio feedback](https://forms.gle/QJ7KQixfkiCwTt8n9)
- **Preprod user evidence:** [View feedback and wallet records](https://docs.google.com/spreadsheets/d/1IqjmJ3tC7LX8i5YqrYwW_5IZ8cbCZW_sJHEM4gfxjkM/edit?usp=sharing)



## Screenshots

<table>
  <tr>
    <td><img width="1876" height="1005" alt="image" src="https://github.com/user-attachments/assets/3d4b67ca-271b-4e35-9a11-89a0de01a17b" /><br><sub>Home page</sub></td>
    <td><img width="1876" height="1005" alt="image" src="https://github.com/user-attachments/assets/87ef94ca-a480-43da-98bc-ad5d4f821ab1" /><br><sub>University portal</sub></td>
  </tr>
  <tr>
    <td><img width="1876" height="1005" alt="image" src="https://github.com/user-attachments/assets/96b69809-e025-406c-a4ec-a2dceaacc060" /><br><sub>How It Works</sub></td>
    <td><img width="1876" height="1005" alt="image" src="https://github.com/user-attachments/assets/9ca93635-ec0f-4779-a9c0-7ea3ee2484d7" /><br><sub>CI passing</sub></td>
  </tr>
</table>

---

## ❌ The Problem

Credential fraud is a massive global issue, but current verification systems are broken:
* **Privacy Leakage:** Students are forced to share full academic records (transcripts, DOBs) just to prove a single degree.
* **High Fraud:** PDFs and scanned documents are easily forged.
* **Slow Verification:** Manual background checks take weeks and rely on costly third-party agencies.
* **Replay Attacks:** Once a document is shared, it can be copied or reused maliciously.

## ✅ Our Solution

**ProofFolio** is a privacy-first credential verification protocol built using **Zero-Knowledge Proofs (ZKPs)** on the **Midnight Network**.
It allows universities to issue tamper-proof credentials on-chain. Students can then generate local cryptographic proofs to prove their qualifications to employers *without* revealing their actual personal data.

**One proof. Zero data exposure.**

## 💡 Use Cases

* **Academic Degrees:** Prove graduation year and degree type without sharing grades.
* **Professional Certifications:** Verify active medical, legal, or technical licenses.
* **Skill Badges:** Confirm completion of bootcamps or training programs.
* **KYC / Identity:** (Future scope) Prove age or citizenship without revealing passport details.

## 🛠 Tech Stack

* **Blockchain / Smart Contracts:** Midnight Network, Compact (smart contract language)
* **Zero-Knowledge:** ZK-SNARKs, local ZK circuits, Merkle Tree commitments, Nullifiers
* **Frontend:** React, Next.js (App Router), TypeScript, Tailwind CSS
* **Wallet & Integration:** Lace Wallet, Midnight dApp Connector, Midnight.js

## ✨ Features

* **Authorized Issuer Registry:** Only whitelisted universities can issue credentials to prevent fake institutions.
* **Private Issuance:** Universities only publish a hashed commitment to the blockchain, never the raw data.
* **Instant Verification:** Employers receive a definitive Yes/No response in seconds via blockchain consensus.
* **Replay Protection:** Cryptographic nullifiers ensure that a specific proof cannot be reused.
* **On-Chain Audit Trail:** The ledger publicly tracks the total number of verifications without linking them to individuals.
* **Feedback-Driven Refinement:** User feedback prioritized clearer wallet privacy guidance, mobile spacing, explicit success states, simpler ZK explanations, and clearer revocation/expiry behavior.

## 📜 Contract Address

* **Network:** Midnight Preprod
* **Contract Address:** *8131a6c88f0b726c57bcf471cf8831947749e4dc68bd458c3692af73605f74d3*

## 🔐 Privacy Functions

ProofFolio leverages Midnight's data-protecting architecture:
* **Selective Disclosure:** Students only prove the claims the employer asked for.
* **Local Witness Execution:** Private data (student secret keys, raw credential JSON) stays fully local in the wallet/browser.
* **Zero-Knowledge Proofs:** The network verifies the truth of a statement ("This student holds a valid degree") without ever seeing the inputs that make it true.

## 🔄 Application Flows

1. **University Portal (Issuance)**
   * Registers as an authorized issuer.
   * Inputs student details locally.
   * Hashes the credential and posts the commitment to the Midnight ledger.
2. **Student Portal (Proof Generation)**
   * Imports credential package (metadata + secret key).
   * Generates a local ZK proof satisfying the employer's challenge.
   * Never sends private data to the network.
3. **Employer Portal (Verification)**
   * Receives the proof transaction hash from the student.
   * Validates the proof against the Midnight smart contract.
   * Views verified claims instantly on a secure dashboard.
4. **Preprod Feedback Loop**
   * 50 unique preprod wallet rows are recorded in the linked feedback sheet for user verification.
   * Feedback themes include privacy, selective disclosure, issuer trust, revocation, expiry, replay protection, and auditability.

---

## Feedback Loop

Feedback export contains 52 submissions and 50 unique preprod wallets. Duplicate feedback events remain in source; user counts use unique wallets. See [full feedback log](docs/FEEDBACK.md) and [canonical user evidence](docs/USERS.md).

### Users Onboarded

| User ID | Name | Email | Wallet Address | Feedback Summary |
| --- | --- | --- | --- | --- |
| U001 | Hardika Kathlewar | hardikakathlewar19@gmail.com | mn_addr_preprod1aspq6trgdalzza4ds2dp0faxh9wnlu50ndx7267xw640v24rq2vqqe0n2j | Easy form; liked privacy. |
| U002 | Mohammad Faizan | mohdfaizan8222@gmail.com | mn_addr_preprod1wwzcty42uhgzh42dypa8xdng9v9gvwk0cdj9ca9ej5n2vpjuty6sqcrghs | Verification result should appear faster. |
| U003 | Sami Guide | sami13guide94@gmail.com | mn_addr_preprod13cz34pdy8ev6284j0supwv3k2k0hvj372eeqc40tnws2vqzv20fsegc4s4 | Liked not sharing full transcript. |
| U004 | Bipronil Ghosh | bipronilg@gmail.com | mn_addr_preprod1hr44d9anm8ctghuyk2xxxeqmfucj0339r55sdtjtpf3hymup4eds2tmj33 | Asked for wallet-address example. |
| U005 | Aditya Shrivastav | adityashrivastav5779@gmail.com | mn_addr_preprod189awrytnxxyl2pcqlfc3heu4ca0qme72numltn6tg00qz2zrpr8q7flupg | Employer flow useful for job applications. |
| U006 | Ashish Singh | singhashish7849@gmail.com | mn_addr_preprod18rlnsxalv8s5h37racm8raq9kejvxfrd7xq2hc8du20qp25cx3sqermsmc | Asked for simpler revocation explanation. |
| U007 | Sicky Kumar | sickykumar01@gmail.com | mn_addr_preprod1dzt5w05wehacav5vnpw0avsfd9g9x8p3dx397gn3l6yylqynps3smsyje6 | Clean, uncrowded layout. |
| U008 | Yash Ambaskar | kimetsu119@gmail.com | mn_addr_preprod1j75jkymygy6aww5d2xygyhkpkumgvsr5ru3vk5m7jvycr2afy7qszf7g5n | Asked for shorter project explanation. |
| U009 | Sachin Rathod | sachinrathodsr1212@gmail.com | mn_addr_preprod1lanjtxlqm9fmv7tdw5z2v5z33jgf5066lzzguas4wwrv7gk8y86srxl6yg | Requested final claim-review step. |
| U010 | SRINADH GHANTASALA | 2403031460778@paruluniversity.ac.in | mn_addr_preprod1hfgdtxkyw97rg8qu8y33ahpq92rxv8lphuk9cz3vfh56qwpegnzsqsv7ga | Requested clearer thank-you state. |
| U011 | Sivam Singh | sivamsingh168@gmail.com | mn_addr_preprod1qcjdkfuye967uph3eqhwj0x8jgpn2z95nfq5k0w9qjzhr03hm8kqx4yjz2 | Liked transcript privacy. |
| U012 | Mayank Sengupta | includemayank@gmail.com | mn_addr_preprod1gaf99hsjj4l8l4vn6anm8m9c937s0esegj853xay6tuzkl3qg5ssm6w5l0 | Asked who can see wallet address. |
| U013 | Akshita Srivastava | akshitasrivastava189@gmail.com | mn_addr_preprod1fknxhaa4jzl0l2xxctl9ujq5pc6n227rr0x2jrzxw9yj3kfk7ywq69fp9a | Simple questions; suggested progress bar. |
| U014 | Atharv Gupta | atharvgupta790@gmail.com | mn_addr_preprod19tyx9sm5zlufnd4e2qe7uxndcnqnt8p2ad05z7n2ah87qt0k73sqffy4jn | Issuer trust improved confidence. |
| U015 | Rehan Akhtar | rehanakhtar051181@gmail.com | mn_addr_preprod1kwvl6rdqjhp79ags6hstcsq6k7u66yl4uly0u6dmxw48lfvu920qmgtm7d | Asked to test smaller-phone spacing. |
| U016 | Sri Hasini Sripada | srihasinisripada@gmail.com | mn_addr_preprod1g8xelplenenqx02dvfew449l9vst488mh75vcq8t0nr04e27ddksdmn5m6 | Liked challenge-based replay protection. |
| U017 | Nani Kodiganti | nanikodiganti2006@gmail.com | mn_addr_preprod1r7leppryqu9phlue3t8zd93cqhcvwpm8dldjzap7x0us55j943csulfume | Requested optional user role. |
| U018 | Varun Kumar | varunkohli1817@gmail.com | mn_addr_preprod1zepstj9s62tpzsqa4wpu34afcxdfjvs4gcsq6ks8phht8h5trhxqpc5yrq | Liked control over shared details. |
| U019 | Suneet Jain | suneetjain179@gmail.com | mn_addr_preprod1qavw0htkywu0ltwmnqz8pke4v6m22lt63ls29p422sl9n8cx68eqm02wf9 | Requested student-employer example. |
| U020 | Dr. Sharad Doshi | drsharad81@gmail.com | mn_addr_preprod1ytpkh6lmna6s4nnnx996k8ruhnst0g8qxf7wgz4djcze2djnv5msa94k6m | Liked issued and active checks. |
| U021 | Harnoor Singh | harnoorsingh.online@gmail.com | mn_addr_preprod1xfdeap7cy0jc80k6wzz5403kuxcpf8s5pquq4gm5ml4zzm5cfhus9t8yw4 | Trusted issuer status adds confidence. |
| U022 | Neeru Doshi | neerudoshi8@gmail.com | mn_addr_preprod1p2luty0ugut6gthwjen4n2r5rnvnmv60jr0kgumqup0qwzrmhd0scl6590 | Requested stronger submit confirmation. |
| U023 | Babita Jain | babitajain352@gmail.com | mn_addr_preprod17pdtywmyyuhsnaqsqcjg27ql34mcgtnah54y6w76f45zt757znyq46rzpe | Liked sharing claims separately. |
| U024 | Vijendra Thakur | vijendrat418@gmail.com | mn_addr_preprod1qskzk5e7ufvylw9x8t75enqkr055tyrxrzl9m4muxn75x9a3zvtskxnnn8 | Requested one-time ZK explanation. |
| U025 | Sarika Doshi | sarikadoshi02@gmail.com | mn_addr_preprod1nzmy9hv7uhl9fkdzu7xmumjynt68nq7hncpdq33f48qu7x3w0r9sxqgss8 | Liked audit trail. |
| U026 | Harsh Doshi | hk.doshi63@gmail.com | mn_addr_preprod1fn9ly8h6y205hgfyf5dp68tg6amxce0gjfpjg8jevqquycr3dq7qlyq3zs | Professional feel. |
| U027 | Shweta Athea | atheashweta@gmail.com | mn_addr_preprod1597zqcpg7gr49gl3gg4d4gqvx204eu9za9u90swdeeqakfmscj3q360u4h | Requested clearer valid-until display. |
| U028 | Tanull Jain | tanulljain2411@gmail.com | mn_addr_preprod19y830exy2tg2xu4zhmgvqd7vw0f3x4zyw5evcps3qjpam34henaqxzuvek | Liked minimum disclosure. |
| U029 | Ayush Yadav | ay24sh24@gmail.com | mn_addr_preprod1f7r89sf5y87w6denl07gmzl592zf6khn3lz3kjg3nc9hpn0s3acqhpgk99 | Requested public demo result. |
| U030 | Ayush Yadav | ayushyadav65078@gmail.com | mn_addr_preprod193nvvvk5dw60q090hwg6egcck5gkuw5pelt9tjxu37vg292rxssqaztx4x | Liked wallet connection. |
| U031 | Jainmiah Shaik | skjainmiah@gmail.com | mn_addr_preprod1g3pjegkmjtlyvfcnjscfjfgxksgkt8d0zs04mm0pff372fj4tgfs95dz9v | Requested rating labels. |
| U032 | Kishan Verma | k9891p@gmail.com | mn_addr_preprod1vymq7jm0jer79kmnuynafchrjkjtruugplfl7d7m5cs24pp4gues3grxkl | Requested failed-verification example. |
| U033 | rishabh doshi | rishabh.doshi15@gmail.com | mn_addr_preprod1qdwkgj0706l75y49plqmtxg8muzh0854g4txpa0l38c8c74feujq6lgn0j | Requested clear error messages. |
| U034 | bunny bad | cbunny.bad@gmail.com | mn_addr_preprod1slngheyu46kelzvlu3lvcsdg65chj653grc0c2m9up2qe6sx67hsqxfs08 | Liked concise form. |
| U035 | Sanjeev Sharma | sanjeevshakti@gmail.com | mn_addr_preprod1my00ew7dczpcu9j85rtr66xrtr3vqrmsq9lxt5xjc4lgcxd5kdmse5spmm | Requested more mobile answer space. |
| U036 | Anupam Jaiswal | anupamj0107@gmail.com | mn_addr_preprod16gt45h3d8fhf92s764rw2fwed89zgppw9emxlxmutn4mygvmn6usng9xta | Trusted revocation tracking. |
| U037 | Bhalani Vijay | bhalanivijay@gmail.com | mn_addr_preprod1330vu985dle2umu934ex8t3thepgjp77uwtjq5l2ewjnpne0w5cs59au0l | Liked simple flow despite new technology. |
| U038 | Singara Velan | singaravelancsk@gmail.com | mn_addr_preprod1vzpjefk46y35ryk7ug77f3vdktytgpzem39l50r3vurp96pwhysqyewmc3 | Requested poor/excellent rating labels. |
| U039 | MD FARUKH | farukh1132@gmail.com | mn_addr_preprod1lxy8ukwynvqhtgcghgmknxd86pxne8gm3am5ggd8evps232teayqk67l7a | Liked on-chain institution checks. |
| U040 | Rajjoo Bhai | bhairajjoo@gmail.com | mn_addr_preprod1yktjz8m509s2zhn8q7lsvl8fgtqv568re5hs280z6v023l0t0a7qck73tx | Requested seed-phrase warning. |
| U041 | Pankaj Sharma | pankajcws9729@gmail.com | mn_addr_preprod1nywnjngw9vuqfkdey4fdsmcxn8nrrl5023uyxpral5mnhj62395qsyvwdt | Requested visible wallet privacy note. |
| U042 | Sharad Raut | shrd.raut@gmail.com | mn_addr_preprod14rxrkv5mzaht03q9lzkdv84qkqf3tysmtaka0rcg598pcl7ht2vsm75jqe | Liked portable, challenge-bound proofs. |
| U043 | Ritesh Ranjan | riteshranjan1972@gmail.com | mn_addr_preprod12c8rn82vzr2flwmwe5f7sfqutrc3k0cag6saf7pejmwu9qp0wzxqmnjv09 | Liked question order. |
| U044 | Sainarasimha Peddi Reddy | pvsnarasimha2003@gmail.com | mn_addr_preprod16cmuacx2wvzt2f9ycle4kxvc524n9wf9xa2dpntmxkawnqd2qe3sh84k87 | Interested in employer trial. |
| U045 | Utkarsh Saraswat | buildwithutkarsh@gmail.com | mn_addr_preprod1dgcnaggmqvtzwx66a9vj0pt29spst4mrdm55pxsplzt8n9a6c6xsa5676l | Liked selected claims. |
| U046 | Mirshad Kvr | mirshadkvr19@gmail.com | mn_addr_preprod1h7t2a9j9pgrfhhuu5xee7hulh08rc2pnnrrttuh398s6czq0guesh9z4un | Liked developer read-only checks. |
| U047 | priyanshu pandey | pandeypriyanshu53@gmail.com | mn_addr_preprod16xtt6d9cmjelt9dfvuasckm5dqu6spd9jf9s07ntmhja8s8tcdpskd3la7 | Liked replay protection. |
| U048 | Jiji Philip Varghese | jijlife@gmail.com | mn_addr_preprod1wtm7s7pgww0w3nzr47s5h2xsenkrk6mrsren4ctwj5sm89ttugzsh0ta33 | Requested complete success screen. |
| U049 | Vardhaann Rathore | anaxx34@gmail.com | mn_addr_preprod1332n8d6yhpkag5wft7h3c6jn2tcjupa4cpj07uglgc905vt0k7ps9ywwf4 | Liked proving without full document upload. |
| U050 | Aman kumar | amankhdbensskbesbbe@gmail.com | mn_addr_preprod1a5lmvc0e4d6atv2zcsepxwnaxhglgmaxwjxdqsslsgcpyhmcmvxqyap9a0 | Asked to keep introduction simple. |

### Feedback Implementation

| User ID | Name | Email | Wallet Address | Feedback Summary | Improvement Made | Git Commit ID |
| --- | --- | --- | --- | --- | --- | --- |
| U001 | Hardika Kathlewar | hardikakathlewar19@gmail.com | mn_addr_preprod1aspq6trgdalzza4ds2dp0faxh9wnlu50ndx7267xw640v24rq2vqqe0n2j | Easy form; liked privacy. | Retained concise feedback flow. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U002 | Mohammad Faizan | mohdfaizan8222@gmail.com | mn_addr_preprod1wwzcty42uhgzh42dypa8xdng9v9gvwk0cdj9ca9ej5n2vpjuty6sqcrghs | Verification result should appear faster. | Added explicit verification result states. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U003 | Sami Guide | sami13guide94@gmail.com | mn_addr_preprod13cz34pdy8ev6284j0supwv3k2k0hvj372eeqc40tnws2vqzv20fsegc4s4 | Liked not sharing full transcript. | Retained selective-disclosure credential flow. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U004 | Bipronil Ghosh | bipronilg@gmail.com | mn_addr_preprod1hr44d9anm8ctghuyk2xxxeqmfucj0339r55sdtjtpf3hymup4eds2tmj33 | Asked for wallet-address example. | Added wallet-address format example. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U005 | Aditya Shrivastav | adityashrivastav5779@gmail.com | mn_addr_preprod189awrytnxxyl2pcqlfc3heu4ca0qme72numltn6tg00qz2zrpr8q7flupg | Employer flow useful for job applications. | Retained employer verification workflow. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U006 | Ashish Singh | singhashish7849@gmail.com | mn_addr_preprod18rlnsxalv8s5h37racm8raq9kejvxfrd7xq2hc8du20qp25cx3sqermsmc | Asked for simpler revocation explanation. | Added plain-language revocation guidance. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U007 | Sicky Kumar | sickykumar01@gmail.com | mn_addr_preprod1dzt5w05wehacav5vnpw0avsfd9g9x8p3dx397gn3l6yylqynps3smsyje6 | Clean, uncrowded layout. | Retained uncluttered layout. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U008 | Yash Ambaskar | kimetsu119@gmail.com | mn_addr_preprod1j75jkymygy6aww5d2xygyhkpkumgvsr5ru3vk5m7jvycr2afy7qszf7g5n | Asked for shorter project explanation. | Added shorter plain-language ZK explanation. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U009 | Sachin Rathod | sachinrathodsr1212@gmail.com | mn_addr_preprod1lanjtxlqm9fmv7tdw5z2v5z33jgf5066lzzguas4wwrv7gk8y86srxl6yg | Requested final claim-review step. | Added final claim review before proof submission. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U010 | SRINADH GHANTASALA | 2403031460778@paruluniversity.ac.in | mn_addr_preprod1hfgdtxkyw97rg8qu8y33ahpq92rxv8lphuk9cz3vfh56qwpegnzsqsv7ga | Requested clearer thank-you state. | Added explicit proof success state. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U011 | Sivam Singh | sivamsingh168@gmail.com | mn_addr_preprod1qcjdkfuye967uph3eqhwj0x8jgpn2z95nfq5k0w9qjzhr03hm8kqx4yjz2 | Liked transcript privacy. | Retained transcript privacy messaging. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U012 | Mayank Sengupta | includemayank@gmail.com | mn_addr_preprod1gaf99hsjj4l8l4vn6anm8m9c937s0esegj853xay6tuzkl3qg5ssm6w5l0 | Asked who can see wallet address. | Added visible wallet privacy guidance. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U013 | Akshita Srivastava | akshitasrivastava189@gmail.com | mn_addr_preprod1fknxhaa4jzl0l2xxctl9ujq5pc6n227rr0x2jrzxw9yj3kfk7ywq69fp9a | Simple questions; suggested progress bar. | Kept short form flow; progress bar remains future work. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U014 | Atharv Gupta | atharvgupta790@gmail.com | mn_addr_preprod19tyx9sm5zlufnd4e2qe7uxndcnqnt8p2ad05z7n2ah87qt0k73sqffy4jn | Issuer trust improved confidence. | Retained issuer authorization checks. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U015 | Rehan Akhtar | rehanakhtar051181@gmail.com | mn_addr_preprod1kwvl6rdqjhp79ags6hstcsq6k7u66yl4uly0u6dmxw48lfvu920qmgtm7d | Asked to test smaller-phone spacing. | Kept responsive full-width controls. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U016 | Sri Hasini Sripada | srihasinisripada@gmail.com | mn_addr_preprod1g8xelplenenqx02dvfew449l9vst488mh75vcq8t0nr04e27ddksdmn5m6 | Liked challenge-based replay protection. | Retained challenge-based replay protection. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U017 | Nani Kodiganti | nanikodiganti2006@gmail.com | mn_addr_preprod1r7leppryqu9phlue3t8zd93cqhcvwpm8dldjzap7x0us55j943csulfume | Requested optional user role. | Role field remains feedback-form follow-up. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U018 | Varun Kumar | varunkohli1817@gmail.com | mn_addr_preprod1zepstj9s62tpzsqa4wpu34afcxdfjvs4gcsq6ks8phht8h5trhxqpc5yrq | Liked control over shared details. | Retained selective claim disclosure. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U019 | Suneet Jain | suneetjain179@gmail.com | mn_addr_preprod1qavw0htkywu0ltwmnqz8pke4v6m22lt63ls29p422sl9n8cx68eqm02wf9 | Requested student-employer example. | Clarified student-to-employer flow copy. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U020 | Dr. Sharad Doshi | drsharad81@gmail.com | mn_addr_preprod1ytpkh6lmna6s4nnnx996k8ruhnst0g8qxf7wgz4djcze2djnv5msa94k6m | Liked issued and active checks. | Retained issued/active status checks. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U021 | Harnoor Singh | harnoorsingh.online@gmail.com | mn_addr_preprod1xfdeap7cy0jc80k6wzz5403kuxcpf8s5pquq4gm5ml4zzm5cfhus9t8yw4 | Trusted issuer status adds confidence. | Retained trusted issuer status. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U022 | Neeru Doshi | neerudoshi8@gmail.com | mn_addr_preprod1p2luty0ugut6gthwjen4n2r5rnvnmv60jr0kgumqup0qwzrmhd0scl6590 | Requested stronger submit confirmation. | Added stronger proof submission confirmation. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U023 | Babita Jain | babitajain352@gmail.com | mn_addr_preprod17pdtywmyyuhsnaqsqcjg27ql34mcgtnah54y6w76f45zt757znyq46rzpe | Liked sharing claims separately. | Retained separate claim disclosure. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U024 | Vijendra Thakur | vijendrat418@gmail.com | mn_addr_preprod1qskzk5e7ufvylw9x8t75enqkr055tyrxrzl9m4muxn75x9a3zvtskxnnn8 | Requested one-time ZK explanation. | Added one-time ZK explanation. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U025 | Sarika Doshi | sarikadoshi02@gmail.com | mn_addr_preprod1nzmy9hv7uhl9fkdzu7xmumjynt68nq7hncpdq33f48qu7x3w0r9sxqgss8 | Liked audit trail. | Retained audit trail messaging. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U026 | Harsh Doshi | hk.doshi63@gmail.com | mn_addr_preprod1fn9ly8h6y205hgfyf5dp68tg6amxce0gjfpjg8jevqquycr3dq7qlyq3zs | Professional feel. | Retained professional visual presentation. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U027 | Shweta Athea | atheashweta@gmail.com | mn_addr_preprod1597zqcpg7gr49gl3gg4d4gqvx204eu9za9u90swdeeqakfmscj3q360u4h | Requested clearer valid-until display. | Added clear valid-until display. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U028 | Tanull Jain | tanulljain2411@gmail.com | mn_addr_preprod19y830exy2tg2xu4zhmgvqd7vw0f3x4zyw5evcps3qjpam34henaqxzuvek | Liked minimum disclosure. | Retained minimum-disclosure messaging. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U029 | Ayush Yadav | ay24sh24@gmail.com | mn_addr_preprod1f7r89sf5y87w6denl07gmzl592zf6khn3lz3kjg3nc9hpn0s3acqhpgk99 | Requested public demo result. | Added Midnight explorer transaction link. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U030 | Ayush Yadav | ayushyadav65078@gmail.com | mn_addr_preprod193nvvvk5dw60q090hwg6egcck5gkuw5pelt9tjxu37vg292rxssqaztx4x | Liked wallet connection. | Retained wallet-connected credential ownership flow. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U031 | Jainmiah Shaik | skjainmiah@gmail.com | mn_addr_preprod1g3pjegkmjtlyvfcnjscfjfgxksgkt8d0zs04mm0pff372fj4tgfs95dz9v | Requested rating labels. | Rating labels remain feedback-form follow-up. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U032 | Kishan Verma | k9891p@gmail.com | mn_addr_preprod1vymq7jm0jer79kmnuynafchrjkjtruugplfl7d7m5cs24pp4gues3grxkl | Requested failed-verification example. | Added verification failure state label. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U033 | rishabh doshi | rishabh.doshi15@gmail.com | mn_addr_preprod1qdwkgj0706l75y49plqmtxg8muzh0854g4txpa0l38c8c74feujq6lgn0j | Requested clear error messages. | Added clearer verification error context. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U034 | bunny bad | cbunny.bad@gmail.com | mn_addr_preprod1slngheyu46kelzvlu3lvcsdg65chj653grc0c2m9up2qe6sx67hsqxfs08 | Liked concise form. | Retained concise form flow. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U035 | Sanjeev Sharma | sanjeevshakti@gmail.com | mn_addr_preprod1my00ew7dczpcu9j85rtr66xrtr3vqrmsq9lxt5xjc4lgcxd5kdmse5spmm | Requested more mobile answer space. | Kept responsive spacing in touched flows. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U036 | Anupam Jaiswal | anupamj0107@gmail.com | mn_addr_preprod16gt45h3d8fhf92s764rw2fwed89zgppw9emxlxmutn4mygvmn6usng9xta | Trusted revocation tracking. | Added revoked-credential validity guidance. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U037 | Bhalani Vijay | bhalanivijay@gmail.com | mn_addr_preprod1330vu985dle2umu934ex8t3thepgjp77uwtjq5l2ewjnpne0w5cs59au0l | Liked simple flow despite new technology. | Retained simple user flow around ZK technology. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U038 | Singara Velan | singaravelancsk@gmail.com | mn_addr_preprod1vzpjefk46y35ryk7ug77f3vdktytgpzem39l50r3vurp96pwhysqyewmc3 | Requested poor/excellent rating labels. | Rating labels remain feedback-form follow-up. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U039 | MD FARUKH | farukh1132@gmail.com | mn_addr_preprod1lxy8ukwynvqhtgcghgmknxd86pxne8gm3am5ggd8evps232teayqk67l7a | Liked on-chain institution checks. | Retained on-chain institution verification. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U040 | Rajjoo Bhai | bhairajjoo@gmail.com | mn_addr_preprod1yktjz8m509s2zhn8q7lsvl8fgtqv568re5hs280z6v023l0t0a7qck73tx | Requested seed-phrase warning. | Added seed-phrase safety warning. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U041 | Pankaj Sharma | pankajcws9729@gmail.com | mn_addr_preprod1nywnjngw9vuqfkdey4fdsmcxn8nrrl5023uyxpral5mnhj62395qsyvwdt | Requested visible wallet privacy note. | Added visible wallet privacy note. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U042 | Sharad Raut | shrd.raut@gmail.com | mn_addr_preprod14rxrkv5mzaht03q9lzkdv84qkqf3tysmtaka0rcg598pcl7ht2vsm75jqe | Liked portable, challenge-bound proofs. | Retained challenge-bound proof reuse model. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U043 | Ritesh Ranjan | riteshranjan1972@gmail.com | mn_addr_preprod12c8rn82vzr2flwmwe5f7sfqutrc3k0cag6saf7pejmwu9qp0wzxqmnjv09 | Liked question order. | Retained logical question order. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U044 | Sainarasimha Peddi Reddy | pvsnarasimha2003@gmail.com | mn_addr_preprod16cmuacx2wvzt2f9ycle4kxvc524n9wf9xa2dpntmxkawnqd2qe3sh84k87 | Interested in employer trial. | Employer trial remains future validation work. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U045 | Utkarsh Saraswat | buildwithutkarsh@gmail.com | mn_addr_preprod1dgcnaggmqvtzwx66a9vj0pt29spst4mrdm55pxsplzt8n9a6c6xsa5676l | Liked selected claims. | Retained selected-claims disclosure. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U046 | Mirshad Kvr | mirshadkvr19@gmail.com | mn_addr_preprod1h7t2a9j9pgrfhhuu5xee7hulh08rc2pnnrrttuh398s6czq0guesh9z4un | Liked developer read-only checks. | Retained developer read-only checks. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U047 | priyanshu pandey | pandeypriyanshu53@gmail.com | mn_addr_preprod16xtt6d9cmjelt9dfvuasckm5dqu6spd9jf9s07ntmhja8s8tcdpskd3la7 | Liked replay protection. | Retained replay protection. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U048 | Jiji Philip Varghese | jijlife@gmail.com | mn_addr_preprod1wtm7s7pgww0w3nzr47s5h2xsenkrk6mrsren4ctwj5sm89ttugzsh0ta33 | Requested complete success screen. | Added complete proof success state. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U049 | Vardhaann Rathore | anaxx34@gmail.com | mn_addr_preprod1332n8d6yhpkag5wft7h3c6jn2tcjupa4cpj07uglgc905vt0k7ps9ywwf4 | Liked proving without full document upload. | Retained no-full-document proof flow. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |
| U050 | Aman kumar | amankhdbensskbesbbe@gmail.com | mn_addr_preprod1a5lmvc0e4d6atv2zcsepxwnaxhglgmaxwjxdqsslsgcpyhmcmvxqyap9a0 | Asked to keep introduction simple. | Retained simple introduction copy. | [d140101](https://github.com/gyanrt53732277-hub/ProofFolio/commit/d140101223ca8d204a51ddf93daa03311cd0c6c4) |

Commit history contains 28 meaningful commits. See [public GitHub history](https://github.com/gyanrt53732277-hub/ProofFolio/commits/main).

## 💻 Developer Guide

### Quick Start
```bash
npm install
npm run compile
cd frontend && npm run dev
```

Open `http://localhost:3000/deploy`, connect the 1AM browser extension on Midnight
preprod, enter the deployment admin secret key, and click **Deploy Contract**.
Deployment uses 1AM's proving, balancing, and submission providers in-browser.
No funded server wallet or local proof server is required. The deployed contract
address appears on the page after submission.
Copy that address into `frontend/.env.local` as
`NEXT_PUBLIC_CONTRACT_ADDRESS` for the issuer, student, employer, and admin portals

### Testing & Integration
Use the built-in testing suite to run end-to-end ZK transactions logic:
* **URL:** `http://localhost:3000/developer-integration-guide`
* Provides wallet detection, contract ledger reads, and full lifecycle execution (`registerIssuer`, `issueCredential`, `presentCredential`).
