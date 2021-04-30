---
title: شحن طرد صغير
description: يوفر هذا الموضوع معلومات حول ميزة شحن طرد صغير (SPS). تمكن هذه الميزة Microsoft Dynamics 365 Supply Chain Management من إرسال تفاصيل حول أحدي الحاويات المحزمة إلى الناقل، ثم تتلقي بطاقة الشحن وسعر الشحن ورقم التعقب مره أخرى من هذا الناقل.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910199"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="e9554-104">شحن طرد صغير</span><span class="sxs-lookup"><span data-stu-id="e9554-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9554-105">تمكن ميزه الشحن الجزء الصغير (SPS) Microsoft Dynamics 365 Supply Chain Management من التعامل مع شركات الشحن مباشره عن طريق توفير اطار عمل للاتصال عبر واجات برمجه تطبيقات الناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="e9554-106">تكون هذه الوظيفة مفيده عندما تقوم بشحن أوامر مبيعات فرديه عبر شركات شحن تجاريه بدلا من استخدام شحن الحاوية أو الشحن اقل من حمولة الشاحنة (LTL).</span><span class="sxs-lookup"><span data-stu-id="e9554-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="e9554-107">تتفاعل ميزه SPS مع شركه الشحن الخاصة بك من خلال *محرك السعر* المخصص.</span><span class="sxs-lookup"><span data-stu-id="e9554-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="e9554-108">يجب ان تقوم المؤسسة الخاصة بك بتطوير محرك المعدل هذا في التعاون مع خدمه الحامل أو لوحه وصل الحامل لديك.</span><span class="sxs-lookup"><span data-stu-id="e9554-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="e9554-109">يتيح محرك الأسعار لـ Supply Chain Management إرسال تفاصيل حول أحدي الحاويات المحزمة إلى الناقل الخاص بك، ثم تتلقي بطاقة الشحن وسعر الشحن ورقم التعقب مره أخرى من هذا الناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="e9554-110">تتم أضافه سعر الشحن الذي يتم إرجاعه إلى أمر التوريد المرتبط كمصاريف متنوعة.</span><span class="sxs-lookup"><span data-stu-id="e9554-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="e9554-111">ويمكن بعد ذلك طباعه تسميه الشحن التي تم إرجاعها باستخدام Zebra Programming Language (ZPL) وتطبيقها علي الشحنة.</span><span class="sxs-lookup"><span data-stu-id="e9554-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="e9554-112">سيقوم الناقل بفحص تسميه الشحن هذه عندما يقوم بانتقاء الحزم الموجودة في المستودع.</span><span class="sxs-lookup"><span data-stu-id="e9554-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="e9554-113">إعداد النظام لدعم SPS</span><span class="sxs-lookup"><span data-stu-id="e9554-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="e9554-114">قبل البدء في استخدام وظيفة SPS، يجب تشغيل ميزه SPS في أداره الميزات وأضافه محرك السعر الخاص بك وإعداد **أداره النقل** و **الوحدات النمطية** لأداره المستودعات لدعمها.</span><span class="sxs-lookup"><span data-stu-id="e9554-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="e9554-115">تشغيل ميزة SPS</span><span class="sxs-lookup"><span data-stu-id="e9554-115">Turn on the SPS feature</span></span>

