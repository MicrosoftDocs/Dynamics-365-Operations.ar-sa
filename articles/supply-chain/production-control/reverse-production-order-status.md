---
title: "عكس حالة أمر المنتج"
description: "يصف هذا الموضوع كيفية عكس حالة أمر الإنتاج."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d39dfc065a01e4cac6442de44ccc556444e131ce
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="reverse-the-production-order-status"></a><span data-ttu-id="e1474-103">عكس حالة أمر المنتج</span><span class="sxs-lookup"><span data-stu-id="e1474-103">Reverse the production order status</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e1474-104">يصف هذا الموضوع كيفية عكس حالة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e1474-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="e1474-105">إذا قمت بعكس حالة أمر الإنتاج، يتم إرجاع الأمر وكافة العمليات المرتبطة بالمسارات إلى خطوة سابقة في دورة حياة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e1474-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="e1474-106">على سبيل المثال، أمر إنتاج بحالة **مجدول**، وتقوم بتغيير الحالة إلى **تم الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="e1474-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="e1474-107">وفي هذه الحالة، يجب على النظام أولاً تغيير الحالة إلى **مقدر**، وهي الحالة التي تسبق **مجدول** مباشرةً.</span><span class="sxs-lookup"><span data-stu-id="e1474-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="e1474-108">ويمكن بعد ذلك تغيير الحالة إلى الحالة التي تريدها، وهي **تم الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="e1474-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="e1474-109">**ملاحظة:** إذا وصلت حالة الأمر إلى حالة **الإبلاغ عنه كمنتهٍ**، فإنه لا يزال بإمكانك إرجاعها إلى حالة سابقة.</span><span class="sxs-lookup"><span data-stu-id="e1474-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="e1474-110">ومع ذلك، يجب إعادة تشغيل التقدير وجدولة العمليات أو جدولة المهام أو كلٍّ من نوعي الجدولة لتحديث المعلومات الموجودة في الأمر.</span><span class="sxs-lookup"><span data-stu-id="e1474-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="e1474-111">وهذه الخطوة مطلوبة، لأنه يجب إعادة تعيين أية حجوزات لاستهلاك الصنف المتبقي واستهلاك موارد العمليات أيضًا.</span><span class="sxs-lookup"><span data-stu-id="e1474-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="e1474-112">وتشرح بقية هذه المقالة ما يحدث عند عكس حالة أمر الإنتاج بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="e1474-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="e1474-113">من **مقدر** إلى **تم الإنشاء**</span><span class="sxs-lookup"><span data-stu-id="e1474-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="e1474-114">من **مجدول** إلى **مقدر**</span><span class="sxs-lookup"><span data-stu-id="e1474-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="e1474-115">من **تم الإصدار** إلى **مجدول**</span><span class="sxs-lookup"><span data-stu-id="e1474-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="e1474-116">من **مبدوء** إلى **تم الإصدار**</span><span class="sxs-lookup"><span data-stu-id="e1474-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="e1474-117">من مقدر إلى تم الإنشاء</span><span class="sxs-lookup"><span data-stu-id="e1474-117">From Estimated to Created</span></span>
<span data-ttu-id="e1474-118">عند عكس حالة أمر الإنتاج من **مقدر** إلى **تم الإنشاء**، تتم إزالة استهلاك الأصناف التي تم حسابها للأصناف الموجودة في قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="e1474-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="e1474-119">ويتم حذف حركات المخزون في بند الإنتاج، وتتم إعادة تعيين حقل **الحالة الباقية** تتم في بنود قائمة مكونات الصنف لأمر الإنتاج إلى **منتهية**.</span><span class="sxs-lookup"><span data-stu-id="e1474-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="e1474-120">وعند تحديد خياري **المشتريات المشتقة** و**الإنتاج المشتق**، يتم حذف أي أي أوامر شراء أو أوامر إنتاج أساسية.</span><span class="sxs-lookup"><span data-stu-id="e1474-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="e1474-121">إذا قدرت التكاليف لأمر الإنتاج، أو إذا قمت بحجز الأصناف يدوياً بحيث يمكن استخدامها في الإنتاج، فإنه تتم إزالة تلك الحركات.</span><span class="sxs-lookup"><span data-stu-id="e1474-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="e1474-122">من مجدول إلى مقدر</span><span class="sxs-lookup"><span data-stu-id="e1474-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="e1474-123">عندما عكس حالة أمر إنتاج من **مجدول** إلى **مقدر**، تتم إزالة أوقات وتواريخ البداية والنهاية المجدولة.</span><span class="sxs-lookup"><span data-stu-id="e1474-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="e1474-124">وتتم إزالة حجوزات القدرة التي تم إنشاؤها خلال الجدولة، ويتم حذف الوظائف التي تم إنشاؤها خلال جدولة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="e1474-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="e1474-125">وتتم إعادة تعيين كافة المعلومات التي يتم تسجيلها حول جدولة العمليات وجدولة الوظائف في صفحة **تفاصيل أمر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="e1474-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="e1474-126">من تم الإصدار إلى مجدول</span><span class="sxs-lookup"><span data-stu-id="e1474-126">From Released to Scheduled</span></span>
<span data-ttu-id="e1474-127">عندما عكس حالة أمر الإنتاج من **تم الإصدار** إلى **مجدول**، تكون النتيجة الوحيدة التي تحدث هي تغيير في القيمة الموجودة في حقل الحالة.</span><span class="sxs-lookup"><span data-stu-id="e1474-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="e1474-128">من مبدوء إلى تم الإصدار</span><span class="sxs-lookup"><span data-stu-id="e1474-128">From Started to Released</span></span>
<span data-ttu-id="e1474-129">عند عكس حالة أمر الإنتاج من **مبدوء** إلى **تم الإصدار**، يتم إرجاع جميع الأصناف التي تم الإبلاغ عنها كمنتهية إلى حالتها القديمة.</span><span class="sxs-lookup"><span data-stu-id="e1474-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="e1474-130">وإذا تم انتقاء المادة أو كانت عمليات التسليم الداخلية والخارجية موجهة للإنتاج، فإنه يتم عكس هذه الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="e1474-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="e1474-131">ويتم تغيير حقل **الحالة الباقية** في بنود قائمة مكونات الصنف لأمر الإنتاج من **منتهية** إلى **استهلاك المواد**.</span><span class="sxs-lookup"><span data-stu-id="e1474-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="e1474-132">إذا تم تسجيل الوقت أو تم الإبلاغ عن الكميات كمنتهية للعمليات في مسار الإنتاج، فإنه يتم عكس هذه الإعدادات.</span><span class="sxs-lookup"><span data-stu-id="e1474-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="e1474-133">ويتم تغيير حقل **الحالة الباقية** من **منتهية** إلى **استهلاك المسار** في مسار الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="e1474-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="e1474-134">ويتم عكس الإعدادات لكافة الأصناف التي تم ترحيلها إلى أعمال قيد المعالجة أو أعمال تحت التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="e1474-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="e1474-135">وفي صفحة **تفاصيل أمر الإنتاج**، تتم إعادة تعيين الحقول التي تُظهر كمية تم بدء تشغيلها أو الإبلاغ عنها كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="e1474-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="e1474-136">كما تتم إعادة تعيين التواريخ لهذه الحركات.</span><span class="sxs-lookup"><span data-stu-id="e1474-136">The dates for those transactions are also reset.</span></span>




