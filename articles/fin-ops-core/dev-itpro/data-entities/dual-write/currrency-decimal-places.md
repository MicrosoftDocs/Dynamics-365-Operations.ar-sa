---
title: ترحيل نوع بيانات العملة للكتابة الثنائية
description: يوضح هذا الموضوع كيفية تغيير عدد المنازل العشرية التي تدعمها الكتابة الثنائية للعملة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
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
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456804"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="214cf-103">ترحيل نوع بيانات العملة للكتابة الثنائية</span><span class="sxs-lookup"><span data-stu-id="214cf-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="214cf-104">يمكنك زيادة عدد المنازل العشرية المعتمدة لقيم العملات بحد أقصى 10.</span><span class="sxs-lookup"><span data-stu-id="214cf-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="214cf-105">الحد الافتراضي هو أربعة منازل عشرية.</span><span class="sxs-lookup"><span data-stu-id="214cf-105">The default limit is four decimal places.</span></span> <span data-ttu-id="214cf-106">ومن خلال زيادة عدد المنازل العشرية، فإنك تساعد على منع فقدان البيانات عند استخدام الكتابة الثنائية لمزامنة البيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="214cf-107">وتكون الزيادة في عدد المنازل العشرية عبارة عن تغيير في الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="214cf-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="214cf-108">لتنفيذه، يجب عليك طلب مساعدة من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="214cf-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="214cf-109">ويكون لعملية تغيير عدد المنازل العشرية خطوتين:</span><span class="sxs-lookup"><span data-stu-id="214cf-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="214cf-110">اطلب ترحيلاً من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="214cf-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="214cf-111">قم بتغيير المنازل العشرية في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="214cf-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="214cf-112">يجب أن يدعم التطبيق Finance and Operations و Common Data Service عدد المنازل العشرية نفسه في قيم العملات.</span><span class="sxs-lookup"><span data-stu-id="214cf-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="214cf-113">وإلا، يمكن أن يحدث فقدان البيانات عند مزامنة هذه المعلومات بين التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="214cf-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="214cf-114">تعمل عملية الترحيل على إعادة تمكين الطريقة التي يتم بها تخزين قيم سعر العملة وسعر الصرف، ولكنها لا تقوم بتغيير أية بيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="214cf-115">بعد اكتمال الترحيل، يمكن زيادة عدد المنازل العشرية لأكواد العملة والتسعير ويمكن أن يكون للبيانات التي يقوم المستخدمون بإدخالها وعرضها دقة عشرية إضافية.</span><span class="sxs-lookup"><span data-stu-id="214cf-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="214cf-116">يُعد الترحيل أمرًا اختياريًا.</span><span class="sxs-lookup"><span data-stu-id="214cf-116">Migration is optional.</span></span> <span data-ttu-id="214cf-117">إذا كنت قد تستفيد من الدعم لمزيد من المنازل العشرية، نُوصي بوضع الترحيل في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="214cf-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="214cf-118">لا تحتاج المؤسسات التي لا تتطلب القيم والتي تحتوي على أكثر من أربعة منازل عشرية إلى الترحيل.</span><span class="sxs-lookup"><span data-stu-id="214cf-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="214cf-119">طلب ترحيل من Microsoft</span><span class="sxs-lookup"><span data-stu-id="214cf-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="214cf-120">لا يدعم تخزين حقول العملة الموجودة في Common Data Service أكثر من أربعة منازل عشرية.</span><span class="sxs-lookup"><span data-stu-id="214cf-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="214cf-121">وبالتالي، أثناء عملية الترحيل، يتم نسخ قيم العملات إلى حقول داخلية جديدة في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="214cf-122">تحدث هذه العملية باستمرار حتى يتم ترحيل كافة البيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="214cf-123">داخليًا، في نهاية الترحيل، تحل أنواع التخزين الجديدة محل أنواع التخزين القديمة، ولكن لا يتم تغيير قيم البيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="214cf-124">ويمكن بعد ذلك لحقول العملة دعم حتى 10 أماكن عشرية.</span><span class="sxs-lookup"><span data-stu-id="214cf-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="214cf-125">أثناء عملية الترحيل، يمكن متابعة استخدام Common Data Service بدون انقطاع.</span><span class="sxs-lookup"><span data-stu-id="214cf-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="214cf-126">وفي نفس الوقت، يتم تعديل أسعار الصرف بحيث تدعم ما يصل إلى 12 مكانًا عشريًا بدلاً من الحد الحالي الذي يصل إلى 10.</span><span class="sxs-lookup"><span data-stu-id="214cf-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="214cf-127">هذا التغيير مطلوب بحيث يكون عدد المنازل العشرية هو نفسه في كل من التطبيق Finance and Operations و Common Data Service</span><span class="sxs-lookup"><span data-stu-id="214cf-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="214cf-128">لا يقوم الترحيل بتغيير أية بيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-128">Migration doesn't change any data.</span></span> <span data-ttu-id="214cf-129">بعد تحويل حقول العملة وسعر الصرف،، يمكن للمسؤولين تكوين النظام لاستخدام ما يصل إلى 10 أماكن عشرية لحقول العملات عن طريق تحديد عدد المنازل العشرية لكل عملة حركه وللتسعير.</span><span class="sxs-lookup"><span data-stu-id="214cf-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="214cf-130">طلب ترحيل</span><span class="sxs-lookup"><span data-stu-id="214cf-130">Request a migration</span></span>

