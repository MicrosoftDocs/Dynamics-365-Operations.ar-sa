---
title: التعامل مع بيانات التاريخ والوقت في Microsoft Dynamics 365 for Talent
description: اعرف ما يجب أن تتوقعه عند استخدام حقول التاريخ والوقت في Microsoft Dynamics 365 for Talent. تمكّن من تكوين فهم واضح لما يجب توقعه عند التعامل مع بيانات التاريخ والوقت في نموذج في Dynamics 365 for Talent، أو مصدر خارجي أو Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4c652992272ed1a5aecbb4c78f0d11f077149d1
ms.sourcegitcommit: 46bded82aa072adfedcf443629c2adc69f512c09
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/26/2019
ms.locfileid: "1791192"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="69271-104">حقول التاريخ والوقت في Talent</span><span class="sxs-lookup"><span data-stu-id="69271-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69271-105">تعد حقول **التاريخ والوقت** مفهومًا أساسيًا في Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="69271-105">**Date and Time** fields are a fundamental concept in Dynamics 365 for Talent.</span></span> <span data-ttu-id="69271-106">من الضروري فهم كيفية التعامل مع بيانات **التاريخ والوقت** في نموذج Dynamics 365، وCommon Data Service، والمصادر الخارجية.</span><span class="sxs-lookup"><span data-stu-id="69271-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="69271-107">فهم الفرق بين أنواع بيانات حقل التاريخ والتاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="69271-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="69271-108">تحتوي حقول **التاريخ والوقت** على معلومات المنطقة الزمنية، بينما لا تحتوي حقول **التاريخ** على مثل هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="69271-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="69271-109">تعرض حقول **التاريخ** نفس المعلومات في أي موقع.</span><span class="sxs-lookup"><span data-stu-id="69271-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="69271-110">عند إدخال تاريخ في حقل **التاريخ**، يكتب Talent نفس التاريخ في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="69271-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="69271-111">عند عرض البيانات في حقل **التاريخ والوقت**، يقوم Talent بضبط التاريخ والوقت استنادًا إلى المنطقة الزمنية للمستخدم المعينة في نموذج **خيارات المستخدم** (**عام > الإعداد > خيارات المستخدم**).</span><span class="sxs-lookup"><span data-stu-id="69271-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="69271-112">قد لا تكون معلومات التاريخ والوقت التي تقوم بإدخالها في الحقل هي نفسها المعلومات التي تمت كتابتها في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="69271-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="69271-113">[![نموذج خيارات المستخدم](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="69271-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="69271-114">فهم حقول التاريخ والوقت في النماذج</span><span class="sxs-lookup"><span data-stu-id="69271-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="69271-115">عند إدخال البيانات في حقل **التاريخ والوقت**، لا تكون البيانات المعروضة على الشاشة هي نفس البيانات المخزنة في قاعدة البيانات إذا لم يتم تعيين المنطقة الزمنية للمستخدم إلى التوقيت العالمي المتفق عليه (UTC).</span><span class="sxs-lookup"><span data-stu-id="69271-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="69271-116">يتم دائمًا تخزين البيانات في حقول **التاريخ والوقت** بالتوقيت العالمي UTC.</span><span class="sxs-lookup"><span data-stu-id="69271-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="69271-117">[![نموذج العامل](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="69271-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="69271-118">فهم حقول التاريخ والوقت في قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="69271-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="69271-119">عندما يقوم Talent بكتابة قيمة **التاريخ والوقت** في قاعدة البيانات، فإنه يُخزّن البيانات بالتوقيت العالمي UTC.</span><span class="sxs-lookup"><span data-stu-id="69271-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="69271-120">ويسمح ذلك للمستخدمين برؤية أي بيانات في حقل**التاريخ والوقت** بالنسبة إلى المنطقة الزمنية المحددة في خيارات المستخدم الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="69271-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="69271-121">في المثال المبين أعلاه، وقت البدء هو نقطة زمنية، وليس تاريخًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="69271-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="69271-122">بتغيير المنطقة الزمنية للمستخدم المسجل دخوله من GMT + 12:00 إلى GMT UTC، يعرض نفس السجل الذي تم إنشاؤه 04/30/2019 12:00:00 بدلا من 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="69271-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="69271-123">في المثال المبين أدناه، أصبح توظيف الموظف 000724 نشطًا في نفس الوقت بغض النظر عن المنطقة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="69271-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="69271-124">سيكون الموظف نشطًا في 04/30/2019 في المنطقة الزمنية GMT، وهو نفسه 05/01/2019 في المنطقة الزمنية GMT + 12:00.</span><span class="sxs-lookup"><span data-stu-id="69271-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="69271-125">يشير كل منهما إلى نفس النقطة في الوقت وليس كتاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="69271-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="69271-126">[![نموذج العامل](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="69271-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="69271-127">بيانات التاريخ والوقت في Data Management Framework، وExcel، وCommon Data Service، وPower BI</span><span class="sxs-lookup"><span data-stu-id="69271-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="69271-128">تم تصميم كافة تقارير Data Management Framework، ووظائف Excel الإضافية، وCommon Data Service، وPower BI بحيث تتفاعل مع البيانات مباشرة على مستوى قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="69271-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="69271-129">نظرًا لعدم وجود عميل لتعديل بيانات **التاريخ والوقت** إلى المنطقة الزمنية للمستخدم، تكون كافة قيم **التاريخ والوقت** بالتوقيت العالمي (UTC)، مما قد يؤدي إلى بعض الافتراضات غير الصحيحة عند إدخال البيانات أو عرضها.</span><span class="sxs-lookup"><span data-stu-id="69271-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="69271-130">يتم افتراض بيانات **التاريخ والوقت** التي تم إرسالها من خلال DMF، أو Excel، أو Common Data Service على أنها بالتوقيت العالمي (UTC) من قِبل قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="69271-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="69271-131">قد يتسبب هذا في حدوث التباس عند عدم عرض قيمة **التاريخ والوقت** المرسلة كما هو متوقع لأن المستخدم الذي يعرض البيانات ليس لديه المنطقة الزمنية للمستخدم المرسل للبيانات والمعينة بالتوقيت العالمي (UTC).</span><span class="sxs-lookup"><span data-stu-id="69271-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="69271-132">يمكن أن يحدث نفس الشيء بالعكس عند تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="69271-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="69271-133">ويمكن أن تكون بيانات **التاريخ والوقت** الموجودة في كيان DMF الذي تم تصديره مختلفة عما يتم عرضه في عميل Dynamics.</span><span class="sxs-lookup"><span data-stu-id="69271-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="69271-134">عند استخدام مصادر خارجية مثل DMF لعرض البيانات أو تأليفها، فإنه من الضروري الأخذ بالحسبان أن قيم **التاريخ والوقت** تعتبر افتراضيًا بالتوقيت العالمي (UTC) بغض النظر عن المنطقة الزمنية في كمبيوتر المستخدم أو إعدادات المنطقة الزمنية للمستخدم الحالي الخاصة بتلك البيانات.</span><span class="sxs-lookup"><span data-stu-id="69271-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="69271-135">أمثلة عن نفس السجل الذي يتم عرضه في مناطق منتج مختلفة</span><span class="sxs-lookup"><span data-stu-id="69271-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="69271-136">**Talent مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي (UTC)**</span><span class="sxs-lookup"><span data-stu-id="69271-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="69271-137">[![نموذج العامل](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="69271-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="69271-138">**Talent مع منطقة زمنية للمستخدم معينة وفق GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="69271-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="69271-139">[![نموذج العامل](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="69271-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="69271-140">**Excel عبر OData**</span><span class="sxs-lookup"><span data-stu-id="69271-140">**Excel Via OData**</span></span>

<span data-ttu-id="69271-141">[![Excel عبر OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="69271-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="69271-142">**التشغيل المرحلي في DMF**</span><span class="sxs-lookup"><span data-stu-id="69271-142">**DMF Staging**</span></span>

<span data-ttu-id="69271-143">[![التشغيل المرحلي في DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="69271-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="69271-144">**تصدير DMF**</span><span class="sxs-lookup"><span data-stu-id="69271-144">**DMF Export**</span></span>

<span data-ttu-id="69271-145">[![التشغيل المرحلي في DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="69271-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="69271-146">**Excel عبر Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="69271-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="69271-147">[![Excel عبر Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="69271-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="69271-148">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="69271-148">See also</span></span>

[<span data-ttu-id="69271-149">بيانات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="69271-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="69271-150">المناطق الزمنية المفضلة للمستخدم</span><span class="sxs-lookup"><span data-stu-id="69271-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
