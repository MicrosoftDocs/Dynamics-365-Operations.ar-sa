---
title: تكوين فوترة المشروع بين الشركات الشقيقة
description: يوضح هذا الموضوع كيفية إعداد فوترة المشروع بين شركتين في مؤسستك.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144269"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="51929-103">تكوين فوترة المشروع بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="51929-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51929-104">يوضح هذا الموضوع كيفية إعداد فوترة المشروع بين شركتين في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="51929-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="51929-105">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="51929-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="51929-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > المورّدون > كافة المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="51929-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="51929-107">في قائمة **كافة المورّدين**، ابحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="51929-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="51929-108">في جزء الإجراءات، حدد **عام**.</span><span class="sxs-lookup"><span data-stu-id="51929-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="51929-109">حدد **بين الشركات الشقيقة‬**.</span><span class="sxs-lookup"><span data-stu-id="51929-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="51929-110">قم بتعيين **نشط** إلى **نعم** لتمكين التجارة بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="51929-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="51929-111">في حقل **شركة العميل**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="51929-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="51929-112">في الحقل **حسابي**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="51929-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="51929-113">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="51929-113">Select **Save**.</span></span>
9. <span data-ttu-id="51929-114">عد إلى الصفحة الرئيسية بعد إغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="51929-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="51929-115">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها > الإعداد > محددات إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="51929-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="51929-116">حدد علامة تبويب **بين الشركات الشقيقة**.</span><span class="sxs-lookup"><span data-stu-id="51929-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="51929-117">حرّك شريط التمرير إلى **نعم** لتمكين الجداول الزمنية وجدولة الموارد بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="51929-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="51929-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="51929-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="51929-119">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="51929-119">Select **New**.</span></span>
15. <span data-ttu-id="51929-120">في حقل **الكيان القانوني المقرض**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="51929-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="51929-121">حدد خانة الاختيار **إيراد مستحق**.</span><span class="sxs-lookup"><span data-stu-id="51929-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="51929-122">في حقل **فئة الجدول الزمني الافتراضية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="51929-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="51929-123">في حقل **فئة المصروفات الافتراضية‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="51929-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="51929-124">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="51929-124">Select **Save**.</span></span>
20. <span data-ttu-id="51929-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="51929-125">Close the page.</span></span>
21. <span data-ttu-id="51929-126">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها‬‬ > الإعداد > الترحيل > إعداد ترحيل دفتر الأستاذ‬**.</span><span class="sxs-lookup"><span data-stu-id="51929-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="51929-127">في الحقل **أنواع حسابات دفتر الأستاذ**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="51929-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="51929-128">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="51929-128">Select **New**.</span></span>
24. <span data-ttu-id="51929-129">في حقل **الحساب الرئيسي** للصف الجديد، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="51929-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="51929-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="51929-130">Select **Save**.</span></span>
26. <span data-ttu-id="51929-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="51929-131">Close the page.</span></span>
27. <span data-ttu-id="51929-132">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها‬‬ > الإعداد > الأسعار > سعر التحويل‬**.</span><span class="sxs-lookup"><span data-stu-id="51929-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="51929-133">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="51929-133">Select **New**.</span></span>
29. <span data-ttu-id="51929-134">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="51929-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="51929-135">في حقل **الكيان القانوني المقرض**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="51929-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="51929-136">في حقل **نموذج سعر التحويل**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="51929-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="51929-137">في حقل **التسعير‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="51929-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="51929-138">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="51929-138">Select **Save**.</span></span>

