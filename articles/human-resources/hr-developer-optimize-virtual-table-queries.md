---
title: تحسين استعلامات الجدول الظاهري لـ Dataverse
description: تحسين أداء استعلامات الجداول الظاهرية في Dataverse واستكشاف أخطاء هذا الأداء وإصلاحها
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8026abd5c3e0f9b78e8c016731fd7785490bc945
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891092"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="0d3cf-103">تحسين استعلامات الجدول الظاهري لـ Dataverse</span><span class="sxs-lookup"><span data-stu-id="0d3cf-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="0d3cf-104">إصدار</span><span class="sxs-lookup"><span data-stu-id="0d3cf-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="0d3cf-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="0d3cf-105">Overview</span></span>

<span data-ttu-id="0d3cf-106">عند استخدام الجداول الظاهرية في Dataverse لتطوير عمليات التكامل واتصالات البيانات الأخرى مع Dynamics 365 Human Resources، يمكنك مواجهة مشاكل في الأداء تتعلق بالاستعلامات في مقابل الجداول الظاهرية.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="0d3cf-107">يمكن أن يحدث تنفيذ الاستعلام البطيء عبر عملاء متعددين أو واجهات متعددة.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="0d3cf-108">على سبيل المثال، قد تواجه المشكلة في الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="0d3cf-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="0d3cf-109">عند الاستعلام عن أحد الجداول الظاهرية من خلال واجهة API للويب في Dataverse</span><span class="sxs-lookup"><span data-stu-id="0d3cf-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="0d3cf-110">عند إنشاء Power App في مقابل جدول ظاهري</span><span class="sxs-lookup"><span data-stu-id="0d3cf-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="0d3cf-111">عند إنشاء تقرير Power BI على جدول ظاهري</span><span class="sxs-lookup"><span data-stu-id="0d3cf-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="0d3cf-112">تتوفر لدى جميع هذا الواجهات إمكانية إظهار المشكلة في الأداء.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="0d3cf-113">أحد أسباب الأداء البطيء مع الجداول الظاهرية في Dataverse لـ Human Resources هو أعمدة المفاتيح الخارجية للجدول الظاهري المرتبط [بخصائص التنقل](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) في الجدول.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="0d3cf-114">عند إنشاء خصائص التنقل لجدول ظاهري، يُضاف عمود مفتاح خارجي تلقائيًا إلى الجدول لتمثيل قيمة المفتاح لعمود مفتاح الجدول الظاهري ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="0d3cf-115">على سبيل المثال، يُضاف العمود **_mshr_fk_person_id_value** إلى الكيان **mshr_hcmworkerbaseentity** باستخدام خاصية المفتاح الخارجي من الكيان **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="0d3cf-116">بسبب كيفية المحافظة على قيم أعمدة المفاتيح الخارجية هذه في جدول، قد يتسبب جلب القيم في إحداث تأثير سلبي على أداء استعلام في مقابل الجدول الظاهري.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="0d3cf-117">الأعراض المحتملة</span><span class="sxs-lookup"><span data-stu-id="0d3cf-117">Potential symptoms</span></span>