<span data-ttu-id="214cf-131">لجعل هذه الميزة متوفرة، أرسل بريدًا إلكترونيًا **CDSExpandDecimal@microsoft.com**، وقم بتضمين المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="214cf-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="214cf-132">**الموضوع:** طلب تمكين الدعم العشري الموسع لـ \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="214cf-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="214cf-133">**النص الأساسي:** أريد تمكين الدعم العشري الموسع لمؤسستي \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="214cf-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="214cf-134">سيتصل بك أحد ممثلي Microsoft خلال ثلاثة أيام عمل للخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="214cf-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="214cf-135">عند طلب ترحيل، يجب أن تكون على علم بالتفاصيل التالية والتخطيط لها وفقًا لذلك:</span><span class="sxs-lookup"><span data-stu-id="214cf-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="214cf-136">ويعتمد الوقت المطلوب لترحيل البيانات على حجم البيانات في النظام.</span><span class="sxs-lookup"><span data-stu-id="214cf-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="214cf-137">يمكن أن يستغرق ترحيل قواعد البيانات الكبيرة عدة أيام.</span><span class="sxs-lookup"><span data-stu-id="214cf-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="214cf-138">يزداد حجم قاعدة البيانات مؤقتًا أثناء تشغيل الترحيل، لأن هناك حاجة إلى مساحة إضافية للفهارس.</span><span class="sxs-lookup"><span data-stu-id="214cf-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="214cf-139">يتم تحرير معظم المساحة الإضافية عند اكتمال الترحيل.</span><span class="sxs-lookup"><span data-stu-id="214cf-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="214cf-140">أثناء عملية الترحيل، في حالة حدوث أخطاء تمنع اكتمال الترحيل، يقوم النظام برفع التنبيهات إلى دعم Microsoft ، بحيث يمكن لفريق الدعم التدخل.</span><span class="sxs-lookup"><span data-stu-id="214cf-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="214cf-141">ومع ذلك، حتى في حالة حدوث أخطاء أثناء الترحيل، تظل Common Data Service متوفرة بشكل كامل للاستخدام المنتظم.</span><span class="sxs-lookup"><span data-stu-id="214cf-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="214cf-142">لم يتم التراجع عن عملية الترحيل.</span><span class="sxs-lookup"><span data-stu-id="214cf-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="214cf-143">تغيير عدد المنازل العشرية</span><span class="sxs-lookup"><span data-stu-id="214cf-143">Changing the number of decimal places</span></span>

