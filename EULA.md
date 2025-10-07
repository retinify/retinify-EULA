# retinify End User License Agreement (EULA)
**Issued:** 2025-10-07 (Tokyo)  
**Controlling Language:** English (a Japanese translation may be provided for convenience only)

Copyright © 2025 the Licensor. All rights reserved.  
“retinify” is a trademark of the Licensor (registered in Japan; registration or pending status may vary by jurisdiction).  
**Licensor (current):** Sensui Yagi — **Contact:** contact@retinify.ai

> **Non-Legal Summary (non-binding)**  
> Source-available (not OSI open source). **You may redistribute the source code (modified or unmodified) freely**, provided that **this same EULA** is passed down to all recipients **without change**, and **no re-licensing** occurs. You may view/modify source for internal use and ship compiled binaries in your Product.  
> Each Product is royalty-free until its lifetime Gross Revenue reaches USD 1,000,000; thereafter pay 5% on the excess, reported quarterly. **Downstream redistributors and recipients owe royalties (if any) directly to the Licensor under §8, see §8.10.**  
> Licensor-provided Models may be redistributed **verbatim only** (byte-identical). Internal conversions (e.g., TensorRT engine) are allowed but **not redistributable**.  
> This EULA is managed by **Issue Date** (not version numbers). Changes are posted with an Effective Date and take effect after a notice period (see §15).

---

## 1. Definitions
1.1 **Licensor:** the rights holder granting this EULA, including any successor or assign per §17. The current Licensor is Sensui Yagi.  
1.2 **Affiliate:** any entity that controls, is controlled by, or is under common control with a party, where “control” means >50% ownership or the ability to direct management.  
1.3 **Software:** source code, build scripts, toolchains, and related materials in the applicable retinify repository for this release, excluding **Models** and other non-code assets unless expressly stated.  
1.4 **Model:** any machine-learning artifact provided **by the Licensor** with this release (e.g., ONNX, weight checkpoints, tokenizer files) intended for inference or further training.  
1.5 **Third-Party Model:** a machine-learning artifact provided by a third party and included or referenced; governed solely by its own license (see §9; precedence clarified in §5.0).  
1.6 **Verbatim Model:** a Model that is byte-identical to an official Licensor release and verifiable by filename/version and/or published cryptographic hash (e.g., SHA-256).  
1.7 **Non-Verbatim Model:** any model/weights file that is not a Verbatim Model, including Converted Models and Derivative Models.  
1.8 **Converted Model:** any non-verbatim representation of a Model/weights (e.g., TensorRT plan/engine, CoreML, TFLite, TorchScript, altered precision/quantization, pruning).  
1.9 **Derivative Model:** any model derived from or substantially using a Model (fine-tuning, adapters/LoRA, distillation, pruning, quantization, format conversion, merged weights).  
1.10 **Derivative Work (Software):** any work based upon or incorporating the Software, excluding independent works communicating only via public APIs.  
1.11 **Model Output:** results produced by executing a Model or Derivative Model (e.g., disparities, confidence maps, embeddings).  
1.12 **Product:** any software, device, service, or feature (including SaaS/on-prem) that links to, incorporates, executes, or provides access to the Software and/or a Model/Non-Verbatim Model in production. Each app, game, device SKU, or SaaS service counts as a separate Product unless aggregated under **Product Family** in §1.13/§8.9.  
1.13 **Product Family:** a set of Products that share a substantially similar codebase or core functionality, including forks, sequels, remasters, regional variants, OEM/branded variants, or SKU splits that are materially the same for end users.  
1.14 **Gross Revenue:** all consideration received or receivable for a Product by you, your Affiliates, or your channel partners acting on your behalf (resellers, app stores, OEMs), including sales, subscriptions, usage fees, support/maintenance tied to the Product, integration fees, professional services bundled or required to use the Product, in-app purchases, and advertising/sponsorship revenue attributable to the Product, less only: (i) taxes/VAT remitted, (ii) payment processor fees, (iii) store/platform commissions, and (iv) refunds/chargebacks actually paid. Non-cash consideration (barter, tokens, credits, in-kind) is valued at fair market value when received. No other deductions (e.g., salaries, hosting, COGS, marketing, distributor margins beyond platform commissions) are permitted.  
→ **Allocation Priority.** Allocation shall follow, in order: (i) auditable feature-level usage metrics, (ii) contractually stated price of the feature, (iii) reasonable stand-alone price of comparable functionality (see Exhibit A).  
1.15 **Organization:** a legal entity together with its controlled subsidiaries.  
1.16 **Internal Use:** use within an Organization without external distribution and without monetization specific to the Product.  
1.17 **Official Hosting Platform:** Licensor-designated hosting (e.g., the official GitHub organization **github.com/retinify** and Licensor-controlled container registries).  
1.18 **TPM:** technical protection measures (license keys, activation, device binding, metering, feature gating, remote disable).  
1.19 **Header Files:** C/C++ headers (.h/.hpp) and interface definitions provided by the Licensor for building against the Software.  
1.20 **Minimal Runtime Components:** object code/libraries of the Software that are **strictly required at runtime** for your Product to function as linked/embedded against the Software; excludes samples, tests, tools, or materials intended to enable use of the Software independently of your Product. **Debug symbols** may be included where required by platform packaging or compliance, provided they do not alter functionality or public APIs.  
1.21 **Including** means “including, without limitation.”  
1.22 **Lifetime Gross Revenue Start:** for a Product (or Product Family per §8.9), the first day of the month in which revenue attributable to that Product (or Family) is first recognized.

