---
title: الشروع في العمل مع خدمة محاسبة التكاليف
description: يوفر هذا الموضوع تفاصيل الترخيص وتعليمات التثبيت لخدمة محاسبة التكاليف.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276884"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="6bfda-103">الشروع في العمل مع خدمة محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="6bfda-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="6bfda-104">تتوفر الوظائف الموضحة في هذا الموضوع كجزء من إصدار معاينة خاص.</span><span class="sxs-lookup"><span data-stu-id="6bfda-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="6bfda-105">تخضع محتويات هذا الموضوع والوظائف الموضحة للتغيير.</span><span class="sxs-lookup"><span data-stu-id="6bfda-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="6bfda-106">للحصول على مزيد من المعلومات حول إصدارات المعاينة، راجع [الأسئلة المتداولة حول تحديثات خدمة إصدار واحد](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="6bfda-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="6bfda-107">تتيح لك خدمة محاسبة التكاليف إجراء محاسبة متعددة للمخزون في دفاتر الأستاذ العام لمحاسبة التكاليف التي قمت بإعدادها.</span><span class="sxs-lookup"><span data-stu-id="6bfda-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="6bfda-108">يمكنك إقران كل دفتر أستاذ لمحاسبة التكاليف بـ *اصطلاح*.</span><span class="sxs-lookup"><span data-stu-id="6bfda-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="6bfda-109">والاصطلاح هو مجموعة من الأنواع التالية من سياسات المحاسبة:</span><span class="sxs-lookup"><span data-stu-id="6bfda-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="6bfda-110">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="6bfda-110">Cost object</span></span>
- <span data-ttu-id="6bfda-111">أساس قياس الإدخال</span><span class="sxs-lookup"><span data-stu-id="6bfda-111">Input measurement basis</span></span>
- <span data-ttu-id="6bfda-112">افتراض تدفق التكلفة</span><span class="sxs-lookup"><span data-stu-id="6bfda-112">Cost flow assumption</span></span>
- <span data-ttu-id="6bfda-113">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="6bfda-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="6bfda-114">حتى بعد تشغيل خدمة محاسبة التكاليف، ما يزال بإمكانك إجراء محاسبة المخزون في Microsoft Dynamics 365 Supply Chain Management، كما هو معتاد.</span><span class="sxs-lookup"><span data-stu-id="6bfda-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="6bfda-115">تعد خدمة محاسبة التكاليف وظيفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="6bfda-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="6bfda-116">ولجعل ميزاتها متوفرة، يجب أن تثبتها من Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6bfda-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6bfda-117">بالتالي، يمكنك اختيار تقييمها في بيئة اختبار قبل تشغيلها في بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6bfda-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="6bfda-118">خدمة محاسبة التكاليف لا تدعم حاليًا كافة ميزات إدارة التكلفة المدمجة في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6bfda-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6bfda-119">بالتالي، من المهم أن تجري تقييمًا بشأن ما إذا كانت مجموعة الميزات المتوفرة حاليًا ستلبي متطلباتك أم لا.</span><span class="sxs-lookup"><span data-stu-id="6bfda-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="6bfda-120">الترخيص</span><span class="sxs-lookup"><span data-stu-id="6bfda-120">Licensing</span></span>

<span data-ttu-id="6bfda-121">يجري ترخيص خدمة محاسبة التكاليف معًا مع الميزات القياسية لمحاسبة المخزون المتوفرة لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6bfda-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="6bfda-122">لا يتعين عليك شراء ترخيص إضافي لاستخدام خدمة محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="6bfda-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="6bfda-123">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="6bfda-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bfda-124">لاستخدام خدمة محاسبة التكاليف، يجب أن يكون لديك بيئة عالية الاتاحة تم تمكين LCS عليها (ليس بيئة OneBox)، ويجب أن يتم تشغيل Dynamics 365 Supply Chain Management الإصدار 10.0.11 أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="6bfda-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="6bfda-125">لاستخدام خدمة محاسبة التكاليف، قم بتثبيت الوظيفة الإضافية لخدمة محاسبة التكاليف لـ Supply Chain Management كما هو موضح في الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="6bfda-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="6bfda-126">سجل الدخول إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="6bfda-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="6bfda-127">انتقل إلى **إدارة ميزة المعاينة**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="6bfda-128">حدد علامة الزائد (**+**).</span><span class="sxs-lookup"><span data-stu-id="6bfda-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="6bfda-129">في حقل **الرمز**، أدخل مفتاح بيتا للوظيفة الإضافية لخدمة محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="6bfda-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="6bfda-130">(ينبغي أن تكون استلمت المفتاح الخاص بك بواسطة البريد الإلكتروني.)</span><span class="sxs-lookup"><span data-stu-id="6bfda-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="6bfda-131">حدد **إلغاء الحظر**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="6bfda-132">افتح بيئة LCS حيث تريد إضافة الخدمة بها.</span><span class="sxs-lookup"><span data-stu-id="6bfda-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="6bfda-133">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="6bfda-134">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="6bfda-135">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="6bfda-136">حدد **خدمة محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="6bfda-137">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="6bfda-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="6bfda-138">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-138">Select **Install**.</span></span>

1. <span data-ttu-id="6bfda-139">في علامة التبويب السريعة **الوظائف الإضافية للبيئة**، يجب أن تشاهد خدمة محاسبة التكاليف قد تم تثبيتها.</span><span class="sxs-lookup"><span data-stu-id="6bfda-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="6bfda-140">بعد بضع دقائق، يجب أن تغير الحالة من **قيد التثبيت** إلى **مثبت**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="6bfda-141">(قد تحتاج إلى تحديث الصفحة لعرض هذا التغيير.) في تلك النقطة، تكون خدمة محاسبة التكاليف جاهزة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="6bfda-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="6bfda-142">إعداد التكامل</span><span class="sxs-lookup"><span data-stu-id="6bfda-142">Set up the integration</span></span>

<span data-ttu-id="6bfda-143">لإعداد التكامل بين خدمة محاسبة الكاليف و Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="6bfda-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="6bfda-144">انتقل إلى **إدارة النظام > إدارة الميزات**</span><span class="sxs-lookup"><span data-stu-id="6bfda-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="6bfda-145">حدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="6bfda-146">افتح علامة تبويب **الكل** وابحث عن الميزة التي تسمى *خدمة محاسبة التكاليف*.</span><span class="sxs-lookup"><span data-stu-id="6bfda-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="6bfda-147">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="6bfda-148">انتقل إلى **إدارة التكاليف > خدمة محاسبة التكاليف > الإعداد > معلمات خدمة محاسبة التكاليف > معلمات التكاملات**.</span><span class="sxs-lookup"><span data-stu-id="6bfda-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="6bfda-149">في حقل **معرف التطبيق**، أدخل الرمز التالي:</span><span class="sxs-lookup"><span data-stu-id="6bfda-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="6bfda-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="6bfda-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="6bfda-151">في حقل **نقطة نهاية خدمة البيانات**، أدخل عنوان URL التالي:</span><span class="sxs-lookup"><span data-stu-id="6bfda-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="6bfda-152">في حقل **نقطة نهاية خدمة محاسبة التكاليف**، أدخل عنوان URL التالي:</span><span class="sxs-lookup"><span data-stu-id="6bfda-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="6bfda-153">الآن خدمة محاسبة التكاليف جاهزة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="6bfda-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="6bfda-154">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="6bfda-154">Related resources</span></span>

[<span data-ttu-id="6bfda-155">الصفحة الرئيسية لخدمة محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="6bfda-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