<span data-ttu-id="214cf-144">بعد اكتمال الترحيل، تستطيع Common Data Service تخزين الأعداد التي تحتوي على منازل عشرية أكثر.</span><span class="sxs-lookup"><span data-stu-id="214cf-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="214cf-145">يمكن للمسؤولين اختيار عدد المنازل العشرية المستخدمة لأكواد العملات المحددة والأسعار.</span><span class="sxs-lookup"><span data-stu-id="214cf-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="214cf-146">حينها، يمكن لمستخدمي Microsoft Power Apps و Power BI و Power Automate عرض الأرقام واستخدامها التي تحتوي على منازل عشرية أكثر.</span><span class="sxs-lookup"><span data-stu-id="214cf-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="214cf-147">لإجراء هذا التغيير، يجب تحديث الإعدادات التالية في Power Apps:</span><span class="sxs-lookup"><span data-stu-id="214cf-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="214cf-148">**إعدادات النظام: دقه العملة للأسعار** - يحدد الحقل **تحديد دقة العملة لتي سيتم استخدامها للتسعير خلال النظام** كيفية تصريف العملة للمؤسسة عند تحديد **دقه التسعير**.</span><span class="sxs-lookup"><span data-stu-id="214cf-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="214cf-149">**إدارة الأعمال: العملات** – يتيح لك الحقل **دقة سعر العمل** بتحديد عدد مخصص من المنازل العشرية لعملة محددة.</span><span class="sxs-lookup"><span data-stu-id="214cf-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="214cf-150">يوجد احتياطي للإعداد على مستوى المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="214cf-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="214cf-151">توجد بعض القيود:</span><span class="sxs-lookup"><span data-stu-id="214cf-151">There are some limitations:</span></span>

+ <span data-ttu-id="214cf-152">لا يمكنك تكوين حقل العملة في أحد الكيانات.</span><span class="sxs-lookup"><span data-stu-id="214cf-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="214cf-153">يمكنك تحديد أكثر من أربعة منازل عشرية في مستويات **التسعير** و **عملة الحركة**.</span><span class="sxs-lookup"><span data-stu-id="214cf-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="214cf-154">إعدادات النظام: دقه العملة بالنسبة للأسعار</span><span class="sxs-lookup"><span data-stu-id="214cf-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="214cf-155">بعد اكتمال الترحيل، يمكن للمسؤولين تعيين دقه العملة.</span><span class="sxs-lookup"><span data-stu-id="214cf-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="214cf-156">انتقل إلى **الإعدادات \> الإدارة**، وحدد **إعدادات النظام**.</span><span class="sxs-lookup"><span data-stu-id="214cf-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="214cf-157">بعد ذلك، في علامة التبويب **عام**، قم بتغيير قيمة الحقل **تعييم دقة العملة التي يتم استخدامها للتسعير خلال النظام**، كما هو موضح في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="214cf-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![إعدادات النظام للعملة](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="214cf-159">إدارة الأعمال: العملات</span><span class="sxs-lookup"><span data-stu-id="214cf-159">Business Management: Currencies</span></span>

<span data-ttu-id="214cf-160">إذا كنت ترغب في أن تختلف دقه العملة لعملة محددة عن دقه العملة المستخدمة في التسعير، فإنه يمكنك تغييرها.</span><span class="sxs-lookup"><span data-stu-id="214cf-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="214cf-161">انتقل إلى **الإعدادات \> إدارة الأعمال**، حدد **العملات**، وحدد العملة المراد تغييرها.</span><span class="sxs-lookup"><span data-stu-id="214cf-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="214cf-162">ثم قم بتعيين الحقل **دقه العملة** إلى عدد المنازل العشرية الذي تريده، كما هو مبين في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="214cf-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![إعدادات العملة لإعدادات محلية معينة](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="214cf-164">الكيانات: حقل العملة</span><span class="sxs-lookup"><span data-stu-id="214cf-164">Entities: Currency field</span></span>

<span data-ttu-id="214cf-165">يتم تحديد عدد المنازل العشرية التي يمكن تكوينها لحقول عملة معينة على أربعة.</span><span class="sxs-lookup"><span data-stu-id="214cf-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>
