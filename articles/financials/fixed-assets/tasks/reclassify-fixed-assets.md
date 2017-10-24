--- 
title: "إعادة تصنيف الأصول الثابتة"
description: "لإعادة تصنيف أصل ثابت، يتعين عليك تحويله إلى مجموعة أصول ثابتة جديدة، أو تعيين رقم أصل ثابت جديد له في نفس المجموعة."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fda4d71b050edde2752536985b18ebcad203d078
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="6c569-103">إعادة تصنيف الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="6c569-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c569-104">لإعادة تصنيف أصل ثابت، يتعين عليك تحويله إلى مجموعة أصول ثابتة جديدة، أو تعيين رقم أصل ثابت جديد له في نفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="6c569-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="6c569-105">عند إعادة تصنيف أصل ثابت:</span><span class="sxs-lookup"><span data-stu-id="6c569-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="6c569-106">• يتم إنشاء كل نماذج قيم الأصل الثابت الموجود للأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="6c569-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="6c569-107">يتم نسخ أية معلومات كانت معدة للأصل الثابت الأولي إلى الأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="6c569-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="6c569-108">تكون حالة نماذج القيم للأصل الثابت الأولي "مغلق".</span><span class="sxs-lookup"><span data-stu-id="6c569-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="6c569-109">• تحتوي نماذج القيم الجديدة للأصل الثابت الجديد على تاريخ إعادة التصنيف في الحقل "تاريخ الاستحواذ".</span><span class="sxs-lookup"><span data-stu-id="6c569-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="6c569-110">يتم نسخ التاريخ الموجود في حقل "تاريخ تشغيل الإهلاك‬" من معلومات الأصل الأولي.</span><span class="sxs-lookup"><span data-stu-id="6c569-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="6c569-111">إذا كان الإهلاك قد بدأ بالفعل، فسيعرض الحقل "التاريخ الذي تم فيه آخر تشغيل للإهلاك‬" تاريخ إعادة التصنيف.</span><span class="sxs-lookup"><span data-stu-id="6c569-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="6c569-112">• يتم إلغاء حركات الأصل الثابت الموجود للأصل الثابت الأولي، ويعاد إنشاءها للأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="6c569-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="6c569-113">انتقل إلى الأصول الثابتة > المهام الدورية > إعادة تصنيف‬.</span><span class="sxs-lookup"><span data-stu-id="6c569-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="6c569-114">في حقل "مجموعة الأصول الثابتة:"، حدد المجموعة لإعادة تصنيفها.</span><span class="sxs-lookup"><span data-stu-id="6c569-114">In the Fixed asset group field, selet the group to reclassify.</span></span>
3. <span data-ttu-id="6c569-115">في حقل "رقم الأصل الثابت"، حدد الأصل الثبت لإعادة تصنيفه.</span><span class="sxs-lookup"><span data-stu-id="6c569-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="6c569-116">في حقل "مجموعة الأصول الثابتة الجديدة‬"، حدد مجموعة لتحويل الأصل الثابت إليها.</span><span class="sxs-lookup"><span data-stu-id="6c569-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="6c569-117">إذا كانت مجموعة الأصول الثابتة الجديدة مرفقة بتسلسل رقمي، فسيتم تحديث حقل "رقم الأصل الثابت الجديد" بالرقم من التسلسل الرقمي لمجموعة الأصول الثابتة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="6c569-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="6c569-118">وإلا، فسيتم تحديث حقل "رقم الأصل الثابت الجديد" برقم من التسلسل الرقمي الذي تم إعداده في صفحة "محددات الأصول الثابتة‬".</span><span class="sxs-lookup"><span data-stu-id="6c569-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="6c569-119">إذا لم يتم إعداد تسلسل رقمي في صفحة "محددات الأصول الثابتة‬"، فأدخل رقمًا في الحقل "رقم الأصل الثابت الجديد‬".</span><span class="sxs-lookup"><span data-stu-id="6c569-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="6c569-120">في حقل "تاريخ إعادة التصنيف"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6c569-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="6c569-121">في حقل "مسلسل الإيصال‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6c569-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="6c569-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6c569-122">Click OK.</span></span>


