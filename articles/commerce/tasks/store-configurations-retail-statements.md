---
title: " تكوينات المتجر لحساب بيانات Retail"
description: يتناول هذا الإجراء تكوينات المتجر التي تؤثر على كيفية إنشاء كشوفات حساب Commerce وترحيلها.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b73282abd2df92b3f466f7c1c6c210173001fd7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021457"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="77508-103"> تكوينات المتجر لحساب بيانات Retail</span><span class="sxs-lookup"><span data-stu-id="77508-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="77508-104">يتناول هذا الإجراء تكوينات المتجر التي تؤثر على كيفية إنشاء كشوفات حساب Commerce وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="77508-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="77508-105">ويتم تناول الأبعاد المالية في المتاجر في إجراء آخر.</span><span class="sxs-lookup"><span data-stu-id="77508-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="77508-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="77508-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="77508-107">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > البيع بالتجزئة والتجارة > القنوات > المتاجر > جميع المتاجر**.</span><span class="sxs-lookup"><span data-stu-id="77508-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="77508-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="77508-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="77508-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="77508-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="77508-110">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="77508-110">Click **Edit**.</span></span>
5. <span data-ttu-id="77508-111">تؤثر الإعدادات الموجودة على علامة التبويب السريعة **كشف الحساب/الإقفال** على إنشاء كشف الحساب والتحقق من الصحة والترحيل للمتجر.</span><span class="sxs-lookup"><span data-stu-id="77508-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="77508-112">قم بتوسيع علامة التبويب السريعة **كشف الحساب/الإقفال**.</span><span class="sxs-lookup"><span data-stu-id="77508-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="77508-113">في حقل **طريقة كشف الحساب‬**، حدد الطريقة التي تريد استخدامها لتجميع بنود كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="77508-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="77508-114">حدد "نعم" في **كشف حساب واحد لكل يوم‬** إذا كان ينبغي إنشاء كشف حساب واحد كل يوم عند إنشاء كشوفات حساب من الوظيفة الدفعية لإنشاء كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="77508-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="77508-115">يحدد حقل **احتساب إقرار الدفع** ما إذا كان ينبغي إضافة إقرارات الدفع معًا أو إذا كان يجب استخدام آخر إقرار.</span><span class="sxs-lookup"><span data-stu-id="77508-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="77508-116">في حقل **التقريب**، حدد حساب دفتر الأستاذ لترحيل الفروق التقريبية إليه.</span><span class="sxs-lookup"><span data-stu-id="77508-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="77508-117">في حقل **الحد الأقصى لمبلغ فرق التقريب**، يمكنك إدخال الحد الأقصى لمبلغ فرق التقريب المسموح به.</span><span class="sxs-lookup"><span data-stu-id="77508-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="77508-118">في حقل **الترحيل**، يمكنك إدخال الحد الأقصى لفرق الترحيل الإجمالي المسموح به لكشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="77508-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="77508-119">في حقل **الوردية**، يمكنك إدخال الحد الأقصى للفرق الإجمالي ضمن الوردية في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="77508-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="77508-120">في حقل **الحركة**، يمكنك إدخال الحد الأقصى للفرق الإجمالي في بند كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="77508-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="77508-121">في حقل **أسلوب الإقفال**، يمكنك تحديد ما إذا كان ينبغي أن تكون الحركات التي سيتم تضمينها في كشف الحساب جزءًا من الوردية المقفلة أم إذا كان يمكن أن تكون أي حركات ضمن نطاق تاريخ/وقت محدد.</span><span class="sxs-lookup"><span data-stu-id="77508-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="77508-122">في حقل **نهاية يوم العمل**، يمكنك إدخال وقت إذا كان ينبغي ترحيل الحركات التي تحدث بعد منتصف الليل مع اليوم السابق.</span><span class="sxs-lookup"><span data-stu-id="77508-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="77508-123">حدد "نعم" في **الترحيل كيوم عمل‬** إذا كان ينبغي ترحيل الحركات التي تحدث بعد منتصف الليل كجزء من اليوم السابق.</span><span class="sxs-lookup"><span data-stu-id="77508-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="77508-124">حدد "نعم" في **التقسيم حسب طريقة كشف الحساب‬** للحصول على كشوفات الحساب التي تم إنشاؤها لكل طريقة كشف حساب محددة.</span><span class="sxs-lookup"><span data-stu-id="77508-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="77508-125">قد يكون هذا مفيدًا إذا كان أداء الترحيل بحاجة إلى التحسين للمتاجر التي لها كميات كبيرة من الحركات نظرًا لأنها ستنشئ العديد من كشوفات الحساب الأصغر التي يمكن معالجتها بالتوازي.</span><span class="sxs-lookup"><span data-stu-id="77508-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="77508-126">على علامة التبويب السريعة **عام** في حقل **العميل الافتراضية**، يمكنك تحديد حساب العميل المراد استخدامه للمبيعات للعملاء المباشرين.</span><span class="sxs-lookup"><span data-stu-id="77508-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  
