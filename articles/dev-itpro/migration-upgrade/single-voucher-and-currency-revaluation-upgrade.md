---
title: "ترقية إعادة تقييم العملة والإيصال الواحد"
description: "تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يوضح هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="06bb6-104">ترقية إعادة تقييم العملة والإيصال الواحد</span><span class="sxs-lookup"><span data-stu-id="06bb6-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="06bb6-105">تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="06bb6-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="06bb6-106">يوضح هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="06bb6-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="06bb6-107">اتبع هذه الخطوات عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="06bb6-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="06bb6-108">قبل الترقية إلى Dynamics 365 for Operations، أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="06bb6-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="06bb6-109">عيّن الحقل **الطريقة** إلى **تاريخ الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="06bb6-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="06bb6-110">يتم إنشاء حركة إعادة تقييم تعكس عملية إعادة تقييم العملة الأجنبية الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="06bb6-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="06bb6-111">لذلك، يتم تقييم الحركات المفتوحة بعملة المحاسبة الأصلية الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="06bb6-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="06bb6-112">أجرِ الترقية إلى Dynamics 365 for Operations الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="06bb6-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="06bb6-113">أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة مرة ثانية.</span><span class="sxs-lookup"><span data-stu-id="06bb6-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="06bb6-114">في هذه المرة، عيّن **الطريقة** إلى **القياسية**.</span><span class="sxs-lookup"><span data-stu-id="06bb6-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="06bb6-115">يتم إنشاء حركة إعادة تقييم جديدة استناداً إلى أسعار الصرف الحالية.</span><span class="sxs-lookup"><span data-stu-id="06bb6-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="06bb6-116">تسجل هذه الحركة الأرباح/الخسائر غير المحققة وحساب دفتر الأستاذ للملخص الصحيح.</span><span class="sxs-lookup"><span data-stu-id="06bb6-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





