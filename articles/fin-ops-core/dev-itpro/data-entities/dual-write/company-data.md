---
title: مفهوم الشركة في Dataverse
description: يوضح هذا الموضوع تكامل بيانات الشركة بين Finance and Operations وDataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f0e3950f2b35dd8b8dbf50601b7d6b6d624863e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683665"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="b0321-103">مفهوم الشركة في Dataverse</span><span class="sxs-lookup"><span data-stu-id="b0321-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="b0321-104">في Finance and Operations، مفهوم *الشركة* عبارة عن مفهوم قانوني ومفهوم خاص بالأعمال.</span><span class="sxs-lookup"><span data-stu-id="b0321-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="b0321-105">وهو أيضًا عبارة عن حدود أمان ورؤية للبيانات.</span><span class="sxs-lookup"><span data-stu-id="b0321-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="b0321-106">يعمل المستخدمون دائمًا في سياق شركة واحدة، وتتم تجزئة معظم البيانات حسب الشركة.</span><span class="sxs-lookup"><span data-stu-id="b0321-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="b0321-107">لا يوجد مفهوم مكافئ في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b0321-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="b0321-108">المفهوم الأقرب هو *وحدة الأعمال*، وهي عبارة عن حدود أمان ورؤية في المقام الأول لبيانات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b0321-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="b0321-109">هذا المفهوم ليس لديه الآثار القانونية أو التجارية نفسها كمفهوم الشركة.</span><span class="sxs-lookup"><span data-stu-id="b0321-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="b0321-110">نظرًا لعدم اعتبار وحدة الأعمال والشركة كمفهومين متساويين، فمن غير الممكن فرض تعيين واحد إلى واحد (1:1) بينهما لغرض تكامل Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b0321-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="b0321-111">ومع ذلك، ولأنه يجب على المستخدمين، بشكل افتراضي، أن يكونوا قادرين على رؤية الصفوف نفسها في التطبيق وDataverse، قدمت Microsoft كيانًا جديدًا في Dataverse مسمى cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="b0321-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new entity in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="b0321-112">هذا الكيان يعتبر مكافئًا لكيان الشركة في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b0321-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="b0321-113">للمساعدة على ضمان أن تكون رؤية الصفوف مكافئة بين التطبيق وDataverse، ننصح بالإعداد التالي للبيانات في Dataverse:</span><span class="sxs-lookup"><span data-stu-id="b0321-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="b0321-114">لكل صف شركة Finance and Operations تم تمكينه للكتابة المزدوجة، يتم إنشاء صف شركة cdm\_.</span><span class="sxs-lookup"><span data-stu-id="b0321-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="b0321-115">عند إنشاء صف cdm\_Company وتمكينه للكتابة المزدوجة، يتم إنشاء وحدة أعمال افتراضية تحمل الاسم نفسه.</span><span class="sxs-lookup"><span data-stu-id="b0321-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="b0321-116">على الرغم من إنشاء فريق افتراضي لوحدة الأعمال هذه بشكل تلقائي، لا يتم استخدام وحدة الأعمال.</span><span class="sxs-lookup"><span data-stu-id="b0321-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="b0321-117">يتم إنشاء فريق مالك منفصل له نفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="b0321-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="b0321-118">ويقترن أيضًا بوحدة الأعمال.</span><span class="sxs-lookup"><span data-stu-id="b0321-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="b0321-119">وبشكل افتراضي، فإن مالك أي صف يتم إنشاؤه في وكتابته بشكل مزدوج إلى Dataverse يتم تعيينه إلى فريق "مالك DW" المرتبط بوحدة الأعمال المقترنة.</span><span class="sxs-lookup"><span data-stu-id="b0321-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="b0321-120">يبين الرسم التوضيحي التالي مثالاً عن إعداد البيانات هذا في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b0321-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![إعداد البيانات في Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="b0321-122">بسبب هذا التكوين، فإن أي صف يرتبط بشركة USMF سيكون مملوكًا من قِبل فريق يرتبط بوحدة أعمال USMF في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b0321-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="b0321-123">وبالتالي، بإمكان أي مستخدم لديه حق الوصول إلى وحدة الأعمال هذه من خلال دور أمان تم تعيينه إلى الرؤية على مستوى وحدة الأعمال رؤية هذه الصفوف الآن.</span><span class="sxs-lookup"><span data-stu-id="b0321-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="b0321-124">يوضح المثال التالي كيف يمكن استخدام الفرق لتوفير الوصول الصحيح إلى هذه الصفوف.</span><span class="sxs-lookup"><span data-stu-id="b0321-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="b0321-125">يتم تعيين دور "مدير المبيعات" لأعضاء فريق "مبيعات USMF".</span><span class="sxs-lookup"><span data-stu-id="b0321-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="b0321-126">بإمكان المستخدمين الذين يؤدون دور "مدير المبيعات" الوصول إلى أي صفوف هي أعضاء في نفس وحدة الأعمال التي هم أعضاء فيها.</span><span class="sxs-lookup"><span data-stu-id="b0321-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="b0321-127">يرتبط فريق "مبيعات USMF" بوحدة أعمال USMF التي تم ذكرها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="b0321-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="b0321-128">وبالتالي، يمكن لأعضاء فريق "مبيعات USMF" رؤية أي حساب مملوك من قبل مستخدم "USMF DW"، ومصدره كيان شركة USMF في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b0321-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![كيف يمكن استخدام الفرق](media/dual-write-company-2.png)

<span data-ttu-id="b0321-130">كما يظهر في الرسم التوضيحي السابق، هذا التعيين 1:1 بين وحدة الأعمال والشركة والفريق هو مجرد نقطة بداية.</span><span class="sxs-lookup"><span data-stu-id="b0321-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="b0321-131">في هذا المثال، يتم إنشاء وحدة أعمال جديدة "أوروبا" في Dataverse كأصل لكل من DEMF وESMF.</span><span class="sxs-lookup"><span data-stu-id="b0321-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="b0321-132">وحدة الأعمال الجذر الجديدة هذه لا علاقة لها بالكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="b0321-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="b0321-133">ومع ذلك، يمكن استخدامها لمنح أعضاء فريق "مبيعات اليورو" حق الوصول إلى بيانات الحساب في كل من DEMF وESMF عن طريق تعيين رؤية البيانات إلى **وحدة الأعمال الأصل/التابعة** في دور الأمان المقترن.</span><span class="sxs-lookup"><span data-stu-id="b0321-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="b0321-134">الموضوع الأخير للمناقشة هو كيف تحدد الكتابة المزدوجة الفريق المالك الذي يجب تعيين الصفوف إليه.</span><span class="sxs-lookup"><span data-stu-id="b0321-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="b0321-135">يتم التحكم في هذا السلوك بواسطة الحقل **الفريق المالك الافتراضي** على صف cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="b0321-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company row.</span></span> <span data-ttu-id="b0321-136">عند تمكين صف cdm\_للكتابة المزدوجة، يقوم مكون إضافي بشكل تلقائي بإنشاء وحدة الأعمال المقترنة والفريق المالك (إذا لم يكن موجودًا بعد)، ويعيّن حقل **الفريق المالك الافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="b0321-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="b0321-137">يمكن للمسؤول تغيير هذا الحقل إلى قيمة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="b0321-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="b0321-138">ومع ذلك، لا يمكن للمسؤول مسح الحقل طالما تم تمكين الكيان للكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="b0321-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="b0321-139">![حقل الفريق المالك الافتراضي](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="b0321-139">![Default owning team field](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="b0321-140">تجزئة بيانات الشركة والتمهيد</span><span class="sxs-lookup"><span data-stu-id="b0321-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="b0321-141">يؤدي تكامل Dataverse إلى إحضار تماثل الشركة باستخدام معرف الشركة لتجزئة البيانات.</span><span class="sxs-lookup"><span data-stu-id="b0321-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="b0321-142">كما يبين الرسم التوضيحي التالي، يتم توسيع جميع الجداول الخاصة بالشركة بحيث تكون لها علاقة واحد إلى متعدد (N:1) مع كيان cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="b0321-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="b0321-143">![علاقة N:1 بين كيان خاص بالشركة وكيان cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="b0321-143">![N:1 relationship between a company-specific entity and the cdm_Company entity](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="b0321-144">بالنسبة إلى الصفوف، بعد إضافة شركة وحفظها، تصبح القيمة للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="b0321-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="b0321-145">لذلك، يجب على المستخدمين التأكد من تحديد الشركة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="b0321-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="b0321-146">وحدها الصفوف التي تحتوي على بيانات الشركة مؤهلة للكتابة المزدوجة بين التطبيق وDataverse.</span><span class="sxs-lookup"><span data-stu-id="b0321-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="b0321-147">بالنسبة إلى بيانات Dataverse الموجودة، ستكون تجربة التمهيد التي يديرها المسؤول متوفرة قريبًا.</span><span class="sxs-lookup"><span data-stu-id="b0321-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="b0321-148">ملء اسم الشركة تلقائيًا في تطبيق مشاركة العملاء</span><span class="sxs-lookup"><span data-stu-id="b0321-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="b0321-149">توجد العديد من الطرق لملء اسم الشركة تلقائيًا في تطبيق مشاركة العملاء.</span><span class="sxs-lookup"><span data-stu-id="b0321-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="b0321-150">إذا كنت مسؤول نظام، يُمكنك تعيين الشركة الافتراضية من خلال الانتقال إلى **الإعدادات المتقدمة > النظام > الأمان > المستخدمين**. </span><span class="sxs-lookup"><span data-stu-id="b0321-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="b0321-151">افتح نموذج **المستخدم**، وفي قسم **معلومات المؤسسة** ، قم بتعيين قيمة **الشركة إلى القيمة الافتراضية في النماذج**.</span><span class="sxs-lookup"><span data-stu-id="b0321-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="قم بتعيين الشركة الافتراضية في قسم معلومات المؤسسة.":::

+ <span data-ttu-id="b0321-153">إذا كان لديك حق الوصول لـ **الكتابة** إلى كيان **SystemUser** لمستوى **وحدة الأعمال** ، فمن ثم يُمكنك تغيير الشركة الافتراضية في أي نموذج من خلال تحديد شركة من القائمة المنسدلة الخاصة بـ **الشركة**.</span><span class="sxs-lookup"><span data-stu-id="b0321-153">If you have **Write** access to the **SystemUser** entity for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="تغيير اسم الشركة في حساب جديد.":::

+ <span data-ttu-id="b0321-155">إذا كان لديك حق الوصول لـ **الكتابة** إلى البيانات في أكثر من شركة، فمن ثم يُمكنك تغيير الشركة الافتراضية عن طريق اختيار صف يخص شركة مختلفة.</span><span class="sxs-lookup"><span data-stu-id="b0321-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="يؤدي اختيار أحد الصفوف إلى تغيير الشركة الافتراضية.":::

+ <span data-ttu-id="b0321-157">إذا كنت من مكونيّ النظام أو المسؤول، وتريد ملء بيانات الشركة تلقائيًا في نموذج مخصص، فيمكنك استخدام [أحداث النموذج](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="b0321-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="b0321-158">قم بإضافة مرجع  JavaScript **msdyn_/DefaultCompany.js** واستخدم الأحداث التالية.</span><span class="sxs-lookup"><span data-stu-id="b0321-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="b0321-159">يُمكنك استخدام أيًا من النماذج الجاهزة، على سبيل المثال، نموذج **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="b0321-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="b0321-160">حدث **OnLoad** للنموذج: قم بتعيين حقل **defaultCompany**. </span><span class="sxs-lookup"><span data-stu-id="b0321-160">**OnLoad** event for the form: Set the **defaultCompany** field.</span></span>
    + <span data-ttu-id="b0321-161">حدث **OnChange** لحقل **الشركة**: قم بتعيين حقل **updateDefaultCompany**. </span><span class="sxs-lookup"><span data-stu-id="b0321-161">**OnChange** event for the **Company** field: Set the **updateDefaultCompany** field.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="b0321-162">تطبيق التصفية استنادًا إلى سياق الشركة</span><span class="sxs-lookup"><span data-stu-id="b0321-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="b0321-163">لتطبيق التصفية استنادًا إلى سياق الشركة في النماذج المخصصة الخاصة بك أو في حقوق البحث المخصصة المضافة إلى النماذج القياسية، افتح النموذج واستخدم قسم **تصفية السجلات ذات الصلة** لتطبيق عامل تصفية الشركة.</span><span class="sxs-lookup"><span data-stu-id="b0321-163">To apply filtering based on the company context on your custom forms or on custom lookup fields added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="b0321-164">يجب تعيين هذا لكل حقل بحث يتطلب تصفية استنادًا إلى الشركة الأساسية في صف مُحدد.</span><span class="sxs-lookup"><span data-stu-id="b0321-164">You must set this for each lookup field that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="b0321-165">يتم عرض الإعداد الخاص بـ **الحساب** في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="b0321-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="تطبيق سياق الشركة":::

