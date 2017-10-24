--- 
title: " تكوينات المتجر لحساب بيانات Retail"
description: "يتناول هذا الإجراء تكوينات لمتجر البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cac676c9c6ebb6769fe7e30ac08a2c8334befc24
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="ec93d-103"> تكوينات المتجر لحساب بيانات Retail</span><span class="sxs-lookup"><span data-stu-id="ec93d-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ec93d-104">يتناول هذا الإجراء تكوينات لمتجر البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="ec93d-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="ec93d-105">ويتم تناول الأبعاد المالية في متاجر البيع بالتجزئة في إجراء آخر.</span><span class="sxs-lookup"><span data-stu-id="ec93d-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="ec93d-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="ec93d-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="ec93d-107">انتقل إلى البيع بالتجزئة والتجارة > القنوات > متاجر البيع بالتجزئة > جميع متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="ec93d-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="ec93d-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="ec93d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ec93d-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ec93d-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ec93d-110">تؤثر الإعدادات الموجودة في قسم كشف الحساب/الإقفال على إنشاء كشف الحساب والتحقق من الصحة والترحيل للمتجر.</span><span class="sxs-lookup"><span data-stu-id="ec93d-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="ec93d-111">قم بفتح قسم كشف الحساب/الإقفال.</span><span class="sxs-lookup"><span data-stu-id="ec93d-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="ec93d-112">حدد الطريقة التي تريد استخدامها لتجميع بنود كشف الحساب بواسطة.</span><span class="sxs-lookup"><span data-stu-id="ec93d-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="ec93d-113">حدد "نعم" إذا ينبغي أن يتم إنشاء كشف حساب واحد كل يوم عند إنشاء كشوفات حساب من الوظيفة الدفعية لإنشاء كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="ec93d-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="ec93d-114">يحدد حقل "‏‫احتساب إقرار الدفع" ما إذا كان ينبغي إضافة إقرارات الدفع معًا أو إذا كان يجب استخدام آخر إقرار.</span><span class="sxs-lookup"><span data-stu-id="ec93d-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="ec93d-115">حدد حساب دفتر الأستاذ لترحيل الفروق التقريبية إليه.</span><span class="sxs-lookup"><span data-stu-id="ec93d-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="ec93d-116">في حقل "الحد الأقصى لمبلغ فرق التقريب"، يمكنك إدخال الحد الأقصى لمبلغ فرق التقريب المسموح به.</span><span class="sxs-lookup"><span data-stu-id="ec93d-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="ec93d-117">في حقل "ترحيل"، يمكنك إدخال الحد الأقصى لفرق الترحيل الإجمالي المسموح به لكشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="ec93d-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="ec93d-118">في حقل "الوردية"، يمكنك إدخال الحد الأقصى للفرق الإجمالي ضمن الوردية في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="ec93d-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="ec93d-119">في حقل "الحركة"، يمكنك إدخال الحد الأقصى للفرق الإجمالي في بند كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="ec93d-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="ec93d-120">في حقل أسلوب الإقفال، يمكنك تحديد ما إذا كان ينبغي أن تكون الحركات التي سيتم تضمينها في كشف الحساب جزءًا من الوردية المقفلة أم إذا كان يمكن أن تكون أي حركات ضمن نطاق تاريخ/وقت محدد.</span><span class="sxs-lookup"><span data-stu-id="ec93d-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="ec93d-121">في حقل "نهاية يوم العمل"، يمكنك إدخال وقت إذا كان ينبغي ترحيل الحركات التي تحدث بعد منتصف الليل مع اليوم السابق.</span><span class="sxs-lookup"><span data-stu-id="ec93d-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="ec93d-122">حدد "نعم" إذا كان ينبغي ترحيل الحركات التي تحدث بعد منتصف الليل كجزء من اليوم السابق.</span><span class="sxs-lookup"><span data-stu-id="ec93d-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="ec93d-123">حدد "نعم" للحصول على كشوفات الحساب التي تم إنشاؤها لكل طريقة كشف حساب محددة.</span><span class="sxs-lookup"><span data-stu-id="ec93d-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="ec93d-124">قد يكون هذا مفيدًا إذا كان أداء الترحيل بحاجة إلى التحسين للمتاجر التي لها كميات كبيرة من الحركات نظرًا لأنها ستنشئ العديد من كشوفات الحساب الأصغر التي يمكن معالجتها بالتوازي.</span><span class="sxs-lookup"><span data-stu-id="ec93d-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="ec93d-125">في حقل "العميل الافتراضي"، يمكنك تحديد حساب العميل المراد استخدامه للمبيعات للعملاء المباشرين.</span><span class="sxs-lookup"><span data-stu-id="ec93d-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


