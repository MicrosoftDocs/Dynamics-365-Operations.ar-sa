---
title: نظرة عامة على الكتابة الثنائية
description: يوفر هذا الموضوع نظرة عامة على الكتابة الثنائية. الكتابة الثنائية هي بنية أساسية توفر تفاعلاً قريبًا من الوقت الفعلي بين تطبيقات Microsoft Dynamics 365 المستندة إلى النموذج وتطبيقات Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075966"
---
# <a name="dual-write-overview"></a><span data-ttu-id="b84e3-104">نظرة عامة على الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="b84e3-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="b84e3-105">ما الكتابة الثنائية؟</span><span class="sxs-lookup"><span data-stu-id="b84e3-105">What is dual-write?</span></span>

<span data-ttu-id="b84e3-106">الكتابة الثنائية هي بنية أساسية جاهزة توفر تفاعلاً قريبًا من الوقت الفعلي بين تطبيقات مستندة إلى النموذج في Microsoft Dynamics 365 وتطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b84e3-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="b84e3-107">عندما تتدفق بيانات حول العملاء والمنتجات والأشخاص والعمليات خارج حدود التطبيق، فإنه يتم تمكين كافة الأقسام في مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="b84e3-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="b84e3-108">وتوفر الكتابة الثنائية دمجًا مرتبطًا بقوة وثنائي الاتجاه بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="b84e3-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b84e3-109">أي تغيير بيانات في تطبيقات Finance and Operations يتسبب في الكتابة في Common Data Service، وأي تغيير في البيانات في Common Data Service يتسبب في الكتابة في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b84e3-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="b84e3-110">يوفر تدفق البيانات المؤتمت هذا تجربة متكاملة للمستخدم عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="b84e3-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![علاقة البيانات بين التطبيقات](media/dual-write-overview.jpg)

<span data-ttu-id="b84e3-112">تتضمن الكتابة الثنائية جانبين: جانب *البنية الأساسية* وجانب *التطبيق*.</span><span class="sxs-lookup"><span data-stu-id="b84e3-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="b84e3-113">البنية الأساسية</span><span class="sxs-lookup"><span data-stu-id="b84e3-113">Infrastructure</span></span>

<span data-ttu-id="b84e3-114">البنية الأساسية ثنائية الكتابة قابلة للتوسعة والاعتمادية، وتتضمن ميزات المفتاح التالية:</span><span class="sxs-lookup"><span data-stu-id="b84e3-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="b84e3-115">تدفق البيانات المتزامن وثنائي الاتجاه بين التطبيقات</span><span class="sxs-lookup"><span data-stu-id="b84e3-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="b84e3-116">المزامنة مع أوضاع التشغيل والإيقاف المؤقت والتسوية لدعم النظام أثناء وضع عبر الإنترنت ودون اتصال/عدم تزامن.</span><span class="sxs-lookup"><span data-stu-id="b84e3-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="b84e3-117">القدرة على مزامنة البيانات الأولية بين التطبيقات</span><span class="sxs-lookup"><span data-stu-id="b84e3-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="b84e3-118">العرض الموحد لسجلات النشاط والأخطاء لمسؤولي البيانات</span><span class="sxs-lookup"><span data-stu-id="b84e3-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="b84e3-119">القدرة على تكوين التنبيهات والحدود المخصصة، وللاشتراك في الإخطارات</span><span class="sxs-lookup"><span data-stu-id="b84e3-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="b84e3-120">واجهة مستخدم بديهية (UI) للتصفية والتحويلات</span><span class="sxs-lookup"><span data-stu-id="b84e3-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="b84e3-121">القدرة على تعيين تبعيات الكيانات والعلاقات وعرضها</span><span class="sxs-lookup"><span data-stu-id="b84e3-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="b84e3-122">قابلية التوسعة لكل من الكيانات والخرائط القياسية والمخصصة</span><span class="sxs-lookup"><span data-stu-id="b84e3-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="b84e3-123">إدارة دورة حياة التطبيق الموثوق</span><span class="sxs-lookup"><span data-stu-id="b84e3-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="b84e3-124">تجربة الإعداد الجاهز للعملاء الجدد</span><span class="sxs-lookup"><span data-stu-id="b84e3-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="b84e3-125">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="b84e3-125">Application</span></span>

