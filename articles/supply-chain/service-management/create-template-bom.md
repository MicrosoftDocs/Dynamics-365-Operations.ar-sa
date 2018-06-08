---
title: "إنشاء شجرة مواد قالب"
description: "يمكنك إنشاء قائمة مكونات الصنف القالب باستخدام طرق متنوعة."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="5ee09-103">إنشاء شجرة مواد قالب</span><span class="sxs-lookup"><span data-stu-id="5ee09-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5ee09-104">يمكنك إنشاء شجرة مواد قالب باستخدام الطرق التالية.</span><span class="sxs-lookup"><span data-stu-id="5ee09-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="5ee09-105">بالنسبة لجميع الطرق، يعد حقلا **من تاريخ** و **إلى تاريخ** اختياريين وللمعلومات فقط.</span><span class="sxs-lookup"><span data-stu-id="5ee09-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="5ee09-106">إنشاء شجرة مواد قالب يدويًا</span><span class="sxs-lookup"><span data-stu-id="5ee09-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="5ee09-107">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="5ee09-108">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="5ee09-109">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد خيار **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="5ee09-110">في حقل **رقم الصنف**، أدخل صنفًا من نوع **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="5ee09-111">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="5ee09-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="5ee09-112">في الحقلين **من تاريخ** و**إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="5ee09-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="5ee09-113">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-113">Click **OK**.</span></span>

<span data-ttu-id="5ee09-114">يتم إنشاء شجرة مواد قالب فارغة جديدة.</span><span class="sxs-lookup"><span data-stu-id="5ee09-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="5ee09-115">إنشاء شجرة مواد قالب تستند إلى شجرة مواد قالب أخرى</span><span class="sxs-lookup"><span data-stu-id="5ee09-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="5ee09-116">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="5ee09-117">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="5ee09-118">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد خيار **قائمة مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="5ee09-119">في الحقل **رقم المرجع**، حدد قائمة مكونات صنف قالب موجودة لنسخها إلى قائمة مكونات الصنف القالب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5ee09-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="5ee09-120">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="5ee09-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="5ee09-121">في الحقلين **من تاريخ** و**إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="5ee09-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="5ee09-122">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-122">Click **OK**.</span></span>

<span data-ttu-id="5ee09-123">يتم إنشاء شجرة مواد قالب جديدة باستخدام بنود تتطابق مع البنود الموجودة في شجرة مواد القالب الأصلية.</span><span class="sxs-lookup"><span data-stu-id="5ee09-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="5ee09-124">إنشاء شجرة مواد قالب تستند إلى شجرة مواد صنف</span><span class="sxs-lookup"><span data-stu-id="5ee09-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="5ee09-125">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="5ee09-126">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="5ee09-127">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="5ee09-128">في **رقم المرجع** ، حدد إصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="5ee09-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="5ee09-129">يتم نسخ صنف من نوع قائمة مكونات الصنف إلى **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="5ee09-130">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="5ee09-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="5ee09-131">في الحقلين **من تاريخ** و**إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="5ee09-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="5ee09-132">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-132">Click **OK**.</span></span>

<span data-ttu-id="5ee09-133">يتم إنشاء قائمة مكونات صنف قالب جديدة باستخدام البنود المتوافقة مع البنود الموجودة في قائمة مكونات الصنف المدرجة في **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="5ee09-134">إنشاء شجرة مواد قالب تستند إلى شجرة مواد إنتاج</span><span class="sxs-lookup"><span data-stu-id="5ee09-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="5ee09-135">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="5ee09-136">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="5ee09-137">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد **الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="5ee09-138">في حقل **رقم المرجع**، حدد قائمة مكونات الصنف للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="5ee09-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="5ee09-139">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="5ee09-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="5ee09-140">في الحقلين **من تاريخ** و**إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="5ee09-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="5ee09-141">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-141">Click **OK**.</span></span>

<span data-ttu-id="5ee09-142">يتم إنشاء قائمة جديدة من قوائم مكونات الصنف القالب باستخدام البنود المتوافقة مع البنود الموجودة في قائمة مكونات الصنف المدرجة في **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5ee09-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ee09-143">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="5ee09-143">See also</span></span>

[<span data-ttu-id="5ee09-144">شجرة المواد القالب </span><span class="sxs-lookup"><span data-stu-id="5ee09-144">Template BOMs</span></span>](template-boms.md)

  


