# TM265 — SAP Joule for Consultants: Unified Knowledge for Requirements and Designs
## Hands-On Session: MM Consultant Edition — From Workshop to Specification
### Powered by Scope Item 18J · Requisitioning & Direct Procurement

> **Session Code:** TM265
> **Session Duration:** 🕓 ~100 minutes
> **Level:** Intermediate
> **Persona:** MM Functional Consultant
> **Prerequisites:** Access credentials provided by session speakers

---

## Session Overview

In this hands-on session, you will follow **Raj Kumar** — an MM consultant who just walked out of a 56-minute Fit-to-Standard workshop — as he uses every major J4C capability to turn a raw transcript into a complete documentation package: user stories, sprint backlog, functional specification, pseudo code, and a steering committee deck.

Every feature is grounded in a real MM consulting scenario on SAP best practice scope item **18J — Requisitioning and Direct Procurement**.

---

## Exercise Agenda

| Exercise | Topic | Est. Time |
|---|---|---|
| 0 | Access & Setup | 10 min |
| — | **Concept: Three Ways to Make J4C Personal** | **10 min** |
| — | 🔷 **Use Case 1 — Workshop to Specification** | |
| 1 | Expert Workspace: Create the Fit-to-Standard Workshop Expert | 20 min |
| 2 | File Upload: Workshop Transcript | 15 min |
| 3 | Document Generation | 15 min |
| — | 🔶 **Use Case 2 — Requirements from BPD to Specification** | |
| 4 | Custom Knowledge Grounding | 15 min |
| — | Wrap-up & Q&A | 5 min |
| **Total** | | **90 min** |

---

## Exercise 0 — Access Joule for Consultants

**Estimated Time: 🕓 10 minutes**

> **📍 Raj's Story** | *Today, 57 minutes after the workshop ended*
>
> The 18J Fit-to-Standard workshop just wrapped. 56 minutes, 14 user stories captured, four GAPs identified, four BAdI enhancements scoped. Raj Kumar closes his notebook and opens his laptop. He has a commitment to Ankit: functional specification drafts before the 22nd. He has a recording transcript and J4C.
>
> He opens Joule for Consultants. This is where the documentation work begins.

In a new browser tab, open SAP Joule for Consultants:

> **URL:** `https://internal-event-sap-joule-for-consultants-marcus-1r5l4cxm.eu10.sapdas.cloud.sap/joule`

Log in using the credentials provided. You should land on the **J4C Home screen**.

---

---

## Three Ways to Make J4C Personal

**Estimated Time: 🕓 10 minutes**

> 📖 **Reference:** [SAP Joule for Consultants Gets Personal at SAP Sapphire 2026](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-joule-for-consultants-gets-personal-at-sap-sapphire-2026/ba-p/14404400)

Out of the box, J4C is grounded in SAP's 9 TB knowledge base. But every engagement is different. Raj's engagement has JouleTech-specific procurement policies, a just-completed workshop transcript, and four custom BAdI developments the SAP knowledge base has never seen.

At SAP Sapphire 2026, SAP introduced three complementary ways to bring customer-specific context into J4C. The right choice depends on how long you need the context to last and who needs access to it.

> **Important:** None of these files are ever used to train the underlying LLM. Your content stays yours.

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   ORGANISATIONAL   ┤  Custom Knowledge Grounding                   │
│                    │  · Entire J4C tenant                          │
│                    │  · JouleTech procurement policy docs, SOPs    │
│                    │                                               │
│   PROJECT /        ┤  Expert Workspace File Upload                 │
│   ENGAGEMENT       │  · Persistent across all conversations        │
│                    │  · 18J workshop artefacts, BAdI specs         │
│                    │                                               │
│   CONVERSATION     ┤  Prompt-Level File Upload                     │
│                    │  · This conversation only, 7-day auto-delete  │
│                    │  · The transcript Raj just received           │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

