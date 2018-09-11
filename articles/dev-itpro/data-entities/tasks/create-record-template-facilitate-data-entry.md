--- 
title: "إنشاء قالب سجل لتسهيل إدخال البيانات"
description: "يوضح هذا الإجراء كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد."
author: margoc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d64f32de2fb90397a72d938b937bd1f90e675287
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="c8b7d-103">إنشاء قالب سجل لتسهيل إدخال البيانات</span><span class="sxs-lookup"><span data-stu-id="c8b7d-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8b7d-104">يوضح هذا الإجراء كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="c8b7d-105">في هذا الإجراء، ستقوم بإنشاء سجل جديد لأجهزة الكمبيوتر المحمولة الجديدة التي يجب أن تُضاف إلى الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="c8b7d-106">يستخدم هذا الإجراء الشركة النموذجية USMF.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="c8b7d-107">انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c8b7d-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-108">Click New.</span></span>
3. <span data-ttu-id="c8b7d-109">في حقل "مجموعة الأصول الثابتة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="c8b7d-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c8b7d-111">على سبيل المثال، أدخل "كمبيوتر محمول لقائد في الشركة".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="c8b7d-112">في الحقل "اسم البحث‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="c8b7d-113">على سبيل المثال، أدخل "كمبيوتر محمول".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="c8b7d-114">قم بتوسيع قسم "المعلومات التقنية".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="c8b7d-115">في الحقل "النوع‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="c8b7d-116">في الحقل "نموذج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="c8b7d-117">في الحقل "سنة الطراز‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="c8b7d-118">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="c8b7d-119">انقر فوق "معلومات السجل".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-119">Click Record info.</span></span>
12. <span data-ttu-id="c8b7d-120">انقر فوق "قالب المستخدم".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-120">Click User template.</span></span>
13. <span data-ttu-id="c8b7d-121">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c8b7d-122">على سبيل المثال، أدخل "كمبيوتر محمول للشركة".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="c8b7d-123">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8b7d-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c8b7d-124">على سبيل المثال، أدخل "كمبيوتر محمول للشركة".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="c8b7d-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-125">Click OK.</span></span>
16. <span data-ttu-id="c8b7d-126">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="c8b7d-126">Click Close.</span></span>


