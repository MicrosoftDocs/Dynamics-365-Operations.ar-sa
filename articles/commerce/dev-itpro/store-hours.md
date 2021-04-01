---
title: إنشاء ساعات المتجر وتغييرها
description: يوضح هذا الموضوع كيفيه إنشاء ساعات المتجر وتحديثها في Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 00c532dfa9ceed2cda6652496d874cb82785dc7b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230630"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="5921c-103">إنشاء ساعات المتجر وتغييرها</span><span class="sxs-lookup"><span data-stu-id="5921c-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="5921c-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5921c-104">Overview</span></span>

<span data-ttu-id="5921c-105">من مكان واحد، بإمكان بائعي التجزئة إنشاء ساعات المتجر وصيانتها وإدارتها لمتاجر مختلفة عبر المناطق الجغرافية.</span><span class="sxs-lookup"><span data-stu-id="5921c-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="5921c-106">بعد ذلك، يمكن إظهار ساعات المتجر على الوحدات الطرفية لنقاط البيع (POS).</span><span class="sxs-lookup"><span data-stu-id="5921c-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="5921c-107">وبهذه الطريقة، سيتمكن أمناء الصناديق من مشاركه ساعات المتجر مع العملاء ومساعده المتسوقين الذين يهتمون بالمخزون في متاجر أخرى.</span><span class="sxs-lookup"><span data-stu-id="5921c-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="5921c-108">ويمكن أيضًا طباعه ساعات المتجر على الإيصالات، إذا احتاج العملاء إلى العودة إلى المتجر في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="5921c-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="5921c-109">يمكن تكوين العديد من ساعات المتجر عبر قنوات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="5921c-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="5921c-110">وتتضمن هذه القنوات المتاجر التقليدية ومراكز الاتصال والأجهزة المحمولة ومواقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5921c-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="5921c-111">إذا كان على العميل استلام المنتجات التي طلبها من متجر آخر، فبإمكان أمين الصندوق تحديد التواريخ التي يكون فيها استلام المنتجات متاحًا في ذلك المتجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="5921c-112">ستوفر ميزة البحث في المتجر مرجعًا إلى التواريخ وأوقات المتجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="5921c-113">بإمكان أمين الصندوق تحديد التاريخ والموقع، كما يمكنه طباعة إيصال الاستلام الذي يتضمن ساعات المتجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="5921c-114">تتوفر هذه الوظيفة في الإصدار 8.1.2 والإصدارات اللاحقة من Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="5921c-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="5921c-115">تكوين ساعات المتجر</span><span class="sxs-lookup"><span data-stu-id="5921c-115">Configure store hours</span></span>

<span data-ttu-id="5921c-116">اتبع الخطوات التالية لتكوين ساعات المتجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="5921c-117">انتقل إلى **البيع بالتجزئة والتجارة** \> **إعداد القناة** \> **ساعات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="5921c-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="5921c-118">حدد **جديد** لإنشاء قالب جديد لساعات المتجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="5921c-119">لاستخدام قالب موجود، حدد القالب في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="5921c-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="5921c-120">في مربع الحوار‏‎ **إضافة نطاق**، حدد نطاق التاريخ وساعات المتجر وأيام العطل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5921c-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="5921c-121">إذا لم تكن ساعات المتجر عرضة للتغير، فحدد **لا تنتهي أبدًا** في حقل **تاريخ الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="5921c-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="5921c-122">إذا كانت ساعات المتجر خاصة بشهر أو أسبوع أو يوم محدد، فعليك تعيين التواريخ في الحقلين **تاريخ البدء** و **تاريخ الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="5921c-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5921c-123">يمكنك إنشاء قوالب متعددة ذات تواريخ بدء وانتهاء متراكبة.</span><span class="sxs-lookup"><span data-stu-id="5921c-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="5921c-124">وبالتالي، يمكنك، على سبيل المثال، تحديد ساعات المتجر لمتاجر في مناطق زمنية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="5921c-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="5921c-125">![إضافة مربع حوار نطاق](../dev-itpro/media/Storehours1.png "إضافة مربع حوار نطاق")</span><span class="sxs-lookup"><span data-stu-id="5921c-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="5921c-126">اربط قالب ساعات المتجر بالمتاجر حيث سيتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="5921c-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="5921c-127">في مربع الحوار **اختيار عُقد المؤسسة‬**، حدد المتاجر والمناطق والمؤسسات التي يجب ربط القالب بها.</span><span class="sxs-lookup"><span data-stu-id="5921c-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="5921c-128">يمكن ربط قالب ساعات متجر واحد بكل متجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="5921c-129">استخدم أزرار الأسهم لتحديد المتاجر أو المناطق أو المؤسسات.</span><span class="sxs-lookup"><span data-stu-id="5921c-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="5921c-130">سيكون التقويم متاحًا للمتاجر أو لمجموعات المتاجر، سيكون مرئيًا عند نقطة البيع كمرجع.</span><span class="sxs-lookup"><span data-stu-id="5921c-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="5921c-131">![اختيار مربع حوار عُقد المؤسسة](../dev-itpro/media/Storehours2.png "اختيار مربع حوار عُقد المؤسسة")</span><span class="sxs-lookup"><span data-stu-id="5921c-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="5921c-132">في صفحة **جدول التوزيع‬**، شغّل الوظيفتين **1070** و **1090** لجعل ساعات المتجر متوفرة لنقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="5921c-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="5921c-133">إضافة ساعات المتجر إلى إيصالات مطبوعة</span><span class="sxs-lookup"><span data-stu-id="5921c-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="5921c-134">اتبع الخطوات التالية لإضافة ساعات المتجر إلى إيصالات المطبوعة لنقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="5921c-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="5921c-135">افتح مصمم الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="5921c-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="5921c-136">حدد **التذييل** في الركن الأيمن السفلي.</span><span class="sxs-lookup"><span data-stu-id="5921c-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="5921c-137">اسحب عنصر‏‎ **ساعات المتجر** من الجزء الأيمن إلى التذييل الموجود في أسفل قالب الإيصال.</span><span class="sxs-lookup"><span data-stu-id="5921c-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="5921c-138">يمكنك تحرير التسمية الافتراضية في عنصر **ساعات المتجر** كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="5921c-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="5921c-139">احفظ الإيصال وأغلق مصمم الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="5921c-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="5921c-140">في صفحة **جدول التوزيع**، شغّل الوظيفتين **1070** و **1090**.</span><span class="sxs-lookup"><span data-stu-id="5921c-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="5921c-141">سجل الدخول إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="5921c-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="5921c-142">أكمل عملية البيع، ثم اختر طباعة الإيصال.</span><span class="sxs-lookup"><span data-stu-id="5921c-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="5921c-143">تتضمن إيصالات نقطة البيع الآن ساعات المتجر.</span><span class="sxs-lookup"><span data-stu-id="5921c-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="5921c-144">إذا تم تضمين أي أيام عطل في القالب، فستظهر على الإيصال.</span><span class="sxs-lookup"><span data-stu-id="5921c-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="5921c-145">![مثال على الإيصال](../dev-itpro/media/Storehours3.png "مثال على الإيصال")</span><span class="sxs-lookup"><span data-stu-id="5921c-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]