| | Prompt-Level Upload | Expert Workspace Upload | Custom Knowledge Grounding |
|---|---|---|---|
| **Scope** | Single conversation | One Expert / user | Entire J4C tenant |
| **Who sets it up** | Any user | Any user | Administrator |
| **Persistence** | Auto-deleted after 7 days | Persists until deleted | Persists until removed |
| **Storage limit** | Up to 10 MB per file | 1 GB total / 10 MB per file | Depends on data repository |
| **Supported formats** | PDF, TXT, DOCX, XLSX, CSV, MD · PNG, JPEG, JPG, WEBP | PDF, TXT, DOCX, XLSX, CSV, MD · PNG, JPEG, JPG, WEBP | PDF, DOCX, HTML, TXT · PNG, JPEG, JPG, TIFF, PPT |
| **Best for** | Workshop transcript, one-off analysis | Recurring engagement context | Shared org standards, SOPs |
| **Hands-on exercise** | Exercise 3 ↓ | Exercise 1 ↓ | Exercise 2 ↓ |


---

---

---

## 🔷 Use Case 1 — Workshop to Specification
*Expert Workspace · File Upload · Document Generation*

---

## Exercise 1 — Expert Workspace: Create the Fit-to-Standard Workshop Expert

**Estimated Time: 🕓 20 minutes**

> **📍 Raj's Story** | *Monday, 1:00 PM*
>
> The 18J workshop just ended. 14 user stories captured, four GAPs identified, four BAdI enhancements scoped. Every FIT/GAP call Raj made in that room — the logic, the rationale, the clean core judgements — lives only in his head. The junior consultant joining next week will need those same answers. So will the customer's project manager when they challenge a GAP decision.
>
> Raj's first move: codify what he learned. He creates the 18J Fit-to-Standard Analyst Expert so anyone on the team can open a new conversation, ask "is this a fit?", and get a consistent, scoped answer — without needing to have been in the room.

### Exercise 1.1 — Create a Fit-to-Standard Analyst Expert

The FTS Expert captures your workshop knowledge in a reusable form. When a consultant — or the customer's project team — asks about a specific requirement, the Expert classifies it against SAP 18J standard capabilities consistently, every time.

1. Navigate to **Console → Expert Workspace**.
2. Click the **Expert Library** tab.
3. Select **"Fit-to-Standard Analyst"** template, or use a **Starter Template** to build from scratch.
4. Name it *"18J Fit-to-Standard Analyst"* and click **Save**.
5. Click **Edit Instructions** and apply this structure:

```
ROLE: You are an SAP MM Fit-to-Standard analyst specialising in scope item 18J — Requisitioning and Direct Procurement on SAP S/4HANA Cloud Private Edition. Your job is to map customer requirements against SAP standard capabilities and produce clear FIT / PARTIAL FIT / GAP classifications with rationale.

CONTEXT:
- Customer: JouleTech Industries (B2B industrial equipment manufacturer)
- Company Code: 2330
- Workshop findings: 10 standard user stories confirmed FIT, 4 GAPs identified with BAdI approach (ME_PROCESS_REQ_CUST, ME_PROCESS_PO_CUST)
- Scope boundary: vendor currency check scoped to Purchase Organisation YYYY only; document currency check applies to all of Company Code 2330

CLASSIFICATION FORMAT — use for every requirement:
- Classification: FIT | PARTIAL FIT | GAP
- SAP Standard Capability: what the standard delivers out of the box
- Delta (if PARTIAL FIT or GAP): what is missing from standard
- Recommended Approach: configuration path, or BAdI / clean core extension option
- Clean Core Status: COMPLIANT | REVIEW NEEDED
```

6. Click **Add Suggested Questions** and add:
   - *"The customer wants PR approvals based on cost centre hierarchy — is this a FIT in SAP S/4HANA release strategy?"*
   - *"Can SAP standard handle a hard-block on PRs where document currency differs from company code currency?"*
   - *"Is manual entry of a free-text business justification on PRs for critical materials a FIT or GAP?"*

7. Save the instructions.

