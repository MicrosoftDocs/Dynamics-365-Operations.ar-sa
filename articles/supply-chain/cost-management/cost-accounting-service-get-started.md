---
title: الشروع في العمل مع خدمة محاسبة التكاليف (معاينة خاصة)
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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1f602116edabc424b6cbee541e268df017912d3c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011837"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="5834d-103">الشروع في العمل مع خدمة محاسبة التكاليف (معاينة خاصة)</span><span class="sxs-lookup"><span data-stu-id="5834d-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="5834d-104">تتوفر الوظائف الموضحة في هذا الموضوع كجزء من إصدار معاينة خاص.</span><span class="sxs-lookup"><span data-stu-id="5834d-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="5834d-105">تخضع محتويات هذا الموضوع والوظائف الموضحة للتغيير.</span><span class="sxs-lookup"><span data-stu-id="5834d-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="5834d-106">للحصول على مزيد من المعلومات حول إصدارات المعاينة، راجع [الأسئلة المتداولة حول تحديثات خدمة إصدار واحد](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="5834d-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="5834d-107">تتيح لك خدمة محاسبة التكاليف إجراء محاسبة متعددة للمخزون في دفاتر الأستاذ العام لمحاسبة التكاليف التي قمت بإعدادها.</span><span class="sxs-lookup"><span data-stu-id="5834d-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="5834d-108">يمكنك إقران كل دفتر أستاذ لمحاسبة التكاليف بـ *اصطلاح*.</span><span class="sxs-lookup"><span data-stu-id="5834d-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="5834d-109">والاصطلاح هو مجموعة من الأنواع التالية من سياسات المحاسبة:</span><span class="sxs-lookup"><span data-stu-id="5834d-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="5834d-110">كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="5834d-110">Cost object</span></span>
- <span data-ttu-id="5834d-111">أساس قياس الإدخال</span><span class="sxs-lookup"><span data-stu-id="5834d-111">Input measurement basis</span></span>
- <span data-ttu-id="5834d-112">افتراض تدفق التكلفة</span><span class="sxs-lookup"><span data-stu-id="5834d-112">Cost flow assumption</span></span>
- <span data-ttu-id="5834d-113">عنصر التكلفة</span><span class="sxs-lookup"><span data-stu-id="5834d-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="5834d-114">حتى بعد تشغيل خدمة محاسبة التكاليف، ما يزال بإمكانك إجراء محاسبة المخزون في Microsoft Dynamics 365 Supply Chain Management، كما هو معتاد.</span><span class="sxs-lookup"><span data-stu-id="5834d-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="5834d-115">تعد خدمة محاسبة التكاليف وظيفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="5834d-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="5834d-116">ولجعل ميزاتها متوفرة، يجب أن تثبتها من Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5834d-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5834d-117">بالتالي، يمكنك اختيار تقييمها في بيئة اختبار قبل تشغيلها في بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="5834d-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="5834d-118">خدمة محاسبة التكاليف لا تدعم حاليًا كافة ميزات إدارة التكلفة المدمجة في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5834d-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5834d-119">بالتالي، من المهم أن تجري تقييمًا بشأن ما إذا كانت مجموعة الميزات المتوفرة حاليًا ستلبي متطلباتك أم لا.</span><span class="sxs-lookup"><span data-stu-id="5834d-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="5834d-120">كيف تحصل على خدمة محاسبة التكاليف (معاينة خاصة)</span><span class="sxs-lookup"><span data-stu-id="5834d-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5834d-121">لاستخدام خدمة محاسبة التكاليف، يجب أن يكون لديك بيئة عالية الاتاحة تم تمكين LCS عليها (ليس بيئة OneBox)، ويجب أن يتم تشغيل Dynamics 365 Supply Chain Management الإصدار 10.0.11 أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="5834d-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="5834d-122">للتسجيل في المعاينة الخاصة لخدمة محاسبة التكاليف، الرجاء إرسال معرف بيئة LCS الخاص بك بالبريد الإلكتروني إلى [خدمة محاسبة التكاليف (المعاينة الخاصة)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="5834d-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="5834d-123">عند اعتمادك للبرنامج، سنرسل لك بريدًا إلكترونيًا للمتابعة يحتوي على مفتاح بيتا لخدمة محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="5834d-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="5834d-124">عند استلام مفتاح بيتا، يمكنك المتابعة عن طريق [تثبيت الوظيفة الإضافية](#install).</span><span class="sxs-lookup"><span data-stu-id="5834d-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="5834d-125">الترخيص</span><span class="sxs-lookup"><span data-stu-id="5834d-125">Licensing</span></span>

<span data-ttu-id="5834d-126">يجري ترخيص خدمة محاسبة التكاليف معًا مع الميزات القياسية لمحاسبة المخزون المتوفرة لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5834d-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="5834d-127">لا يتعين عليك شراء ترخيص إضافي لاستخدام خدمة محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="5834d-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="5834d-128">تثبيت الوظيفة الإضافية</span><span class="sxs-lookup"><span data-stu-id="5834d-128">Install the add-in</span></span>

<span data-ttu-id="5834d-129">لاستخدام خدمة محاسبة التكاليف، قم بتثبيت الوظيفة الإضافية لخدمة محاسبة التكاليف لـ Supply Chain Management كما هو موضح في الإجراء التالي.</span><span class="sxs-lookup"><span data-stu-id="5834d-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="5834d-130">[التسجيل](#sign-up) في خدمة محاسبة التكاليف (معاينة خاصة).</span><span class="sxs-lookup"><span data-stu-id="5834d-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="5834d-131">سجل الدخول إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="5834d-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="5834d-132">انتقل إلى **إدارة ميزة المعاينة**.</span><span class="sxs-lookup"><span data-stu-id="5834d-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="5834d-133">حدد علامة الزائد (**+**).</span><span class="sxs-lookup"><span data-stu-id="5834d-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="5834d-134">في حقل **الرمز**، أدخل مفتاح بيتا للوظيفة الإضافية لخدمة محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="5834d-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="5834d-135">(ينبغي أن تكون استلمت المفتاح الخاص بك بواسطة البريد الإلكتروني.)</span><span class="sxs-lookup"><span data-stu-id="5834d-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="5834d-136">حدد **إلغاء الحظر**.</span><span class="sxs-lookup"><span data-stu-id="5834d-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="5834d-137">افتح بيئة LCS حيث تريد إضافة الخدمة بها.</span><span class="sxs-lookup"><span data-stu-id="5834d-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="5834d-138">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="5834d-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="5834d-139">قم بالتمرير لأسفل إلى علامة التبويب السريعة **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="5834d-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="5834d-140">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="5834d-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="5834d-141">حدد **خدمة محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="5834d-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="5834d-142">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="5834d-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="5834d-143">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="5834d-143">Select **Install**.</span></span>

1. <span data-ttu-id="5834d-144">في علامة التبويب السريعة **الوظائف الإضافية للبيئة**، يجب أن تشاهد خدمة محاسبة التكاليف قد تم تثبيتها.</span><span class="sxs-lookup"><span data-stu-id="5834d-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="5834d-145">بعد بضع دقائق، يجب أن تغير الحالة من **قيد التثبيت** إلى **مثبت**.</span><span class="sxs-lookup"><span data-stu-id="5834d-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="5834d-146">(قد تحتاج إلى تحديث الصفحة لعرض هذا التغيير.) في تلك النقطة، تكون خدمة محاسبة التكاليف جاهزة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="5834d-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="5834d-147">إعداد التكامل</span><span class="sxs-lookup"><span data-stu-id="5834d-147">Set up the integration</span></span>

<span data-ttu-id="5834d-148">لإعداد التكامل بين خدمة محاسبة الكاليف و Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="5834d-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="5834d-149">انتقل إلى **إدارة النظام > إدارة الميزات**</span><span class="sxs-lookup"><span data-stu-id="5834d-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="5834d-150">حدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="5834d-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="5834d-151">افتح علامة تبويب **الكل** وابحث عن الميزة التي تسمى *خدمة محاسبة التكاليف*.</span><span class="sxs-lookup"><span data-stu-id="5834d-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="5834d-152">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="5834d-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="5834d-153">انتقل إلى **إدارة التكاليف > خدمة محاسبة التكاليف > الإعداد > معلمات خدمة محاسبة التكاليف > معلمات التكاملات**.</span><span class="sxs-lookup"><span data-stu-id="5834d-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="5834d-154">في حقل **معرف التطبيق**، أدخل الرمز التالي:</span><span class="sxs-lookup"><span data-stu-id="5834d-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="5834d-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="5834d-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="5834d-156">في حقل **نقطة نهاية خدمة البيانات**، أدخل عنوان URL التالي:</span><span class="sxs-lookup"><span data-stu-id="5834d-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="5834d-157">في حقل **نقطة نهاية خدمة محاسبة التكاليف**، أدخل عنوان URL التالي:</span><span class="sxs-lookup"><span data-stu-id="5834d-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="5834d-158">الآن خدمة محاسبة التكاليف جاهزة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="5834d-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5834d-159">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="5834d-159">Related resources</span></span>

[<span data-ttu-id="5834d-160">الصفحة الرئيسية لخدمة محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="5834d-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
