---
title: أخذ عينات من صنف أداره الجودة
description: يصف هذا الموضوع كيفية إعداد عينات العنصر.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956527"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="1e4d7-103">أخذ عينات من صنف أداره الجودة</span><span class="sxs-lookup"><span data-stu-id="1e4d7-103">Quality management item sampling</span></span>

<span data-ttu-id="1e4d7-104">يتم استخدام نماذج الأصناف كجزء من عمليه اقتران الجودة.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="1e4d7-105">وهو يحدد مقدار المخزون الفعلي الحالي الذي يجب فحصه.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="1e4d7-106">يمكن أن يستند أخذ العينات إلى كميات ثابتة أو نسبة مئوية أو لوحة الترخيص الكاملة.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="1e4d7-107">إعداد أخذ عينات الصنف‬</span><span class="sxs-lookup"><span data-stu-id="1e4d7-107">Set up item sampling</span></span>

<span data-ttu-id="1e4d7-108">اتبع هذه الخطوات لإعداد عينات العنصر.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="1e4d7-109">انتقل إلى **إدارة المخزون \> إعداد \> مراقبة الجودة‬ \> أخذ عينات للصنف‬**.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="1e4d7-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-110">Select **New**.</span></span>
1. <span data-ttu-id="1e4d7-111">في الحقل **أخذ عينات للصنف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="1e4d7-112">في حقل **الوصف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="1e4d7-113">في الحقل **القيمة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="1e4d7-114">ترتبط هذه القيمة بقيمة مواصفات الكمية المحددة في الحقل المجاور.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="1e4d7-115">في قسم **العملية**، حدد خانة الاختيار **الحظر الكامل** إذا كان يجب حظر الكمية الكاملة أو كمية بند الأمر في حالة فشل الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="1e4d7-116">في حاله إلغاء تحديد خانه الاختيار هذه، سيتم حظر الأصناف الموجودة في أمر الجودة فقط في حاله فشل الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="1e4d7-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-117">Select **Save**.</span></span>
1. <span data-ttu-id="1e4d7-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="1e4d7-119">توفر ميزة *‏‫إدارة الجودة لعمليات المستودعات‬* إمكانات أخذ عينات إضافية للأصناف.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="1e4d7-120">ويقوم بإضافة لـ *نطاق أخذ العينات للصنف* ويتيح لك تحديد لوحة ترخيص كاملة كمواصفة للكمية.</span><span class="sxs-lookup"><span data-stu-id="1e4d7-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="1e4d7-121">إذا قمت بتشغيل هذه الميزة، فراجع [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="1e4d7-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