<span data-ttu-id="e9554-116">قبل أن تتمكن من استخدام ميزة SPS، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="e9554-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="e9554-117">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e9554-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e9554-118">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e9554-119">**الوحدة النمطية:** *إدارة النقل*</span><span class="sxs-lookup"><span data-stu-id="e9554-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="e9554-120">**اسم الميزة:** *شحن طرد صغير*</span><span class="sxs-lookup"><span data-stu-id="e9554-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="e9554-121">توزيع وإعداد محركات السعر</span><span class="sxs-lookup"><span data-stu-id="e9554-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="e9554-122">لا تتضمن Supply Chain Management اي محرك أسعار.</span><span class="sxs-lookup"><span data-stu-id="e9554-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="e9554-123">يجب الحصول علي إيه محركات أسعار تحتاجها أو إنشائها، ثم اضافتها إلى النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e9554-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="e9554-124">علي الرغم من ذلك ، توفر Microsoft محرك الأسعار التجريبي الذي يمكنك استخدامه لاجراء الاختبار.</span><span class="sxs-lookup"><span data-stu-id="e9554-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="e9554-125">تنزيل محرك الأسعار التجريبي ونشره</span><span class="sxs-lookup"><span data-stu-id="e9554-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="e9554-126">اتبع الخطوات التالية للحصول علي محرك الأسعار التجريبي.</span><span class="sxs-lookup"><span data-stu-id="e9554-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="e9554-127">في GitHub، قم بتنزيل [مكتبه الارتباط الحيوي (DLL) لمحرك الأسعار التجريبي](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="e9554-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="e9554-128">علي خادم Supply Chain Management، قم بحفظ DLL في المجلد **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="e9554-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="e9554-129">إنشاء وتوزيع محركات الأسعار الوظيفية</span><span class="sxs-lookup"><span data-stu-id="e9554-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="e9554-130">للحصول علي معلومات حول كيفيه إنشاء ونشر محركات الأسعار الوظيفية بحيث يمكن استخدامها في بيئة الإنتاج أو الاختبار، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="e9554-131">إنشاء محرك إدارة نقل جديد</span><span class="sxs-lookup"><span data-stu-id="e9554-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="e9554-132">إعداد محركات إدارة النقل</span><span class="sxs-lookup"><span data-stu-id="e9554-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="e9554-133">لمزيد من المعلومات حول كيفيه إنشاء محرك أسعار SPS، راجع نشر المدونة التالي: [شحن طرد صغير: كيفيه رفع وظائف شحن الطرد الصغير في Microsoft Dynamics365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="e9554-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="e9554-134">إعداد محرك السعر في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e9554-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="e9554-135">بعد إنشاء ونشر محرك السعر لـ SPS، اتبع الخطوات التالية لإعدادها.</span><span class="sxs-lookup"><span data-stu-id="e9554-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="e9554-136">انتقل إلى **إدارة النقل  \> إعداد \> المحركات \> محرك السعر الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="e9554-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="e9554-137">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e9554-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="e9554-138">في الصف الجديد، عيّن الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="e9554-139">**محرك الأسعار** – ادخل اسما فريدا لمحرك السعر.</span><span class="sxs-lookup"><span data-stu-id="e9554-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="e9554-140">إذا كنت تستخدم محرك السعر التجريبي، فادخل *محرك السعر التجريبي*.</span><span class="sxs-lookup"><span data-stu-id="e9554-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="e9554-141">**الاسم** - ادخل وصفا قصيرا لمحرك السعر.</span><span class="sxs-lookup"><span data-stu-id="e9554-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="e9554-142">إذا كنت تستخدم محرك السعر التجريبي، فادخل *محرك السعر التجريبي*.</span><span class="sxs-lookup"><span data-stu-id="e9554-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="e9554-143">**معرف بيانات تعريف التصنيف** - حدد الأساس الذي ينبغي استخدامه لحساب سعر الصرف الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e9554-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="e9554-144">علي سبيل المثال، قد يتم حساب السعر بناء علي المسافة.</span><span class="sxs-lookup"><span data-stu-id="e9554-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="e9554-145">إذا كنت تستخدم محرك السعر التجريبي، فيمكنك ترك هذا الحقل فارغا.</span><span class="sxs-lookup"><span data-stu-id="e9554-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="e9554-146">**تجميع المحرك** – ادخل اسم ملف حزمه DLL التي قمت بنشرها.</span><span class="sxs-lookup"><span data-stu-id="e9554-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="e9554-147">إذا كنت تستخدم محرك السعر التجريبي، فادخل *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="e9554-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="e9554-148">**فئة المحرك** – ادخل اسم الفئة التي تم تاسيسها لمحرك السعر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e9554-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="e9554-149">إذا كنت تستخدم محرك السعر التجريبي، فادخل *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="e9554-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e9554-150">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="e9554-150">Example scenario</span></span>

<span data-ttu-id="e9554-151">يوضح هذا المثال كيفيه إعداد SPS واستخدامها بعد إعداد النظام كما هو موضح سابقا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="e9554-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="e9554-152">يستخدم هذا السيناريو محرك معدل السعر التجريبي المذكور مسبقا.</span><span class="sxs-lookup"><span data-stu-id="e9554-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e9554-153">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="e9554-153">Make demo data available</span></span>

<span data-ttu-id="e9554-154">للعمل بهذا السيناريو باستخدام السجلات والقيم التجريبية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="e9554-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="e9554-155">بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="e9554-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="e9554-156">إعداد السيناريو</span><span class="sxs-lookup"><span data-stu-id="e9554-156">Set up the scenario</span></span>

<span data-ttu-id="e9554-157">بالنسبة لسيناريو هذا المثال، يجب ان يكون لديك ناقل تجريبي ومجموعه ناقل ونهج تعبئة وملف تعريف التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e9554-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="e9554-158">توضح الأقسام الفرعية التالية كيفيه إعداد السجلات المطلوبة للسيناريو.</span><span class="sxs-lookup"><span data-stu-id="e9554-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="e9554-159">في سيناريو الإنتاج، تمثل عمليه الإعداد عاده العملية الموضحة هنا.</span><span class="sxs-lookup"><span data-stu-id="e9554-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="e9554-160">ومع ذلك، سيتم تعيين قيم مختلفة.</span><span class="sxs-lookup"><span data-stu-id="e9554-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="e9554-161">إعداد شركات الشحن</span><span class="sxs-lookup"><span data-stu-id="e9554-161">Set up carriers</span></span>

<span data-ttu-id="e9554-162">اتبع هذه الخطوات لإعداد ناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="e9554-163">انتقل إلى **إدارة النقل \> إعداد \> شركات النقل‬‬ \> شركات الشحن‬‬**.</span><span class="sxs-lookup"><span data-stu-id="e9554-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="e9554-164">في جزء الإجراءات، حدد **جديد** لإضافة ناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="e9554-165">في الرأس، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="e9554-166">**شركة الشحن:** *الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e9554-167">**الاسم:** *الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e9554-168">**الوضع:** *الأرض*</span><span class="sxs-lookup"><span data-stu-id="e9554-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="e9554-169">في علامة التبويب السريعة **نظرة عامة**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e9554-170">**تنشيط واجهات شركات الشحن:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="e9554-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="e9554-171">**تنشيط تسعير الناقل:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="e9554-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="e9554-172">في علامة التبويب السريعة **الخدمات**، حدد **جديد** لإضافة خدمة إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e9554-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="e9554-173">قم بتعيين القيم التالية للخدمة الجديدة:</span><span class="sxs-lookup"><span data-stu-id="e9554-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="e9554-174">**خدمه الناقل:** *خدمة الناقل التجريبية*</span><span class="sxs-lookup"><span data-stu-id="e9554-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e9554-175">**الاسم:** *خدمة الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e9554-176">**وسيلة النقل:** *الجو*</span><span class="sxs-lookup"><span data-stu-id="e9554-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="e9554-177">ادخل قيمًا إجباريه لكافة الحقول الأخرى حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e9554-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="e9554-178">(عند حفظ سجل شركه الشحن الجديد، سيتم إنشاء وضع جديد للتسليم، وسيتم تعيين حقل  **وضع التسليم** بشكل تلقائي.)</span><span class="sxs-lookup"><span data-stu-id="e9554-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="e9554-179">في علامة التبويب السريعة **ملفات تعريف التسعير**، حدد **جديد** لإنشاء ملف تعريف تسعير إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e9554-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="e9554-180">قم بتعيين القيم التالية لملف التعريف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e9554-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="e9554-181">**ملف تعريف الأسعار:** *خدمه الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e9554-182">**الاسم:** *خدمة الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e9554-183">**محرك الأسعار:** *محرك السعر التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="e9554-184">ادخل قيمًا إجباريه لكافة الحقول الأخرى حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e9554-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="e9554-185">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e9554-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="e9554-186">للحصول على مزيد من المعلومات حول كيفية الناقل، راجع [إعداد شركات الشحن](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="e9554-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="e9554-187">إعداد حسابات خدمه الناقل</span><span class="sxs-lookup"><span data-stu-id="e9554-187">Set up carrier service accounts</span></span>

<span data-ttu-id="e9554-188">اتبع هذه الخطوات لإعداد خدمة الناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="e9554-189">انتقل إلى **إدارة النقل \> إعداد \> التسعير \> حساب خدمة الناقل**.</span><span class="sxs-lookup"><span data-stu-id="e9554-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="e9554-190">في جزء الإجراءات، حدد **جديد** لإضافة حساب خدمة الناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="e9554-191">قم بتعيين القيم التالية للحساب الجديد:</span><span class="sxs-lookup"><span data-stu-id="e9554-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="e9554-192">**شركة الشحن:** *الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e9554-193">**خدمه الناقل:** *خدمة الناقل التجريبية*</span><span class="sxs-lookup"><span data-stu-id="e9554-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="e9554-194">**رقم حساب عميل الناقل:** رقم حساب عميل الناقل المستخدم للتحقق من الاتصال ومصادقته علي شركه الشحن.</span><span class="sxs-lookup"><span data-stu-id="e9554-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="e9554-195">سيقوم الناقل بتوفير هذه القيمة.</span><span class="sxs-lookup"><span data-stu-id="e9554-195">Your carrier will provide this value.</span></span> <span data-ttu-id="e9554-196">إذا كنت تستخدم الخدمه التجريبية، يمكنك إدخال قيمه عشوائية.</span><span class="sxs-lookup"><span data-stu-id="e9554-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="e9554-197">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="e9554-197">**Site:** *6*</span></span>
    - <span data-ttu-id="e9554-198">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="e9554-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9554-199">وغالبا ما تكون قيمه **رقم حساب عميل الناقل** هي القيمة الوحيدة المطلوبة لمصادقه الاتصال.</span><span class="sxs-lookup"><span data-stu-id="e9554-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="e9554-200">ومع ذلك، إذا كان الناقل الخاص بك يتطلب معلمات مصادقه اضافيه، فيجب علي مؤسستك تخصيص هذه الصفحة لأضافه الحقول الإضافية حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e9554-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="e9554-201">إعداد سياسة تعبئة الحاويات</span><span class="sxs-lookup"><span data-stu-id="e9554-201">Set up a container packing policy</span></span>

<span data-ttu-id="e9554-202">اتبع هذه الخطوات لإعداد سياسة تعبئة حاوية.</span><span class="sxs-lookup"><span data-stu-id="e9554-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="e9554-203">إذا لم تكن قد قمت بالفعل بإعداد تعريف طابعه ZPL، فاستخدم تطبيق عامل توجيه المستند لإعداده.</span><span class="sxs-lookup"><span data-stu-id="e9554-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="e9554-204">لمزيد من المعلومات، راجع [نظره عامه حول طباعه المستند](../../fin-ops-core/dev-itpro/analytics/print-documents.md) والمواضيع ذات الصله.</span><span class="sxs-lookup"><span data-stu-id="e9554-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="e9554-205">انتقل إلى **إدارة المستودعات \> الإعداد \> الحاويات \> سياسات تعبئة الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="e9554-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="e9554-206">في جزء الإجراءات، حدد **جديد** لإضافة سياسة تعبئة الحاويات.</span><span class="sxs-lookup"><span data-stu-id="e9554-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="e9554-207">في رأس السياسة الجديدة، عيِّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="e9554-208">**سياسة تعبئة الحاوية:** *سياسة التعبئة التجريبية*</span><span class="sxs-lookup"><span data-stu-id="e9554-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="e9554-209">**الوصف:** أدخل وصفًا للسياسة.</span><span class="sxs-lookup"><span data-stu-id="e9554-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="e9554-210">في علامة التبويب السريعة **نظرة عامة**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e9554-211">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="e9554-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e9554-212">**الموقع الافتراضي للشحنة النهائية:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="e9554-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="e9554-213">**وحدة الوزن:** *كجم*</span><span class="sxs-lookup"><span data-stu-id="e9554-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="e9554-214">**سياسة إغلاق الحاوية:** *الإصدار التلقائي*</span><span class="sxs-lookup"><span data-stu-id="e9554-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="e9554-215">**سياسة إصدار الحاوية:** *الإتاحة في موقع الشحن النهائي*</span><span class="sxs-lookup"><span data-stu-id="e9554-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="e9554-216">في علامة التبويب السريعة **بيان الحاوية**، يمكنك تعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e9554-217">**البيان التلقائي عند إغلاق الحاوية:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="e9554-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="e9554-218">**متطلبات البيان الخاصة بالحاوية:** *أداره النقل*</span><span class="sxs-lookup"><span data-stu-id="e9554-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="e9554-219">**طباعه محتويات الحاوية:** *لا*</span><span class="sxs-lookup"><span data-stu-id="e9554-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="e9554-220">في علامة التبويب السريعة **طباعة بطاقة الناقل**، يمكنك تعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e9554-221">**طباعه بطاقة حاويه الشحن:** *دائما*</span><span class="sxs-lookup"><span data-stu-id="e9554-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="e9554-222">**اسم الطابعة**: اسم الطابعة ZPL التي ينبغي عليها طباعه بطاقات الشحن</span><span class="sxs-lookup"><span data-stu-id="e9554-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="e9554-223">إعداد ملف تعريف التعبئة</span><span class="sxs-lookup"><span data-stu-id="e9554-223">Set up a packing profile</span></span>

<span data-ttu-id="e9554-224">لإعداد ملف تعريف التعبئة، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="e9554-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="e9554-225">انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> ملفات تعريف التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="e9554-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="e9554-226">في جزء الإجراءات، حدد **جديد** لإضافة ملف تعريف التعبئة إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e9554-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="e9554-227">قم بتعيين القيم التالية لملف التعريف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e9554-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="e9554-228">**معرف ملف تعريف التعبئة:** *ملف تعريف التعبئة التوضيحية*</span><span class="sxs-lookup"><span data-stu-id="e9554-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="e9554-229">**الوصف:** أدخل وصفًا لملف التعريف</span><span class="sxs-lookup"><span data-stu-id="e9554-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="e9554-230">**سياسة تعبئة الحاوية:** *سياسة التعبئة التجريبية*</span><span class="sxs-lookup"><span data-stu-id="e9554-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="e9554-231">**وضع معرف الحاوية:** *تلقائي*</span><span class="sxs-lookup"><span data-stu-id="e9554-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="e9554-232">**نوع الحاوية:** *صندوق صغير*</span><span class="sxs-lookup"><span data-stu-id="e9554-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="e9554-233">إعداد عميل لاستخدام ناقل SPS</span><span class="sxs-lookup"><span data-stu-id="e9554-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="e9554-234">اتبع هذه الخطوات لإعداد عميل بحيث يمكنه استخدام شركه الشحن التي قمت بإنشاءها.</span><span class="sxs-lookup"><span data-stu-id="e9554-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="e9554-235">انتقل إلى **الحسابات المدينة \> العملاء \> جميع العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e9554-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="e9554-236">في الشبكة، ابحث عن العميل *US-027* وحدده.</span><span class="sxs-lookup"><span data-stu-id="e9554-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="e9554-237">في جزء الإجراءات، في علامة تبويب **عام** في مجموعة **إعداد‬**، حدد **حسابات عميل الناقل**.</span><span class="sxs-lookup"><span data-stu-id="e9554-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="e9554-238">في الصفحة **حسابات عميل الناقل**، في جزء الاجراء، حدد **جديد** لأضافه حساب إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e9554-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="e9554-239">قم بتعيين القيم التالية للحساب الجديد:</span><span class="sxs-lookup"><span data-stu-id="e9554-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="e9554-240">**شركة الشحن:** *الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e9554-241">**رقم حساب عميل الناقل:** *12345* (القيمة غير هامه لهذا السيناريو، ولكن سيتم الاشاره اليها في القسم التالي).</span><span class="sxs-lookup"><span data-stu-id="e9554-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="e9554-242">الانتقال عبر مثال السيناريو</span><span class="sxs-lookup"><span data-stu-id="e9554-242">Go through the example scenario</span></span>

<span data-ttu-id="e9554-243">بعد إعداد كافة عينات البيانات كما هو موضح في المقطع السابق، ستكون جاهزا للانتقال عبر سيناريو المثال.</span><span class="sxs-lookup"><span data-stu-id="e9554-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="e9554-244">إنشاء أمر المبيعات ومعالجة العمل</span><span class="sxs-lookup"><span data-stu-id="e9554-244">Create a sales order and process the work</span></span>

<span data-ttu-id="e9554-245">لإنشاء أمر مبيعات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e9554-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="e9554-246">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="e9554-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e9554-247">حدد **جديد** لإنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e9554-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="e9554-248">في مربع الحوار **إنشاء أمر مبيعات**، قم بتعيين **حساب العميل** على *US-027*.</span><span class="sxs-lookup"><span data-stu-id="e9554-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="e9554-249">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="e9554-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="e9554-250">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="e9554-250">The new sales order is opened.</span></span> <span data-ttu-id="e9554-251">في علامة التبويب السريعة **رأس أمر التوريد**، قم بتعيين حقل **رقم حساب عميل الناقل** إلى القيمة التي قمت بتحديدها لهذا العميل في وقت سابق ( *12345*).</span><span class="sxs-lookup"><span data-stu-id="e9554-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="e9554-252">في قسم **بنود أمر التوريد**، قم باضافه بند مبيعات وقم بتعيين القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="e9554-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="e9554-253">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e9554-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="e9554-254">**الكمية:** *1*</span><span class="sxs-lookup"><span data-stu-id="e9554-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="e9554-255">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="e9554-255">**Site:** *6*</span></span>
    - <span data-ttu-id="e9554-256">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="e9554-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e9554-257">قم بالتبديل إلى طريقة عرض **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="e9554-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="e9554-258">في علامة التبويب السريعة **التسليم**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e9554-259">**شركة الشحن:** *الناقل التجريبي*</span><span class="sxs-lookup"><span data-stu-id="e9554-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="e9554-260">**خدمه الناقل:** *خدمة الناقل التجريبية*</span><span class="sxs-lookup"><span data-stu-id="e9554-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="e9554-261">قم بالتبديل مرة أخرى إلى طريقة عرض **البنود**.</span><span class="sxs-lookup"><span data-stu-id="e9554-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="e9554-262">إذا تمت مطالبتك بتحديث وضع التسليم لبنود المبيعات، فحدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e9554-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="e9554-263">في القسم **بنود أمر التوريد**، حدد بند الأمر الذي قمت بإعداده سابقا ، ثم حدد **المخزون\> حجز**.</span><span class="sxs-lookup"><span data-stu-id="e9554-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="e9554-264">في صفحة **الحجز**، حدد **حجز لوط** لحجز الكمية الكاملة للبند المحدد في المستودع.</span><span class="sxs-lookup"><span data-stu-id="e9554-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="e9554-265">قم بإغلاق صفحة **الحجز** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e9554-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="e9554-266">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="e9554-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e9554-267">يتم إنشاء العمل لنقل الأصناف من موقع الانتقاء إلى محطه التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e9554-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="e9554-268">في **بنود أمر المبيعات**، حدد **المستودع \> تفاصيل الشحن**.</span><span class="sxs-lookup"><span data-stu-id="e9554-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="e9554-269">في الصفحة **تفاصيل الشحنة**، قم بتسجيل معرف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="e9554-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="e9554-270">ستحتاج اليه عند حزم الحزمة الخاصة بالشحنة في محطه التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e9554-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="e9554-271">قم بإغلاق صفحة **تفاصيل الشحن** للعودة إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e9554-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="e9554-272">قم بتدوين رقم أمر التوريد ، ثم انتقل إلى **أداره المستودعات\>عمل\> كل العمل**.</span><span class="sxs-lookup"><span data-stu-id="e9554-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="e9554-273">استخدم رقم أمر التوريد للبحث عن العمل الذي تم إنشاؤه للأمر وتحديده.</span><span class="sxs-lookup"><span data-stu-id="e9554-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="e9554-274">في جزء "الإجراءات"، على علامة تبويب **عمل**، حدد **إكمال العمل**.</span><span class="sxs-lookup"><span data-stu-id="e9554-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="e9554-275">في الصفحة **إكمال العمل**، في الحقل **معرف المستخدم**، حدد معرف المستخدم.</span><span class="sxs-lookup"><span data-stu-id="e9554-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="e9554-276">بعد ذلك، في جزء الإجراءات، حدد **التحقق من صحة العمل**.</span><span class="sxs-lookup"><span data-stu-id="e9554-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="e9554-277">إذا تجاوز العمل عملية التحقق من الصحة، حدد **إكمال العمل** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e9554-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="e9554-278">يتم وضع علامة علي العمل كمكتمل لمحاكاة عمليه نقل الأصناف إلى محطه التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e9554-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="e9554-279">تعبئة الشحنة.</span><span class="sxs-lookup"><span data-stu-id="e9554-279">Pack the shipment</span></span>

<span data-ttu-id="e9554-280">لتعبئة الشحنة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e9554-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="e9554-281">انتقل إلى **إداة المستودعات \> إعداد \> العامل**، وتاكد من ان حساب المستخدم الخاص بك مقترن بحساب عامل لأداره المستودعات.</span><span class="sxs-lookup"><span data-stu-id="e9554-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="e9554-282">انتقل إلى **إدارة المستودعات \> الانتقاء والتعبئة في حاويات \> التعبئة**.</span><span class="sxs-lookup"><span data-stu-id="e9554-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="e9554-283">في مربع الحوار **تحديد محطة التعبئة**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="e9554-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e9554-284">**الموقع:** *6*</span><span class="sxs-lookup"><span data-stu-id="e9554-284">**Site:** *6*</span></span>
    - <span data-ttu-id="e9554-285">**المستودع:** *62*</span><span class="sxs-lookup"><span data-stu-id="e9554-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="e9554-286">**الموقع:** *التعبئة*</span><span class="sxs-lookup"><span data-stu-id="e9554-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="e9554-287">**معرف ملف تعريف التعبئة:** *ملف تعريف التعبئة التوضيحية*</span><span class="sxs-lookup"><span data-stu-id="e9554-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="e9554-288">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e9554-288">Select **OK**.</span></span>
1. <span data-ttu-id="e9554-289">تظهر الصفحة **التعبئة‬**.</span><span class="sxs-lookup"><span data-stu-id="e9554-289">The **Pack** page appears.</span></span> <span data-ttu-id="e9554-290">في سيناريو الإنتاج، يقوم العامل بفحص لوحه الترخيص أو معرف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="e9554-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="e9554-291">ومع ذلك ، بالنسبة لهذا السيناريو ، افتح الصفحة **كافة الشحنات**، وابحث عن رقم الشحنة الخاص بالشحنة التي قمت بإنشاءها.</span><span class="sxs-lookup"><span data-stu-id="e9554-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="e9554-292">ثم ادخل هذه القيمة في حقل **لوحه الترخيص أو الشحن** في الصفحة **الحزمة**.</span><span class="sxs-lookup"><span data-stu-id="e9554-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="e9554-293">بدلاً من ذلك، ادخل معرف الشحنة الذي قمت بتسجيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="e9554-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="e9554-294">في جزء الإجراءات، حدد **حاوية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="e9554-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="e9554-295">يظهر مربع الحوار الذي يظهر تفاصيل حول الحاوية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="e9554-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="e9554-296">اترك القيم الافتراضية، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e9554-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="e9554-297">في الصفحة **الحزمة**، علي علامة التبويب السريعة **تعبئة الصنف**، في الحقل **المعرف**، حدد *A0002* لحزم هذا الصنف.</span><span class="sxs-lookup"><span data-stu-id="e9554-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="e9554-298">تتم أضافه الصنف إلى الحاوية.</span><span class="sxs-lookup"><span data-stu-id="e9554-298">The item is added to the container.</span></span>
1. <span data-ttu-id="e9554-299">في جزء الإجراءات‬، حدد **حاويات للشحنة**.</span><span class="sxs-lookup"><span data-stu-id="e9554-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="e9554-300">تحتوي الصفحة **الحاوية للشحنة** التي تظهر علي صف للحاويه التي قمت بإنشاءها.</span><span class="sxs-lookup"><span data-stu-id="e9554-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="e9554-301">ومع ذلك، فان الحقل **معرف بيان الحاوية** الموجود في هذا الصف فارغ حاليا، لأنك لم تتلقي بعد عنوان الشحن ورقم التعقب من شركه الشحن.</span><span class="sxs-lookup"><span data-stu-id="e9554-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="e9554-302">في جزء الإجراءات، حدد **إغلاق الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="e9554-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="e9554-303">في مربع الحوار **إغلاق الحاوية**، قم بتعيين الحقل **الإجمالي الوزن** إلى *1 كجم*، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e9554-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="e9554-304">ينبغي الآن طباعه بطاقة الشحن علي طابعه ZPL التي قمت بتحديدها مسبقا.</span><span class="sxs-lookup"><span data-stu-id="e9554-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="e9554-305">يجب أن تشبه المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="e9554-305">It should resemble the following example.</span></span>

    <span data-ttu-id="e9554-306">![مثال لتسميه الشحن](media/sps-label-example.png "مثال لتسميه الشحن")</span><span class="sxs-lookup"><span data-stu-id="e9554-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="e9554-307">لاحظ انه تمت أضافه **معرف بيان الحاوية** و **إجمالي الشحن** باعتبارها مستلمه من الناقل.</span><span class="sxs-lookup"><span data-stu-id="e9554-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]