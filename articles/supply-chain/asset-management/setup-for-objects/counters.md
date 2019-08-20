---
title: قياسات الأصول
description: يشرح هذا الموضوع كيفية إنشاء أنواع قياسات الأصول في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783049"
---
# <a name="asset-measures"></a><span data-ttu-id="3df7f-103">قياسات الأصول</span><span class="sxs-lookup"><span data-stu-id="3df7f-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3df7f-104">يشرح هذا الموضوع كيفية إنشاء أنواع قياسات الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="3df7f-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="3df7f-105">تُستخدم أنواع قياسات الأصول لإجراء تسجيلات القياسات على الأصول، على سبيل المثال، فيما يتعلق بعدد ساعات الإنتاج، أو الكمية المنتجة على الأصل.</span><span class="sxs-lookup"><span data-stu-id="3df7f-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="3df7f-106">ترتبط أنواع الأصول بأنواع قياسات الأصول.</span><span class="sxs-lookup"><span data-stu-id="3df7f-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="3df7f-107">وهذا يعني أنه لا يمكن استخدام قياس الأصل على أحد الأصول إلا إذا تم إعداد قياس الأصل على نوع الأصل المستخدم في الأصل.</span><span class="sxs-lookup"><span data-stu-id="3df7f-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="3df7f-108">قبل أن تتمكن من إجراء تسجيلات القياسات على الأصول، تقوم أولاً إنشاء أنواع قياسات الأصول التي تريد استخدامها في **العدادات**.</span><span class="sxs-lookup"><span data-stu-id="3df7f-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="3df7f-109">بعد ذلك، يمكنك إنشاء تسجيلات القياسات على الأصول في **قياسات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="3df7f-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="3df7f-110">يمكن استخدام قياسات الأصول في خطط الصيانة.</span><span class="sxs-lookup"><span data-stu-id="3df7f-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="3df7f-111">بإمكان بند خطة الصيانة أن يكون من نوع "العداد"، على سبيل المثال، فيما يتعلق بعدد ساعات الإنتاج أو الكمية المنتجة.</span><span class="sxs-lookup"><span data-stu-id="3df7f-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="3df7f-112">ويمكن تحديث تسجيل قياس الأصول يدويًا أو تلقائيًا استنادًا إلى ساعات الإنتاج أو الكمية المنتجة.</span><span class="sxs-lookup"><span data-stu-id="3df7f-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="3df7f-113">يمكن إعداد قياس الأصل لاستخدام إحدى طرق التحديث الثلاث (محددة في الحقل **تحديث** في **العدادات**):</span><span class="sxs-lookup"><span data-stu-id="3df7f-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="3df7f-114">يدوي - يجب تسجيل قيم قياس الأصول يدويًا.</span><span class="sxs-lookup"><span data-stu-id="3df7f-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="3df7f-115">ساعات الإنتاج - يتم تحديث العداد تلقائيًا استنادًا إلى عدد ساعات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3df7f-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="3df7f-116">كمية الإنتاج - يتم تحديث العداد تلقائيًا استنادًا إلى كميات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3df7f-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="3df7f-117">إذا تم استخدام الكمية المنتجة، فسيتم تضمين *جميع* الأصناف المسجلة في تسجيلات القياس، الكمية الجيدة بالإضافة إلى الكمية التي تتضمن أخطاء.</span><span class="sxs-lookup"><span data-stu-id="3df7f-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="3df7f-118">من الممكن دائمًا إجراء تسجيلات يدوية لقياس الأصول، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="3df7f-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="3df7f-119">إنشاء أنواع عدادات لتسجيلات عدادات الأصول</span><span class="sxs-lookup"><span data-stu-id="3df7f-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="3df7f-120">حدد **إدارة الأصول** > **الإعداد** > **أنواع‏‎ الأصول** > **العدادات‏‎**.</span><span class="sxs-lookup"><span data-stu-id="3df7f-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="3df7f-121">حدد **جديد** لإنشاء نوع قياس أصول جديد.</span><span class="sxs-lookup"><span data-stu-id="3df7f-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="3df7f-122">أدخل معرفًا في حقل **العداد** واسم عداد في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="3df7f-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="3df7f-123">على علامة التبويب السريعة **عام**، حدد وحدة قياس في حقل **الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="3df7f-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="3df7f-124">في الحقل‏‎ **تحديث**، حدد طريقة التحديث المراد استخدامها لقياس الأصل.</span><span class="sxs-lookup"><span data-stu-id="3df7f-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="3df7f-125">حدد "نعم" على زر التبديل **توارث قيم العداد** إذا كان يجب على الأصول التابعة في بنية أصول أن ترث بشكل تلقائي تسجيلات قياسات الأصول التي تم إجراؤها على الأصل الأساسي.</span><span class="sxs-lookup"><span data-stu-id="3df7f-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="3df7f-126">في حقل **إجمالي المجموع‬**، حدد طريقة الجمع المراد استخدامها لقياس أصل باستخدام نوع قياس الأصل هذا.</span><span class="sxs-lookup"><span data-stu-id="3df7f-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="3df7f-127">التحديد القياسي المستخدم لإضافة قيم مسجلة باستمرار إلى القيمة الإجمالية هو "الجمع".</span><span class="sxs-lookup"><span data-stu-id="3df7f-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="3df7f-128">يمكن استخدام "المتوسط" إذا تم إعداد قياس الأصل لمراقبة حد، على سبيل المثال، فيما يتعلق بدرجة الحرارة أو الاهتزازات أو تآكل الأصل نتيجة الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="3df7f-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="3df7f-129">في الحقل **انحراف أعلى‬**، أدخل المستوى الأعلى بالنسبة المئوية للتحقق مما إذا كانت تسجيلات قياس الأصول اليدوية ضمن نطاق متوقع.</span><span class="sxs-lookup"><span data-stu-id="3df7f-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="3df7f-130">تستند عملية التحقق من الصحة إلى زيادة خطية في تسجيلات قياسات الأصول الموجودة.</span><span class="sxs-lookup"><span data-stu-id="3df7f-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="3df7f-131">في الحقل **انحراف تحت‬‬**، أدخل المستوى الأدنى بالنسبة المئوية للتحقق مما إذا كانت تسجيلات قياس الأصول اليدوية ضمن نطاق متوقع.</span><span class="sxs-lookup"><span data-stu-id="3df7f-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="3df7f-132">تستند عملية التحقق من الصحة إلى انخفاض خطي في تسجيلات قياسات الأصول الموجودة.</span><span class="sxs-lookup"><span data-stu-id="3df7f-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="3df7f-133">في حقل **النوع**، حدد نوع الرسالة (معلومات، تحذير، خطأ) التي سيتم عرضها في حالة حدوث انحرافات خارج النطاق المحدد عند إجراء تسجيلات قياسات أصول يدوية.</span><span class="sxs-lookup"><span data-stu-id="3df7f-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="3df7f-134">على علامة التبويب السريعة **أنواع الأصول**، أضف أنواع الأصول التي يجب أن تكون قادرة على استخدام مقياس الأصول.</span><span class="sxs-lookup"><span data-stu-id="3df7f-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="3df7f-135">على علامة التبويب السريعة **قياسات الأصل ذات الصلة**، أضف قياسات الأصول التي تريد تحديثها تلقائيًا عند تحديث قياس الأصل هذا.</span><span class="sxs-lookup"><span data-stu-id="3df7f-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="3df7f-136">لا يتم تحديث قياس الأصل المرتبط تلقائيًا إلا إذا كان قياس الأصل ذا الصلة يحتوي على نوع الأصل، الذي يرتبط به، في إعداد قياس الأصل.</span><span class="sxs-lookup"><span data-stu-id="3df7f-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="3df7f-137">على سبيل المثال: يمكنك إعداد قياس أصل "لساعات الإنتاج" وإضافة نوع الأصل "محرك الشاحنة".</span><span class="sxs-lookup"><span data-stu-id="3df7f-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="3df7f-138">وعندما يتم تحديث قياس الأصل هذا، يتم أيضًا تحديث عداد ذي صلة "الزيت" بنفس قيم قياس الأصول.</span><span class="sxs-lookup"><span data-stu-id="3df7f-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="3df7f-139">يتضمن الإعداد في **العدادات** الإعداد على "الساعات".</span><span class="sxs-lookup"><span data-stu-id="3df7f-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="3df7f-140">كذلك الأمر، يجب إضافة نوع الأصل "محرك الشاحنة" على قياس الأصل "الزيت" إلى علامة التبويب السريعة **أنواع الأصول** لضمان علاقة قياسات الأصول.</span><span class="sxs-lookup"><span data-stu-id="3df7f-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="3df7f-141">راجع لقطات الشاشة أدناه للحصول على مثال على الإعداد على قياسات الأصول "الساعات" و"الزيت".</span><span class="sxs-lookup"><span data-stu-id="3df7f-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="3df7f-142">عند إضافة أنواع الأصول إلى نوع قياس أصل في **العدادات**، يُضاف قياس الأصل هذا تلقائيًا إلى أنواع الأصول على علامة التبويب السريعة **العدادات** في [أنواع الأصول](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="3df7f-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![الشكل 1](media/071-setup-for-objects.png)