---

## 2. Scope; Non-Consumer Use
This EULA governs business and developer use. If mandatory consumer protection laws apply, nothing in this EULA excludes or limits non-waivable rights or remedies; disclaimers/limitations apply only to the extent permitted by such laws.

### 2A. Assent; Eligibility (Deemed Acceptance)
By downloading, cloning, pulling, installing, building, executing, accessing, or otherwise using any part of the Software or Models (including obtaining updates, artifacts, or containers), you agree to be bound by this EULA on behalf of yourself and your Organization. If you do not agree, do not download, install, build, execute, access, or use; promptly delete all copies and cease distribution. You represent that you have authority to bind your Organization.

---

## 3. License Grant
Subject to full compliance, the Licensor grants you a non-exclusive, worldwide, non-transferable, revocable license to:  
(a) access, view, and locally copy the Software from the Official Hosting Platform;  
(b) modify the Software to create Derivative Works (Software) for Internal Use or inclusion in a Product;  
(c) use and distribute object code of the Software as part of a Product, consistent with §§4–8;  
(d) access and locally copy Licensor-provided **Models**; redistribute **Verbatim Models** per §5.1; convert Models for **Internal Use** per §5.5; **redistribute Header Files and Minimal Runtime Components per §5.4**.  
No patent, trademark, publicity, data, or other IP rights are granted except as expressly stated. **No implied licenses are granted.**  
**For clarity, redistribution of the Software’s source code is governed by §4.2 and §4.3.**

---

## 4. Collaboration; Source Code Redistribution; Compatibility
4.1 **Forking on Platform.** Fork/clone on the Official Hosting Platform for evaluation, collaboration, and contributions back to the Licensor.

4.2 **Source Redistribution (Permitted; Same-EULA Only).**  
You may redistribute the **source code** of the Software, in whole or in part, **modified or unmodified**, by any medium (including public mirrors and forks), **provided that all of the following are met**:  
(a) **Same EULA (Unmodified).** Every recipient receives the source **solely under this same EULA, verbatim and unmodified**, as the sole license governing the Software. You **may not** add, replace, or layer any other license terms (including OSS/copyleft terms) that purport to govern the Software.  
(b) **No Re-licensing / No Sub-Licensing of the Software Itself.** You may not re-license, sub-license, or otherwise grant rights in the Software under any terms other than this EULA. You may license **your contributions** or separate works under your chosen terms, but not in a way that imposes any obligations or restrictions on the Software beyond this EULA.  
(c) **Preservation of Notices.** You must retain all copyright notices, trademarks, license headers, and legal notices. A copy of this EULA must be included at the top level of the redistributed source (e.g., `EULA` or `EULA.md`).  
(d) **Attribution of Modifications.** Material modifications must be documented in a `CHANGES` or `NOTICE` file with the date and the name of the modifying party. This does not convert the Software’s license.  
(e) **No Circumvention.** Redistribution must not include or facilitate TPM circumvention or any tool primarily intended to bypass §5.2 (Model restrictions).  
(f) **Downstream Economic Terms Intact.** You must not represent any fee you charge for access, hosting, support, or distribution of the source as a “license fee” for the Software. **All royalties under §8 (if any) remain payable directly by the Product maker to the Licensor.** You may charge reasonable distribution/support fees that are economically independent of royalties.  
(g) **Flow-Down & Acceptance.** You must require your recipients to accept this EULA (click-through, shrink-wrap, or repository-gated acceptance is acceptable) **before** cloning, downloading, or using the Software.

