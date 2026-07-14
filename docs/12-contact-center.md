# Dynamics 365 Contact Center Licensing

> **Sources:** Dynamics 365 Licensing Guide (July 2026) + Microsoft Learn. Last updated 2026-07-14.

Dynamics 365 Contact Center is a **Copilot-first** contact center solution that brings intelligence, automation, and efficiency to every customer engagement channel.[LG p.17] It is a cloud-based product that works with the CRM solution of your choice, or with Dynamics 365 Customer Service Enterprise (as an add-on) or as part of Dynamics 365 Customer Service Premium.[LG p.17][Learn: Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)

## The three Contact Center offers

Contact Center is sold as three per-user offers:[LG p.17-19][LG p.20]

| Offer | Channels | What it includes |
|---|---|---|
| **Contact Center Digital** | Digital messaging + chat | Unified routing (50 record routes/user/month, excluding chats/calls/texts).[LG p.17] |
| **Contact Center Voice** | Native voice | 2,000 Intelligent Voicebot (IVR) min/user/month, 6,000 Call Intelligence min/user/month, 35 GB Dataverse file storage for call recording.[LG p.18] |
| **Contact Center (Digital + Voice)** | Digital + voice | A bundle of both, including all capacity entitlements of each.[LG p.19] |

All three are licensed **per user**.[LG p.17-19]

## Standalone vs. add-on to Customer Service

Contact Center can be consumed in three ways:

1. **Standalone with your own CRM** — Contact Center is built to work with your existing CRM solution.[LG p.17][Learn: Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)
2. **As an add-on to Customer Service Enterprise** — Customer Service Enterprise licensed users are eligible to purchase Contact Center add-ons for Digital, Voice, or both.[LG p.27]
3. **Bundled inside Customer Service Premium** — Customer Service Premium includes Customer Service Enterprise **and** Contact Center (Digital + Voice).[LG p.25][LG p.27]

For the Customer Service side of these combinations, see [Dynamics 365 Customer Service Licensing](./11-customer-service.md).

## Contact Center Digital

Contact Center Digital is licensed per user and provides customer engagement across **digital messaging and chat channels**.[LG p.17] Capacity entitlements include **Unified Routing with 50 record routes/user/month** (excluding chats, calls, and text messages). Copilot credits are purchased separately.[LG p.17]

### Contact Center Digital capacity

| Capability | Included capacity | Add-ons |
|---|---|---|
| Record routing (excluding chats, calls, text messages) | 50 record routes/user/month | Unified Routing add-on: 10K record routes/tenant/month; Copilot Studio: Copilot Credits |

Source: [LG p.17]. Capacity is pooled at the tenant level.[LG p.17]

## Contact Center Voice

Contact Center Voice is licensed per user and provides **native voice capabilities**.[LG p.18] Capacity entitlements include:[LG p.18]

- **2,000 Intelligent Voicebot (IVR) minutes/user/month** — usable as a conversational IVR bot authored in Microsoft Copilot Studio. Any generative AI capabilities require Copilot Credits, purchased separately.[LG p.18]
- **6,000 Call Intelligence (transcription) minutes/user/month** — covers call transcription, sentiment analysis, AI suggestions, call insights, and topic clustering.[LG p.18]
- **35 GB of Dataverse file storage** for call recording (accrued per USL, pooled at tenant level).[LG p.18]

### Contact Center Voice capacity

| Capability | Included capacity | Add-on capacity |
|---|---|---|
| Intelligent Voicebot minutes | 2,000 minutes/user/month | 500 minutes/tenant/month |
| Call Intelligence minutes | 6,000 minutes/user/month | 500 minutes/tenant/month |
| Dataverse File storage (call recording) | 35 GB | — |

Source: [LG p.19]. Capacity is pooled at the tenant level.[LG p.19]

### Microsoft Teams Phone extensibility (Voice)

