---
title: التحديث التلقائي لعدادات الأصول
description: يصف هذا الموضوع التحديث التلقائي لعدادات الأصول‬ في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421190"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="8d2e7-103">التحديث التلقائي لعدادات الأصول</span><span class="sxs-lookup"><span data-stu-id="8d2e7-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d2e7-104">لمزيد من المعلومات حول التسجيل اليدوي لعدادات الأصول، راجع [التحديث اليدوي لعدادات الأصول](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="8d2e7-105">للحصول علي معلومات حول كيفية إعداد عدادات الأصول، راجع [العدادات](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="8d2e7-106">يمكن أيضًا تحديث قيم العدادات بشكل تلقائي من تسجيلات الإنتاج، استنادًا إلى ساعات الإنتاج أو كمية الإنتاج (وهذه هي، الكمية التي يتم إنتاجها).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="8d2e7-107">ويتم القيام بهذا التحديث في صفحة **تحديث عدادات الأصول** .</span><span class="sxs-lookup"><span data-stu-id="8d2e7-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="8d2e7-108">يمكنك تحديث أصل واحد أو عدة أصول عن طريق إعداد معلمة واحدة، **من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="8d2e7-109">تحدد هذه المعلمة تاريخ البدء لتسجيلات الإنتاج (ساعات الإنتاج أو كميات الإنتاج).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="8d2e7-110">بمعني آخر، يقوم بتحديد التاريخ الذي ينبغي تحديث قيم العداد بداية منه.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="8d2e7-111">سيتم تضمين كافة الأصول المرتبطة بأحد الموارد، *وتلك* التي لها عدادات أصول، والتي تم إعدادها ليتم تحديثها استنادًا إلى ساعات الإنتاج أو الكمية المنتجة، في تحديث تلقائي.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="8d2e7-112">سوف يتم إنشاء قيم عدادات جديدة.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-112">New counter values will be created.</span></span>

<span data-ttu-id="8d2e7-113">بالنسبة للعدادات التي تستند إلى كميه الإنتاج، يتضمن الجرد كلاً من الكمية الجيدة والكمية التي بها خطأ المسجلة.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="8d2e7-114">وإذا كانت الوحدة المستخدمة لتسجيل الكمية المنتجة مختلفة عن الوحدة المستخدمة في العداد، سيتم تحويل الكمية بحيث تتوافق مع وحدة العداد.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="8d2e7-115">كما ورد أعلاه، يمكن تحديث العدادات التلقائية من تسجيلات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="8d2e7-116">وبالتالي، يجب أن يكون الأصل الذي تريد تحديث عداداته بشكل تلقائي مرتبطًا بمورد (الجهاز).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="8d2e7-117">عند تسجيل الكميات المنتجة أو ساعات الإنتاج في المورد، يمكنك تحديث عدادات الأصول المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="8d2e7-118">حدد **إدارة‏‎ الأصول‏‎** > **دوري** > **الأصول‏‎** > **تحديث عدادات الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="8d2e7-119">حدد تاريخ بدء التحديث التلقائي في الحقل **من تاريخ** .</span><span class="sxs-lookup"><span data-stu-id="8d2e7-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="8d2e7-120">التاريخ الموجود في هذا الحقل هو تاريخ "العمل قيد التقدم" من **حركات‏‎ المسار** (**التحكم بالإنتاج‬** > **الاستعلامات والتقارير‬** > **الإنتاج‬‏‎** > **حركات‏‎ المسار** > حقل **التاريخ‏‎ الفعلي**).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="8d2e7-121">في علامة التبويب السريع **السجلات المطلوب تضمينها‬** ، يمكنك تحديد أصول، وأنواع أصول أو موارد معينة للتحديث التلقائي.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="8d2e7-122">حدد **عامل التصفية** ، وقم بإجراء التحديدات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="8d2e7-123">في علامة التبويب السريعة **تشغيل في الخلفية‬**، يمكنك إعداد التحديث التلقائي كوظيفة دفعية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="8d2e7-124">يبين الرسم التوضيحي التالي مثالاً لمربع الحوار **تحديث عدادات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![الشكل 1](media/12-work-orders.png)

5. <span data-ttu-id="8d2e7-126">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-126">Select **OK**.</span></span> 

<span data-ttu-id="8d2e7-127">بعد الانتهاء من تحديث عداد الأصول التلقائي، يمكنك عرض تسجيلات العدادات المرتبطة بالأصل في صفحة **عدادات الأصول** .</span><span class="sxs-lookup"><span data-stu-id="8d2e7-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="8d2e7-128">حدد **إدارة الأصول** > **عام** > **الأصول** > **جميع الأصول**، حدد الأصل، ثم في جزء الإجراءات، في علامة التبويب **الأصل** ، في المجموعة **الوقائية** ، حدد **العدادات**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="8d2e7-129">في صفحة **قيمة الأصول المجمعة** ، يمكنك الحصول على نظرة عامة حول التسجيل الأخير الذي تم إجراؤه على جميع أنواع العدادات في جميع الأصول.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="8d2e7-130">حدد **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **قيمة الأصول المجمعة**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="8d2e7-131">تُشبه هذه الصفحة صفحة **عدادات الأصول** ، ولكن لا يمكنك إضافة تسجيلات أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="8d2e7-132">إنها للحصول على نظرة عامة فقط.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-132">It's for overview only.</span></span>

<span data-ttu-id="8d2e7-133">يبين الرسم التوضيحي التالي مثالاً لصفحة **قيمة الأصول المجمعة**.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![الشكل 2](media/13-work-orders.png)

<span data-ttu-id="8d2e7-135">لاحظ النقاط التالية:</span><span class="sxs-lookup"><span data-stu-id="8d2e7-135">Note the following points:</span></span>

- <span data-ttu-id="8d2e7-136">لا يزال بإمكانك إنشاء تسجيلات يدوية لقيم العدادات لأنواع العدادات التي يتم تحديثها بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="8d2e7-137">لمزيد من المعلومات، راجع [التحديث اليدوي لعدادات الأصول](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="8d2e7-138">يمكنك إعداد عدادات مرتبطة بعداد آخر.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="8d2e7-139">في هذه الحالة، عند تحديث عداد، يتم تحديث العدادات ذات الصلة تلقائيًا في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="8d2e7-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="8d2e7-140">للحصول علي المزيد من المعلومات حول كيفية إعداد العدادات ذات الصلة، راجع [العدادات](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="8d2e7-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