4.3 **No Re-licensing; Mandatory Flow-Down.**  
You may not re-license or sub-license the Software or Models by themselves. **All recipients must be bound by this same EULA** (or by a signed enterprise agreement with the Licensor). You shall flow down terms at least as protective as this EULA in any ancillary terms you use, provided that such ancillary terms **cannot modify, diminish, or supersede this EULA** with respect to the Software or Models. Any attempt to apply copyleft or network-source-availability obligations to the Software is void.

4.4 **Copyleft Constraints; Compatibility Exception.** You may not combine or distribute the Software or Models in a manner that subjects them, in whole or part, to copyleft or similar reciprocal terms. Combining or linking the Software with third-party components under permissive or weak-copyleft licenses (e.g., MIT, BSD, Apache-2.0, LGPL) is permitted to the extent required by those licenses, provided that (i) no terms purport to re-license or impose copyleft or source-availability obligations on the Software itself, and (ii) your distribution complies with §5 and this EULA. Obligations imposed by a third-party open-source license on the third-party component itself (including notice, attribution, source-offer, and, for LGPL, dynamic-linking requirements) remain fully applicable and control for that component.  
→ **LGPL Static-Link Option.** Where LGPL components are **statically** linked due to platform constraints, you must provide a relinking mechanism or object files as required by the applicable LGPL terms.

4.5 **Patent Peace (Defensive Termination).** If you or your Affiliate initiates a patent claim alleging that the Software or Models infringe your patent, your rights under this EULA terminate automatically upon filing, to the maximum extent permitted by law.

---

## 5. Models: Verbatim-Only Redistribution; Third-Party Precedence
**5.0 Scope.** §5 applies **only** to Models provided by the Licensor under this EULA. **Third-Party Models** are governed **solely** by their respective licenses; in case of conflict, third-party terms **control** for those models (§9).  
5.1 **Verbatim Rule.** You may redistribute **Verbatim Models only** (byte-identical to the Licensor’s release), standalone or bundled with your Product, if you (i) include this EULA, (ii) retain notices/identifiers (filenames/version and checksum if provided), and (iii) do not remove identifiers or technical measures.  
5.2 **Non-Verbatim Prohibition.** Any non-identical file is **Non-Verbatim** and may **not** be distributed (Converted/Derivative models; repackaged, encrypted, or fragmented weights **where the primary purpose is to reconstruct non-verbatim artifacts by anyone other than the end user for strictly local execution**; or any transformed weights).  
5.3 **Remote Access.** Exposing a Model solely via remote execution (SaaS/API) is permitted; **you may not provide any functionality that exports, reconstructs, or makes available Non-Verbatim Models or training derivatives to end users, nor any tool primarily intended to do so.**  
5.4 **Redistributable Interfaces & Minimal Runtime.**  
You may redistribute, as part of your **Product** or your Product’s **developer SDK** for that Product, **(a) Header Files** (§1.19) and **(b) Minimal Runtime Components** (§1.20) strictly required to compile, link, or run your Product, subject to the conditions below. **No separate REDISTRIBUTABLES list is required.**  
**Conditions.** Redistribution under this §5.4 is permitted only if:  
(1) **Bundled Only:** Distributed solely as part of your Product (or its SDK) and not as a general-purpose retinify distribution.  
(2) **Unmodified Functionality:** Items are unmodified except for build/packaging metadata that does not alter functionality or public APIs.  
(3) **Minimum Necessary:** Include only what is strictly required; do not include samples, tests, or developer tools enabling independent use of the Software apart from your Product.  
(4) **EULA & Notices:** Include this EULA and retain all notices.  
(5) **No Model Workarounds:** Do not distribute any fragment, encrypted blob, script, or tool primarily intended to reconstruct or export **Non-Verbatim Models** or to bypass §5.2.  
(6) **SDK Scope:** If provided in a developer SDK, access and use are limited to developing add-ons or integrations **for that specific Product**.  
5.5 **Internal Conversions.** You may generate Non-Verbatim artifacts **solely for Internal Use** (e.g., device-local TensorRT build at install/first-run, local caching). Do not distribute such artifacts in any form.  
5.6 **Inline/Templated Code.** Code from Header Files compiled into your binaries via templates/inline/LTO is treated as object code. This does not convert any other source into redistributable material.  
5.7 **Static Linking & LTO.** Permitted; distribution of resulting binaries is allowed. This does not authorize distribution of non-redistributable source or Non-Verbatim Models.

