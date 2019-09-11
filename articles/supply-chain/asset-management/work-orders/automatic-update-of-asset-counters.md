---
title: التحديث التلقائي لعدادات الأصول
description: يصف هذا الموضوع التحديث التلقائي لعدادات الأصول‬ في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875490"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="36259-103">التحديث التلقائي لعدادات الأصول</span><span class="sxs-lookup"><span data-stu-id="36259-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="36259-104">في القسم السابق، تم وصف التسجيل اليدوي لعدادات الأصول.</span><span class="sxs-lookup"><span data-stu-id="36259-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="36259-105">تم وصف إعداد عدادات الأصول في [العدادات](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="36259-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="36259-106">يمكن أيضًا تحديث قيم العدادات بشكل تلقائي من تسجيلات الإنتاج، استنادًا إلى ساعات الإنتاج أو كمية الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="36259-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="36259-107">تجري هذه العملية في **تحديث عدادات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="36259-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="36259-108">يمكنك تحديث أصل واحد أو عدة أصول عن طريق إدراج معلمة واحدة، **من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="36259-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="36259-109">تحدد هذه المعلمة تاريخ بدء تسجيلات الإنتاج (الساعات أو الكمية التي تم إنتاجها)، مما يعني تاريخ البدء الذي يجب تحديث قيم العداد منه.</span><span class="sxs-lookup"><span data-stu-id="36259-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="36259-110">سيتم تضمين كافة الأصول المرتبطة بأحد الموارد *وتلك* التي لها عدادات أصول، والتي تم إعدادها ليتم تحديثها استنادًا إلى الكمية المنتجة أو ساعات الإنتاج، في تحديث تلقائي، وسيتم إنشاء قيم عدادات جديدة.</span><span class="sxs-lookup"><span data-stu-id="36259-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="36259-111">فيما يتعلق بالعدادات التي تستند إلى كميه الإنتاج، يتم تضمين الكمية الجيدة بالإضافة إلى كمية الأخطاء المسجلة في الحساب.</span><span class="sxs-lookup"><span data-stu-id="36259-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="36259-112">وإذا كانت الوحدة المستخدمة لتسجيل الكمية المنتجة مختلفة عن الوحدة المستخدمة في العداد، سيتم تحويل الكمية بحيث تتوافق مع وحدة العداد.</span><span class="sxs-lookup"><span data-stu-id="36259-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="36259-113">كما ورد أعلاه، يمكن تحديث العدادات التلقائية من تسجيلات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="36259-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="36259-114">وبالتالي، يجب أن يكون الأصل الذي تريد تحديث عداداته بشكل تلقائي مرتبطًا بمورد (الجهاز).</span><span class="sxs-lookup"><span data-stu-id="36259-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="36259-115">توفر الأوصاف التالية نظرة عامة حول إعداد أوامر الإنتاج ومعالجتها (في الوحدة النمطية **التحكم بالإنتاج**)، والتي تستخدم كأساس للتحديث التلقائي‏‎ للعدادات في الوحدة النمطية **إدارة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="36259-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="36259-116">عند تسجيل الكميات المنتجة أو ساعات الإنتاج في المورد، يمكنك تحديث عدادات الأصول المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="36259-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="36259-117">انقر فوق **إدارة‏‎ الأصول‏‎** > **دوري** > **الأصول‏‎** > **تحديث عدادات الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="36259-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="36259-118">حدد تاريخ بدء التحديث التلقائي في الحقل **من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="36259-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="36259-119">التاريخ الموجود في هذا الحقل هو تاريخ "العمل قيد التقدم" من **حركات‏‎ المسار** (**التحكم بالإنتاج‬** > **الاستعلامات والتقارير‬** > **الإنتاج‬‏‎** > **حركات‏‎ المسار** > حقل **التاريخ‏‎ الفعلي**).</span><span class="sxs-lookup"><span data-stu-id="36259-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="36259-120">إذا أردت تحديد أصول أو أنواع أصول أو موارد معينة للتحديث التلقائي، فانقر فوق **تصفية** على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**، وقم بإجراء التحديدات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="36259-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="36259-121">على علامة التبويب السريعة **تشغيل في الخلفية‬**، يمكنك إعداد التحديث التلقائي كوظيفة دفعية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="36259-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![الشكل 1](media/12-work-orders.png)

5. <span data-ttu-id="36259-123">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36259-123">Click **OK**.</span></span> <span data-ttu-id="36259-124">عند الانتهاء من التحديث التلقائي لعدادت الأصول، يمكنك رؤية تسجيلات العداد ذات الصلة بالأصل في **عدادات الأصول** (**إدارة الأصول** > **عام** > **الأصول‏‎** > **كل الأصول‏‎** > تحديد أصل > زر **العدادات**).</span><span class="sxs-lookup"><span data-stu-id="36259-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="36259-125">في **إجماليات عدادات الأصول**، يمكنك الحصول على نظرة عامة حول التسجيل الأخير الذي تم إجراؤه على جميع أنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="36259-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="36259-126">انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **قيمة الأصول المجمعة**.</span><span class="sxs-lookup"><span data-stu-id="36259-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="36259-127">طريقة العرض هذه تشبه **عدادات الأصول** إلى حد كبير، ولكن لا يمكنك إضافة تسجيلات أو تحريرها في **قيمة الأصول المجمعة**.</span><span class="sxs-lookup"><span data-stu-id="36259-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="36259-128">إنها للحصول على نظرة عامة فقط.</span><span class="sxs-lookup"><span data-stu-id="36259-128">It is for overview only.</span></span>

![الشكل 2](media/13-work-orders.png)


- <span data-ttu-id="36259-130">لا يزال من الممكن إنشاء تسجيلات يدوية لقيم العدادات لأنواع العدادات التي يتم تحديثها بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="36259-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="36259-131">لمزيد من المعلومات، راجع القسم "التحديث اليدوي لعدادات الأصول".</span><span class="sxs-lookup"><span data-stu-id="36259-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="36259-132">يمكنك إعداد العدادات المرتبطة بعداد آخر، مما يعني انه عند تحديث عداد، يتم تحديث العدادات المرتبطة بشكل تلقائي في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="36259-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="36259-133">فيما يتعلق بإعداد العدادات المرتبطة، راجع [العدادات](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="36259-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
