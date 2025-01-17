---
title: "Data, Privacy, and Security for Microsoft 365 Copilot"
ms.author: danbrown
author: DHB-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: microsoft-365-copilot
ms.localizationpriority: medium
ms.collection: Tier1
description: "Provides information about Microsoft 365 Copilot works, along with information about privacy and security aspects of Copilot."
hideEdit: true
ms.date: 09/11/2023
---

# Data, Privacy, and Security for Microsoft 365 Copilot

> [!IMPORTANT]
> The information in this article only applies to the [Microsoft 365 Copilot Early Access Program](/microsoft-365/admin/copilot/m365-early-access-program), an invite-only paid preview program for commercial customers. Details are subject to change.

[Microsoft 365 Copilot](https://www.microsoft.com/microsoft-365/blog/2023/03/16/introducing-microsoft-365-copilot-a-whole-new-way-to-work/) is a sophisticated processing and orchestration engine that provides AI-powered productivity capabilities by coordinating the following components:

- Large language models (LLMs)
- Content in Microsoft Graph, such as emails, chats, and documents that you have permission to access.
- The Microsoft 365 apps that you use every day, such as Word and PowerPoint.

For an overview of how these three components work together, watch these videos:

- [The Copilot System: Explained by Microsoft](https://www.youtube.com/watch?v=E5g20qmeKpg)
- [How Microsoft 365 Copilot works](https://www.youtube.com/watch?v=B2-8wrF9Okc)


> [!IMPORTANT]
> - Microsoft 365 Copilot is compliant with our existing privacy, security, and compliance commitments to Microsoft 365 commercial customers, including the General Data Protection Regulation (GDPR) and European Union (EU) Data Boundary.
> - Prompts, responses, and data accessed through Microsoft Graph aren't used to train foundation LLMs, including those used by Microsoft 365 Copilot.

The information in this article is intended to help provide answers to the following questions:

- [How does Microsoft 365 Copilot work?](#how-does-microsoft-365-copilot-work)
- [How does Microsoft 365 Copilot use your proprietary organizational data?](#how-does-microsoft-365-copilot-use-your-proprietary-organizational-data)
- [How does Microsoft 365 Copilot protect sensitive organizational information and data?](#how-does-microsoft-365-copilot-protect-sensitive-organizational-data)
- [How does Microsoft 365 Copilot meet regulatory compliance requirements?](#meeting-regulatory-compliance-requirements)
- [How do I prepare my organization for Microsoft 365 Copilot?](#preparing-your-organization-for-microsoft-365-copilot)
- [Can I trust the content that Microsoft 365 Copilot creates? Who owns that content?](#about-the-content-that-microsoft-365-copilot-creates)
- [What are Microsoft's commitments to using AI responsibly?](#committed-to-responsible-ai)

> [!NOTE]
> Microsoft 365 Copilot will continue to evolve over time with new capabilities. To keep up to date on Microsoft 365 Copilot or ask questions, visit the [Microsoft 365 Copilot community](https://techcommunity.microsoft.com/t5/microsoft-365-copilot/ct-p/Microsoft365Copilot) on the Microsoft Tech Community.

## How does Microsoft 365 Copilot work?

Microsoft 365 Copilot capabilities that users see in Microsoft 365 apps and other surfaces appear as intelligent features, functionality, and prompting capability. Our foundation LLMs and proprietary Microsoft technologies work together in an underlying system that helps you securely access, use, and manage your organizational data.

- **Microsoft 365 apps** (such as Word, Excel, PowerPoint, Outlook, Teams, and Loop) operate with Microsoft 365 Copilot to support users in the context of their work. For example, Copilot in Word is designed to assist users specifically in the process of creating, understanding, and editing documents. In a similar way, Copilot in the other apps helps users in the context of their work within those apps.

- **Chat** enables Microsoft 365 Copilot users to make use of cross-app intelligence, which allows users with a simpler way to work with multiple apps. Chat uses the power of the foundation LLMs, a user's organizational data, and a user's apps to generate a response. Chat is available in a range of experiences, including Teams (chat), Bing, Microsoft Edge, and the Microsoft 365 app.

- **Microsoft Graph** has long been fundamental to Microsoft 365. It includes information about the relationships between users, activities, and your organization’s data. The Microsoft Graph API brings more context from customer signals into the prompt, such as information from emails, chats, documents, and meetings. For more information, see [Overview of Microsoft Graph](/graph/overview) and [Major services and features in Microsoft Graph](/graph/overview-major-services).

- **Semantic Index** for Copilot uses multiple LLMs that sit on top of Microsoft Graph to interpret user queries and produce sophisticated, meaningful, and multilingual responses that help you to be more productive. It allows you to search quickly through billions of vectors (mathematical representations of features or attributes) to help connect you with relevant and actionable information in your organization. For more information, [review this video](https://www.youtube.com/watch?v=KtsVRCsdvoU).

The following diagram provides a visual representation of how Microsoft 365 Copilot works.

:::image type="content" source="../images/privacy/how-microsoft-365-copilot-works.png" alt-text="Diagram that shows the relationship among the components of Microsoft 365 Copilot, such as Microsoft Graph and LLM":::

Here's an explanation of how Microsoft 365 Copilot works:

- Copilot receives an input prompt from a user in an app, such as Word or PowerPoint.

- Copilot then pre-processes the input prompt through an approach called grounding, which improves the specificity of the prompt, to help you get answers that are relevant and actionable to your specific task. The prompt can include text from input files or other content discovered by Copilot, and Copilot sends this prompt to the LLM for processing. Copilot only accesses data that an individual user has existing access to, based on, for example, existing Microsoft 365 role-based access controls.

- Copilot takes the response from the LLM and post-processes it. This post-processing includes other grounding calls to Microsoft Graph, responsible AI checks, security, compliance and privacy reviews, and command generation.

- Copilot returns the response to the app, where the user can review and assess the response.

Microsoft 365 Copilot iteratively processes and orchestrates these sophisticated services to help produce results that are relevant to your organization because they're contextually based on your organizational data.

## How does Microsoft 365 Copilot use your proprietary organizational data?

Microsoft 365 Copilot provides value by connecting LLMs to your organizational data. Microsoft 365 Copilot accesses content and context through Microsoft Graph. It can generate responses anchored in your organizational data, such as user documents, emails, calendar, chats, meetings, and contacts. Microsoft 365 Copilot combines this content with the user’s working context, such as the meeting a user is in now, the email exchanges the user has had on a topic, or the chat conversations the user had last week. Microsoft 365 Copilot uses this combination of content and context to help provide accurate, relevant, and contextual responses.

> [!IMPORTANT]
> Prompts, responses, and data accessed through Microsoft Graph aren't used to train foundation LLMs, including those used by Microsoft 365 Copilot.

Microsoft 365 Copilot only surfaces organizational data to which individual users have at least view permissions. It's important that you're using the permission models available in Microsoft 365 services, such as SharePoint, to help ensure the right users or groups have the right access to the right content within your organization.  

Microsoft 365 Copilot only searches for information from the user’s tenant. It doesn't search other tenants that the user might have access to, such as a tenant where the user is a Microsoft Entra B2B guest.

When you input prompts using Microsoft 365 Copilot, the information contained within your prompts, the data they retrieve, and the generated responses remain within the Microsoft 365 service boundary, in keeping with our current privacy, security, and compliance commitments.

> [!NOTE]
> We may use customer feedback, which is optional, to improve Microsoft 365 Copilot, just like we use customer feedback to improve other Microsoft 365 services and Microsoft 365 apps. We don't use this feedback to train the foundation LLMs used by Microsoft 365 Copilot. Customers can manage feedback through admin controls. For more information, see [Manage Microsoft feedback for your organization](/microsoft-365/admin/manage/manage-feedback-ms-org).

### Extensibility of Microsoft 365 Copilot

While Microsoft 365 Copilot is already able to use the apps and data within the Microsoft 365 ecosystem, many users still depend on various external tools and services for work management and collaboration. Customers can address this gap by extending Microsoft 365 Copilot to enable users to work with their third-party tools and services. This can be done through extending Microsoft 365 Copilot by building a plug-in or by connecting to an external data source. For more information, see [Extend Microsoft 365 Copilot](/microsoftteams/platform/copilot/how-to-extend-copilot).

### About the content that Microsoft 365 Copilot creates

The responses that generative AI produces aren't guaranteed to be 100% factual. While we continue to improve responses, users should still use their judgment when reviewing the output before sending them to others. Our Microsoft 365 Copilot capabilities provide useful drafts and summaries to help you achieve more while giving you a chance to review the generated AI rather than fully automating these tasks.

We continue to improve algorithms to proactively address issues, such as misinformation and disinformation, content blocking, data safety, and preventing the promotion of harmful or discriminatory content in line with our [responsible AI principles](https://www.microsoft.com/ai/our-approach).

Microsoft doesn't claim ownership of the output of the service. That said, we don't make a determination on whether a customer’s output is copyright protected or enforceable against other users. This is because generative AI systems may produce similar responses to similar prompts or queries from multiple customers. Consequently, multiple customers may have or claim rights in content that is the same or substantially similar.

If a third party sues a commercial customer for copyright infringement for using Microsoft’s Copilots or the output they generate, we'll defend the customer and pay the amount of any adverse judgments or settlements that result from the lawsuit, as long as the customer used the guardrails and content filters we have built into our products. For more information, see [Microsoft announces new Copilot Copyright Commitment for customers](https://blogs.microsoft.com/on-the-issues/2023/09/07/copilot-copyright-commitment-ai-legal-concerns/).

## How does Microsoft 365 Copilot protect sensitive organizational data?

The permissions model within your Microsoft 365 tenant can help ensure that data won't unintentionally leak between users, groups, and tenants. Microsoft 365 Copilot presents only data that each individual can access using the same underlying controls for data access used in other Microsoft 365 services. Semantic Index honors the user identity-based access boundary so that the grounding process only accesses content that the current user is authorized to access. For more information, see Microsoft’s [privacy policy and service documentation](https://privacy.microsoft.com/).  

When you have data that's encrypted by Microsoft Purview Information Protection, it won't be returned by Microsoft 365 Copilot unless the user is granted at least the [View usage right](/azure/information-protection/configure-usage-rights#usage-rights-and-descriptions). This encryption can be applied by [sensitivity labels](/purview/sensitivity-labels) or by restricted permissions in Microsoft 365 apps by using Information Rights Management (IRM). While Microsoft 365 Copilot generated content currently doesn't inherit the most restrictive permissions or label from the source, Microsoft 365 Copilot cites the original source, which will retain the protection.

We already implement multiple forms of protection to help prevent customers from compromising Microsoft 365 services and applications or gaining unauthorized access to other tenants or the Microsoft 365 system itself. Here are some examples of those forms of protection:

- Logical isolation of customer content within each tenant for Microsoft 365 services is achieved through Microsoft Entra ID authorization and role-based access control. For more information, see [Microsoft 365 isolation controls](/compliance/assurance/assurance-microsoft-365-isolation-controls).

- Microsoft uses rigorous physical security, background screening, and a multi-layered encryption strategy to protect the confidentiality and integrity of customer content.

- Microsoft 365 uses service-side technologies that encrypt customer content at rest and in transit, including BitLocker, per-file encryption, Transport Layer Security (TLS) and Internet Protocol Security (IPsec). For specific details about encryption in Microsoft 365, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).

- Your control over your data is reinforced by Microsoft's commitment to comply with broadly applicable privacy laws, such as the GDPR, and privacy standards, such as ISO/IEC 27018, the world’s first international code of practice for cloud privacy.

- For content accessed through Microsoft 365 Copilot plug-ins, encryption can exclude programmatic access, thus limiting the plug-in from accessing the content. For more information, see [Configure usage rights for Azure Information Protection](/azure/information-protection/configure-usage-rights).

## Microsoft 365 Copilot and the EU Data Boundary

Microsoft 365 Copilot doesn't change existing data processing and residency commitments that are applicable to Microsoft 365 tenants. Microsoft 365 Copilot calls to the LLM are routed to the closest data centers in the region, but also can call into other regions where capacity is available during high utilization periods.

For European Union (EU) users, we have additional safeguards to comply with the [EU Data Boundary](/privacy/eudb/eu-data-boundary-learn). EU traffic stays within the EU Data Boundary while worldwide traffic can be sent to the EU and other countries or regions for LLM processing.

## Meeting regulatory compliance requirements

As regulation in the AI space evolves, Microsoft will continue to adapt and respond to fulfill future regulatory requirements.

Microsoft 365 Copilot is built on top of Microsoft’s current commitments to data security and privacy in the enterprise. There's no change to these commitments. Microsoft 365 Copilot is integrated into Microsoft 365 and adheres to all existing privacy, security, and compliance commitments to Microsoft 365 commercial customers. For more information, see [Microsoft Compliance](/compliance).

> [!NOTE]
> Currently, Microsoft 365 Copilot operates under the terms of the Early Access Program. When Microsoft 365 Copilot becomes generally available, it will operate under the [Microsoft 365 Product Terms](https://www.microsoft.com/licensing/terms/productoffering/Microsoft365/).

Beyond adhering to regulations, we prioritize an open dialogue with our customers, partners, and regulatory authorities to better understand and address concerns, thereby fostering an environment of trust and cooperation. We acknowledge that privacy, security, and transparency aren't just features, but prerequisites in the AI-driven landscape at Microsoft.

## Additional information

### Other details about Microsoft 365 Copilot

- Microsoft 365 Copilot use Azure OpenAI services for processing, not OpenAI’s publicly available services.
- Microsoft 365 Copilot uses a combination of Generative Pre-Trained Transformers (GPT) models, including GPT 4. GPT is an example of a large language model (LLM).
- For information about the difference between Microsoft 365 Copilot and ChatGPT, see [ChatGPT vs. Microsoft 365 Copilot: What's the difference?](https://support.microsoft.com/topic/8fdec864-72b1-46e1-afcb-8c12280d712f).

### Committed to responsible AI

As AI is poised to transform our lives, we must collectively define new rules, norms, and practices for the use and impact of this technology. Microsoft has been on a Responsible AI journey since 2017, when we defined our principles and approach to ensuring this technology is used in a way that is driven by ethical principles that put people first.

At Microsoft, we're guided by our [AI principles](https://www.microsoft.com/ai/our-approach), our [Responsible AI Standard](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE5cmFl), and decades of research on AI, grounding, and privacy-preserving machine learning. A multidisciplinary team of researchers, engineers and policy experts reviews our AI systems for potential harms and mitigations — refining training data, filtering to limit harmful content, query- and result-blocking sensitive topics, and applying Microsoft technologies like [InterpretML](https://www.microsoft.com/research/uploads/prod/2020/05/InterpretML-Whitepaper.pdf) and [Fairlearn](https://fairlearn.org/) to help detect and correct data bias. We make it clear how the system makes decisions by noting limitations, linking to sources, and prompting users to review, fact-check, and adjust content based on subject-matter expertise. For more information, see [Governing AI: A Blueprint for the Future](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RW14Gtw).

We aim to help our customers use our AI products responsibly, sharing our learnings, and building trust-based partnerships. For these new services, we want to provide our customers with information about the intended uses, capabilities, and limitations of our AI platform service, so they have the knowledge necessary to make responsible deployment choices. We also share resources and templates with developers inside organizations and with independent software vendors (ISVs), to help them build effective, safe, and transparent AI solutions.

### Preparing your organization for Microsoft 365 Copilot

To access and use Microsoft 365 Copilot, there are certain prerequisites you need to meet. For example, you must have a Microsoft E3 or Microsoft E5 subscription plan and be using Microsoft Entra accounts. There are also requirements for using Microsoft 365 Copilot in specific apps, such as having the new Outlook for Windows. For more information, see the following resources:

- [How to prepare for Microsoft 365 Copilot](https://techcommunity.microsoft.com/t5/microsoft-365-copilot/how-to-prepare-for-microsoft-365-copilot/ba-p/3851566)
- [Get started with Copilot in Microsoft 365](/microsoft-365/admin/copilot/m365-copilot-setup)
- [Microsoft 365 Copilot adoption site](https://adoption.microsoft.com/copilot/)

Beyond the basic prerequisites and product-specific requirements, there are some ways that you can prepare your organization now so that when you’re ready to deploy Microsoft 365 Copilot, you get the most benefit of its capabilities. For example, make sure your organization has the right information access controls and policies in place. Remember, Microsoft 365 Copilot only retrieves information the user explicitly has access to, such as files stored in SharePoint. For more information, [watch this video](https://youtu.be/oeX0lsMA69U).

### Other Microsoft products that make use of AI

The following links provide information about some other Microsoft products that make use of AI.

- [Bing](https://blogs.microsoft.com/blog/2023/02/07/reinventing-search-with-a-new-ai-powered-microsoft-bing-and-edge-your-copilot-for-the-web/)
- [Microsoft Designer](https://create.microsoft.com/learn/articles/how-to-image-prompts-dall-e-ai)
- [Azure AI](https://azure.microsoft.com/solutions/ai/#overview)
- [Microsoft Dynamics 365 Copilot](https://blogs.microsoft.com/blog/2023/03/06/introducing-microsoft-dynamics-365-copilot/)
- [Microsoft Security Copilot](https://www.microsoft.com/security/business/ai-machine-learning/microsoft-security-copilot?rtc=1)
- [GitHub Copilot](https://github.blog/2023-03-22-github-copilot-x-the-ai-powered-developer-experience/)
- [Copilot in Power Platform](https://cloudblogs.microsoft.com/powerplatform/2023/03/16/power-platform-is-leading-a-new-era-of-ai-generated-low-code-app-development/)