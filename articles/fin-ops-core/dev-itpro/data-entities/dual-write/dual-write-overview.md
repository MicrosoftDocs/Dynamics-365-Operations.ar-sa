---
title: نظرة عامة على الكتابة المزدوجة
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
ms.openlocfilehash: 8957065bcadc3f33adb60c2a8f2be78710289631
ms.sourcegitcommit: d03f301633175b15d46690fc97067820bf21579f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2020
ms.locfileid: "3775137"
---
# <a name="dual-write-overview"></a><span data-ttu-id="d65b1-104">نظرة عامة على الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="d65b1-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="d65b1-105">ما الكتابة الثنائية؟</span><span class="sxs-lookup"><span data-stu-id="d65b1-105">What is dual-write?</span></span>

<span data-ttu-id="d65b1-106">الكتابة المزدوجة‬ هي بنية أساسية جاهزة توفر تفاعلاً قريبًا من الوقت الفعلي بين تطبيقات Customer Engagement وتطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d65b1-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="d65b1-107">عندما تتدفق بيانات حول العملاء والمنتجات والأشخاص والعمليات خارج حدود التطبيق، فإنه يتم تمكين كافة الأقسام في مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="d65b1-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="d65b1-108">وتوفر الكتابة الثنائية دمجًا مرتبطًا بقوة وثنائي الاتجاه بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="d65b1-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="d65b1-109">أي تغيير بيانات في تطبيقات Finance and Operations يتسبب في الكتابة في Common Data Service، وأي تغيير في البيانات في Common Data Service يتسبب في الكتابة في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d65b1-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="d65b1-110">يوفر تدفق البيانات المؤتمت هذا تجربة متكاملة للمستخدم عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="d65b1-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![علاقة البيانات بين التطبيقات](media/dual-write-overview.jpg)

<span data-ttu-id="d65b1-112">تتضمن الكتابة الثنائية جانبين: جانب *البنية الأساسية* وجانب *التطبيق*.</span><span class="sxs-lookup"><span data-stu-id="d65b1-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="d65b1-113">البنية الأساسية</span><span class="sxs-lookup"><span data-stu-id="d65b1-113">Infrastructure</span></span>

<span data-ttu-id="d65b1-114">البنية الأساسية ثنائية الكتابة قابلة للتوسعة والاعتمادية، وتتضمن ميزات المفتاح التالية:</span><span class="sxs-lookup"><span data-stu-id="d65b1-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="d65b1-115">تدفق البيانات المتزامن وثنائي الاتجاه بين التطبيقات</span><span class="sxs-lookup"><span data-stu-id="d65b1-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="d65b1-116">المزامنة مع أوضاع التشغيل والإيقاف المؤقت والتسوية لدعم النظام أثناء وضع عبر الإنترنت ودون اتصال/عدم تزامن.</span><span class="sxs-lookup"><span data-stu-id="d65b1-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="d65b1-117">القدرة على مزامنة البيانات الأولية بين التطبيقات</span><span class="sxs-lookup"><span data-stu-id="d65b1-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="d65b1-118">طريقة عرض مدمجة لسجلات النشاط والأخطاء لمسؤولي البيانات</span><span class="sxs-lookup"><span data-stu-id="d65b1-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="d65b1-119">القدرة على تكوين التنبيهات والحدود المخصصة، وللاشتراك في الإخطارات</span><span class="sxs-lookup"><span data-stu-id="d65b1-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="d65b1-120">واجهة مستخدم بديهية (UI) للتصفية والتحويلات</span><span class="sxs-lookup"><span data-stu-id="d65b1-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="d65b1-121">القدرة على تعيين تبعيات الكيانات والعلاقات وعرضها</span><span class="sxs-lookup"><span data-stu-id="d65b1-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="d65b1-122">قابلية التوسعة لكل من الكيانات والخرائط القياسية والمخصصة</span><span class="sxs-lookup"><span data-stu-id="d65b1-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="d65b1-123">إدارة دورة حياة التطبيق الموثوق</span><span class="sxs-lookup"><span data-stu-id="d65b1-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="d65b1-124">تجربة الإعداد الجاهز للعملاء الجدد</span><span class="sxs-lookup"><span data-stu-id="d65b1-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="d65b1-125">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="d65b1-125">Application</span></span>

