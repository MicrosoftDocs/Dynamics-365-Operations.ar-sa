--- 
title: "إنشاء قالب سجل لتسهيل إدخال البيانات"
description: "يوضح هذا الإجراء كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد."
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6f8d804133f8e9c6f47420d41df8d9430381e2fe
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="50eae-103">إنشاء قالب سجل لتسهيل إدخال البيانات</span><span class="sxs-lookup"><span data-stu-id="50eae-103">Create a record template to facilitate data entry</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50eae-104">يوضح هذا الإجراء كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="50eae-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="50eae-105">في هذا الإجراء، ستقوم بإنشاء سجل جديد لأجهزة الكمبيوتر المحمولة الجديدة التي يجب أن تُضاف إلى الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="50eae-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="50eae-106">يستخدم هذا الإجراء الشركة النموذجية USMF.</span><span class="sxs-lookup"><span data-stu-id="50eae-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="50eae-107">انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="50eae-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="50eae-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="50eae-108">Click New.</span></span>
3. <span data-ttu-id="50eae-109">في حقل "مجموعة الأصول الثابتة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="50eae-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="50eae-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="50eae-111">على سبيل المثال، أدخل "كمبيوتر محمول لقائد في الشركة".</span><span class="sxs-lookup"><span data-stu-id="50eae-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="50eae-112">في الحقل "اسم البحث‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="50eae-113">على سبيل المثال، أدخل "كمبيوتر محمول".</span><span class="sxs-lookup"><span data-stu-id="50eae-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="50eae-114">قم بتوسيع قسم "المعلومات التقنية".</span><span class="sxs-lookup"><span data-stu-id="50eae-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="50eae-115">في الحقل "النوع‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="50eae-116">في الحقل "نموذج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="50eae-117">في الحقل "سنة الطراز‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="50eae-118">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="50eae-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="50eae-119">انقر فوق "معلومات السجل".</span><span class="sxs-lookup"><span data-stu-id="50eae-119">Click Record info.</span></span>
12. <span data-ttu-id="50eae-120">انقر فوق "قالب المستخدم".</span><span class="sxs-lookup"><span data-stu-id="50eae-120">Click User template.</span></span>
13. <span data-ttu-id="50eae-121">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="50eae-122">على سبيل المثال، أدخل "كمبيوتر محمول للشركة".</span><span class="sxs-lookup"><span data-stu-id="50eae-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="50eae-123">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="50eae-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="50eae-124">على سبيل المثال، أدخل "كمبيوتر محمول للشركة".</span><span class="sxs-lookup"><span data-stu-id="50eae-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="50eae-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="50eae-125">Click OK.</span></span>
16. <span data-ttu-id="50eae-126">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="50eae-126">Click Close.</span></span>


