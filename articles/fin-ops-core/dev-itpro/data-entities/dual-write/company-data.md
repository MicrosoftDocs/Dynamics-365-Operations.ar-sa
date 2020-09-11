---
title: مفهوم الشركة في Common Data Service
description: يوضح هذا الموضوع تكامل بيانات الشركة بين Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728403"
---
# <a name="company-concept-in-common-data-service"></a><span data-ttu-id="8694b-103">مفهوم الشركة في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8694b-103">Company concept in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="8694b-104">في Finance and Operations، مفهوم *الشركة* عبارة عن مفهوم قانوني ومفهوم خاص بالأعمال.</span><span class="sxs-lookup"><span data-stu-id="8694b-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="8694b-105">وهو أيضًا عبارة عن حدود أمان ورؤية للبيانات.</span><span class="sxs-lookup"><span data-stu-id="8694b-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="8694b-106">يعمل المستخدمون دائمًا في سياق شركة واحدة، وتتم تجزئة معظم البيانات حسب الشركة.</span><span class="sxs-lookup"><span data-stu-id="8694b-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="8694b-107">لا يوجد مفهوم مكافئ في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8694b-107">Common Data Service doesn't have an equivalent concept.</span></span> <span data-ttu-id="8694b-108">المفهوم الأقرب هو *وحدة الأعمال*، وهي عبارة عن حدود أمان ورؤية في المقام الأول لبيانات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="8694b-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="8694b-109">هذا المفهوم ليس لديه الآثار القانونية أو التجارية نفسها كمفهوم الشركة.</span><span class="sxs-lookup"><span data-stu-id="8694b-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="8694b-110">نظرًا لعدم اعتبار وحدة الأعمال والشركة كمفهومين متساويين، فمن غير الممكن فرض تعيين واحد إلى واحد (1:1) بينهما لغرض تكامل Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8694b-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Common Data Service integration.</span></span> <span data-ttu-id="8694b-111">ومع ذلك، ولأنه يجب على المستخدمين، بشكل افتراضي، أن يكونوا قادرين على رؤية السجلات نفسها في التطبيق وCommon Data Service، قدمت Microsoft كيانًا جديدًا في Common Data Service مسمى cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="8694b-111">However, because users must, by default, be able to see the same records in the application and Common Data Service, Microsoft has introduced a new entity in Common Data Service that is named cdm\_Company.</span></span> <span data-ttu-id="8694b-112">هذا الكيان يعتبر مكافئًا لكيان الشركة في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="8694b-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="8694b-113">للمساعدة على ضمان أن تكون رؤية السجلات مكافئة بين التطبيق وCommon Data Service، ننصح بالإعداد التالي للبيانات في Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="8694b-113">To help guarantee that visibility of records is equivalent between the application and Common Data Service out of the box, we recommend the following setup for data in Common Data Service:</span></span>

+ <span data-ttu-id="8694b-114">لكل سجل شركة Finance and Operations تم تمكينه للكتابة المزدوجة، يتم إنشاء سجل شركة cdm\_.</span><span class="sxs-lookup"><span data-stu-id="8694b-114">For each Finance and Operations Company record that is enabled for dual-write, an associated cdm\_Company record is created.</span></span>
+ <span data-ttu-id="8694b-115">عند إنشاء سجل cdm\_Company وتمكينه للكتابة المزدوجة، يتم إنشاء وحدة أعمال افتراضية تحمل الاسم نفسه.</span><span class="sxs-lookup"><span data-stu-id="8694b-115">When a cdm\_Company record is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="8694b-116">على الرغم من إنشاء فريق افتراضي لوحدة الأعمال هذه بشكل تلقائي، لا يتم استخدام وحدة الأعمال.</span><span class="sxs-lookup"><span data-stu-id="8694b-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="8694b-117">يتم إنشاء فريق مالك منفصل له نفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="8694b-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="8694b-118">ويقترن أيضًا بوحدة الأعمال.</span><span class="sxs-lookup"><span data-stu-id="8694b-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="8694b-119">وبشكل افتراضي، فإن مالك أي سجل يتم إنشاؤه في وكتابته بشكل مزدوج إلى Common Data Service يتم تعيينه إلى فريق "مالك DW" المرتبط بوحدة الأعمال المقترنة.</span><span class="sxs-lookup"><span data-stu-id="8694b-119">By default, the owner of any record that is created and dual-written to Common Data Service is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="8694b-120">يبين الرسم التوضيحي التالي مثالاً عن إعداد البيانات هذا في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8694b-120">The following illustration shows an example of this data setup in Common Data Service.</span></span>

![إعداد البيانات في Common Data Service](media/dual-write-company-1.png)