---

## 6. Allowed, Exempt, and Prohibited Uses
6.1 **Royalty-Free Uses (always free):** (i) Internal Use; (ii) non-commercial academic/research; (iii) prototyping, evaluation, pre-release testing (no public monetization).  
6.2 **Prohibited:** (i) removing/obscuring notices; (ii) re-licensing/sub-licensing the Software/Models by themselves; (iii) reverse-engineering or circumventing TPM **except as permitted by law per §7**; (iv) using Licensor trademarks (including “retinify”) in names/domains/marketing without consent; (v) violating law or third-party rights (privacy, IP, export/sanctions).  
6.3 **Model Output.** Model Output belongs to the user/Organization operating the Product. This EULA imposes no license on Output; you remain responsible for lawful use.  
6.4 **Benchmarking & Public Claims.** You may publish benchmarks or comparisons **provided that** (i) they are accurate, reproducible, and not misleading, (ii) you disclose versions, settings, datasets, and hardware, (iii) you comply with Licensor trademark guidelines for any trademark use, and (iv) **synthetic-only results are clearly labeled as such**. **No prior written consent is required** to the extent permitted by applicable law. **Nothing in this Section restricts lawful, good-faith benchmarking or comparisons; the parties acknowledge this Section is not intended to restrict competition lawfully permitted under applicable antitrust/competition laws.**

---

## 7. TPM; Anti-Circumvention; Interoperability Carve-Out
The Licensor may require keys, activation, device binding, metering, feature gating, or remote disable for breach/fraud/security. Do not bypass, share, or disable TPM. Offline use, if permitted, may be time-limited and require periodic re-activation. Shipping fragments, encrypted blobs, scripts, or tools whose primary purpose is to reconstruct Non-Verbatim models outside the end user’s device-local build from a Verbatim Model obtained by that end user is prohibited.  
→ **Good-Faith Safeguards.** The Licensor will use commercially reasonable efforts to avoid false positives and to notify you without undue delay if a suspension was erroneously triggered, and will use reasonable efforts to restore erroneously suspended access **within five (5) business days after confirmation**.  
**Interoperability Carve-Out.** Nothing herein prohibits reverse engineering or circumvention **to the limited extent necessary to achieve interoperability with independently created software**, and **only** where such acts are permitted by applicable law and no more information is disclosed or used than strictly necessary.

---