Teams Phone extensibility lets you configure Teams Phone — with the Teams pay-as-you-go Calling Plan, Operator Connect, or Direct Routing — as a single integrated telephony solution with Contact Center.[LG p.18] Two sets of licenses are required: a **Contact Center service line** (a no-cost Teams Phone Resource Account license plus a PSTN connectivity option) and **Contact Center service reps** (each rep needs a Dynamics 365 Contact Center USL, a Microsoft Teams license, and a Microsoft Teams Phone license).[LG p.18] Teams Phone extensibility pricing is separate and not included in the Contact Center license.[LG p.20] Install/config prerequisites for the voice channel are described on Microsoft Learn.[Learn: Install the voice channel](https://learn.microsoft.com/dynamics365/customer-service/administer/voice-channel-install)

## Contact Center (Digital + Voice)

Contact Center is licensed per user and provides customer engagement across **digital and voice channels** for an all-in-one solution. It is a **bundle** that includes both Contact Center Digital and Contact Center Voice, with all their capacity entitlements.[LG p.19]

## Copilot capabilities

Contact Center is a **Copilot-first** product. Its key capabilities include AI-driven self-service and autonomous agents, AI-led proactive engagement, conversation summaries, IVR and AI agents, sentiment analysis, live transcription and translation, unified routing across voice and digital channels, and Copilot that summarizes conversations, drafts responses/emails, and surfaces knowledge.[Learn: Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)

### Dynamics 365 Contact Center Agents

To use the prebuilt Dynamics 365 Contact Center Agents, a user must be licensed with Dynamics 365 Contact Center.[LG p.17] The agents are the **Knowledge Management Agent**, **Quality Assurance Agent**, **Customer Assist Agent**, and **Customer Intent Agent**.[LG p.17][LG p.20] Across all three offers, the Contact Center Agents **require Copilot Credits, purchased separately**.[LG p.20] Generative AI features of the Intelligent Voicebot (IVR) also require Copilot Credits.[LG p.18]

## Included Dataverse capacity (default, per subscription)

| Capacity | Contact Center Digital | Contact Center Voice | Contact Center (Digital + Voice) |
|---|---|---|---|
| Unified Routing | 50 record routes/user/month | 50 record routes/user/month | 50 record routes/user/month |
| Intelligent Voicebot minutes | — | 2K/user/month | 2K/user/month |
| Call Intelligence minutes | — | 6K/user/month | 6K/user/month |
| **Dataverse Database** | 30 GB | 30 GB | 30 GB |
| Accrued per USL | 250 MB | 250 MB | 250 MB |
| **Dataverse File** | 40 GB | 40 GB | 40 GB |
| Accrued per USL | 2 GB | 35 GB | 35 GB |
| **Dataverse Log** | 2 GB | 2 GB | 2 GB |

Source: [LG p.20]. Unified Routing counts exclude chats, calls, and text messages, and additional capacity is available for purchase.[LG p.20]

## Pricing

This knowledge base does not quote dollar figures because prices change. For current per-user pricing of each Contact Center offer, see the official **[Dynamics 365 Contact Center pricing page](https://www.microsoft.com/dynamics-365/products/contact-center/pricing)**.[Learn: Provision channels in Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/provision-channels) Add-ins can also be purchased through the Microsoft 365 admin center.[Learn: System requirements for Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/system-requirements-contact-center)

## Sources

- Dynamics 365 Licensing Guide (July 2026), p.17
- Dynamics 365 Licensing Guide (July 2026), p.18
- Dynamics 365 Licensing Guide (July 2026), p.19
- Dynamics 365 Licensing Guide (July 2026), p.20
- Dynamics 365 Licensing Guide (July 2026), p.25
- Dynamics 365 Licensing Guide (July 2026), p.27
- [Microsoft Learn — Dynamics 365 Contact Center overview](https://learn.microsoft.com/dynamics365/contact-center/implement/overview-contact-center)
- [Microsoft Learn — System requirements for Dynamics 365 Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/system-requirements-contact-center)
- [Microsoft Learn — Provision channels in Dynamics 365 Contact Center](https://learn.microsoft.com/dynamics365/contact-center/implement/provision-channels)
- [Microsoft Learn — Install the voice channel](https://learn.microsoft.com/dynamics365/customer-service/administer/voice-channel-install)
- [Dynamics 365 Contact Center pricing page](https://www.microsoft.com/dynamics-365/products/contact-center/pricing)

---
[⬅ Back to Index](./Index.md)
