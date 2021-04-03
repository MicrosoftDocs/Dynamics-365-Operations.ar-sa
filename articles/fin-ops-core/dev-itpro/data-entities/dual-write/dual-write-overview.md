---
title: نظرة عامة على الكتابة المزدوجة
description: يوفر هذا الموضوع نظرة عامة على الكتابة المزدوجة التي توفر تفاعلاً قريبًا من الوقت الفعلي بين تطبيقات Customer Engagement وتطبيقات Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6cc02b483a2975dd3be28032ea7e90b540945492
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561268"
---
# <a name="dual-write-overview"></a><span data-ttu-id="af83f-103">نظرة عامة على الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="af83f-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="af83f-104">ما الكتابة الثنائية؟</span><span class="sxs-lookup"><span data-stu-id="af83f-104">What is dual-write?</span></span>

<span data-ttu-id="af83f-105">الكتابة المزدوجة‬ هي بنية أساسية جاهزة توفر تفاعلاً قريبًا من الوقت الفعلي بين تطبيقات Customer Engagement وتطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="af83f-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="af83f-106">عندما تتدفق بيانات حول العملاء والمنتجات والأشخاص والعمليات خارج حدود التطبيق، فإنه يتم تمكين كافة الأقسام في مؤسسة.</span><span class="sxs-lookup"><span data-stu-id="af83f-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="af83f-107">وتوفر الكتابة الثنائية دمجًا مرتبطًا بقوة وثنائي الاتجاه بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="af83f-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="af83f-108">أي تغيير بيانات في تطبيقات Finance and Operations يتسبب في الكتابة في Dataverse، وأي تغيير في البيانات في Dataverse يتسبب في الكتابة في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="af83f-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="af83f-109">يوفر تدفق البيانات المؤتمت هذا تجربة متكاملة للمستخدم عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="af83f-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![علاقة البيانات بين التطبيقات](media/dual-write-overview.jpg)

<span data-ttu-id="af83f-111">تتضمن الكتابة الثنائية جانبين: جانب *البنية الأساسية* وجانب *التطبيق*.</span><span class="sxs-lookup"><span data-stu-id="af83f-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="af83f-112">البنية الأساسية</span><span class="sxs-lookup"><span data-stu-id="af83f-112">Infrastructure</span></span>

<span data-ttu-id="af83f-113">البنية الأساسية ثنائية الكتابة قابلة للتوسعة والاعتمادية، وتتضمن ميزات المفتاح التالية:</span><span class="sxs-lookup"><span data-stu-id="af83f-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="af83f-114">تدفق البيانات المتزامن وثنائي الاتجاه بين التطبيقات</span><span class="sxs-lookup"><span data-stu-id="af83f-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="af83f-115">المزامنة مع أوضاع التشغيل والإيقاف المؤقت والتسوية لدعم النظام أثناء وضع عبر الإنترنت ودون اتصال/عدم تزامن.</span><span class="sxs-lookup"><span data-stu-id="af83f-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="af83f-116">القدرة على مزامنة البيانات الأولية بين التطبيقات</span><span class="sxs-lookup"><span data-stu-id="af83f-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="af83f-117">طريقة عرض مدمجة لسجلات النشاط والأخطاء لمسؤولي البيانات</span><span class="sxs-lookup"><span data-stu-id="af83f-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="af83f-118">القدرة على تكوين التنبيهات والحدود المخصصة، وللاشتراك في الإخطارات</span><span class="sxs-lookup"><span data-stu-id="af83f-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="af83f-119">واجهة مستخدم بديهية (UI) للتصفية والتحويلات</span><span class="sxs-lookup"><span data-stu-id="af83f-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="af83f-120">القدرة على تعيين تبعيات الجداول والعلاقات وعرضها</span><span class="sxs-lookup"><span data-stu-id="af83f-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="af83f-121">قابلية التوسعة لكل من الجداول والخرائط القياسية والمخصصة</span><span class="sxs-lookup"><span data-stu-id="af83f-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="af83f-122">إدارة دورة حياة التطبيق الموثوق</span><span class="sxs-lookup"><span data-stu-id="af83f-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="af83f-123">تجربة الإعداد الجاهز للعملاء الجدد</span><span class="sxs-lookup"><span data-stu-id="af83f-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="af83f-124">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="af83f-124">Application</span></span>