## 8. Royalties & Enterprise Terms
8.1 **Rate & Threshold.** For each Product, pay **5%** of **Gross Revenue above USD 1,000,000 lifetime**.  
8.2 **Aggregation Across Affiliates/Channels.** Gross Revenue is aggregated across your Organization, Affiliates, and channel partners acting on your behalf, worldwide. Revenues collected by platforms/ad networks/payment intermediaries are included once credited or remitted.  
8.3 **Allocation.** For multi-component Products, bundles, or OEM arrangements, attribute a fair portion of Gross Revenue to functionality depending on the Software/Model. If such functionality is a primary driver of demand or technically required for the marketed use, the allocated portion shall be not less than a pro-rata share based on feature usage or, absent reliable usage metrics, not less than the highest standalone price of comparable functionality.  
8.4 **Recognition & Currency.** Royalties accrue when consideration is earned or received, whichever is earlier, under GAAP/IFRS principles applied consistently. **Convert non-USD amounts using the WM/Refinitiv Closing Spot rate at the last business day of the calendar quarter. Royalties shall be paid in USD by wire transfer to the account designated by the Licensor, unless the Licensor approves JPY payments at the TTM rate published by MUFG Bank at quarter-end. Amounts are exclusive of withholding taxes. If any withholding is required by law, you shall (i) deduct and remit such tax, (ii) provide valid tax receipts, and (iii) use reasonable efforts to apply treaty reductions; no gross-up applies unless agreed in an Enterprise Agreement.** Non-cash consideration is valued at fair market value when received. **No set-off or netting across Products or periods.** **Upon request, the Licensor will issue commercially reasonable receipts or invoices (including VAT-compliant invoices where legally required) reflecting amounts paid. You shall provide any forms reasonably necessary to apply treaty-reduced withholding rates.**  
→ **FX Fallback.** If the WM/Refinitiv rate is unavailable, use the **Bank of Japan** published rate for the same date.  
8.5 **Reporting & Payment.** Within 30 days after each calendar quarter (**measured in JST, UTC+9**), submit a royalty report **for each Product for any quarter in which Royalty is due** and pay due royalties.  
**Zero/Skip Reporting.** You may **submit a simplified zero report** or **skip the quarterly report** for a Product if **both** of the following are true for that calendar quarter:  
(a) the Product generated **no Gross Revenue** attributable under this EULA **or** the Product’s **lifetime Gross Revenue remains below USD 1,000,000**, and  
(b) you have **no royalty payable** for that quarter for the Product.  
To skip, you must either (i) file a **No-Activity Confirmation** (one-click or short form as provided by the Licensor) or (ii) record the skip via the Licensor’s designated portal/API if available. **If the Licensor’s portal/API is not available, you may submit a No-Activity Confirmation or royalty report by email to **finance@retinify.ai** (or **contact@retinify.ai** as fallback), using a reasonable template that states Product name, period, Gross Revenue, and calculation basis.** **Each No-Activity Confirmation must be retained for five (5) years and include Product name, quarter (JST), statement of zero (0) Gross Revenue or sub-threshold status, calculation basis, signatory name, and timestamp.**  
If you fail to report where royalties are due, the Licensor may reasonably estimate amounts due based on available data; such estimates are binding absent manifest error. Provide underlying sales counts, ASP, platform statements, and basis of allocation on request.  
**Failure to Report / Reminder.** **If you neither submit a royalty report where due nor record a No-Activity Confirmation for two consecutive quarters, the Licensor may issue a notice requiring a report within 15 days; failure to respond permits reasonable estimation under §8.5 and suspension under §8.6.**  
8.6 **Late & Willful.** Overdue amounts accrue interest at the lesser of 1%/month or the maximum allowed by law. Willful underreporting (>10% underpayment or repeated failures) may trigger: (i) 2× assessed shortfall as liquidated damages, (ii) suspension of keys/updates, and (iii) termination under §15, **to the maximum extent permitted by law**.  
8.7 **Anti-Avoidance.** You may not split, rebrand, or restructure materially the same Product to evade thresholds/royalties. Revenue from support, maintenance, training, integrations, custom features, or hosting necessary to use the Product is included. Donations/sponsorships tied to the Product are included.  
8.8 **Enterprise Options.** The Licensor may offer enterprise terms (e.g., buy-out, capped royalty, permission to distribute Non-Verbatim models).  
8.9 **Product Family Aggregation.** Where multiple SKUs/regional variants/OEM-branded or minor-revision Products are **materially the same** for end users, they constitute a **Product Family** and their revenues **aggregate** toward a **single** USD 1,000,000 lifetime threshold and ongoing royalty computation.  
8.10 **Downstream Royalty Direct-Pay; No Interception.**  
Redistribution of the Software (including source) does **not** entitle any redistributor to collect or retain royalties due under this EULA. **Each Product maker (including any downstream recipient) owes royalties, if any, directly to the Licensor** under §§8.1–8.9. Redistributors may charge reasonable hosting/support fees, **but must not label or collect them as “license fees” for the Software** and must not represent that royalties are payable to anyone other than the Licensor. Upon reasonable request, a redistributor shall (i) point downstream Product makers to the Licensor’s reporting portal or contact, and (ii) provide a standard notice stating that royalties under this EULA, if applicable, are payable directly to the Licensor.