<span data-ttu-id="d65b1-126">تعمل الكتابة المزدوجة على إنشاء تعيين بين المفاهيم في تطبيقات Finance and Operations والمفاهيم في تطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d65b1-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="d65b1-127">يدعم هذا التكامل السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="d65b1-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="d65b1-128">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="d65b1-128">Integrated customer master</span></span>
+ <span data-ttu-id="d65b1-129">الوصول إلى بطاقات ولاء العملاء ونقاط المكافآت</span><span class="sxs-lookup"><span data-stu-id="d65b1-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="d65b1-130">تجربه إدارة المنتج الموحدة</span><span class="sxs-lookup"><span data-stu-id="d65b1-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="d65b1-131">توعية التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d65b1-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="d65b1-132">أصل المورّد المتكامل</span><span class="sxs-lookup"><span data-stu-id="d65b1-132">Integrated vendor master</span></span>
+ <span data-ttu-id="d65b1-133">الوصول إلى البيانات المالية وبيانات مرجع الضريبة</span><span class="sxs-lookup"><span data-stu-id="d65b1-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="d65b1-134">تجربة محرك أسعار حسب الطلب</span><span class="sxs-lookup"><span data-stu-id="d65b1-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="d65b1-135">تجربة العميل المتوقع إلى النقدية المتكامل</span><span class="sxs-lookup"><span data-stu-id="d65b1-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="d65b1-136">القدرة على القيام بخدمة الأصول في المنزل والأصول الخاصة بالعملاء من خلال وكلاء الحقول</span><span class="sxs-lookup"><span data-stu-id="d65b1-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="d65b1-137">خبرة الشراء إلى الدفع المتكاملة</span><span class="sxs-lookup"><span data-stu-id="d65b1-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="d65b1-138">الأنشطة والملاحظات المتكاملة لبيانات ومستندات العميل</span><span class="sxs-lookup"><span data-stu-id="d65b1-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="d65b1-139">القدرة على البحث عن توفر المخزون الحالي والتفاصيل</span><span class="sxs-lookup"><span data-stu-id="d65b1-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="d65b1-140">خبرة المشروع إلى النقد</span><span class="sxs-lookup"><span data-stu-id="d65b1-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="d65b1-141">القدرة على معالجة العديد من العناوين والأدوار من خلال مفهوم الطرف</span><span class="sxs-lookup"><span data-stu-id="d65b1-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="d65b1-142">إدارة مصدر واحد للمستخدمين</span><span class="sxs-lookup"><span data-stu-id="d65b1-142">Single source management for users</span></span>
+ <span data-ttu-id="d65b1-143">القنوات المتكاملة للبيع بالتجزئة والتسويق</span><span class="sxs-lookup"><span data-stu-id="d65b1-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="d65b1-144">الرؤية في العروض الترويجية والخصومات</span><span class="sxs-lookup"><span data-stu-id="d65b1-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="d65b1-145">وظائف طلب الخدمة</span><span class="sxs-lookup"><span data-stu-id="d65b1-145">Request-for-service functions</span></span>
+ <span data-ttu-id="d65b1-146">عمليات الخدمة المبسطة</span><span class="sxs-lookup"><span data-stu-id="d65b1-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="d65b1-147">أفضل الأسباب لاستخدام الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="d65b1-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="d65b1-148">يوفر الكتابة الثنائية تكاملاً عبر تطبيقات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d65b1-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="d65b1-149">يقوم إطار العمل القوي هذا بربط البيئات ويعمل على تمكين تطبيقات عمل مختلفة من العمل معًا.</span><span class="sxs-lookup"><span data-stu-id="d65b1-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="d65b1-150">فيما يلي الأسباب الرئيسية لوجوب استخدام الكتابة الثنائية:</span><span class="sxs-lookup"><span data-stu-id="d65b1-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="d65b1-151">وتوفر الكتابة الثنائية دمجًا مرتبطًا بقوة وثنائي الاتجاه وفي الوقت الفعلي تقريباً بين تطبيقات Finance and Operations وتطبيقات مستندة إلى النموذج في Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d65b1-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="d65b1-152">يعمل هذا الدمج على جعل Microsoft Dynamics 365 متجرًا واحدًا لجميع حلول الأعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d65b1-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="d65b1-153">ينتقل العملاء الذين يستخدمون Dynamics 365 Financeو Dynamics 365 Supply Chain Management، ولكن لا يستخدمون حلولاً غير تابعة لـ Microsoft لإدارة علاقة العملاء (CRM)، إلى Dynamics 365 لدعم الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="d65b1-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="d65b1-154">البيانات الواردة من العملاء والمنتجات والعمليات والمشاريع وإنترنت الأشياء (IoT) تنساب تلقائيًا إلى Common Data Service خلال الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="d65b1-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="d65b1-155">يُعد هذا الاتصال مفيدًا للغاية للأعمال المهتمة بتوسعات Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="d65b1-155">This connection is useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="d65b1-156">تتبع البنية الأساسية للكتابة الثنائية مبدأ بدون كود/كود منخفض.</span><span class="sxs-lookup"><span data-stu-id="d65b1-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="d65b1-157">مطلوب مجهود الهندسة الأدنى لتوسيع الخرائط القياسية من جدول إلى جدول ولتضمين خرائط مخصصة.</span><span class="sxs-lookup"><span data-stu-id="d65b1-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="d65b1-158">يدعم الكتابة الثنائية كلاً من الوضع عبر الإنترنت والوضع دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="d65b1-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="d65b1-159">تُعد Microsoft هي الشركة الوحيدة التي تقدم الدعم للوضع المتصل ودون اتصال.</span><span class="sxs-lookup"><span data-stu-id="d65b1-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="d65b1-160">ما الذي تعنيه الكتابة المزدوجة لمطوري ومهندسي تطبيقات Customer Engagement؟</span><span class="sxs-lookup"><span data-stu-id="d65b1-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="d65b1-161">تعمل الكتابة المزدوجة على أتمتة تدفق البيانات بين تطبيقات Finance and Operations وتطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d65b1-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="d65b1-162">تتكون الكتابة المزدوجة من حلين من AppSource تم تثبيتهما على Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d65b1-162">Dual-write consists of two AppSource solutions that are installed on Common Data Service.</span></span> <span data-ttu-id="d65b1-163">تقوم الحلول بتوسيع مخطط الكيان والمكونات الإضافية وعمليات سير العمل على Common Data Service بحيث يمكن تغيير حجمها إلى حجم ERP.</span><span class="sxs-lookup"><span data-stu-id="d65b1-163">The solutions expand the entity schema, plugins, and workflows on Common Data Service so that they can scale to ERP size.</span></span> <span data-ttu-id="d65b1-164">للحصول على تنفيذ ناجح، يجب على مطوري ومهندسي تطبيقات Customer Engagement فهم هذه التغييرات والتعاون مع نظرائهم في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d65b1-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="d65b1-165">لإنشاء تماثل مع تطبيقات Finance and Operations، تنشئ الكتابة المزدوجة بعض التغييرات الهامة في مخطط Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d65b1-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Common Data Service schema.</span></span> <span data-ttu-id="d65b1-166">إذا كنت على دراية بالخطة، فيمكنك تجنب بعض الإصلاحات في التصميم والتطوير في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="d65b1-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="d65b1-167">عند تثبيت حزمة AppSource للكتابة المزدوجة، ستتوفر مفاهيم جديدة في Common Data Service، مثل الشركة والطرف.</span><span class="sxs-lookup"><span data-stu-id="d65b1-167">When the dual-write AppSource package is installed, Common Data Service will have new concepts such as company and party.</span></span> <span data-ttu-id="d65b1-168">من شأن هذه المفاهيم أن تساعد التطبيقات المبنية على Common Data Service، بما في ذلك Dynamics 365 Sales وDynamics 365 Marketing وDynamics 365 Customer Service وDynamics 365 Field Service، على التفاعل بطريقة سلسة مع تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d65b1-168">These concepts help applications built on Common Data Service, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="d65b1-169">يتم توحيد الأنشطة والملاحظات وتوسعها لدعم كل من C1s (مستخدمي النظام) وC2s (عملاء النظام).</span><span class="sxs-lookup"><span data-stu-id="d65b1-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="d65b1-170">لمنع فقدان البيانات أثنا إرسال العملات بين تطبيقات Finance and Operations وCommon Data Service، ستتمكن من توسيع عدد المنازل العشرية في نوع بيانات العملة لتطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d65b1-170">To prevent data loss during currency transmission between Finance and Operations apps and the Common Data Service, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="d65b1-171">تقوم هذه الميزة بإجراء ترجمة تلقائية للسجلات الموجودة إلى الحالة الموسعة الجديدة عند طبقة بيانات التعريف.</span><span class="sxs-lookup"><span data-stu-id="d65b1-171">The feature autotranslates existing records to the new extended state at the metadata layer.</span></span> <span data-ttu-id="d65b1-172">أثناء هذه العملية، يتم تحويل قيمة العملة إلى بيانات عشرية بدلا من بيانات خاصة بالأموال، وتدعم قيمة العملة 10 منازل عشرية.</span><span class="sxs-lookup"><span data-stu-id="d65b1-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="d65b1-173">هذه الميزة اختيارية ولا تحتاج المؤسسات التي لا تتطلب أكثر من 4 منازل عشرية من الدقة إلى الاشتراك فيها.</span><span class="sxs-lookup"><span data-stu-id="d65b1-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="d65b1-174">لمزيد من المعلومات، راجع [ترحيل نوع بيانات العملة للكتابة المزدوجة](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="d65b1-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="d65b1-175">[سيُضاف سريان التاريخ](../../dev-tools/date-effectivity.md) إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d65b1-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Common Data Service.</span></span> <span data-ttu-id="d65b1-176">وسيدعم البيانات السابقة والحالية والمستقبلية على الكيان نفسه.</span><span class="sxs-lookup"><span data-stu-id="d65b1-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="d65b1-177">يتم دعم [تحويلات وحدة](../../../../supply-chain/pim/tasks/manage-unit-measure.md) المنتج للمنتجات وعروض الأسعار والأوامر والفواتير.</span><span class="sxs-lookup"><span data-stu-id="d65b1-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="d65b1-178">لمزيد من المعلومات حول التغييرات القادمة، راجع [الميزات الجديدة أو المتغيرة في الكتابة المزدوجة](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="d65b1-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

