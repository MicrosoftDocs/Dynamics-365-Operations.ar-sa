---
title: "الاحتفاظ بأنواع الأكواد الشريطية"
description: "يوضح هذا الإجراء كيفية إعداد تعريف كود شريطي جديد يمكن استخدامه بعد ذلك كجزء من تقرير قائمة الانتقاء."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: bc863ce86c4dc3cbdd3a1df881eb7a6efeea1656
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="fac1d-103">الاحتفاظ بأنواع الأكواد الشريطية</span><span class="sxs-lookup"><span data-stu-id="fac1d-103">Maintain bar code types</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fac1d-104">يوضح هذا الإجراء كيفية إعداد تعريف كود شريطي جديد يمكن استخدامه بعد ذلك كجزء من تقرير قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="fac1d-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="fac1d-105">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="fac1d-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="fac1d-106">إذا كنت تستخدم USMF، فيمكنك استخدام القيم المعروضة التي تم استخدامها كأمثلة.</span><span class="sxs-lookup"><span data-stu-id="fac1d-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="fac1d-107">وعادة ما تُنفذ هذه المهام عن طريق مدير مستودع.</span><span class="sxs-lookup"><span data-stu-id="fac1d-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="fac1d-108">انتقل إلى الأكواد الشريطية.</span><span class="sxs-lookup"><span data-stu-id="fac1d-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="fac1d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fac1d-109">Click New.</span></span>
3. <span data-ttu-id="fac1d-110">في الحقل "الكود الشريطي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fac1d-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="fac1d-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fac1d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fac1d-112">في الحقل "نوع الكود الشريطي"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="fac1d-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="fac1d-113">إذا كنت تستخدم USMF، يمكنك تحديد "الكود 39".</span><span class="sxs-lookup"><span data-stu-id="fac1d-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="fac1d-114">في الحقل" الحجم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fac1d-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="fac1d-115">في الحقل "الحد الأقصى للطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fac1d-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="fac1d-116">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="fac1d-116">Click Save.</span></span>
9. <span data-ttu-id="fac1d-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fac1d-117">Close the page.</span></span>
10. <span data-ttu-id="fac1d-118">انتقل إلى معلمات إدارة المخزون والمستودعات.</span><span class="sxs-lookup"><span data-stu-id="fac1d-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="fac1d-119">في الحقل "إعداد الكود الشريطي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="fac1d-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="fac1d-120">حدد إعداد الكود الشريطي الذي قمت بإنشائه سابقًا، ولكن انتبه إلى أن تنسيق الكود الشريطي يجب أن يطابق تنسيق المعرف الفريد لنوع السجل المستخدم في العملية.</span><span class="sxs-lookup"><span data-stu-id="fac1d-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="fac1d-121">على سبيل المثال، بالنسبة لمسارات الانتقاء، يجب أن يطابق تنسيق الكود الشريطي تنسيق مرجع مسار الانتقاء الذي يكون تسلسلاً رقميًا في العادة.</span><span class="sxs-lookup"><span data-stu-id="fac1d-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="fac1d-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="fac1d-122">Click Save.</span></span>
13. <span data-ttu-id="fac1d-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fac1d-123">Close the page.</span></span>