---

## 9. Third-Party Software, Models & Data
Third-party components, **Third-Party Models**, and datasets remain under their own terms. **In the event of a conflict between this EULA and a third-party license applicable to a third-party component/model/data, the third-party terms control solely for that item.** You must include any legally required third-party license texts with your distribution and comply with attribution/source-offer obligations for such dependencies.

---

## 10. Contributions, Feedback, Pre-release
Contributions made on the Official Hosting Platform are licensed to the Licensor under terms compatible with this EULA; the Licensor may re-license them to distribute the Software/Models. You warrant you own/convey necessary rights. The Licensor may require a CLA/DCO.  
Feedback is granted to the Licensor on a **non-exclusive, worldwide, perpetual, irrevocable, royalty-free, fully paid, sublicensable** basis for any purpose.  
Pre-release materials are confidential unless published by the Licensor.

---

## 11. Warranty Disclaimer
TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE SOFTWARE AND MODELS ARE PROVIDED “AS IS” AND “AS AVAILABLE,” WITH NO WARRANTIES OF ANY KIND, EXPRESS, IMPLIED, OR STATUTORY, INCLUDING WITHOUT LIMITATION ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, NON-INFRINGEMENT, QUIET ENJOYMENT, ACCURACY, OR THAT ERRORS OR DEFECTS WILL BE CORRECTED. THE LICENSOR DOES NOT WARRANT THAT THE SOFTWARE/MODELS OR ANY OUTPUTS WILL BE UNINTERRUPTED, SECURE, OR FREE OF HARMFUL COMPONENTS, OR THAT THEY WILL MEET YOUR REQUIREMENTS OR ACHIEVE ANY PARTICULAR RESULTS. NO ADVICE OR INFORMATION (ORAL OR WRITTEN) CREATES ANY WARRANTY. THE LICENSOR HAS NO OBLIGATION TO PROVIDE SUPPORT, UPDATES, OR SERVICE LEVELS, EXCEPT AS MAY BE EXPRESSLY AGREED IN A SEPARATE SIGNED ENTERPRISE AGREEMENT, **TO THE FULLEST EXTENT PERMITTED BY APPLICABLE LAW**.

---

## 12. Limitation of Liability; High-Risk Uses
12.1 **Exclusion of Certain Damages.** TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE LICENSOR SHALL NOT BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, EXEMPLARY, OR PUNITIVE DAMAGES, OR FOR ANY LOSS OF PROFITS, REVENUE, GOODWILL, OR DATA, OR COST OF SUBSTITUTE GOODS OR SERVICES, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.  
12.2 **Aggregate Cap.** TO THE MAXIMUM EXTENT PERMITTED BY LAW, THE LICENSOR’S AGGREGATE LIABILITY FOR ALL CLAIMS ARISING OUT OF OR RELATING TO THE SOFTWARE, MODELS, OR THIS EULA SHALL NOT EXCEED **THE GREATER OF (A) USD 25,000 OR (B) THE TOTAL FEES AND ROYALTIES YOU ACTUALLY PAID TO THE LICENSOR UNDER THIS EULA IN THE TWELVE (12) MONTHS PRECEDING THE EVENT**, EVEN IF ANY REMEDY FAILS OF ITS ESSENTIAL PURPOSE, **UNLESS OTHERWISE AGREED IN A SIGNED ENTERPRISE AGREEMENT**.  
12.3 **Carve-Outs Required by Law.** NOTHING IN THIS EULA EXCLUDES OR LIMITS LIABILITY TO THE EXTENT THAT SUCH EXCLUSION OR LIMITATION IS PROHIBITED BY MANDATORY LAW, INCLUDING LIABILITY FOR WILLFUL MISCONDUCT OR GROSS NEGLIGENCE UNDER APPLICABLE LAW, OR (WHERE SUCH LIMITATION IS NOT PERMITTED) FOR DEATH OR PERSONAL INJURY CAUSED BY NEGLIGENCE.  
12.4 **High-Risk Uses.** THE SOFTWARE/MODELS ARE NOT DESIGNED FOR HIGH-RISK USES (MEDICAL, LIFE SUPPORT, AVIATION, NUCLEAR, AUTONOMOUS DRIVING, OR OTHER SAFETY-CRITICAL). YOU MUST NOT USE THEM IN SUCH SETTINGS; IF YOU DO, YOU ASSUME ALL RISK AND SHALL INDEMNIFY THE LICENSOR UNDER §13.  
12.5 **Exclusive Remedies.** YOUR SOLE AND EXCLUSIVE REMEDIES FOR ANY CLAIM RELATING TO THE SOFTWARE/MODELS OR THIS EULA ARE THOSE EXPRESSLY PROVIDED IN THIS EULA.