<span data-ttu-id="8694b-122">بسبب هذا التكوين، فإن أي سجل يرتبط بشركة USMF سيكون مملوكًا من قِبل فريق يرتبط بوحدة أعمال USMF في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8694b-122">Because of this configuration, any record that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Common Data Service.</span></span> <span data-ttu-id="8694b-123">وبالتالي، بإمكان أي مستخدم لديه حق الوصول إلى وحدة الأعمال هذه من خلال دور أمان تم تعيينه إلى الرؤية على مستوى وحدة الأعمال رؤية هذه السجلات الآن.</span><span class="sxs-lookup"><span data-stu-id="8694b-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those records.</span></span> <span data-ttu-id="8694b-124">يوضح المثال التالي كيف يمكن استخدام الفرق لتوفير الوصول الصحيح إلى هذه السجلات.</span><span class="sxs-lookup"><span data-stu-id="8694b-124">The following example shows how teams can be used to provide the correct access to those records.</span></span>

+ <span data-ttu-id="8694b-125">يتم تعيين دور "مدير المبيعات" لأعضاء فريق "مبيعات USMF".</span><span class="sxs-lookup"><span data-stu-id="8694b-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="8694b-126">بإمكان المستخدمين الذين يؤدون دور "مدير المبيعات" الوصول إلى أي سجلات هي أعضاء في نفس وحدة الأعمال التي هم أعضاء فيها.</span><span class="sxs-lookup"><span data-stu-id="8694b-126">Users who have the "Sales Manager" role can access any account records that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="8694b-127">يرتبط فريق "مبيعات USMF" بوحدة أعمال USMF التي تم ذكرها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="8694b-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="8694b-128">وبالتالي، يمكن لأعضاء فريق "مبيعات USMF" رؤية أي حساب مملوك من قبل مستخدم "USMF DW"، ومصدره كيان شركة USMF في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8694b-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![كيف يمكن استخدام الفرق](media/dual-write-company-2.png)

