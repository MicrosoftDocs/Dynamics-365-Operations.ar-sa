---
title: إنشاء بُنى القواعد المتقدمة وتعيينها
description: يشرح هذا الموضوع كيفية إنشاء وتعيين بنية قاعدة متقدمة إلى بنية حساب.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439830"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="d1b4e-103">إنشاء بُنى القواعد المتقدمة وتعيينها</span><span class="sxs-lookup"><span data-stu-id="d1b4e-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1b4e-104">يشرح هذا الموضوع كيفية إنشاء وتعيين بنية قاعدة متقدمة إلى بنية حساب.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="d1b4e-105">يستخدم هذا الدليل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="d1b4e-106">إنشاء بنية قاعدة متقدمة</span><span class="sxs-lookup"><span data-stu-id="d1b4e-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="d1b4e-107">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > دليل الحسابات > البنى > بنى القواعد المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="d1b4e-108">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="d1b4e-109">في الحقل **بنية القاعدة المتقدمة**، اكتب اسمًا لوصف بنية القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="d1b4e-110">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-110">Select **OK**.</span></span>
5. <span data-ttu-id="d1b4e-111">حدد **إضافة شريحة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="d1b4e-112">في قائمة المقاطع، حدد بُعدًا ماليًا.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="d1b4e-113">على سبيل المثال، **تخزين**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="d1b4e-114">حدد **إضافة شريحة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="d1b4e-115">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="d1b4e-116">قم بتطبيق بنية قاعدة متقدمة على بنية حساب.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="d1b4e-117">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > دليل الحسابات > البنى > تكوين بنى الحسابات‬**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="d1b4e-118">في القائمة، ابحث عن بنية الحساب التي تريد تطبيق القاعدة المتقدمة عليها وحددها.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="d1b4e-119">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-119">Select **Edit**.</span></span> <span data-ttu-id="d1b4e-120">ويمكنك أيضًا تحديد **قواعد متقدمة**، وسيُطلب منك وضع بنية الحساب في **الوضع مسودة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="d1b4e-121">حدد **قواعد متقدمة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="d1b4e-122">حدد **جديد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="d1b4e-123">في الحقل **قاعدة متقدمة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="d1b4e-124">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="d1b4e-125">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-125">Select **Create**.</span></span>
9. <span data-ttu-id="d1b4e-126">حدد **إضافة معايير جديدة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="d1b4e-127">في حقل **المكان**، حدد الحساب الرئيسي أو بُعدًا ماليًا.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="d1b4e-128">في حقل **عامل التشغيل**، حدد أحد الخيارات، مثل **بين** و **يتضمن**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="d1b4e-129">في حقل **القيمة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="d1b4e-130">في الحقل **خلال**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="d1b4e-131">حدد **إضافة** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="d1b4e-132">في القائمة، ابحث عن بنية القاعدة المتقدمة التي تريد استخدامها عند موافقة المعايير التي يتم إدخالها.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="d1b4e-133">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-133">Select **Add**.</span></span>
17. <span data-ttu-id="d1b4e-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-134">Close the page.</span></span>
18. <span data-ttu-id="d1b4e-135">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="d1b4e-135">Select **Activate**.</span></span>