<span data-ttu-id="af83f-125">تعمل الكتابة المزدوجة على إنشاء تعيين بين المفاهيم في تطبيقات Finance and Operations والمفاهيم في تطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="af83f-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="af83f-126">يدعم هذا التكامل السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="af83f-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="af83f-127">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="af83f-127">Integrated customer master</span></span>
+ <span data-ttu-id="af83f-128">الوصول إلى بطاقات ولاء العملاء ونقاط المكافآت</span><span class="sxs-lookup"><span data-stu-id="af83f-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="af83f-129">تجربه إدارة المنتج الموحدة</span><span class="sxs-lookup"><span data-stu-id="af83f-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="af83f-130">توعية التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="af83f-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="af83f-131">أصل المورّد المتكامل</span><span class="sxs-lookup"><span data-stu-id="af83f-131">Integrated vendor master</span></span>
+ <span data-ttu-id="af83f-132">الوصول إلى البيانات المالية وبيانات مرجع الضريبة</span><span class="sxs-lookup"><span data-stu-id="af83f-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="af83f-133">تجربة محرك أسعار حسب الطلب</span><span class="sxs-lookup"><span data-stu-id="af83f-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="af83f-134">تجربة العميل المتوقع إلى النقدية المتكامل</span><span class="sxs-lookup"><span data-stu-id="af83f-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="af83f-135">القدرة على القيام بخدمة الأصول في المنزل والأصول الخاصة بالعملاء من خلال وكلاء الحقول</span><span class="sxs-lookup"><span data-stu-id="af83f-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="af83f-136">خبرة الشراء إلى الدفع المتكاملة</span><span class="sxs-lookup"><span data-stu-id="af83f-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="af83f-137">الأنشطة والملاحظات المتكاملة لبيانات ومستندات العميل</span><span class="sxs-lookup"><span data-stu-id="af83f-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="af83f-138">القدرة على البحث عن توفر المخزون الحالي والتفاصيل</span><span class="sxs-lookup"><span data-stu-id="af83f-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="af83f-139">خبرة المشروع إلى النقد</span><span class="sxs-lookup"><span data-stu-id="af83f-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="af83f-140">القدرة على معالجة العديد من العناوين والأدوار من خلال مفهوم الطرف</span><span class="sxs-lookup"><span data-stu-id="af83f-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="af83f-141">إدارة مصدر واحد للمستخدمين</span><span class="sxs-lookup"><span data-stu-id="af83f-141">Single source management for users</span></span>
+ <span data-ttu-id="af83f-142">القنوات المتكاملة للبيع بالتجزئة والتسويق</span><span class="sxs-lookup"><span data-stu-id="af83f-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="af83f-143">الرؤية في العروض الترويجية والخصومات</span><span class="sxs-lookup"><span data-stu-id="af83f-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="af83f-144">وظائف طلب الخدمة</span><span class="sxs-lookup"><span data-stu-id="af83f-144">Request-for-service functions</span></span>
+ <span data-ttu-id="af83f-145">عمليات الخدمة المبسطة</span><span class="sxs-lookup"><span data-stu-id="af83f-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="af83f-146">أفضل الأسباب لاستخدام الكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="af83f-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="af83f-147">يوفر الكتابة الثنائية تكاملاً عبر تطبيقات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="af83f-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="af83f-148">يقوم إطار العمل القوي هذا بربط البيئات ويعمل على تمكين تطبيقات عمل مختلفة من العمل معًا.</span><span class="sxs-lookup"><span data-stu-id="af83f-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="af83f-149">فيما يلي الأسباب الرئيسية لوجوب استخدام الكتابة الثنائية:</span><span class="sxs-lookup"><span data-stu-id="af83f-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="af83f-150">وتوفر الكتابة الثنائية دمجًا مرتبطًا بقوة وثنائي الاتجاه وفي الوقت الفعلي تقريباً بين تطبيقات Finance and Operations وتطبيقات مستندة إلى النموذج في Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="af83f-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="af83f-151">يعمل هذا الدمج على جعل Microsoft Dynamics 365 متجرًا واحدًا لجميع حلول الأعمال الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="af83f-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="af83f-152">ينتقل العملاء الذين يستخدمون Dynamics 365 Financeو Dynamics 365 Supply Chain Management، ولكن لا يستخدمون حلولاً غير تابعة لـ Microsoft لإدارة علاقة العملاء (CRM)، إلى Dynamics 365 لدعم الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="af83f-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="af83f-153">البيانات الواردة من العملاء والمنتجات والعمليات والمشاريع وإنترنت الأشياء (IoT) تنساب تلقائيًا إلى Dataverse خلال الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="af83f-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="af83f-154">يُعد هذا الاتصال مفيدًا للغاية للأعمال المهتمة بتوسعات Power Platform.</span><span class="sxs-lookup"><span data-stu-id="af83f-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="af83f-155">تتبع البنية الأساسية للكتابة الثنائية مبدأ بدون كود/كود منخفض.</span><span class="sxs-lookup"><span data-stu-id="af83f-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="af83f-156">مطلوب مجهود الهندسة الأدنى لتوسيع الخرائط القياسية من جدول إلى جدول ولتضمين خرائط مخصصة.</span><span class="sxs-lookup"><span data-stu-id="af83f-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="af83f-157">يدعم الكتابة الثنائية كلاً من الوضع عبر الإنترنت والوضع دون اتصال.</span><span class="sxs-lookup"><span data-stu-id="af83f-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="af83f-158">تُعد Microsoft هي الشركة الوحيدة التي تقدم الدعم للوضع المتصل ودون اتصال.</span><span class="sxs-lookup"><span data-stu-id="af83f-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="af83f-159">ما الذي تعنيه الكتابة المزدوجة لمطوري ومهندسي تطبيقات Customer Engagement؟</span><span class="sxs-lookup"><span data-stu-id="af83f-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="af83f-160">تعمل الكتابة المزدوجة على أتمتة تدفق البيانات بين تطبيقات Finance and Operations وتطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="af83f-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="af83f-161">تتكون الكتابة المزدوجة من حلين من AppSource تم تثبيتهما على Dataverse.</span><span class="sxs-lookup"><span data-stu-id="af83f-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="af83f-162">تقوم الحلول بتوسيع مخطط الجدول والمكونات الإضافية وعمليات سير العمل على Dataverse بحيث يمكن تغيير حجمها إلى حجم ERP.</span><span class="sxs-lookup"><span data-stu-id="af83f-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="af83f-163">للحصول على تنفيذ ناجح، يجب على مطوري ومهندسي تطبيقات Customer Engagement فهم هذه التغييرات والتعاون مع نظرائهم في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="af83f-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="af83f-164">لإنشاء تماثل مع تطبيقات Finance and Operations، تنشئ الكتابة المزدوجة بعض التغييرات الهامة في مخطط Dataverse.</span><span class="sxs-lookup"><span data-stu-id="af83f-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="af83f-165">إذا كنت على دراية بالخطة، فيمكنك تجنب بعض الإصلاحات في التصميم والتطوير في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="af83f-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="af83f-166">عند تثبيت حزمة AppSource للكتابة المزدوجة، ستتوفر مفاهيم جديدة في Dataverse، مثل الشركة والطرف.</span><span class="sxs-lookup"><span data-stu-id="af83f-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="af83f-167">من شأن هذه المفاهيم أن تساعد التطبيقات المبنية على Dataverse، بما في ذلك Dynamics 365 Sales وDynamics 365 Marketing وDynamics 365 Customer Service وDynamics 365 Field Service، على التفاعل بطريقة سلسة مع تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="af83f-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="af83f-168">يتم توحيد الأنشطة والملاحظات وتوسعها لدعم كل من C1s (مستخدمي النظام) وC2s (عملاء النظام).</span><span class="sxs-lookup"><span data-stu-id="af83f-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="af83f-169">لمنع فقدان البيانات أثنا إرسال العملات بين تطبيقات Finance and Operations وDataverse، ستتمكن من توسيع عدد المنازل العشرية في نوع بيانات العملة لتطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="af83f-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="af83f-170">تقوم هذه الميزة بإجراء ترجمة تلقائية للصفوف الموجودة إلى الحالة الموسعة الجديدة عند طبقة بيانات التعريف.</span><span class="sxs-lookup"><span data-stu-id="af83f-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="af83f-171">أثناء هذه العملية، يتم تحويل قيمة العملة إلى بيانات عشرية بدلا من بيانات خاصة بالأموال، وتدعم قيمة العملة 10 منازل عشرية.</span><span class="sxs-lookup"><span data-stu-id="af83f-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="af83f-172">هذه الميزة اختيارية ولا تحتاج المؤسسات التي لا تتطلب أكثر من 4 منازل عشرية من الدقة إلى الاشتراك فيها.</span><span class="sxs-lookup"><span data-stu-id="af83f-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="af83f-173">لمزيد من المعلومات، راجع [ترحيل نوع بيانات العملة للكتابة المزدوجة](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="af83f-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="af83f-174">[سيُضاف سريان التاريخ](../../dev-tools/date-effectivity.md) إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="af83f-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="af83f-175">وسيدعم البيانات السابقة والحالية والمستقبلية على الجدول نفسه.</span><span class="sxs-lookup"><span data-stu-id="af83f-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="af83f-176">يتم دعم [تحويلات وحدة](../../../../supply-chain/pim/tasks/manage-unit-measure.md) المنتج للمنتجات وعروض الأسعار والأوامر والفواتير.</span><span class="sxs-lookup"><span data-stu-id="af83f-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="af83f-177">لمزيد من المعلومات حول التغييرات القادمة، راجع [الميزات الجديدة أو المتغيرة في الكتابة المزدوجة](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="af83f-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]