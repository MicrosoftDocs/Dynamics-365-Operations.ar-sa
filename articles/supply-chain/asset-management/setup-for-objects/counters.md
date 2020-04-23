---
title: قياسات الأصول
description: يشرح هذا الموضوع كيفية إنشاء أنواع قياسات الأصول في إدارة الأصول.
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
ms.openlocfilehash: d128a7d20891353927441bb343831876d72aecbe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208882"
---
# <a name="counters"></a><span data-ttu-id="04253-103">العدادات</span><span class="sxs-lookup"><span data-stu-id="04253-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04253-104">يشرح هذا الموضوع كيفية إنشاء أنواع العدادات في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="04253-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="04253-105">تُستخدم أنواع العدادات لإجراء تسجيلات العدادات على الأصول، على سبيل المثال، فيما يتعلق بعدد ساعات الإنتاج، أو الكمية المنتجة على الأصل.</span><span class="sxs-lookup"><span data-stu-id="04253-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="04253-106">ترتبط أنواع الأصول بأنواع العدادات.</span><span class="sxs-lookup"><span data-stu-id="04253-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="04253-107">وهذا يعني أنه لا يمكن استخدام العداد على أحد الأصول إلا إذا تم إعداد العداد على نوع الأصل المستخدم في الأصل.</span><span class="sxs-lookup"><span data-stu-id="04253-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="04253-108">قبل أن تتمكن من إجراء تسجيلات العدادات على الأصول، تقوم أولاً بإنشاء أنواع العدادات التي تريد استخدامها في **العدادات**.</span><span class="sxs-lookup"><span data-stu-id="04253-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="04253-109">بعد ذلك، يمكنك إنشاء تسجيلات العدادات على الأصول في **العدادات**.</span><span class="sxs-lookup"><span data-stu-id="04253-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="04253-110">يمكن استخدام العدادات في خطط الصيانة.</span><span class="sxs-lookup"><span data-stu-id="04253-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="04253-111">بإمكان بند خطة الصيانة أن يكون من نوع "العداد"، على سبيل المثال، فيما يتعلق بعدد ساعات الإنتاج أو الكمية المنتجة.</span><span class="sxs-lookup"><span data-stu-id="04253-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="04253-112">ويمكن تحديث تسجيل العداد يدويًا أو تلقائيًا استنادًا إلى ساعات الإنتاج أو الكمية المنتجة.</span><span class="sxs-lookup"><span data-stu-id="04253-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="04253-113">يمكن إعداد العداد لاستخدام إحدى طرق التحديث الثلاث (محددة في الحقل **تحديث** في **العدادات**):</span><span class="sxs-lookup"><span data-stu-id="04253-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="04253-114">يدوي - يجب تسجيل قيم العداد يدويًا.</span><span class="sxs-lookup"><span data-stu-id="04253-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="04253-115">ساعات الإنتاج - يتم تحديث العداد تلقائيًا استنادًا إلى عدد ساعات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="04253-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="04253-116">كمية الإنتاج - يتم تحديث العداد تلقائيًا استنادًا إلى كميات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="04253-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="04253-117">إذا تم استخدام الكمية المنتجة، فسيتم تضمين *جميع* الأصناف المسجلة في تسجيلات العداد، الكمية الجيدة بالإضافة إلى الكمية التي تتضمن أخطاء.</span><span class="sxs-lookup"><span data-stu-id="04253-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="04253-118">من الممكن دائمًا إجراء تسجيلات يدوية للعداد، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="04253-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="04253-119">إنشاء أنواع عدادات لتسجيلات عدادات الأصول</span><span class="sxs-lookup"><span data-stu-id="04253-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="04253-120">حدد **إدارة الأصول** > **الإعداد** > **أنواع‏‎ الأصول** > **العدادات‏‎**.</span><span class="sxs-lookup"><span data-stu-id="04253-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="04253-121">حدد **جديد** لإنشاء نوع عداد جديد.</span><span class="sxs-lookup"><span data-stu-id="04253-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="04253-122">أدخل معرفًا في حقل **العداد** واسم عداد في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="04253-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="04253-123">على علامة التبويب السريعة **عام** ، حدد وحدة العداد في حقل **الوحدة** .</span><span class="sxs-lookup"><span data-stu-id="04253-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="04253-124">في الحقل‏‎ **تحديث** ، حدد طريقة التحديث المراد استخدامها للعداد.</span><span class="sxs-lookup"><span data-stu-id="04253-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="04253-125">حدد "نعم" على زر التبديل **توارث قيم العداد** إذا كان يجب على الأصول التابعة في بنية الأصول أن ترث بشكل تلقائي تسجيلات العداد التي تم إجراؤها على الأصل الأساسي.</span><span class="sxs-lookup"><span data-stu-id="04253-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="04253-126">في حقل **إجمالي المجموع‬** ، حدد طريقة التجميع المراد استخدامها للعداد باستخدام نوع العداد هذا.</span><span class="sxs-lookup"><span data-stu-id="04253-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="04253-127">التحديد القياسي المستخدم لإضافة قيم مسجلة باستمرار إلى القيمة الإجمالية هو "الجمع".</span><span class="sxs-lookup"><span data-stu-id="04253-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="04253-128">يمكن استخدام "المتوسط" إذا تم إعداد العداد لمراقبة حد، على سبيل المثال، فيما يتعلق بدرجة الحرارة أو الاهتزازات أو تآكل الأصل نتيجة الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="04253-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="04253-129">في الحقل **انحراف لأعلى‬** ، أدخل المستوى الأعلى بالنسبة المئوية للتحقق مما إذا كانت تسجيلات العداد اليدوية ضمن نطاق متوقع.</span><span class="sxs-lookup"><span data-stu-id="04253-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="04253-130">تستند عملية التحقق من الصحة إلى زيادة خطية في تسجيلات العداد الموجودة.</span><span class="sxs-lookup"><span data-stu-id="04253-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="04253-131">في الحقل **انحراف تحت‬** ، أدخل المستوى الأقل بالنسبة المئوية للتحقق مما إذا كانت تسجيلات العداد اليدوية ضمن نطاق متوقع.</span><span class="sxs-lookup"><span data-stu-id="04253-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="04253-132">تستند عملية التحقق من الصحة إلى انخفاض خطي في تسجيلات العداد الموجودة.</span><span class="sxs-lookup"><span data-stu-id="04253-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="04253-133">في حقل **النوع** ، حدد نوع الرسالة (معلومات، تحذير، خطأ) التي سيتم عرضها في حالة حدوث انحرافات خارج النطاق المحدد عند إجراء تسجيلات العداد اليدوية.</span><span class="sxs-lookup"><span data-stu-id="04253-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="04253-134">على علامة التبويب السريعة **أنواع الأصول** ، أضف أنواع الأصول التي يجب أن تكون قادرة على استخدام العداد.</span><span class="sxs-lookup"><span data-stu-id="04253-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="04253-135">على علامة التبويب السريعة **عدادات الأصل ذات الصلة** ، أضف العداد الذي تريد تحديثه تلقائيًا عند تحديث هذا العداد.</span><span class="sxs-lookup"><span data-stu-id="04253-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="04253-136">لا يتم تحديث العداد ذو الصلة تلقائيًا إلا إذا كان العداد ذو الصلة يحتوي على نوع الأصل، الذي يرتبط به، في إعداد العداد.</span><span class="sxs-lookup"><span data-stu-id="04253-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="04253-137">على سبيل المثال: يمكنك إعداد العداد "لساعات الإنتاج" وإضافة نوع الأصل "محرك الشاحنة".</span><span class="sxs-lookup"><span data-stu-id="04253-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="04253-138">وعندما يتم تحديث هذا العداد، يتم أيضًا تحديث عداد "الزيت" ذي الصلة بنفس قيم العداد.</span><span class="sxs-lookup"><span data-stu-id="04253-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="04253-139">يتضمن الإعداد في **العدادات** الإعداد على "الساعات".</span><span class="sxs-lookup"><span data-stu-id="04253-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="04253-140">كذلك الأمر، يجب إضافة نوع الأصل "محرك الشاحنة" على عداد "الزيت" إلى علامة التبويب السريعة **أنواع الأصول** لضمان علاقة العداد.</span><span class="sxs-lookup"><span data-stu-id="04253-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="04253-141">راجع لقطات الشاشة أدناه للحصول على مثال على الإعداد على عدادات "الساعات" و"الزيت".</span><span class="sxs-lookup"><span data-stu-id="04253-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="04253-142">عند إضافة أنواع الأصول إلى نوع العداد في **العدادات**، يُضاف هذا العداد تلقائيًا إلى أنواع الأصول على علامة التبويب السريعة **العدادات** في [أنواع الأصول](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="04253-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![الشكل 1](media/071-setup-for-objects.png)

