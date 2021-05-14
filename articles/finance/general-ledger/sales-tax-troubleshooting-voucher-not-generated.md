---
title: لم يتم إنشاء الإيصال
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد عندما يجب إنشاء قسيمة ولكن لا.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947592"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="5a12f-103">لم يتم إنشاء الإيصال</span><span class="sxs-lookup"><span data-stu-id="5a12f-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a12f-104">إذا كان يجب إنشاء إيصال، لا تعرض صفحة **حركات الإيصالات** أي إيصالات، اتبع الخطوات الواردة في الأقسام التالية كما هو مطلوب لاستكشاف هذه المشكلة وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="5a12f-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="5a12f-105">[![صفحة حركات الإيصال التي لا تحتوي على قسائم](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="5a12f-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="5a12f-106">فحص إمكانية تطبيق الضرائب</span><span class="sxs-lookup"><span data-stu-id="5a12f-106">Check the tax applicability</span></span>

1. <span data-ttu-id="5a12f-107">انتقل إلى **الضريبة** \> **المهام الدورية** \> **لم يتم نقل إدخالات دفتر يومية الأستاذ الفرعي**.</span><span class="sxs-lookup"><span data-stu-id="5a12f-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="5a12f-108">إذا كان هناك سجل دفتر يومية، فحدده، ثم حدد **نقل الآن**.</span><span class="sxs-lookup"><span data-stu-id="5a12f-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="5a12f-109">[![زر التحويل الآن في صفحة إدخالات دفتر يومية الأستاذ الفرعي التي لم يتم نقلها بعد](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="5a12f-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="5a12f-110">افتح صفحة **حركات الإيصالات** مرة أخرى لمعرفة ما إذا كان قد تم إنشاء الإيصال أو لا.</span><span class="sxs-lookup"><span data-stu-id="5a12f-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="5a12f-111">حدد ما إذا كان التخصيص موجودًا</span><span class="sxs-lookup"><span data-stu-id="5a12f-111">Determine whether customization exists</span></span>

<span data-ttu-id="5a12f-112">إذا كنت قد أكملت الخطوات الواردة في القسم السابق ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="5a12f-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="5a12f-113">في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.</span><span class="sxs-lookup"><span data-stu-id="5a12f-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
