--- 
title: "حساب إهلاك الأصول الثابتة عبر الكيانات القانونية"
description: "استخدم هذا الإجراء لتغيير مجموعة الأصول الثابتة التي تم تعيين أصل ثابت لها."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1e065ad8b18d6d0871f6127daec2d4f46f094e5
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="b91b0-103">حساب إهلاك الأصول الثابتة عبر الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="b91b0-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b91b0-104">استخدم هذا الإجراء لتغيير مجموعة الأصول الثابتة التي تم تعيين أصل ثابت لها.</span><span class="sxs-lookup"><span data-stu-id="b91b0-104">Use this procedure to change the fixed asset group that a fixed asset is assigned to.</span></span> <span data-ttu-id="b91b0-105">يجب تعيين الأصول الثابتة إلى مجموعة الأصول الثابتة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="b91b0-105">Fixed assets should be assigned to the correct fixed asset group.</span></span> <span data-ttu-id="b91b0-106">يتم استخدام مجموعة الأصول الثابتة عند إنشاء الاستعلامات والتقارير، وإعداد الأصول الثابتة الجديدة، ودمج دفاتر الأستاذ وترحيل حركات الأصول الثابتة لحسابات دفتر الأستاذ المناسبة.</span><span class="sxs-lookup"><span data-stu-id="b91b0-106">The fixed asset group is used when you create inquiries and reports, set up new fixed assets, and integrate ledgers and post fixed asset transactions to the appropriate ledger accounts.</span></span>

<span data-ttu-id="b91b0-107">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="b91b0-107">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="b91b0-108">انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="b91b0-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b91b0-109">حدد الأصل الثابت الذي تريد تغيير مجموعة الأصول الثابتة له.</span><span class="sxs-lookup"><span data-stu-id="b91b0-109">Select the fixed asset to change the fixed asset group for.</span></span>
3. <span data-ttu-id="b91b0-110">انقر فوق "تغيير مجموعة الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="b91b0-110">Click Change fixed asset group.</span></span>
4. <span data-ttu-id="b91b0-111">في الحقل "مجموعة جديدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b91b0-111">In the New group field, enter or select a value.</span></span>
5. <span data-ttu-id="b91b0-112">عيّن خيار "رقم الأصل الثابت الجديد" إلى "نعم" لتعيين رقم أصل ثابت إلى الأصل الثابت المحدد.</span><span class="sxs-lookup"><span data-stu-id="b91b0-112">Set the New fixed asset number option to Yes to assign a fixed asset number to the selected fixed asset.</span></span>
    * <span data-ttu-id="b91b0-113">يصبح حقل "رقم الأصل الثابت‬" متوفرًا عند تعيين الخيار "رقم الأصل الثابت الجديد‬" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="b91b0-113">The Fixed asset number field becomes available when the New fixed asset number option is set to Yes.</span></span>   <span data-ttu-id="b91b0-114">وفي حالة إعداد ترقيم تلقائي للأصول الثابتة، يعرض هذا الحقل رقم الأصل الثابت المتوفر التالي.</span><span class="sxs-lookup"><span data-stu-id="b91b0-114">If automatic numbering is set up for fixed assets, this field shows the next available fixed asset number.</span></span> <span data-ttu-id="b91b0-115">ويمكنك تغيير الرقم.</span><span class="sxs-lookup"><span data-stu-id="b91b0-115">You can change the number.</span></span>   <span data-ttu-id="b91b0-116">في حالة إعداد الترقيم اليدوي للأصول الثابتة، يكون هذا الحقل فارغًا ويجب إدخال رقم الأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="b91b0-116">If manual numbering is set up for fixed assets, this field is blank, and you must enter the new fixed asset number.</span></span>  
6. <span data-ttu-id="b91b0-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b91b0-117">Click OK.</span></span>
7. <span data-ttu-id="b91b0-118">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="b91b0-118">Click Yes.</span></span>


