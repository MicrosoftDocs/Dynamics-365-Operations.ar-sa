---
title: فهم حقول التاريخ والوقت
description: اعرف ما يجب أن تتوقعه عند استخدام حقول التاريخ والوقت في Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efda2b54f9228ac539e6ba2d18f85bf3ad15a6ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802421"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="d80ea-103">فهم حقول التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="d80ea-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d80ea-104">تعد حقول **التاريخ والوقت** مفهومًا أساسيًا في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d80ea-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d80ea-105">من الضروري فهم كيفية التعامل مع بيانات **التاريخ والوقت** في النماذج، وDataverse، والمصادر الخارجية.</span><span class="sxs-lookup"><span data-stu-id="d80ea-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="d80ea-106">فهم الفرق بين أنواع بيانات حقل التاريخ والتاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="d80ea-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="d80ea-107">تحتوي حقول **التاريخ والوقت** على معلومات المنطقة الزمنية، بينما لا تحتوي حقول **التاريخ** على مثل هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="d80ea-108">تعرض حقول **التاريخ** نفس المعلومات في أي موقع.</span><span class="sxs-lookup"><span data-stu-id="d80ea-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="d80ea-109">عند إدخال تاريخ في حقل **التاريخ**، يكتب Human Resources نفس التاريخ في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="d80ea-110">عند عرض البيانات في حقل **التاريخ والوقت**، يقوم Human Resources بضبط التاريخ والوقت استنادًا إلى المنطقة الزمنية للمستخدم المعينة في نموذج **خيارات المستخدم** (**عام > الإعداد > خيارات المستخدم**).</span><span class="sxs-lookup"><span data-stu-id="d80ea-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="d80ea-111">قد لا تكون معلومات التاريخ والوقت التي تقوم بإدخالها في الحقل هي نفسها المعلومات التي تمت كتابتها في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="d80ea-112">[![نموذج خيارات المستخدم](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="d80ea-113">فهم حقول التاريخ والوقت في النماذج</span><span class="sxs-lookup"><span data-stu-id="d80ea-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="d80ea-114">لا تكون بيانات **التاريخ والوقت** المعروضة على الشاشة هي نفس البيانات المخزنة في قاعدة البيانات إذا لم يتم تعيين المنطقة الزمنية للمستخدم إلى التوقيت العالمي المتفق عليه (UTC).</span><span class="sxs-lookup"><span data-stu-id="d80ea-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d80ea-115">يتم دائمًا تخزين البيانات في حقول **التاريخ والوقت** بالتوقيت العالمي UTC.</span><span class="sxs-lookup"><span data-stu-id="d80ea-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="d80ea-116">[![نموذج العامل UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="d80ea-117">فهم حقول التاريخ والوقت في قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="d80ea-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="d80ea-118">عندما يقوم Human Resources بكتابة قيمة **التاريخ والوقت** في قاعدة البيانات، فإنه يُخزّن البيانات بالتوقيت العالمي UTC.</span><span class="sxs-lookup"><span data-stu-id="d80ea-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="d80ea-119">ويسمح ذلك للمستخدمين برؤية أي بيانات في حقل **التاريخ والوقت** بالنسبة إلى المنطقة الزمنية المحددة في خيارات المستخدم الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="d80ea-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="d80ea-120">في المثال المبين أعلاه، وقت البدء هو نقطة زمنية، وليس تاريخًا محددًا.</span><span class="sxs-lookup"><span data-stu-id="d80ea-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="d80ea-121">بتغيير المنطقة الزمنية للمستخدم المسجل دخوله من GMT + 12:00 إلى GMT UTC، يعرض نفس السجل 04/30/2019 12:00:00 بدلا من 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="d80ea-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="d80ea-122">في المثال المبين أدناه، أصبح توظيف الموظف 000724 نشطًا في نفس الوقت بغض النظر عن المنطقة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="d80ea-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="d80ea-123">سيكون الموظف نشطًا في 04/30/2019 في المنطقة الزمنية GMT، وهو نفسه 05/01/2019 في المنطقة الزمنية GMT + 12:00.</span><span class="sxs-lookup"><span data-stu-id="d80ea-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="d80ea-124">يشير كل منهما إلى نفس النقطة في الوقت وليس كتاريخ معين.</span><span class="sxs-lookup"><span data-stu-id="d80ea-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="d80ea-125">[![نموذج العامل GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="d80ea-126">بيانات التاريخ والوقت في Data Management Framework، وExcel، وDataverse، وPower BI</span><span class="sxs-lookup"><span data-stu-id="d80ea-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="d80ea-127">تم تصميم كافة تقارير Data Management Framework، ووظائف Excel الإضافية، وDataverse، وPower BI بحيث تتفاعل مع البيانات مباشرة على مستوى قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="d80ea-128">نظرًا لعدم وجود عميل لتعديل بيانات **التاريخ والوقت** إلى المنطقة الزمنية للمستخدم، تكون كافة قيم **التاريخ والوقت** بالتوقيت العالمي (UTC)، مما قد يؤدي إلى بعض الافتراضات غير الصحيحة عند إدخال البيانات أو عرضها.</span><span class="sxs-lookup"><span data-stu-id="d80ea-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="d80ea-129">يتم افتراض بيانات **التاريخ والوقت** التي تم إرسالها من خلال DMF، أو Excel، أو Dataverse على أنها بالتوقيت العالمي (UTC) من قِبل قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="d80ea-130">قد يتسبب هذا في حدوث التباس عند عدم عرض قيمة **التاريخ والوقت** المرسلة كما هو متوقع لأن المستخدم الذي يعرض البيانات ليس لديه المنطقة الزمنية للمستخدم المرسل للبيانات والمعينة بالتوقيت العالمي (UTC).</span><span class="sxs-lookup"><span data-stu-id="d80ea-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="d80ea-131">يمكن أن يحدث نفس الشيء بالعكس عند تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="d80ea-132">ويمكن أن تكون بيانات **التاريخ والوقت** الموجودة في كيان DMF الذي تم تصديره مختلفة عن ما يتم عرضه في عميل Dynamics.</span><span class="sxs-lookup"><span data-stu-id="d80ea-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="d80ea-133">عند استخدام مصادر خارجية مثل DMF لعرض البيانات أو تأليفها، خذ بالحسبان أن قيم **التاريخ والوقت** تعتبر افتراضيًا بالتوقيت العالمي (UTC) بغض النظر عن المنطقة الزمنية في كمبيوتر المستخدم أو إعدادات المنطقة الزمنية للمستخدم الحالي الخاصة بتلك البيانات.</span><span class="sxs-lookup"><span data-stu-id="d80ea-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="d80ea-134">أمثلة عن نفس السجل الذي يتم عرضه في مناطق منتج مختلفة</span><span class="sxs-lookup"><span data-stu-id="d80ea-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="d80ea-135">**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي (UTC)**</span><span class="sxs-lookup"><span data-stu-id="d80ea-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="d80ea-136">[![تعيين نموذج العامل إلى UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="d80ea-137">**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="d80ea-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="d80ea-138">[![تعيين نموذج العامل إلى GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="d80ea-139">**Excel عبر OData**</span><span class="sxs-lookup"><span data-stu-id="d80ea-139">**Excel Via OData**</span></span>

<span data-ttu-id="d80ea-140">[![Excel عبر OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="d80ea-141">**التشغيل المرحلي في DMF**</span><span class="sxs-lookup"><span data-stu-id="d80ea-141">**DMF Staging**</span></span>

<span data-ttu-id="d80ea-142">[![التشغيل المرحلي في DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="d80ea-143">**تصدير DMF**</span><span class="sxs-lookup"><span data-stu-id="d80ea-143">**DMF Export**</span></span>

<span data-ttu-id="d80ea-144">[![تصدير DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="d80ea-145">**Excel عبر Dataverse**</span><span class="sxs-lookup"><span data-stu-id="d80ea-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="d80ea-146">[![Excel عبر Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="d80ea-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="d80ea-147">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d80ea-147">See also</span></span>

[<span data-ttu-id="d80ea-148">بيانات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="d80ea-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="d80ea-149">المناطق الزمنية المفضلة للمستخدم</span><span class="sxs-lookup"><span data-stu-id="d80ea-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]