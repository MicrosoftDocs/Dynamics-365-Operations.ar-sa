---
title: تحديد الأقسام الجديدة
description: الأقسام هي وحدات تشغيل تمثل منطقة وظيفية للشركة، مثل المبيعات أو المحاسبة.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a20b98e755cf5269b72d245156bbd44fd71a3185
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190570"
---
# <a name="define-new-departments"></a><span data-ttu-id="a1b58-103">تحديد الأقسام الجديدة</span><span class="sxs-lookup"><span data-stu-id="a1b58-103">Define new departments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1b58-104">الأقسام هي وحدات تشغيل تمثل منطقة وظيفية للشركة، مثل المبيعات أو المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-104">Departments are operating units that represent a functional area of a business, such as sales or accounting.</span></span> <span data-ttu-id="a1b58-105">تمتلك العديد من الشركات تدرجات هرمية للمؤسسات تعرض مختلف الأقسام داخل الشركة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-105">Many companies have organizational hierarchies that display the various departments within a business.</span></span> <span data-ttu-id="a1b58-106">يتناول هذا الإجراء عملية إنشاء الأقسام وإضافة تلك الأقسام إلى التدرج الهرمي لأقسام المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-106">This procedure walks through the process of creating departments, and adding those departments to an organizations departmental hierarchy.</span></span> <span data-ttu-id="a1b58-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="a1b58-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a1b58-108">انتقل إلى الموارد البشرية > الأقسام > الأقسام.</span><span class="sxs-lookup"><span data-stu-id="a1b58-108">Go to Human resources > Departments > Departments.</span></span>
2. <span data-ttu-id="a1b58-109">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="a1b58-109">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="a1b58-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a1b58-111">مثال: ‏‫فوترة مشروع</span><span class="sxs-lookup"><span data-stu-id="a1b58-111">Example: Project billing</span></span>  
4. <span data-ttu-id="a1b58-112">في حقل "مذكرة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-112">In the Memo field, type a value.</span></span>
    * <span data-ttu-id="a1b58-113">مثال: ‏‫فوترة مشروع</span><span class="sxs-lookup"><span data-stu-id="a1b58-113">Example: Project billing</span></span>  
5. <span data-ttu-id="a1b58-114">في حقل "المدير"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a1b58-114">In the Manager field, enter or select a value.</span></span>
    * <span data-ttu-id="a1b58-115">مثال: جودي كريستيانسين</span><span class="sxs-lookup"><span data-stu-id="a1b58-115">Example: Jodi Christiansen</span></span>  
6. <span data-ttu-id="a1b58-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a1b58-116">Click Save.</span></span>
7. <span data-ttu-id="a1b58-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-117">Close the page.</span></span>
8. <span data-ttu-id="a1b58-118">انتقل إلى الموارد البشرية > الأقسام > التدرج الهرمي للأقسام.</span><span class="sxs-lookup"><span data-stu-id="a1b58-118">Go to Human resources > Departments > Department hierarchy.</span></span>
9. <span data-ttu-id="a1b58-119">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a1b58-119">Click Edit.</span></span>
10. <span data-ttu-id="a1b58-120">انقر فوق إدراج.</span><span class="sxs-lookup"><span data-stu-id="a1b58-120">Click Insert.</span></span>
11. <span data-ttu-id="a1b58-121">انقر فوق القسم.</span><span class="sxs-lookup"><span data-stu-id="a1b58-121">Click Department.</span></span>
12. <span data-ttu-id="a1b58-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a1b58-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a1b58-123">مثال: ‏‫فوترة مشروع</span><span class="sxs-lookup"><span data-stu-id="a1b58-123">Example: Project billing</span></span>  
13. <span data-ttu-id="a1b58-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a1b58-124">Click OK.</span></span>
14. <span data-ttu-id="a1b58-125">انقر فوق "نشر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="a1b58-125">Click Publish to open the drop dialog.</span></span>
15. <span data-ttu-id="a1b58-126">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="a1b58-126">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="a1b58-127">عند نشر التدرج الهرمي للقسم، يمكنك تحديد متى يتم تفعيل التغييرات.</span><span class="sxs-lookup"><span data-stu-id="a1b58-127">When publishing the department hierarchy, you can select when to make the changes effective.</span></span> <span data-ttu-id="a1b58-128">يمكن أن يكون تاريخ التغييرات في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="a1b58-128">Changes can be future dated.</span></span> <span data-ttu-id="a1b58-129">على سبيل المثال، قد تعرف أنه في بداية السنة المالية الخاصة بك، سيتم إضافة قسم إضافي.</span><span class="sxs-lookup"><span data-stu-id="a1b58-129">For example, you may know that at the beginning of your fiscal year you will be adding an additional department.</span></span> <span data-ttu-id="a1b58-130">يمكنك تعيين تاريخ السريان الخاص بك إلى بداية السنة المالية، وستصبح التغييرات على التدرج الهرمي سارية المفعول في ذلك التاريخ.</span><span class="sxs-lookup"><span data-stu-id="a1b58-130">You can set your effective date to the beginning of the fiscal year, and the changes to the hierarchy will be effective on that date.</span></span>  
16. <span data-ttu-id="a1b58-131">في حقل "وصف التغييرات‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a1b58-131">In the Describe changes field, type a value.</span></span>
17. <span data-ttu-id="a1b58-132">انقر فوق "نشر".</span><span class="sxs-lookup"><span data-stu-id="a1b58-132">Click Publish.</span></span>