> **💡 Expert lifecycle:** This is an Explore-phase Expert. Its value is highest during and immediately after Fit-to-Standard workshops — when requirements are being classified and GAPs are being scoped. Once Realize begins, the Procurement Advisor (Exercise 1 optional extension) takes over as the primary Expert.


### Exercise 1.2 — Use the FTS Expert in a New Conversation

This is the core pattern: the Expert is built once, then consultants and the customer's project team open it in fresh conversations to extract and classify workshop findings — without re-explaining the context each time.

1. Click **New Conversation** (top left).
2. In the Expert picker, select **"18J Fit-to-Standard Analyst"**.
3. Upload **`FTS-18J-Workshop-Transcript.docx`** using the attachment icon.
4. Submit **Prompt 1** from the JouleTech prompt library, filling in the placeholders:

   > *"As a MM consultant, a fit to standard workshop is conducted in **[Procurement]** on business process scope item **[18J — Requisitioning and Direct Procurement]**. Based on attached fit to standard workshop transcript, extract user stories in a table with list of user stories, Personas and tag user stories as standard or gap."*

5. Review the output — a structured table of ~14 user stories, each tagged **STANDARD** or **GAP**, with persona column.

> **💡 The key insight:** The Expert's instructions shape how J4C reads the transcript. Without the FTS Expert active, the same prompt gives a generic summary. With the Expert, every response follows the FIT/PARTIAL FIT/GAP classification format you defined in Exercise 1.1.


### Exercise 1.3 — Share with the Team Next to You

Turn to the team sitting next to you. Ask one of them for their J4C email address and share your **18J Fit-to-Standard Analyst** Expert with them.

1. From **My Experts**, find your **18J Fit-to-Standard Analyst** card and click **Share**.
2. Ask someone from the neighbouring team for their email address (same J4C tenant).
3. Enter their email and click **Share**.
4. If the neighbouring team shares their Expert back with you, open it and compare — notice how different instructions produce different classification behaviour.

> **⚠️ Note:** Only instructions are shared — attached files are not included. Each recipient gets an independent copy they can customise without affecting your original.


---

## Exercise 2 — File Upload: Workshop Transcript

**Estimated Time: 🕓 20 minutes**

> **📍 Raj's Story** | *Monday, 2:00 PM*
>
> The Expert is set up. The grounding pipeline is live with JouleTech's policy documents and the WRICEF template. Now Raj brings in the raw material: the workshop transcript. He uploads it to a new conversation and runs the six prompts — extracting user stories, tagging FIT and GAP, generating the sprint backlog, and producing the first draft functional specification. Each prompt builds on the previous one in the same conversation thread.

**Supported formats and limits:**

| Format | Max Size | Additional Limits | Notes |
|---|---|---|---|
| PDF | 10 MB | ~600,000 chars · ~100 pages | Embedded images not processed |
| TXT | 10 MB | ~600,000 chars | — |
| DOCX | 10 MB | ~600,000 chars | Embedded images not processed |
| XLSX | 10 MB | — | — |
| CSV | 10 MB | — | — |
| MD | 10 MB | ~600,000 chars | — |
| PNG, JPEG, JPG, WEBP | 10 MB | Max 3072 × 3072 px | — |


### Exercise 2.1 — Analyse the Workshop Transcript

1. Start a **new conversation** in J4C.
2. Upload **`FTS-18J-Workshop-Transcript.docx`** using the attachment icon.
3. Submit:

   > **Example query:**
   > *"This is the transcript from a Fit-to-Standard workshop on SAP scope item 18J — Requisitioning. Summarise the session in 5 bullet points: the process steps covered, the key FIT confirmations, the GAP items identified with the proposed BAdI approach for each, and any scope boundaries agreed."*

4. Review the response. Notice how J4C picks up the exact scope boundary confirmed at the end of the session — vendor currency check scoped to Purchase Organisation YYYY only, document currency check applying to all of Company Code 2330.

> **💡 Keep this conversation open.** The transcript is loaded as context. Continue in this same conversation for Exercise 2.2 — the prompt library prompts pick up from here.