<span data-ttu-id="0d3cf-118">مثال يمكن فيه مشاهدة هذا التأثير في الاستعلامات في مقابل كيان العامل (**mshr_hcmworkerentity**) أو العامل الأساسي (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="0d3cf-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="0d3cf-119">قد تشاهد ملف بيان إصدار الأداء بنفس الطرق القليلة المختلفة:</span><span class="sxs-lookup"><span data-stu-id="0d3cf-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="0d3cf-120">**تنفيذ بطيء للاستعلام**: قد يؤدي الاستعلام في مقابل الجدول الظاهري إلى إرجاع النتائج المتوقعة، ولكنه تنفيذ الاستعلام قد يستغرق وقتًا أطول من المتوقع.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="0d3cf-121">**انقضاء مهلة الاستعلام**: قد تنقضي مهلة الاستعلام مع ظهور رسالة الخطأ التالية: "تم الحصول على رمز مميز لاستدعاء Finance and Operations، ولكن Finance and Operations أرجع خطأ من النوع InternalServerError."</span><span class="sxs-lookup"><span data-stu-id="0d3cf-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="0d3cf-122">**خطأ غير متوقع**: قد يرجع الاستعلام نوع الخطأ 400 مع الرسالة التالية: "حدث خطأ غير متوقع."</span><span class="sxs-lookup"><span data-stu-id="0d3cf-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![نوع الخطأ 400 على HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="0d3cf-124">**التقييد‬**: قد يستخدم الاستعلام موارد الخادم بشكل زائد، ويصبح عرضة للتقييد.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="0d3cf-125">في هذه الحالة، يرجع الاستعلام رسالة الخطأ التالية: "تم الحصول على رمز مميز لاستدعاء Finance and Operations، ولكن Finance and Operations أرجع خطأ من النوع 429."</span><span class="sxs-lookup"><span data-stu-id="0d3cf-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="0d3cf-126">لمزيد من المعلومات حول التقييد في Human Resources، راجع [الأسئلة المتداولة حول التقييد](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="0d3cf-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![نوع الخطأ 429 على HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="0d3cf-128">الدقة</span><span class="sxs-lookup"><span data-stu-id="0d3cf-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="0d3cf-129">تقييد عدد الأعمدة المضمنة في استعلام البيانات</span><span class="sxs-lookup"><span data-stu-id="0d3cf-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="0d3cf-130">مع الجداول الظاهرية، أحد الأساليب الأكثر قدرة على تحسين أداء الاستعلام هو تقييد عدد الأعمدة المحددة في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="0d3cf-131">الإرشاد العام حول تحسين أداء الاستعلام هو تحديد عدد الأعمدة المرتجعة في استعلامك بحيث يقتصر فقط على الخصائص التي تحتاج إليها.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="0d3cf-132">ويصح هذا الأمر بشكل خاص مع أعمده المفاتيح الخارجية في الجداول الظاهرية.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="0d3cf-133">إذا لم تكن بحاجه إلى القيم الموجودة في أعمدة المفاتيح الخارجية الخاصة بالتكامل أو التقرير، فعليك بناء الاستعلام لتحديد فقط الأعمدة التي تحتاج اليها، باستثناء أعمدة المفاتيح الخارجية.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="0d3cf-134">تحديد الأعمدة في استعلام OData</span><span class="sxs-lookup"><span data-stu-id="0d3cf-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="0d3cf-135">عند إجراء استعلام على جدول ظاهري خلال واجهة API الويب في Dataverse، يمكنك تقييد عدد الأعمدة المضمنة في الاستعلام باستخدام خيار استعلام النظام **$select**، وتحدد الأعمدة التي تريد نتائج مرتجعة لها.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="0d3cf-136">لتحسين الأداء إلى أقصى حد، استبعد أعمدة المفاتيح الخارجية (تلك الموجودة مع البادئة **_mshr_FK_**) من الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="0d3cf-137">على سبيل المثال، سيتضمن الاستعلام التالي في مقابل الكيان **mshr_hcmworkerbaseentity** فقط الأعمدة المضمنة في بند خيار الاستعلام **$select**، باستثناء قيم المفاتيح الخارجية.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="0d3cf-138">ويوفر ذلك تحسينات ملحوظة في الأداء على استعلام يتضمن جميع أعمدة الجدول.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="0d3cf-139">تنطبق أيضًا التوصية الخاصة بتقييد عدد الأعمدة المحددة عند استخدام خيار الاستعلام **$expand** لتوسيع الاستعلام إلى الجداول الظاهرية ذات الصلة عبر خصائص التنقل.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="0d3cf-140">على سبيل المثال، يتضمن الاستعلام التالي أعمدة من الكيان **mshr_hcmworkerbaseentity** مع أعمدة موسعة من الكيان **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="0d3cf-141">لاحظ أن خيار الاستعلام **$select** مضمن أيضًا في بند خيار الاستعلام **$expand**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="0d3cf-142">عند استخدام هذه الطريقة لاسترداد البيانات باستخدام خيار الاستعلام **$select** في بند خيار الاستعلام **$expand**، سترى عادةً تحسينات أكبر في الأداء عندما تكون خاصية التنقل بين الكيانات علاقة متعدد إلى واحد.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="0d3cf-143">قد لا ترى نفس الانخفاض في وقت تنفيذ الاستعلام عند توسيع علاقة واحد إلى متعدد.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="0d3cf-144">لمزيد من المعلومات حول تعريف علامة الجداول الظاهرية في Dataverse، راجع [علاقات الجداول](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="0d3cf-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="0d3cf-145">لمزيد من المعلومات حول استخدام خيارات استعلام النظام **$select** و **$expand** في واجهة API الويب في Dataverse، راجع [استرداد سجلات الكيان بواسطة استعلام](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="0d3cf-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="0d3cf-146">تحديد الأعمدة في Power BI</span><span class="sxs-lookup"><span data-stu-id="0d3cf-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="0d3cf-147">إذا واجهت أي إشارة من الإشارات التي ورد ذكرها سابقًا تتعلق ببطء الأداء عند إنشاء تقرير Power BI في مقابل جدول ظاهري في Dataverse، يمكنك تحسين الأداء باستبعاد أعمدة المفاتيح الخارجية من الأعمدة المحددة من الجدول للتقرير.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="0d3cf-148">على سبيل المثال، إذا كنت تستخدم Power BI Desktop لإنشاء تقرير في مقابل الكيان **mshr_hcmworkerbaseentity**، فيمكنك استخدام الخطوات التالية لتحديد الأعمدة التي تريد تضمينه في استعلام التقرير.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="0d3cf-149">في Power BI Desktop، حدد **المزيد...** من القائمة المنسدلة **إحضار البيانات** على شريط الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="0d3cf-150">في نافذة **إحضار البيانات**، أدخل **Common Data Service** في مربع البحث، وحدد موصل **Common Data Service**، وحدد **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="0d3cf-151">في حقل **Url‏‎ الخادم** في نافذة Common Data Service، أدخل URI المؤسسة لبيئة Dataverse وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![أدخل URI لبيئة Dataverse.](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="0d3cf-153">في نافذة المتصفح، قم بتوسيع عقدة **الكيانات**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="0d3cf-154">في مربع البحث، أدخل **mshr_hcmworkerbaseentity**، وحدد الكيان.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="0d3cf-155">حدد **تحويل البيانات**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="0d3cf-156">في نافذة Power Query Editor، حدد **المحرر المتقدم**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="0d3cf-157">في نافذة **المحرر المتقدم**، حدّث الاستعلام بحيث يبدو مماثلاً لما يلي، مع إضافة أعمدة إلى الصفيف أو إزالتها منه حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![تحديث الاستعلام في المحرر المتقدم في Power Query Editor](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="0d3cf-159">حدد **تم**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0d3cf-160">إذا تلقيت في السابق خطأ من النوع 429 من الاستعلام قبل التحديث، فقد تحتاج إلى انتظار فترة لإعادة المحاولة قبل تحديث الاستعلام لإكماله بنجاح.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="0d3cf-161">انقر فوق **إغلاق وتطبيق** على شريط إجراء Power Query Editor.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="0d3cf-162">عندئذ يمكنك بدء بناء تقرير Power BI في مقابل الأعمدة المحددة من الجدول الظاهري.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="0d3cf-163">تحديد الأعمدة في Power Apps</span><span class="sxs-lookup"><span data-stu-id="0d3cf-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="0d3cf-164">بطريقة مماثلة لاستعلامات واجهات API الويب في Dataverse وفي Power BI، يمكنك تحسين أداء الاستعلام لتطبيقات Power Apps بالاستناد إلى الجداول الظاهرية في Dataverse باستثناء أعمدة الجداول ذات الصلة من تطبيقك.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="0d3cf-165">إذا تم تضمين أي أعمدة من جدول ذي صلة في صفحة، فإن عنوان URL الخاص بالطلب الذي تم إنشاؤه لإحضار البيانات سيتضمن خصائص المفاتيح الخارجية للجدول ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="0d3cf-166">يؤدي ذلك، كما في أمثلة [تحديد الأعمدة في استعلام ODat](#selecting-columns-in-power-apps) أعلاه إلى تقليل الأداء من خلال التسبب في حدوث عمليات بحيث إضافية عن البيانات.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="0d3cf-167">لحل هذه المشكلة، يمكنك التحقق من عدم تضمين حقول بيانات من الجداول ذات الصلة على أي نموذج بيانات في Power App.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="0d3cf-168">في جزء طريقة العرض الشجرة، حدد نموذج البيانات للشاشة.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="0d3cf-169">في جزء **الخصائص**، حدد **تحرير** على خاصية **الحقول**.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="0d3cf-170">في جزء **البيانات**، تأكد من أن الحقول المحددة ليس حقول الجدول الظاهري لمصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="0d3cf-171">على سبيل المثال، إذا كان أحد حقول البيانات المضمنة في الصفحة في التطبيق يشير إلى جدول آخر، مثل **ThisItem.Worker.Name**، حيث **Worker** هو الجدول ذو الصلة، فهناك احتمال بحدوث أداء منخفض عند إحضار البيانات.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="0d3cf-172">يمكنك استخدام [مراقبة Power Apps](/powerapps/maker/monitor-overview) للتأكد من تضمين فقط الأعمدة التي تحتاج إليها في الاستعلام للحصول على بيانات Power App.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="0d3cf-173">يمكنك عرض عنوان URL المكون لعمليات getRows للتأكد من أن الأعمدة التي حددتها لتطبيقك ستكون مثالية لاسترداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![استخدم مراقبة Power Apps لتحليل عملية getData](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="0d3cf-175">تصفية استعلام البيانات</span><span class="sxs-lookup"><span data-stu-id="0d3cf-175">Filtering the data query</span></span>

<span data-ttu-id="0d3cf-176">هناك طريقة أخرى لتحسين أداء تنفيذ الاستعلام وهي تقييد عدد السجلات المرتجعة في نتائج الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="0d3cf-177">يمكنك القيام بذلك عن طريق تصفية النتائج كي تتلقي السجلات التي تحتاجها فقط.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="0d3cf-178">راجع [تصفية النتائج](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) لمزيد من المعلومات حول تصفية بيانات الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="0d3cf-179">تحديد حجم الصفحة للاستعلام</span><span class="sxs-lookup"><span data-stu-id="0d3cf-179">Limiting the page size of the query</span></span>

<span data-ttu-id="0d3cf-180">إذا كنت تعمل مع مجموعات بيانات كبيره ، يمكنك تقسيم نتائج الاستعلام إلى صفحات متعددة عن طريق أضافه `odata.maxpagesize`راس التفضيل إلى استعلامات البيانات.</span><span class="sxs-lookup"><span data-stu-id="0d3cf-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="0d3cf-181">لمزيد من المعلومات حول ترقيم الصفحات، راجع [تحديد عدد الكيانات التي سيتم إرجاعها في الصفحة](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="0d3cf-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="0d3cf-182">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="0d3cf-182">See also</span></span>

- [<span data-ttu-id="0d3cf-183">تكوين جداول Dataverse الظاهرية</span><span class="sxs-lookup"><span data-stu-id="0d3cf-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="0d3cf-184">‏‫الأسئلة المتداولة حول الجداول الظاهرية في ‬‏‫Human Resources‬‏‫</span><span class="sxs-lookup"><span data-stu-id="0d3cf-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="0d3cf-185">‏‫الأسئلة المتداولة حول التقييد</span><span class="sxs-lookup"><span data-stu-id="0d3cf-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]