<span data-ttu-id="8694b-130">كما يظهر في الرسم التوضيحي السابق، هذا التعيين 1:1 بين وحدة الأعمال والشركة والفريق هو مجرد نقطة بداية.</span><span class="sxs-lookup"><span data-stu-id="8694b-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="8694b-131">في هذا المثال، يتم إنشاء وحدة أعمال جديدة "أوروبا" في Common Data Service كأصل لكل من DEMF وESMF.</span><span class="sxs-lookup"><span data-stu-id="8694b-131">In this example, a new "Europe" business unit is manually created in Common Data Service as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="8694b-132">وحدة الأعمال الجذر الجديدة هذه لا علاقة لها بالكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="8694b-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="8694b-133">ومع ذلك، يمكن استخدامها لمنح أعضاء فريق "مبيعات اليورو" حق الوصول إلى بيانات الحساب في كل من DEMF وESMF عن طريق تعيين رؤية البيانات إلى **وحدة الأعمال الأصل/التابعة** في دور الأمان المقترن.</span><span class="sxs-lookup"><span data-stu-id="8694b-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="8694b-134">الموضوع الأخير للمناقشة هو كيف تحدد الكتابة المزدوجة الفريق المالك الذي يجب تعيين السجلات إليه.</span><span class="sxs-lookup"><span data-stu-id="8694b-134">A final topic to discuss is how dual-write determines which owner team it should assign records to.</span></span> <span data-ttu-id="8694b-135">يتم التحكم في هذا السلوك بواسطة الحقل **الفريق المالك الافتراضي** على سجل cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="8694b-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company record.</span></span> <span data-ttu-id="8694b-136">عند تمكين سجل cdm\_للكتابة المزدوجة، يقوم مكون إضافي بشكل تلقائي بإنشاء وحدة الأعمال المقترنة والفريق المالك (إذا لم يكن موجودًا بعد)، ويعيّن حقل **الفريق المالك الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="8694b-136">When a cdm\_Company record is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="8694b-137">يمكن للمسؤول تغيير هذا الحقل إلى قيمة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="8694b-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="8694b-138">ومع ذلك، لا يمكن للمسؤول مسح الحقل طالما تم تمكين الكيان للكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="8694b-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="8694b-139">![حقل الفريق المالك الافتراضي](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="8694b-139">![Default owning team field](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="8694b-140">تجزئة بيانات الشركة والتمهيد</span><span class="sxs-lookup"><span data-stu-id="8694b-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="8694b-141">يؤدي تكامل Common Data Service إلى إحضار تماثل الشركة باستخدام معرف الشركة لتجزئة البيانات.</span><span class="sxs-lookup"><span data-stu-id="8694b-141">Common Data Service integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="8694b-142">كما يبين الرسم التوضيحي التالي، يتم توسيع جميع الكيانات الخاصة بالشركة بحيث تكون لها علاقة واحد إلى متعدد (N:1) مع كيان cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="8694b-142">As the following illustration shows, all company-specific entities are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="8694b-143">![علاقة N:1 بين كيان خاص بالشركة وكيان cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="8694b-143">![N:1 relationship between a company-specific entity and the cdm_Company entity](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="8694b-144">بالنسبة إلى السجلات، بعد إضافة شركة وحفظها، تصبح القيمة للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="8694b-144">For records, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="8694b-145">لذلك، يجب على المستخدمين التأكد من تحديد الشركة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="8694b-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="8694b-146">وحدها السجلات التي تحتوي على بيانات الشركة مؤهلة للكتابة المزدوجة بين التطبيق وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="8694b-146">Only records that have company data are eligible for dual-write between the application and Common Data Service.</span></span>
+ <span data-ttu-id="8694b-147">بالنسبة إلى بيانات Common Data Service الموجودة، ستكون تجربة التمهيد التي يديرها المسؤول متوفرة قريبًا.</span><span class="sxs-lookup"><span data-stu-id="8694b-147">For existing Common Data Service data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="8694b-148">ملء اسم الشركة تلقائيًا في تطبيق مشاركة العملاء</span><span class="sxs-lookup"><span data-stu-id="8694b-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="8694b-149">توجد العديد من الطرق لملء اسم الشركة تلقائيًا في تطبيق مشاركة العملاء.</span><span class="sxs-lookup"><span data-stu-id="8694b-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="8694b-150">إذا كنت مسؤول نظام، يُمكنك تعيين الشركة الافتراضية من خلال الانتقال إلى **الإعدادات المتقدمة > النظام > الأمان > المستخدمين**. </span><span class="sxs-lookup"><span data-stu-id="8694b-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="8694b-151">افتح نموذج **المستخدم**، وفي قسم **معلومات المؤسسة** ، قم بتعيين قيمة **الشركة إلى القيمة الافتراضية في النماذج**.</span><span class="sxs-lookup"><span data-stu-id="8694b-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="قم بتعيين الشركة الافتراضية في قسم معلومات المؤسسة.":::

+ <span data-ttu-id="8694b-153">إذا كان لديك حق الوصول لـ**الكتابة** إلى كيان **SystemUser** لمستوى **وحدة الأعمال** ، فمن ثم يُمكنك تغيير الشركة الافتراضية في أي نموذج من خلال تحديد شركة من القائمة المنسدلة الخاصة بـ**الشركة**.</span><span class="sxs-lookup"><span data-stu-id="8694b-153">If you have **Write** access to the **SystemUser** entity for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="تغيير اسم الشركة في حساب جديد.":::

+ <span data-ttu-id="8694b-155">إذا كان لديك حق الوصول لـ**الكتابة** إلى البيانات في أكثر من شركة، فمن ثم يُمكنك تغيير الشركة الافتراضية عن طريق اختيار سجل يخص شركة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="8694b-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a record that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="يؤدي اختيار أحد السجلات إلى تغيير الشركة الافتراضية.":::

+ <span data-ttu-id="8694b-157">إذا كنت من مكونيّ النظام أو المسؤول، وتريد ملء بيانات الشركة تلقائيًا في نموذج مخصص، فيمكنك استخدام [أحداث النموذج](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="8694b-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="8694b-158">قم بإضافة مرجع  JavaScript **msdyn_/DefaultCompany.js** واستخدم الأحداث التالية.</span><span class="sxs-lookup"><span data-stu-id="8694b-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="8694b-159">يُمكنك استخدام أيًا من النماذج الجاهزة، على سبيل المثال، نموذج **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="8694b-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="8694b-160">حدث **OnLoad** للنموذج: قم بتعيين حقل **defaultCompany**. </span><span class="sxs-lookup"><span data-stu-id="8694b-160">**OnLoad** event for the form: Set the **defaultCompany** field.</span></span>
    + <span data-ttu-id="8694b-161">حدث **OnChange** لحقل **الشركة**: قم بتعيين حقل **updateDefaultCompany**. </span><span class="sxs-lookup"><span data-stu-id="8694b-161">**OnChange** event for the **Company** field: Set the **updateDefaultCompany** field.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="8694b-162">تطبيق التصفية استنادًا إلى سياق الشركة</span><span class="sxs-lookup"><span data-stu-id="8694b-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="8694b-163">لتطبيق التصفية استنادًا إلى سياق الشركة في النماذج المخصصة الخاصة بك أو في حقوق البحث المخصصة المضافة إلى النماذج القياسية، افتح النموذج واستخدم قسم **تصفية السجلات ذات الصلة** لتطبيق عامل تصفية الشركة.</span><span class="sxs-lookup"><span data-stu-id="8694b-163">To apply filtering based on the company context on your custom forms or on custom lookup fields added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="8694b-164">يجب تعيين هذا لكل حقل بحث يتطلب تصفية استنادًا إلى الشركة الأساسية في سجل مُحدد.</span><span class="sxs-lookup"><span data-stu-id="8694b-164">You must set this for each lookup field that requires filtering based on the underlying company on a given record.</span></span> <span data-ttu-id="8694b-165">يتم عرض الإعداد الخاص بـ **الحساب** في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="8694b-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="تطبيق سياق الشركة":::