### Exercise 2.2 — Use the JouleTech Prompt Library — Use a Prompt from the JouleTech Custom Library

> **Note:** The **JouleTech** custom prompt tab has been pre-loaded into this session's tenant — exactly as Raj found it.

1. In the Prompt Library, click the **JouleTech** tab.
2. Select **"Prompt 1 — Extract User Stories from FTS Workshop Transcript"**.
3. Go back to the conversation from Exercise 1.1 (where the transcript is loaded) and paste the prompt, filling in the placeholders:
   - `[WORKSTREAM]` → Procurement
   - `[SCOPE ITEM ID AND NAME]` → 18J — Requisitioning and Direct Procurement
4. Submit and review the user story table.

   **Expected output:** ~14 user stories — 10 STANDARD FIT, 4 GAP (Enhancement-1 through Enhancement-4), each with BAdI reference and scope boundary note.

5. Now use **"Prompt 2 — Generate Sprint Backlog from GAP User Stories"** as a follow-up in the **same conversation**:
   - Fill in Sprint 1 start date: **25 Sep 2026**

   **Expected output:** 4 backlog items (BI-01 through BI-04), sprint assignments, Fibonacci story points, dependencies.

6. Star both MM/18J prompts for fast access on future 18J engagements.

> **💡 How the JouleTech tab was created:** An admin uploaded `MM-18J-Prompt-Library.xlsx` via Console → **Manage Templates** → **Upload Templates**, then toggled status to **Published**. All tenant users see the tab immediately.

### Exercise 2.3 — Multi-File Analysis *(Optional — if time permits)*

— Multi-File Cross-Table Analysis ⭐ Real Customer Use Case

> **💡 Why this matters:** A real customer uploaded multiple SAP data exports and expected J4C to infer the table relationship — without being told how to join them.

1. Start a **new conversation**.
2. Upload **both files at once**:
   - **`jouletech-material-master.csv`** — material master (MATNR, description, status)
   - **`jouletech-open-orders.csv`** — open sales order line items (MATNR, customer, value)
3. Do **not** explain the relationship. Submit:

   > **Example query:**
   > *"Which materials have open customer orders but are marked as discontinued or phased out? List the material, customer, order number, quantity, and value."*

4. J4C should infer MATNR as the join key and return materials NT-1005 (MMSTA 30, Phased Out) and NT-1018 (MMSTA 99, Discontinued) — both with live orders.

5. Follow up:

   > *"What is the total open order value by material group? Which group has the highest exposure?"*

---

## Exercise 3 — Document Generation

**Estimated Time: 🕓 15 minutes**

> **📍 Raj's Story** | *Monday, 5:00 PM*
>
> User stories extracted. Sprint backlog drafted. Now Raj moves to document generation. The transcript conversation is still open. He runs Prompt 3 — the functional specification — directly in the same thread.

J4C can generate structured documents — Word (.docx) and PowerPoint (.pptx) — directly from a conversation, without a pre-defined template.

### Exercise 3.1 — Generate the Functional Specification (Word)

