---
title: فهم حقول التاريخ والوقت
description: اعرف ما يجب أن تتوقعه عند استخدام حقول التاريخ والوقت في Microsoft Dynamics 365 Human Resources. تمكّن من تكوين فهم واضح لما يجب توقعه عند التعامل مع بيانات التاريخ والوقت في نموذج في Human Resources أو مصدر خارجي أو Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be1e28d0b842184ce3c4f7bd9748f5e76ac67489
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430085"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="d9961-104">فهم حقول التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="d9961-104">Understand Date and Time fields</span></span>

<span data-ttu-id="d9961-105">تعد حقول **التاريخ والوقت** مفهومًا أساسيًا في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d9961-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d9961-106">من الضروري فهم كيفية التعامل مع بيانات **التاريخ والوقت** في نماذج Dynamics 365 Human Resources، وCommon Data Service، والمصادر الخارجية.</span><span class="sxs-lookup"><span data-stu-id="d9961-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="d9961-107">فهم الفرق بين أنواع بيانات حقل التاريخ والتاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="d9961-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="d9961-108">تحتوي حقول **التاريخ والوقت** على معلومات المنطقة الزمنية، بينما لا تحتوي حقول **التاريخ** على مثل هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="d9961-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="d9961-109">تعرض حقول **التاريخ** نفس المعلومات في أي موقع.</span><span class="sxs-lookup"><span data-stu-id="d9961-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="d9961-110">عند إدخال تاريخ في حقل **التاريخ**، يكتب Human Resources نفس التاريخ في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d9961-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="d9961-111">عند عرض البيانات في حقل **التاريخ والوقت**، يقوم Human Resources بضبط التاريخ والوقت استنادًا إلى المنطقة الزمنية للمستخدم المعينة في نموذج **خيارات المستخدم** (**عام > الإعداد > خيارات المستخدم**).</span><span class="sxs-lookup"><span data-stu-id="d9961-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="d9961-112">قد لا تكون معلومات التاريخ والوقت التي تقوم بإدخالها في الحقل هي نفسها المعلومات التي تمت كتابتها في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d9961-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="d9961-113">[![نموذج خيارات المستخدم](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="d9961-114">فهم حقول التاريخ والوقت في النماذج</span><span class="sxs-lookup"><span data-stu-id="d9961-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="d9961-115">عند إدخال البيانات في حقل **التاريخ والوقت**، لا تكون البيانات المعروضة على الشاشة هي نفس البيانات المخزنة في قاعدة البيانات إذا لم يتم تعيين المنطقة الزمنية للمستخدم إلى التوقيت العالمي المتفق عليه (UTC).</span><span class="sxs-lookup"><span data-stu-id="d9961-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d9961-116">يتم دائمًا تخزين البيانات في حقول **التاريخ والوقت** بالتوقيت العالمي UTC.</span><span class="sxs-lookup"><span data-stu-id="d9961-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="d9961-117">[![نموذج العامل](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="d9961-118">فهم حقول التاريخ والوقت في قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="d9961-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="d9961-119">عندما يقوم Human Resources بكتابة قيمة **التاريخ والوقت** في قاعدة البيانات، فإنه يُخزّن البيانات بالتوقيت العالمي UTC.</span><span class="sxs-lookup"><span data-stu-id="d9961-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="d9961-120">ويسمح ذلك للمستخدمين برؤية أي بيانات في حقل**التاريخ والوقت** بالنسبة إلى المنطقة الزمنية المحددة في خيارات المستخدم الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="d9961-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="d9961-121">في المثال المبين أعلاه، وقت البدء هو نقطة زمنية، وليس تاريخًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="d9961-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="d9961-122">بتغيير المنطقة الزمنية للمستخدم المسجل دخوله من GMT + 12:00 إلى GMT UTC، يعرض نفس السجل الذي تم إنشاؤه 04/30/2019 12:00:00 بدلا من 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="d9961-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="d9961-123">في المثال المبين أدناه، أصبح توظيف الموظف 000724 نشطًا في نفس الوقت بغض النظر عن المنطقة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="d9961-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="d9961-124">سيكون الموظف نشطًا في 04/30/2019 في المنطقة الزمنية GMT، وهو نفسه 05/01/2019 في المنطقة الزمنية GMT + 12:00.</span><span class="sxs-lookup"><span data-stu-id="d9961-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="d9961-125">يشير كل منهما إلى نفس النقطة في الوقت وليس كتاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="d9961-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="d9961-126">[![نموذج العامل](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="d9961-127">بيانات التاريخ والوقت في Data Management Framework، وExcel، وCommon Data Service، وPower BI</span><span class="sxs-lookup"><span data-stu-id="d9961-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="d9961-128">تم تصميم كافة تقارير Data Management Framework، ووظائف Excel الإضافية، وCommon Data Service، وPower BI بحيث تتفاعل مع البيانات مباشرة على مستوى قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d9961-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="d9961-129">نظرًا لعدم وجود عميل لتعديل بيانات **التاريخ والوقت** إلى المنطقة الزمنية للمستخدم، تكون كافة قيم **التاريخ والوقت** بالتوقيت العالمي (UTC)، مما قد يؤدي إلى بعض الافتراضات غير الصحيحة عند إدخال البيانات أو عرضها.</span><span class="sxs-lookup"><span data-stu-id="d9961-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="d9961-130">يتم افتراض بيانات **التاريخ والوقت** التي تم إرسالها من خلال DMF، أو Excel، أو Common Data Service على أنها بالتوقيت العالمي (UTC) من قِبل قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d9961-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="d9961-131">قد يتسبب هذا في حدوث التباس عند عدم عرض قيمة **التاريخ والوقت** المرسلة كما هو متوقع لأن المستخدم الذي يعرض البيانات ليس لديه المنطقة الزمنية للمستخدم المرسل للبيانات والمعينة بالتوقيت العالمي (UTC).</span><span class="sxs-lookup"><span data-stu-id="d9961-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="d9961-132">يمكن أن يحدث نفس الشيء بالعكس عند تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="d9961-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="d9961-133">ويمكن أن تكون بيانات **التاريخ والوقت** الموجودة في كيان DMF الذي تم تصديره مختلفة عما يتم عرضه في عميل Dynamics.</span><span class="sxs-lookup"><span data-stu-id="d9961-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="d9961-134">عند استخدام مصادر خارجية مثل DMF لعرض البيانات أو تأليفها، فإنه من الضروري الأخذ بالحسبان أن قيم **التاريخ والوقت** تعتبر افتراضيًا بالتوقيت العالمي (UTC) بغض النظر عن المنطقة الزمنية في كمبيوتر المستخدم أو إعدادات المنطقة الزمنية للمستخدم الحالي الخاصة بتلك البيانات.</span><span class="sxs-lookup"><span data-stu-id="d9961-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="d9961-135">أمثلة عن نفس السجل الذي يتم عرضه في مناطق منتج مختلفة</span><span class="sxs-lookup"><span data-stu-id="d9961-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="d9961-136">**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي (UTC)**</span><span class="sxs-lookup"><span data-stu-id="d9961-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="d9961-137">[![نموذج العامل](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="d9961-138">**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="d9961-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="d9961-139">[![نموذج العامل](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="d9961-140">**Excel عبر OData**</span><span class="sxs-lookup"><span data-stu-id="d9961-140">**Excel Via OData**</span></span>

<span data-ttu-id="d9961-141">[![Excel عبر OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="d9961-142">**التشغيل المرحلي في DMF**</span><span class="sxs-lookup"><span data-stu-id="d9961-142">**DMF Staging**</span></span>

<span data-ttu-id="d9961-143">[![التشغيل المرحلي في DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="d9961-144">**تصدير DMF**</span><span class="sxs-lookup"><span data-stu-id="d9961-144">**DMF Export**</span></span>

<span data-ttu-id="d9961-145">[![التشغيل المرحلي في DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="d9961-146">**Excel عبر Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="d9961-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="d9961-147">[![Excel عبر Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="d9961-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="d9961-148">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d9961-148">See also</span></span>

[<span data-ttu-id="d9961-149">بيانات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="d9961-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="d9961-150">المناطق الزمنية المفضلة للمستخدم</span><span class="sxs-lookup"><span data-stu-id="d9961-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
