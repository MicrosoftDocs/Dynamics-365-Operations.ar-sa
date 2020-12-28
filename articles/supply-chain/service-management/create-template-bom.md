---
title: إنشاء شجرة مواد قالب
description: يمكنك إنشاء قائمة مكونات الصنف القالب باستخدام طرق متنوعة.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e06283f3b95c5ff6b4376bba63cf5a42d5feeb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421489"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="6c3ad-103">إنشاء شجرة مواد قالب</span><span class="sxs-lookup"><span data-stu-id="6c3ad-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c3ad-104">يمكنك إنشاء شجرة مواد قالب باستخدام الطرق التالية.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="6c3ad-105">بالنسبة لجميع الطرق، يعد حقلا **من تاريخ** و **إلى تاريخ** اختياريين وللمعلومات فقط.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="6c3ad-106">إنشاء شجرة مواد قالب يدويًا</span><span class="sxs-lookup"><span data-stu-id="6c3ad-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="6c3ad-107">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c3ad-108">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c3ad-109">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد خيار **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="6c3ad-110">في حقل **رقم الصنف**، أدخل صنفًا من نوع **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="6c3ad-111">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c3ad-112">في الحقلين **من تاريخ** و **إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c3ad-113">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-113">Click **OK**.</span></span>

<span data-ttu-id="6c3ad-114">يتم إنشاء شجرة مواد قالب فارغة جديدة.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="6c3ad-115">إنشاء شجرة مواد قالب تستند إلى شجرة مواد قالب أخرى</span><span class="sxs-lookup"><span data-stu-id="6c3ad-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="6c3ad-116">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c3ad-117">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c3ad-118">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد خيار **قائمة مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="6c3ad-119">في الحقل **رقم المرجع**، حدد قائمة مكونات صنف قالب موجودة لنسخها إلى قائمة مكونات الصنف القالب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="6c3ad-120">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c3ad-121">في الحقلين **من تاريخ** و **إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c3ad-122">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-122">Click **OK**.</span></span>

<span data-ttu-id="6c3ad-123">يتم إنشاء شجرة مواد قالب جديدة باستخدام بنود تتطابق مع البنود الموجودة في شجرة مواد القالب الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="6c3ad-124">إنشاء شجرة مواد قالب تستند إلى شجرة مواد صنف</span><span class="sxs-lookup"><span data-stu-id="6c3ad-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="6c3ad-125">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c3ad-126">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c3ad-127">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="6c3ad-128">في **رقم المرجع** ، حدد إصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="6c3ad-129">يتم نسخ صنف من نوع قائمة مكونات الصنف إلى **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="6c3ad-130">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c3ad-131">في الحقلين **من تاريخ** و **إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c3ad-132">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-132">Click **OK**.</span></span>

<span data-ttu-id="6c3ad-133">يتم إنشاء قائمة مكونات صنف قالب جديدة باستخدام البنود المتوافقة مع البنود الموجودة في قائمة مكونات الصنف المدرجة في **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="6c3ad-134">إنشاء شجرة مواد قالب تستند إلى شجرة مواد إنتاج</span><span class="sxs-lookup"><span data-stu-id="6c3ad-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="6c3ad-135">انقر فوق **إدارة الخدمة** \> **الإعداد‏‎** \> **كائنات الخدمة** \> **قوائم مكونات الصنف القالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c3ad-136">اضغط على CTRL+N لفتح نموذج **إنشاء قائمة مكونات صنف قالب**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c3ad-137">تحت **نسخ بنود قائمة مكونات الصنف من المرجع**، حدد **الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="6c3ad-138">في حقل **رقم المرجع**، حدد قائمة مكونات الصنف للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="6c3ad-139">في الحقل **الاسم**، أدخل اسمًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c3ad-140">في الحقلين **من تاريخ** و **إلى تاريخ**، أدخل فترة تاريخ تكون فيها قائمة مكونات الصنف القالب نشطة.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c3ad-141">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-141">Click **OK**.</span></span>

<span data-ttu-id="6c3ad-142">يتم إنشاء قائمة جديدة من قوائم مكونات الصنف القالب باستخدام البنود المتوافقة مع البنود الموجودة في قائمة مكونات الصنف المدرجة في **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6c3ad-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c3ad-143">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="6c3ad-143">See also</span></span>

[<span data-ttu-id="6c3ad-144">شجرة المواد القالب </span><span class="sxs-lookup"><span data-stu-id="6c3ad-144">Template BOMs</span></span>](template-boms.md)

  