### 12A. Time Limit to Bring Claims
Any claim arising out of or relating to this EULA, the Software, or the Models must be filed within **twenty-four (24) months** after the cause of action accrues, **except where a longer period is required by applicable law**.

---

## 13. Indemnification; Compliance
You shall defend, indemnify, and hold harmless the Licensor and its Affiliates, officers, employees, and agents from claims, damages, liabilities, and costs (including reasonable attorneys’ fees) arising from: (i) your Products or Model Outputs; (ii) your data/content; (iii) your combination with other items; (iv) your distribution in violation of this EULA; (v) your breach of law/third-party rights.  
You shall comply with applicable laws, including export controls and sanctions; **including without limitation the Foreign Exchange and Foreign Trade Act of Japan (外為法), the U.S. Export Administration Regulations (EAR), and applicable EU dual-use regulations**, and you represent you are not prohibited from receiving the Software/Models.

---

## 14. Records, Audit, and Confidentiality
Maintain complete and accurate books for 5 years. With 15 days’ notice, the Licensor may audit relevant records no more than once/year (unless material breach is reasonably suspected). Audits shall occur during normal business hours, use **a mutually acceptable independent auditor**, and be limited to records reasonably necessary to verify compliance, with **data-minimization** applied.  
**Data Handling.** Auditor access to electronic records shall occur **on-site or via a secure virtual data room (VDR)**. Raw datasets shall **not** be copied offsite except for **de minimis samples** strictly necessary to verify computations; personal or sensitive data shall be **redacted or anonymized where feasible**. The auditor shall be bound by confidentiality and free of conflicts of interest. **The auditor shall not retain copies of personal data or raw transactional data beyond what is strictly necessary; any extracts shall be deleted or returned within 30 days after audit completion, with written confirmation upon request.**  
The Licensor bears audit costs unless material underpayment (>5%) is found, in which case you reimburse audit costs and the shortfall with interest. Audit information is confidential and used solely for compliance verification. You shall procure cooperation from Affiliates and relevant channel partners and ensure agreements include cooperation provisions sufficient for this Section.

---

