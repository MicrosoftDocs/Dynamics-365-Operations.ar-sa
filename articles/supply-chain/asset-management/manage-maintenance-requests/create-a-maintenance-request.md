---
title: إنشاء طلبات صيانة
description: يشرح هذا الموضوع كيفية إنشاء طلب صيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a85125853b3b69d33f07249e0d2aa7592de1cc8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253412"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="6ccac-103">إنشاء طلبات صيانة</span><span class="sxs-lookup"><span data-stu-id="6ccac-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6ccac-104">يمكن استخدام طلبات الصيانة إذا اكتشف عاملو الصيانة أو الإنتاج أن المعدات تحتاج إلى إصلاح، ولكن لا يمكن تنفيذ مهمة الإصلاح على الفور.</span><span class="sxs-lookup"><span data-stu-id="6ccac-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="6ccac-105">**مثال:** أثناء قيام عامل صيانة بإجراء عملية إصلاح، يكتشف وجود أصل آخر في نفس الموقع يحتاج إلى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="6ccac-106">ولكن ليس لدى عامل الصيانة الوقت أو قطع الغيار المطلوبة للقيام بمهمة الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="6ccac-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="6ccac-107">وبالتالي ، ينشئ طلب صيانة على الأصل ويدخل وصفًا قصيرًا للمشكلة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="6ccac-108">يعرض قسم **طلبات الصيانة النشطة** في جزء **المعلومات ذات الصلة‬** على الجانب الأيسر من صفحة **كل الأصول** أو **الأصول‏‎ النشطة** (**إدارة الأصول** \> **عام** \> **الأصول‏‎** \> **كل الأصول** أو **الأصول‏‎ النشطة**) طلبات الصيانة النشطة المرتبطة بالأصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="6ccac-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="6ccac-109">حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="6ccac-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="6ccac-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6ccac-110">Select **New**.</span></span>
3. <span data-ttu-id="6ccac-111">في مربع الحوار **إنشاء طلب**، في الحقل **نوع طلب الصيانة**، حدد نوع طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="6ccac-112">يتم اقتراح نوع افتراضي.</span><span class="sxs-lookup"><span data-stu-id="6ccac-112">A default type is suggested.</span></span>
4. <span data-ttu-id="6ccac-113">في حقل **الوصف**، أدخل اسمًا أو عنوانًا يصف طلب الصيانة بإيجاز.</span><span class="sxs-lookup"><span data-stu-id="6ccac-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="6ccac-114">في حقلي **موقع العمل** و **الأصل**، حدد موقع عمل أو أصل أو مجموعة تتكون من موقع عمل وأصل، وفق احتياجاتك.</span><span class="sxs-lookup"><span data-stu-id="6ccac-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="6ccac-115">يمكنك إنشاء طلب صيانة دون تحديد أصل، ويمكن إضافة الأصل إلى طلب الصيانة فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="6ccac-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="6ccac-116">إذا كان عامل الصيانة الذي قام بتسجيل دخوله يرتبط بمورد مرتبط بأصل، يتم تعيين حقل **الأصل** بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6ccac-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="6ccac-117">إذا كان طلب صيانة مرفق بالأصل المحدد، يظهر شريط رسالة في أعلى مربع الحوار **إنشاء طلب** لإعلامك عن معرف طلب الصيانة الموجود.</span><span class="sxs-lookup"><span data-stu-id="6ccac-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="6ccac-118">كما يعلمك شريط الرسالة إن كان الأصل مغطى باتفاقيه ضمان.</span><span class="sxs-lookup"><span data-stu-id="6ccac-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="6ccac-119">في الحقل‏‎ **مستوى الخدمة**، حدد مستوى خدمة يشير إلى الطابع الملح للطلب.</span><span class="sxs-lookup"><span data-stu-id="6ccac-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="6ccac-120">إذا قمت بتحديد أصل في الخطوة 5، فيمكنك استخدام الحقول **عَرَض الخطأ** و **منطقة الخطأ** و **نوع الخطأ** لإنشاء تسجيل خطأ.</span><span class="sxs-lookup"><span data-stu-id="6ccac-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="6ccac-121">إذا تسبب طلب الصيانة في وقت تعطل الصيانة، فأدخل تاريخ ووقت بدء وقت التعطل.</span><span class="sxs-lookup"><span data-stu-id="6ccac-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="6ccac-122">يتم تعيين حقل **تم البدء بواسطة** إلى اسمك بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6ccac-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="6ccac-123">يتم تعيين حقل **البداية الفعلية‬** إلى التاريخ والوقت الحاليين بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6ccac-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="6ccac-124">ومع ذلك، يمكنك تغيير القيمة كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="6ccac-125">في حقل **الملاحظات**، أدخل أية ملاحظات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="6ccac-126">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6ccac-126">Select **OK**.</span></span>

![إنشاء طلب صيانة](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="6ccac-128">المعالجة اللاحقة لطلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="6ccac-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="6ccac-129">بعد إنشاء طلب صيانة، ولكن قبل تحويله إلى أمر عمل، يجب تحديث مختلف المعلومات المتعلقة به.</span><span class="sxs-lookup"><span data-stu-id="6ccac-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="6ccac-130">بشكل عام، يقوم مخطط أو موظف إداري آخر بإكمال هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="6ccac-131">في صفحة **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**، حدد الطلب الذي يجب التعامل معه، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="6ccac-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="6ccac-132">في طريقة عرض التفاصيل، يمكنك تحديث معلومات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-132">In the details view, you can update various information.</span></span> <span data-ttu-id="6ccac-133">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="6ccac-133">Here are some examples:</span></span>

- <span data-ttu-id="6ccac-134">حدد الأصل وتحقق منه.</span><span class="sxs-lookup"><span data-stu-id="6ccac-134">Select and verify the asset.</span></span> <span data-ttu-id="6ccac-135">إذا كان يجب تحديد أصل مختلف لاحقًا، فيمكنك تعيين الخيار **تم التحقق من الأصل** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="6ccac-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="6ccac-136">حدد مجموعة عاملي صيانة مسؤولة و/أو عامل صيانة مسؤولاً.</span><span class="sxs-lookup"><span data-stu-id="6ccac-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="6ccac-137">لمزيد من المعلومات حول الإعداد المطلوب، راجع [عاملو الصيانة المسؤولون‬](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="6ccac-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="6ccac-138">حدد نوع مهمة الصيانة، وإذا كانت هذه المعلومات ذات صلة، متغير مهمة صيانة ذات صلة ووظيفة تحتاج إلى تدريبات معينة.</span><span class="sxs-lookup"><span data-stu-id="6ccac-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="6ccac-139">في الحقلين **خط العرض** و **خط الطول**، أدخل الإحداثيات الجغرافية.</span><span class="sxs-lookup"><span data-stu-id="6ccac-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="6ccac-140">تُنقل أية إحداثيات مضافة إلى طلب صيانة إلى أمر عمل ذي صلة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6ccac-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![تحديث طلب الصيانة](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="6ccac-142">إذا قمت بتحديد أصل عند إنشاء طلب صيانة، يمكنك إضافة خطأ واحد إلى الأصل.</span><span class="sxs-lookup"><span data-stu-id="6ccac-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="6ccac-143">بعد إنشاء طلب الصيانة، يمكنك إضافة المزيد من الأخطاء، كما تحتاج.</span><span class="sxs-lookup"><span data-stu-id="6ccac-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="6ccac-144">لإضافة أخطاء، حدد **خطأ الأصل** في صفحة **جميع طلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="6ccac-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]