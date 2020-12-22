---
title: إعداد سيناريوهات دفع الفواتير
description: يصف هذا الموضوع كيفية تكوين Dynamics 365 Commerce لدعم مختلف السيناريوهات ذات الصلة بدفع الفواتير.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9fe8fde32549568812a724311781d3515ef7036c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458394"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="ed515-103">إعداد سيناريوهات دفع الفواتير</span><span class="sxs-lookup"><span data-stu-id="ed515-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed515-104">تم توسيع نطاق وظيفة دفع الفواتير في Dynamics 365 Commerce لكي تدعم:</span><span class="sxs-lookup"><span data-stu-id="ed515-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="ed515-105">دفع فواتير أوامر مبيعات متعددة في حركة نقطة بيع واحدة.</span><span class="sxs-lookup"><span data-stu-id="ed515-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="ed515-106">دفع مختلف أنواع فواتير العملاء بما في ذلك فواتير النص الحر والفواتير القائمة على المشاريع والإشعارات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="ed515-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="ed515-107">لتمكين هذه السيناريوهات، يجب تكوين ملف تعريف الوظائف للمتاجر كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="ed515-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="ed515-108">انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> ملفات تعريف نقطة البيع \> ملفات تعريف الوظائف** وحدد ملف تعريف يرتبط بالمتاجر التي تريد إدخال تغييرات عليها.</span><span class="sxs-lookup"><span data-stu-id="ed515-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="ed515-109">على علامة تبويب **الوظائف**، قم بتكوين المعلمات التالية كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="ed515-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="ed515-110">**فاتورة أمر المبيعات** – حدد **نعم** للسماح للمستخدمين بدفع فاتورة أو أكثر تستند إلى أمر مبيعات في حركة نقطة بيع واحدة.</span><span class="sxs-lookup"><span data-stu-id="ed515-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="ed515-111">**فاتورة النص الحر** – حدد **نعم‏‎** للسماح للمستخدمين بدفع فاتورة واحدة أو أكثر تستند إلى نص حر في حركة نقطة بيع واحدة.</span><span class="sxs-lookup"><span data-stu-id="ed515-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="ed515-112">**فاتورة المشروع** – حدد **نعم** للسماح للمستخدمين بدفع فاتورة واحدة أو أكثر تستند إلى مشروع في حركة نقطة بيع واحدة.</span><span class="sxs-lookup"><span data-stu-id="ed515-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="ed515-113">**إشعار دائن لأمر المبيعات** – حدد **نعم** للسماح للمستخدمين بتسوية إشعارات دائنة متعددة تستند إلى أمر مبيعات في مقابل فواتير مفتوحة، أو بمعالجة مبلغ مسترد للعميل لإشعار دائن مفتوح.</span><span class="sxs-lookup"><span data-stu-id="ed515-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="ed515-114">دفع المبالغ الجزئية أو تسويتها غير مدعوم بعد.</span><span class="sxs-lookup"><span data-stu-id="ed515-114">Payment or settlement of partial amounts is not yet supported.</span></span>