## 15. Changes; Term; Termination; Survival
**15.1 Changes (Issue/Effective Dates).** The Licensor may modify this EULA on **reasonable grounds** (including compliance with law/regulation/guidance; security, anti-abuse, TPM or integrity needs; or material product/service/business changes). Each update will state an **Issue Date** and an **Effective Date** at least **30 days** later (**“Notice Period”**). **Materially adverse changes to economic terms (royalty rate/threshold) apply only prospectively** and **only** to Gross Revenue recognized **on or after** the Effective Date. For any release you downloaded before the Effective Date, you may continue under the EULA that accompanied that release (**“Pinned EULA”**) **provided you do not access new keys, updates, or hosting that require acceptance of the then-current EULA**.  
**15.2 Notice.** The Licensor will post changes on the Official Hosting Platform and use commercially reasonable efforts to email registered commercial users. **Posting on the Official Hosting Platform _Releases_ page constitutes notice; security-motivated changes may also be posted via GitHub Security Advisories.**  
**15.3 Objection/Wind-down.** If you reasonably object to a change, you may decline the new EULA, continue under the Pinned EULA for that prior release, and **wind down distribution of updates for up to 90 days**.  
**15.4 Term/Termination.** This EULA is effective until terminated. The Licensor may terminate upon your material breach (including non-payment, circumvention, or unauthorized distribution), after notice and 30 days to cure if curable. Upon termination, cease use and distribution of the Software, Models, and derivatives; you may continue to distribute Products already shipped to end users, provided all due royalties are paid.  
**15.5 Survival.** Sections **8**, 6–14, 12A, and 16–18 survive termination.

---

## 16. Governing Law; Venue; Injunctive Relief; Mandatory Law
This EULA is governed by the laws of Japan. The parties submit to the exclusive jurisdiction of the Tokyo District Court. Given potential irreparable harm, the Licensor may seek injunctive/equitable relief for actual or threatened breaches of §§4–8, 12–15 in any competent court. Conflict-of-laws rules and mandatory laws of applicable jurisdictions may apply where they cannot be waived.  
**Optional Arbitration.** Upon mutual agreement for a specific dispute, the parties may submit the dispute to arbitration administered by the **Japan Commercial Arbitration Association (JCAA)** seated in Tokyo, conducted in English under the JCAA rules. This option does not limit either party’s right to seek interim or injunctive relief in court.

---

## 17. Assignment; Change of Control; Successors
You may not assign this EULA without the Licensor’s consent, except to a successor by merger or sale of substantially all assets, provided the successor assumes all obligations and is not a sanctioned/prohibited party. The Licensor may assign this EULA (including by corporate conversion or transfer of the retinify business). Any unauthorized assignment is void.

---

## 18. Order of Precedence; Severability; No Waiver; Force Majeure; Entire Agreement; Notices; Document History
**Precedence.** A signed Enterprise Agreement (if any) controls; otherwise this EULA controls over ancillary docs.  
If any provision is unenforceable, the rest remains effective (modified to the minimum extent to be enforceable). Failure to enforce is not a waiver. The Licensor is not liable for delays/failures due to events beyond reasonable control. This EULA is the entire agreement for this release and supersedes prior understandings.  
**Notices.** Notices may be provided by posting on the Licensor’s official website or repositories and/or by email to contacts you provide; you agree that such posting constitutes notice.  
**Document History (Issue Dates):** 2025-10-07 (initial public issuance).

---

### Exhibit A — Revenue Attribution (Informative)
**SaaS.** If the retinify-powered feature is core, attribute full subscription/usage revenue; if an optional add-on, attribute that add-on’s revenue.  
**Embedded Device.** If the primary device function depends on the Software/Model, attribute the device price (after allowed deductions); if optional, attribute the incremental option price.  
**Ads/Services.** Attribute advertising revenue and fees for services necessary to use the Product pro-rata to the enabled feature’s usage (see §8.7).  
**Family Rule.** Where Products are materially the same for end users, treat them as a **single Product Family** and **aggregate** revenue toward one threshold (§8.9).  
**Example (Family).** *Variants that differ only in SKU name, region, branding, or cosmetic changes while sharing the same core functionality/codebase are treated as one Product Family.*

### Exhibit B — Verbatim-Only Redistribution Rule (Informative)
**Redistributable.** Only the exact files as distributed by the Licensor for the relevant release (verified by official filename/version and/or published checksum).  
**Not Redistributable.** Any non-identical file is Non-Verbatim and must not be distributed (Converted/Derivative weights; repackaged, encrypted, or fragmented weights intended to reconstruct non-verbatim artifacts by anyone other than the end user for strictly local execution; or any transformed weights).  
**Internal-Only Conversions.** You may generate Non-Verbatim artifacts solely for Internal Use (e.g., device-local TensorRT build at install/first-run). Do not distribute such artifacts in any form.