<span data-ttu-id="b84e3-126">تعمل الكتابة الثنائية على إنشاء تعيين بين المفاهيم في تطبيقات Finance and Operations والمفاهيم في التطبيقات المستندة إلى الطراز في Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b84e3-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="b84e3-127">يدعم هذا التكامل السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="b84e3-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="b84e3-128">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="b84e3-128">Integrated customer master</span></span>
+ <span data-ttu-id="b84e3-129">الوصول إلى بطاقات ولاء العملاء ونقاط المكافآت</span><span class="sxs-lookup"><span data-stu-id="b84e3-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="b84e3-130">تجربه إدارة المنتج الموحدة</span><span class="sxs-lookup"><span data-stu-id="b84e3-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="b84e3-131">توعية التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="b84e3-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="b84e3-132">أصل المورّد المتكامل</span><span class="sxs-lookup"><span data-stu-id="b84e3-132">Integrated vendor master</span></span>
+ <span data-ttu-id="b84e3-133">الوصول إلى البيانات المالية وبيانات مرجع الضريبة</span><span class="sxs-lookup"><span data-stu-id="b84e3-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="b84e3-134">تجربة محرك أسعار حسب الطلب</span><span class="sxs-lookup"><span data-stu-id="b84e3-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="b84e3-135">تجربة العميل المتوقع إلى النقدية المتكامل</span><span class="sxs-lookup"><span data-stu-id="b84e3-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="b84e3-136">القدرة على القيام بخدمة الأصول في المنزل والأصول الخاصة بالعملاء من خلال وكلاء الحقول</span><span class="sxs-lookup"><span data-stu-id="b84e3-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="b84e3-137">خبرة الشراء إلى الدفع المتكاملة</span><span class="sxs-lookup"><span data-stu-id="b84e3-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="b84e3-138">الأنشطة والملاحظات المتكاملة لبيانات ومستندات العميل</span><span class="sxs-lookup"><span data-stu-id="b84e3-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="b84e3-139">القدرة على البحث عن توفر المخزون الحالي والتفاصيل</span><span class="sxs-lookup"><span data-stu-id="b84e3-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="b84e3-140">خبرة المشروع إلى النقد</span><span class="sxs-lookup"><span data-stu-id="b84e3-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="b84e3-141">القدرة على معالجة العديد من العناوين والأدوار من خلال مفهوم الطرف</span><span class="sxs-lookup"><span data-stu-id="b84e3-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="b84e3-142">إدارة مصدر واحد للمستخدمين</span><span class="sxs-lookup"><span data-stu-id="b84e3-142">Single source management for users</span></span>
+ <span data-ttu-id="b84e3-143">القنوات المتكاملة للبيع بالتجزئة والتسويق</span><span class="sxs-lookup"><span data-stu-id="b84e3-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="b84e3-144">الرؤية في العروض الترويجية والخصومات</span><span class="sxs-lookup"><span data-stu-id="b84e3-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="b84e3-145">وظائف طلب الخدمة</span><span class="sxs-lookup"><span data-stu-id="b84e3-145">Request-for-service functions</span></span>
+ <span data-ttu-id="b84e3-146">عمليات الخدمة المبسطة</span><span class="sxs-lookup"><span data-stu-id="b84e3-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="b84e3-147">أفضل الأسباب لاستخدام الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="b84e3-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="b84e3-148">يوفر الكتابة الثنائية تكاملاً عبر تطبيقات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b84e3-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="b84e3-149">يقوم إطار العمل القوي هذا بربط البيئات ويعمل على تمكين تطبيقات عمل مختلفة من العمل معًا.</span><span class="sxs-lookup"><span data-stu-id="b84e3-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="b84e3-150">فيما يلي الأسباب الرئيسية لوجوب استخدام الكتابة الثنائية:</span><span class="sxs-lookup"><span data-stu-id="b84e3-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="b84e3-151">وتوفر الكتابة الثنائية دمجًا مرتبطًا بقوة وثنائي الاتجاه وفي الوقت الفعلي تقريباً بين تطبيقات Finance and Operations وتطبيقات مستندة إلى النموذج في Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b84e3-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="b84e3-152">يعمل هذا الدمج على جعل Microsoft Dynamics 365 متجرًا واحدًا لجميع حلول الأعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b84e3-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="b84e3-153">ينتقل العملاء الذين يستخدمون Dynamics 365 Financeو Dynamics 365 Supply Chain Management، ولكن لا يستخدمون حلولاً غير تابعة لـ Microsoft لإدارة علاقة العملاء (CRM)، إلى Dynamics 365 لدعم الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="b84e3-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="b84e3-154">البيانات الواردة من العملاء والمنتجات والعمليات والمشاريع وإنترنت الأشياء (IoT) تنساب تلقائيًا إلى Common Data Service خلال الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="b84e3-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="b84e3-155">يُعد هذا الاتصال مفيدًا للغاية للأعمال المهتمة بتوسعات Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b84e3-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="b84e3-156">تتبع البنية الأساسية للكتابة الثنائية مبدأ بدون كود/كود منخفض.</span><span class="sxs-lookup"><span data-stu-id="b84e3-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="b84e3-157">مطلوب مجهود الهندسة الأدنى لتوسيع الخرائط القياسية من جدول إلى جدول ولتضمين خرائط مخصصة.</span><span class="sxs-lookup"><span data-stu-id="b84e3-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="b84e3-158">يدعم الكتابة الثنائية كلاً من الوضع عبر الإنترنت والوضع دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="b84e3-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="b84e3-159">تُعد Microsoft هي الشركة الوحيدة التي تقدم الدعم للوضع المتصل ودون اتصال.</span><span class="sxs-lookup"><span data-stu-id="b84e3-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="b84e3-160">ما الكتابة الثنائية للمستخدمين ومهندسي منتجات CRM؟</span><span class="sxs-lookup"><span data-stu-id="b84e3-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="b84e3-161">تعمل الكتابة الثنائية على أتمتة تدفق البيانات بين تطبيقات Finance and Operations و Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b84e3-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b84e3-162">في الإصدارات المستقبلية، سيتم تغيير المفاهيم في التطبيقات المستندة إلى النموذج في Dynamics 365 (على سبيل المثال، العميل وجهه الاتصال وعرض الأسعار والأمر) إلى عملاء السوق المتوسطة والسوق المتوسطة والعليا.</span><span class="sxs-lookup"><span data-stu-id="b84e3-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="b84e3-163">في الإصدار الأول، تتم معالجة معظم الأتمتة بواسطة حلول كتابة ثنائية.</span><span class="sxs-lookup"><span data-stu-id="b84e3-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="b84e3-164">في الإصدارات المستقبلية، ستصبح هذه الحلول جزءًا من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b84e3-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="b84e3-165">ومن خلال فهم التغييرات القادمة إلى Common Data Service، يمكنك حفظ المجهود بنفسك على المدى الطويل.</span><span class="sxs-lookup"><span data-stu-id="b84e3-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="b84e3-166">فيما يلي بعض التغييرات المهمة:</span><span class="sxs-lookup"><span data-stu-id="b84e3-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="b84e3-167">Common Data Service سيكون لها مفاهيم جديدة، مثل الشركة والطرف.</span><span class="sxs-lookup"><span data-stu-id="b84e3-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="b84e3-168">وسوف تؤثر هذه المفاهيم على كافة التطبيقات التي يتم إنشاؤها على Common Data Service، مثل Dynamics 365 Sales وDynamics 365 Marketing وDynamics 365 Customer Service وDynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b84e3-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="b84e3-169">يتم توحيد الأنشطة والملاحظات وتوسعها لدعم كل من C1s (مستخدمي النظام) وC2s (عملاء النظام).</span><span class="sxs-lookup"><span data-stu-id="b84e3-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="b84e3-170">فيما يلي بعض التغييرات المقبلة في Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="b84e3-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="b84e3-171">سيحل نوع البيانات العشري محل نوع البيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="b84e3-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="b84e3-172">سيقوم سريان التاريخ بدعم البيانات السابقة والحالية والمستقبلية في المكان نفسه.</span><span class="sxs-lookup"><span data-stu-id="b84e3-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="b84e3-173">سيكون هناك دعم أكثر للعملة وأسعار الصرف، وستتم مراجعة واجهة برمجة التطبيقات (API) **لسعر الصرف**.</span><span class="sxs-lookup"><span data-stu-id="b84e3-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="b84e3-174">سيتم دعم تحويلات الوحدة.</span><span class="sxs-lookup"><span data-stu-id="b84e3-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="b84e3-175">لمزيد من المعلومات حول التغييرات القادمة، راجع [البيانات في Common Data Service – المرحلة 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span><span class="sxs-lookup"><span data-stu-id="b84e3-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>
