---
title: الاحتفاظ بأنواع الكود الشريطي
description: يوضح هذا الإجراء كيفية إعداد تعريف كود شريطي جديد يمكن استخدامه بعد ذلك كجزء من تقرير قائمة الانتقاء.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 112438417e425b8b77dd56f25e0b6e6db21c5148
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244389"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="66149-103">الاحتفاظ بأنواع الكود الشريطي</span><span class="sxs-lookup"><span data-stu-id="66149-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66149-104">يوضح هذا الإجراء كيفية إعداد تعريف كود شريطي جديد يمكن استخدامه بعد ذلك كجزء من تقرير قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="66149-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="66149-105">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="66149-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="66149-106">إذا كنت تستخدم USMF، فيمكنك استخدام القيم المعروضة التي تم استخدامها كأمثلة.</span><span class="sxs-lookup"><span data-stu-id="66149-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="66149-107">وعادة ما تُنفذ هذه المهام عن طريق مدير مستودع.</span><span class="sxs-lookup"><span data-stu-id="66149-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="66149-108">انتقل إلى الأكواد الشريطية.</span><span class="sxs-lookup"><span data-stu-id="66149-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="66149-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="66149-109">Click New.</span></span>
3. <span data-ttu-id="66149-110">في الحقل "الكود الشريطي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66149-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="66149-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66149-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="66149-112">في الحقل "نوع الكود الشريطي"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="66149-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="66149-113">إذا كنت تستخدم USMF، يمكنك تحديد "الكود 39".</span><span class="sxs-lookup"><span data-stu-id="66149-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="66149-114">في الحقل" الحجم"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="66149-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="66149-115">في الحقل "الحد الأقصى للطول"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="66149-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="66149-116">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="66149-116">Click Save.</span></span>
9. <span data-ttu-id="66149-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66149-117">Close the page.</span></span>
10. <span data-ttu-id="66149-118">انتقل إلى معلمات إدارة المخزون والمستودعات.</span><span class="sxs-lookup"><span data-stu-id="66149-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="66149-119">في الحقل "إعداد الكود الشريطي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="66149-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="66149-120">حدد إعداد الكود الشريطي الذي قمت بإنشائه سابقًا، ولكن انتبه إلى أن تنسيق الكود الشريطي يجب أن يطابق تنسيق المعرف الفريد لنوع السجل المستخدم في العملية.</span><span class="sxs-lookup"><span data-stu-id="66149-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="66149-121">على سبيل المثال، بالنسبة لمسارات الانتقاء، يجب أن يطابق تنسيق الكود الشريطي تنسيق مرجع مسار الانتقاء الذي يكون تسلسلاً رقميًا في العادة.</span><span class="sxs-lookup"><span data-stu-id="66149-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="66149-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="66149-122">Click Save.</span></span>
13. <span data-ttu-id="66149-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66149-123">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]