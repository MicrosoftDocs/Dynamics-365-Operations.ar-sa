---
title: ما الجديد أو المتغير في الإصدار 10.0.6 من Dynamics 365 Supply Chain Management (نوفمبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.6 من Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802909"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="b24de-103">ما الجديد أو المتغير في الإصدار 10.0.6 من Dynamics 365 Supply Chain Management (نوفمبر 2019)</span><span class="sxs-lookup"><span data-stu-id="b24de-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b24de-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.6 من Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b24de-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="b24de-105">رقم بنية هذا الإصدار هو 10.0.234، وهو يتوفر كما يلي:</span><span class="sxs-lookup"><span data-stu-id="b24de-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="b24de-106">بينما يقع تاريخ التوفر العام في نوفمبر، تكون الميزات الجديدة متوفرة للإصدار المبكر في أكتوبر.</span><span class="sxs-lookup"><span data-stu-id="b24de-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="b24de-107">لمزيد من المعلومات حول الإصدار 10.0.6، راجع [موارد إضافية](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="b24de-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="b24de-108">كيان البيانات V2 لنماذج تكوين المنتجات</span><span class="sxs-lookup"><span data-stu-id="b24de-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="b24de-109">تم إطلاق الإصدار الثاني لكيان البيانات "نماذج تكوين المنتجات" (يسمى "نماذج تكوين المنتجات V2").</span><span class="sxs-lookup"><span data-stu-id="b24de-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="b24de-110">كما يجب أن يكون القالب الافتراضي "418-نماذج تكوين المنتجات" موجودًا بحيث يستخدم كيان البيانات الجديد "نماذج تكوين المنتج V2" في قوالب إطار العمل "استيراد/تصدير".</span><span class="sxs-lookup"><span data-stu-id="b24de-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="b24de-111">لن يتم تحديث القالب تلقائيًا بحيث يمكنك تحميل القالب من الافتراضي يدويًا.</span><span class="sxs-lookup"><span data-stu-id="b24de-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="b24de-112">ويقوم الكيان V2 بتصدير صف واحد كملف منفصل في مرفق بدلاً من تضمينه، لحل القيود على حجم كيان V1.</span><span class="sxs-lookup"><span data-stu-id="b24de-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="b24de-113">ما الذي تحتاج إلى فعله للقيام بهذا التغيير؟</span><span class="sxs-lookup"><span data-stu-id="b24de-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="b24de-114">بمجرد إهمال الكيان V1، يجب البدء بالترحيل من V1 إلى V2.</span><span class="sxs-lookup"><span data-stu-id="b24de-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="b24de-115">في حالة استخدام القالب "418-نماذج تكوين المنتج"، يمكنك النقر فوق الزر "تحميل القوالب الافتراضية" وإعادة تحميل القالب "418-نماذج تكوين المنتجات"</span><span class="sxs-lookup"><span data-stu-id="b24de-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="b24de-116">إذا كنت بحاجة إلى الاحتفاظ بالتوافق مع الأنظمة الموجودة، فيمكنك الآن متابعة استخدام القالب الموجود والكيان V1 (المهمل) حتى تقوم بنقل عمليات التكامل الخاصة بك إلى القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="b24de-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="b24de-117">عمليات تحسين إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="b24de-117">Feature management enhancements</span></span>
<span data-ttu-id="b24de-118">تسمح إدارة الميزات الآن بتمكين كافة الميزات الجديدة افتراضيًا، وتتطلب التأكيد لتمكين ميزة ما، وتمكين كافة الميزات التي لم يتم تمكينها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="b24de-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="b24de-119">الطرف المسؤول عن اتفاقية الشراء</span><span class="sxs-lookup"><span data-stu-id="b24de-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="b24de-120">تتوفر لديك الآن القدرة على تحديد الجهات المسؤولة الأساسية والثانوية في نموذج تصنيف اتفاقية الشراء واتفاقيات الشراء الناتجة.</span><span class="sxs-lookup"><span data-stu-id="b24de-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="b24de-121">وهذا يوفر للمستخدم حق الوصول إلى الشخص الذي قام بالإشراف على الاتفاقيات.</span><span class="sxs-lookup"><span data-stu-id="b24de-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="b24de-122">ارتباط RFQ على سطر أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="b24de-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="b24de-123">يمكنك إضافة ارتباط مرجعي من بنود أمر الشراء للرجوع إلى بنود RFQ المقابلة التي تم إنشاؤها منها، مما يسمح بسهولة بتوفير دعم مستند طلب عرض الأسعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="b24de-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b24de-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b24de-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b24de-125">إصلاح الأخطاء</span><span class="sxs-lookup"><span data-stu-id="b24de-125">Bug fixes</span></span>
<span data-ttu-id="b24de-126">للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.6، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="b24de-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="b24de-127">update 30 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="b24de-127">Platform update 30</span></span>
<span data-ttu-id="b24de-128">يتضمن Microsoft Dynamics 365 Supply Chain Management 10.0.6 التحديث Platform update 30.</span><span class="sxs-lookup"><span data-stu-id="b24de-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="b24de-129">لمعرفة المزيد حول Platform update 30، راجع [ما الجديد أو المتغير في Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="b24de-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="b24de-130">Dynamics 365: خطة الموجة 2 لإصدار 2019</span><span class="sxs-lookup"><span data-stu-id="b24de-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="b24de-131">هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟</span><span class="sxs-lookup"><span data-stu-id="b24de-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="b24de-132">راجع [Dynamics 365: خطة الموجة 2 لإصدار 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="b24de-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="b24de-133">لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.</span><span class="sxs-lookup"><span data-stu-id="b24de-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="b24de-134">ميزات Supply Chain Management التي تمت ازالتها وإهمالها</span><span class="sxs-lookup"><span data-stu-id="b24de-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="b24de-135">يوضح الموضوع [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b24de-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="b24de-136">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="b24de-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b24de-137">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="b24de-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b24de-138">قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في الموضوع [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.</span><span class="sxs-lookup"><span data-stu-id="b24de-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="b24de-139">بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا.</span><span class="sxs-lookup"><span data-stu-id="b24de-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="b24de-140">بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.</span><span class="sxs-lookup"><span data-stu-id="b24de-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