1. Go back to the conversation from Exercise 3 (transcript loaded, user stories and backlog already generated).
2. Continue in the **same conversation** with Prompt 3 from the JouleTech prompt library:

   > **Prompt:**
   > *"Generate a Word document: a functional specification for Backlog Item BI-04 — Business Justification for Critical and Strategic Materials. Include the following 7 sections:*
   > *1. Introduction (project background, scope item 18J, Company Code 2330 scope)*
   > *2. Purpose of Document*
   > *3. Why Development is Required (reference the workshop GAP finding)*
   > *4. Technical Details (BAdI ME_PROCESS_REQ_CUST, text type ZBUSJ, classification characteristic ZMAT_CRITICALITY class type 001, message class Z_MM_PROC_MSG message 003)*
   > *5. User Stories (in 'As a / I want / So that' format)*
   > *6. Test Cases (5 test cases as a table: happy path, blank justification block, non-critical material bypass, integration with PR approval, audit log verification)*
   > *7. Document History (Version 1.0, today's date, Author: Raj Kumar)"*

3. Download the `.docx`. This is a production-ready first draft — grounded in the transcript, not fabricated.

### Exercise 3.2 — Generate the Steering Committee Deck (PowerPoint)

1. In a **new conversation**, submit:

   > **Prompt:**
   > *"Create a PowerPoint presentation for the JouleTech steering committee. Title: S/4HANA 18J Requisitioning — Fit-to-Standard Workshop Summary and Next Steps. Include slides: (1) Workshop Overview and Scope, (2) Process Coverage — FIT Confirmations (list all 10 standard user stories), (3) Gap Analysis — 4 Enhancement Items with BAdI approach for each, (4) Sprint Plan — BI-01 through BI-04 with sprint IDs and priorities, (5) Decisions Required from Steering Committee, (6) Next Steps and Timeline. Professional consulting tone. Add speaker notes to each slide."*

2. Download and review the `.pptx`.
3. Iterate:

   > *"Add a slide after slide 2 showing the six 18J process steps as a numbered visual flow."*

### Exercise 3.3 — In-Conversation Technical Specification *(if time permits)*

Continue in the functional spec conversation and submit Prompt 4 (Pseudo Code), Prompt 5 (Technical Specification), and Prompt 6 (Unit Test Script) from the JouleTech prompt library. The full 9-section technical spec — data model, transport strategy, authorizations, exception handling — produced in two follow-up prompts.

> **💡 The distinction:** Exercises 5.1 and 5.2 generate *files*. Exercise 5.3 generates *consulting content in the flow of the conversation* — which you then decide how to package. Both patterns have their place.

---


---

---

## 🔶 Use Case 2 — Requirements from BPD to Specification
*Custom Knowledge Grounding · Document Generation*

---

## Exercise 4 — Custom Knowledge Grounding

**Estimated Time: 🕓 15 minutes**

> **📍 The scenario**
>
> The customer — Nexstream — has provided their **Billing & Invoicing Business Requirements document** (`Business_Requirements_Billing_Invoicing_Nexstream.docx`). The session facilitators have uploaded this file to a SharePoint and connected it to J4C via Custom Knowledge Grounding. J4C can now answer questions directly from the BPD — surfacing how individual requirements map to standard S/4 HANA capabilities, identifying relationships between requirements, and generating functional specifications — without the consultant reading through the entire document.

### Step 1 — Add the BPD to SharePoint

> **📋 Facilitator pre-step (already done for this session):** Upload `Business_Requirements_Billing_Invoicing_Nexstream.docx` to the designated SharePoint site connected to the J4C Custom Knowledge Grounding pipeline.

In your own engagement, the equivalent step is:
1. Upload the customer's BPD to your SharePoint site (or other connected repository — AWS S3, Google Drive, SAP DMS).
2. The grounding pipeline picks it up on its next refresh cycle (daily, or triggered manually).
3. From that point, any J4C conversation can query the document.

### Step 2 — Query the BPD

Custom Knowledge Grounding is already enabled for this session's tenant. Start a new conversation and run both prompts.

1. Click **New Conversation**.
2. Run **Prompt 1**:

   > *"How can REQ-09 can be addressed, the requirement is referred in S/4 HANA BRIM BPD"*

   J4C retrieves REQ-09 from the Nexstream BPD, identifies where it maps to standard S/4 HANA capabilities, and explains the recommended approach — with a source citation referencing the document.

3. Run **Prompt 2** as a follow-up in the **same conversation**:

   > *"Club REQ-12, REQ-13 and REQ-09 and create a functional specification"*

   J4C surfaces the relationships between all three requirements from the BPD and produces a combined functional specification — without the consultant manually cross-referencing them.

4. Run **Prompt 3** as a follow-up in the **same conversation**:

   > *"List down design decision kept on hold for future phase"*

   J4C scans the BPD and extracts all requirements or design decisions that have been deferred, flagged as out-of-scope, or marked for a future phase — giving the project team a ready-made backlog of deferred items without manually reviewing the full document.

> **💡 Why this matters:** Requirements in a BPD are rarely standalone. REQ-09, REQ-12, and REQ-13 may describe related billing rules that belong in a single development object. Grounding lets J4C surface these relationships and cluster them intelligently — work that would take a consultant hours to do manually across a large BPD. The third prompt adds another layer of value: surfacing hidden scope that is easy to miss but critical for future-phase planning.

---


---

## Summary

> **📍 Raj's Story** | *Wednesday, end of day*
>
> Raj started Tuesday morning with a transcript. By Wednesday evening he had:
> - A structured user story table — ready for the project tracker
> - A sprint backlog with 4 items, story points, sprint assignments, and dependencies
> - A functional specification for BI-04 — 7 sections, ready for Ankit's review
> - A steering committee PowerPoint — 6 slides, speaker notes included
> - A 18J Fit-to-Standard Analyst Expert the whole team can use to evaluate new requirements consistently
> - A JouleTech Procurement Advisor his whole team can use for Realize phase work
> - JouleTech's procurement policies accessible in every J4C answer
>
> That's one workshop. One consultant. Five J4C features. Every deliverable the team needs for the next sprint.

By completing this session, you have walked in Raj's shoes across the full breadth of J4C's latest capabilities:

| Feature | What Raj Did | What You Practised |
|---|---|---|
| **Fit-to-Standard Expert** ⭐ | Created the 18J FTS Analyst Expert from workshop findings; used it in a new conversation to evaluate requirements consistently | Created, scoped, and tested a purpose-built FTS Expert |
| **Custom Knowledge Grounding** | Queried JouleTech's grounded documents (WRICEF template, compliance policies) to retrieve company-specific content | Retrieved answers citing source documents; understood what grounding adds vs. SAP base knowledge |
| **Prompt Library** | Ran all 6 prompts in sequence: user stories → backlog → functional spec → pseudo code → technical spec → unit test script | Used the 6-prompt chain from the JouleTech tab in a single conversation |

| **Expert Workspace** | Shared the FTS Expert with a session partner; received and compared their version | Shared an Expert, opened a received copy, compared instruction variations |


| **File Upload** | Uploaded the 18J workshop transcript and ran the 6-prompt chain in a single conversation | Uploaded a DOCX, ran structured prompts, generated output documents |

---

## The 6-Prompt Chain — Quick Reference

All six prompts run sequentially in the same conversation (transcript loaded in Exercise 3). Access them from the **JouleTech** tab in the Prompt Library:

| Prompt | Action | Output | Used In |
|---|---|---|---|
| 1 | Upload transcript → extract user stories | ~14 user stories, STANDARD/GAP tagged | Exercise 3.1 / 3.2 |
| 2 | GAP stories → sprint backlog | 4 backlog items, sprint IDs, story points | Exercise 3.2 |
| 3 | Backlog item → functional specification | 7-section Word document | Exercise 4.1 |
| 4 | Functional spec → pseudo code | Clean Core annotated ABAP stubs | Exercise 4.3 |
| 5 | Functional spec + pseudo code → technical specification | 9-section technical document | Exercise 4.3 |
| 6 | Functional spec + technical spec → unit test script | Test script covering all user stories, expected vs actual results | Exercise 4.3 |

---

## Coming Soon (Not Yet Committed)

| Feature | Description |
|---|---|
| **Document Library** | A centralised library within J4C where generated documents can be saved, organised, and retrieved across conversations |
| **Process Diagram Generation** | AI-generated process flow diagrams (e.g., BPMN-style) directly within J4C |

---

## Appendix — Key SAP Procurement Transactions (18J Reference)

| Activity | Transaction | Module |
|---|---|---|
| Create Purchase Requisition | ME51N | MM-PUR |
| Change / Display PR | ME52N / ME53N | MM-PUR |
| Assign Source of Supply | ME57 | MM-PUR |
| Create Purchase Order | ME21N | MM-PUR |
| Release (Approve) PR | ME54N / ME55 | MM-PUR |
| Monitor PRs | ME5A | MM-PUR |
| Post Goods Receipt | MIGO | MM-IM |
| Post Supplier Invoice | MIRO | FI-AP |
| BAdI: PR Validation | ME_PROCESS_REQ_CUST | MM-PUR |
| BAdI: PO Validation | ME_PROCESS_PO_CUST | MM-PUR |
| ABAP Test Cockpit | ATC | Basis / ABAP |
| Classification System | CL02 / CT04 | Cross-App |

> **💡 Pro tip:** Include the transaction code in your J4C prompt — responses become significantly more specific and actionable.

---

## Sample Files Reference

| File | Used In | Purpose |
|---|---|---|
| `FTS-18J-Workshop-Transcript.docx` | Exercises 1.1, 2.3, 5.1 | Source transcript — upload once, use throughout |
| `jouletech-material-master.csv` | Exercise 3.3 | Material master data for cross-table analysis |
| `jouletech-open-orders.csv` | Exercise 3.3 | Open orders data for cross-table analysis |
| `jouletech-internal-links.txt` | Exercise 1 (optional) | Procurement URL directory for Expert grounding |
| `MM-18J-Prompt-Library.xlsx` | Admin pre-load | The 6 chained prompts for the JouleTech tab |
| `TechEd2026-Custom-Prompt-Library.xlsx` | Admin pre-load | The 8 general consulting prompts for the JouleTech tab |
| `JouleTech-WRICEF-Enhancement-FS-Template.pdf` | Exercise 4 — grounding | JouleTech's standard Enhancement functional specification template (WRICEF-E) |
| `JouleTech-Procurement-Compliance-Framework.pdf` | Exercise 4 — grounding | Mandatory approval gates and compliance checkpoints for procurement and custom developments |
| `JouleTech-Clean-Core-Exemption-Policy.pdf` | Exercise 4 — grounding | Approval chain and process for clean core exemptions (BAdI, custom ABAP) in Company Code 2330 |
| `JouleTech-S4HANA-Project-Charter.docx` | Exercise 4 — grounding | Project scope, go-live date, sponsor approvals, and scope boundaries |
| `JouleTech-Vendor-Management-Policy.pdf` | Exercise 4 — grounding | Vendor currency and bank account rules, approval thresholds by procurement organisation |
| `JouleTech-Internal-Controls-Audit-Policy.pdf` | Exercise 4 — grounding | Audit log and evidence requirements for custom procurement enhancements going to production |

---

## Resources

| Resource | Link |
|---|---|
| **J4C Gets Personal — Sapphire 2026 Blog** ⭐ | [community.sap.com](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-joule-for-consultants-gets-personal-at-sap-sapphire-2026/ba-p/14404400) |
| SAP Joule for Consultants — SAP Help Portal | [help.sap.com](https://help.sap.com/docs/JOULE/3fdd7b321eb24d1b9d40605dce822e84/8e7ef5b756564888a6f0992003b597a4.html) |
| Expert Workspace Guide | [help.sap.com](https://help.sap.com/docs/joule/serviceguide/sap-joule-for-consultants-expert-workspace) |
| Expert Library & Sharing Blog | [community.sap.com](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-joule-for-consultants-expert-workspace-and-new-enhancements/ba-p/14423927) |
| Custom Knowledge Grounding Blog | [community.sap.com](https://community.sap.com/t5/technology-blog-posts-by-sap/enhance-sap-joule-for-consultants-with-custom-knowledge-grounding/ba-p/14404721) |
| Prompt Library — SAP Community Blog | [community.sap.com](https://community.sap.com/t5/technology-blog-posts-by-sap/introducing-the-sap-activate-prompt-library-curated-ai-prompts-for-your/ba-p/14436408) |

---

## Navigation

| Previous | Next |
|---|---|
| Overview | Wrap-up & Feedback |



## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (20xx-)20xx SAP SE or an SAP affiliate company and <your-project> contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP/<your-project>).
