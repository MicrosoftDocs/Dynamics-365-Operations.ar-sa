--- 
title: "إنشاء ملف تعريف للموقع"
description: "يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع، على سبيل المثال، ما إذا كان الموقع يسمح بأصناف مختلطة."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a4a159b0e849a73efb362ccadb841bd25c323290
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-location-profile"></a><span data-ttu-id="d5d8c-103">إنشاء ملف تعريف للموقع</span><span class="sxs-lookup"><span data-stu-id="d5d8c-103">Create a location profile</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5d8c-104">يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع، على سبيل المثال، ما إذا كان الموقع يسمح بأصناف مختلطة.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="d5d8c-105">في هذا الإجراء سوف نقوم بإنشاء ملف تعريف لموقع لا يتطلب التحكم بواسطة لوحة الترخيص‬.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="d5d8c-106">سنقوم بتمكين الأصناف المختلطة وحالات المخزون مختلطة، ونسمح بالجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="d5d8c-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="d5d8c-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d5d8c-108">Click New.</span></span>
2. <span data-ttu-id="d5d8c-109">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="d5d8c-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d5d8c-111">في الحقل "تنسيق الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="d5d8c-112">في الحقل "نوع الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="d5d8c-113">في الحقل "‏‫‏‫معرف ملف تعريف إدارة المساحات‬ "، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="d5d8c-114">حدد "نعم" في حقل "‏‫‏‫السماح بالأصناف المختلطة".</span><span class="sxs-lookup"><span data-stu-id="d5d8c-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d5d8c-115">حدد "نعم" في حقل "‏‫‏‫السماح بحالات المخزون المختلطة".</span><span class="sxs-lookup"><span data-stu-id="d5d8c-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d5d8c-116">حدد "نعم" في حقل "‏‫السماح بالجرد الدوري‬".</span><span class="sxs-lookup"><span data-stu-id="d5d8c-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="d5d8c-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d5d8c-117">Click Save.</span></span>
11. <span data-ttu-id="d5d8c-118">انتقل إلى إدارة المستودعات‬ > إعداد > المستودع > ملفات تعريف الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>


