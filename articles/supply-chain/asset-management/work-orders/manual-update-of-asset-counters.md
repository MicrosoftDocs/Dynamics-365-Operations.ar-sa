---
title: التحديث اليدوي لعدادات الأصول
description: يصف هذا الموضوع التحديث اليدوي لعدادات الأصول‬ في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421186"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="0e281-103">التحديث اليدوي لعدادات الأصول</span><span class="sxs-lookup"><span data-stu-id="0e281-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0e281-104">تُستخدم العدادات لإنشاء تسجيلات في أحد الأصول، مثل التسجيلات الخاصة بعدد الساعات التي تم فيها تشغيل الأصل أو الكمية التي تم إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="0e281-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="0e281-105">قد يكون نوع العداد المحدد للعداد معينًا ليرث قيم العدادات.</span><span class="sxs-lookup"><span data-stu-id="0e281-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="0e281-106">بمعني آخر، يتم تعيين الخيار **توارث قيم عداد الأصول** إلى **نعم** في علامة التبويب السريع **عام** في صفحة **العدادات** (**إدارة الأصول** > **إعداد** > **أنواع الأصول** > **العدادات**).</span><span class="sxs-lookup"><span data-stu-id="0e281-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="0e281-107">في هذه الحالة، عند إنشاء بند عداد جديد من هذا النوع، يتم تحديث كل أصل تابع يستخدم نفس نوع العداد تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="0e281-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="0e281-108">في صفحة **كافة الأصول** ، يمكنك إنشاء تسجيلات العداد للساعات أو الكميات على أصل ما استنادًا إلى قراءاتك على الأصل.</span><span class="sxs-lookup"><span data-stu-id="0e281-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="0e281-109">حدد **إدارة الأصول** > **مشترك** > **الأصول** > **كافة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="0e281-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="0e281-110">حدد الأصل، ثم في جزء الإجراء، ضمن علامة التبويب **الأصل** ، في مجموعة **الوقائي** ، حدد **عدادات**.</span><span class="sxs-lookup"><span data-stu-id="0e281-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="0e281-111">تظهر الصفحة **عدادات الأصول** قائمة بجميع تسجيلات العدادات السابقة التي تم إجراؤها على الأصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e281-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="0e281-112">حدد **جديد** لإنشاء التسجيل.</span><span class="sxs-lookup"><span data-stu-id="0e281-112">Select **New** to create a registration.</span></span> <span data-ttu-id="0e281-113">يتم إدخال الاسم تلقائيًا في حقل **الأصل**.</span><span class="sxs-lookup"><span data-stu-id="0e281-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="0e281-114">في حقل **العداد**، حدد العداد المناسب.</span><span class="sxs-lookup"><span data-stu-id="0e281-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="0e281-115">لا تتوفر سوى العدادات المرتبطة بنوع الأصل المحدد في الأصل.</span><span class="sxs-lookup"><span data-stu-id="0e281-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="0e281-116">يتم إدخال الوحدة ذات الصلة بشكل تلقائي في حقل **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="0e281-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="0e281-117">في الحقل **مُسجل** ، حدد التاريخ والوقت الخاصين بتسجيل العداد.</span><span class="sxs-lookup"><span data-stu-id="0e281-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="0e281-118">في حقل **القيمة** ، ادخل الرقم منذ آخر تسجيل للعداد.</span><span class="sxs-lookup"><span data-stu-id="0e281-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="0e281-119">وبدلاً من ذلك، ادخل إجمالي العدد في حقل **القيمة المجمعة** .</span><span class="sxs-lookup"><span data-stu-id="0e281-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="0e281-120">لاحظ النقاط التالية:</span><span class="sxs-lookup"><span data-stu-id="0e281-120">Note the following points:</span></span>

- <span data-ttu-id="0e281-121">إذا قمت بتثبيت عداد جديد بشكل فعلي على أصل ما، فيجب تسجيل التغيير على الأصل في صفحة **عدادات‏‎ الأصول**.</span><span class="sxs-lookup"><span data-stu-id="0e281-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="0e281-122">بعد ذلك، يجب أن تقوم بإنشاء اثنين من بنود التسجيل التي تحتوي على طوابع زمنيه متماثلة.</span><span class="sxs-lookup"><span data-stu-id="0e281-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="0e281-123">يجب أن يكون البند الأول للعداد الذي تقوم باستبداله.</span><span class="sxs-lookup"><span data-stu-id="0e281-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="0e281-124">في البند المرتبط بالعداد الجديد، حدد خانه الاختيار **إعادة تعيين العداد** .</span><span class="sxs-lookup"><span data-stu-id="0e281-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="0e281-125">في حقل **الإجماليات** ، يتطابق العدد الإجمالي مع مجموع إجماليات العداد لكافة القيم المسجلة في نوع هذا العداد.</span><span class="sxs-lookup"><span data-stu-id="0e281-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="0e281-126">إذا تم تحديد خانة الاختيار **إعادة تعيين العداد** على أحد الأصول باستخدام خطة الصيانة التي يكون نوع الفترة الزمنية الخاص بها "مرة واحدة من..." أو "عند الوصول..."، يظل العداد نشطًا على بند العداد الجديد لأنك قمت بإنشاء بند عداد منفصل وبدأت من جديد باستخدام عداد جديد.</span><span class="sxs-lookup"><span data-stu-id="0e281-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="0e281-127">يبين الرسم التوضيحي التالي مثالاً لصفحة **عدادات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="0e281-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![الشكل 1](media/11-work-orders.png)

<span data-ttu-id="0e281-129">في الصفحة **عدادات الأصول** (**إدارة الأصول** > **استعلامات** > **الأصول** > **عدادات الأصول**)، يمكنك إجراء تسجيلات العداد في العديد من الأصول في نفس الوقت، كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="0e281-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="0e281-130">يمكنك إعداد نطاق لتحديد الانحرافات في تسجيلات العداد يدويًا.</span><span class="sxs-lookup"><span data-stu-id="0e281-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="0e281-131">يمكنك أيضًا تحديد نوع الرسالة التي يتم عرضها في حالة ما إذا كانت التسجيلات خارج النطاق المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e281-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="0e281-132">للحصول على المزيد من المعلومات حول كيفية إعداد العدادات، راجع [العدادات](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="0e281-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

