---
title: تحسين استعلامات الجدول الظاهري لـ Dataverse
description: تحسين أداء استعلامات الجداول الظاهرية في Dataverse واستكشاف أخطاء هذا الأداء وإصلاحها
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f75176781620cd6f845c002876eba6e34d5793e7
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692215"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>تحسين استعلامات الجدول الظاهري لـ Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>إصدار

### <a name="overview"></a>نظرة عامة

عند استخدام الجداول الظاهرية في Dataverse لتطوير عمليات التكامل واتصالات البيانات الأخرى مع Dynamics 365 Human Resources، يمكنك مواجهة مشاكل في الأداء تتعلق بالاستعلامات في مقابل الجداول الظاهرية. يمكن أن يحدث تنفيذ الاستعلام البطيء عبر عملاء متعددين أو واجهات متعددة. على سبيل المثال، قد تواجه المشكلة في الحالات التالية:

- عند الاستعلام عن أحد الجداول الظاهرية من خلال واجهة API للويب في Dataverse
- عند إنشاء Power App في مقابل جدول ظاهري
- عند إنشاء تقرير Power BI على جدول ظاهري

تتوفر لدى جميع هذا الواجهات إمكانية إظهار المشكلة في الأداء.

أحد أسباب الأداء البطيء مع الجداول الظاهرية في Dataverse لـ Human Resources هو أعمدة المفاتيح الخارجية للجدول الظاهري المرتبط [بخصائص التنقل](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) في الجدول. عند إنشاء خصائص التنقل لجدول ظاهري، يُضاف عمود مفتاح خارجي تلقائيًا إلى الجدول لتمثيل قيمة المفتاح لعمود مفتاح الجدول الظاهري ذي الصلة. على سبيل المثال، يُضاف العمود **_mshr_fk_person_id_value** إلى الكيان **mshr_hcmworkerbaseentity** باستخدام خاصية المفتاح الخارجي من الكيان **mshr_dirpersonentity**. بسبب كيفية المحافظة على قيم أعمدة المفاتيح الخارجية هذه في جدول، قد يتسبب جلب القيم في إحداث تأثير سلبي على أداء استعلام في مقابل الجدول الظاهري.

### <a name="potential-symptoms"></a>الأعراض المحتملة

مثال يمكن فيه مشاهدة هذا التأثير في الاستعلامات في مقابل كيان العامل (**mshr_hcmworkerentity**) أو العامل الأساسي (**mshr_hcmworkerbaseentity**). قد تشاهد ملف بيان إصدار الأداء بنفس الطرق القليلة المختلفة:

- **تنفيذ بطيء للاستعلام**: قد يؤدي الاستعلام في مقابل الجدول الظاهري إلى إرجاع النتائج المتوقعة، ولكنه تنفيذ الاستعلام قد يستغرق وقتًا أطول من المتوقع.
- **انقضاء مهلة الاستعلام**: قد تنقضي مهلة الاستعلام مع ظهور رسالة الخطأ التالية: "تم الحصول على رمز مميز لاستدعاء التمويل والعمليات، ولكن التمويل والعمليات أرجع خطأ من النوع InternalServerError."
- **خطأ غير متوقع**: قد يرجع الاستعلام نوع الخطأ 400 مع الرسالة التالية: "حدث خطأ غير متوقع."

  ![نوع الخطأ 400 على HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **التقييد‬**: قد يستخدم الاستعلام موارد الخادم بشكل زائد، ويصبح عرضة للتقييد. في هذه الحالة، يرجع الاستعلام رسالة الخطأ التالية: "تم الحصول على رمز مميز لاستدعاء التمويل والعمليات، ولكن التمويل والعمليات أرجع خطأ من النوع 429." لمزيد من المعلومات حول التقييد في Human Resources، راجع [الأسئلة المتداولة حول التقييد](./hr-admin-integration-throttling-faq.md).

  ![نوع الخطأ 429 على HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>الحل

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>تقييد عدد الأعمدة المضمنة في استعلام البيانات

مع الجداول الظاهرية، أحد الأساليب الأكثر قدرة على تحسين أداء الاستعلام هو تقييد عدد الأعمدة المحددة في الاستعلام. الإرشاد العام حول تحسين أداء الاستعلام هو تحديد عدد الأعمدة المرتجعة في استعلامك بحيث يقتصر فقط على الخصائص التي تحتاج إليها. ويصح هذا الأمر بشكل خاص مع أعمده المفاتيح الخارجية في الجداول الظاهرية. إذا لم تكن بحاجه إلى القيم الموجودة في أعمدة المفاتيح الخارجية الخاصة بالتكامل أو التقرير، فعليك بناء الاستعلام لتحديد فقط الأعمدة التي تحتاج اليها، باستثناء أعمدة المفاتيح الخارجية.

#### <a name="selecting-columns-in-an-odata-query"></a>تحديد الأعمدة في استعلام OData

عند إجراء استعلام على جدول ظاهري خلال واجهة API الويب في Dataverse، يمكنك تقييد عدد الأعمدة المضمنة في الاستعلام باستخدام خيار استعلام النظام **$select**، وتحدد الأعمدة التي تريد نتائج مرتجعة لها. لتحسين الأداء إلى أقصى حد، استبعد أعمدة المفاتيح الخارجية (تلك الموجودة مع البادئة **_mshr_FK_**) من الاستعلام.

على سبيل المثال، سيتضمن الاستعلام التالي في مقابل الكيان **mshr_hcmworkerbaseentity** فقط الأعمدة المضمنة في بند خيار الاستعلام **$select**، باستثناء قيم المفاتيح الخارجية. ويوفر ذلك تحسينات ملحوظة في الأداء على استعلام يتضمن جميع أعمدة الجدول.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

تنطبق أيضًا التوصية الخاصة بتقييد عدد الأعمدة المحددة عند استخدام خيار الاستعلام **$expand** لتوسيع الاستعلام إلى الجداول الظاهرية ذات الصلة عبر خصائص التنقل. على سبيل المثال، يتضمن الاستعلام التالي أعمدة من الكيان **mshr_hcmworkerbaseentity** مع أعمدة موسعة من الكيان **mshr_dirpersonentity**. لاحظ أن خيار الاستعلام **$select** مضمن أيضًا في بند خيار الاستعلام **$expand**.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

عند استخدام هذه الطريقة لاسترداد البيانات باستخدام خيار الاستعلام **$select** في بند خيار الاستعلام **$expand**، سترى عادةً تحسينات أكبر في الأداء عندما تكون خاصية التنقل بين الكيانات علاقة متعدد إلى واحد. قد لا ترى نفس الانخفاض في وقت تنفيذ الاستعلام عند توسيع علاقة واحد إلى متعدد. لمزيد من المعلومات حول تعريف علامة الجداول الظاهرية في Dataverse، راجع [علاقات الجداول](/powerapps/maker/data-platform/create-edit-entity-relationships).

لمزيد من المعلومات حول استخدام خيارات استعلام النظام **$select** و **$expand** في واجهة API الويب في Dataverse، راجع [استرداد سجلات الكيان بواسطة استعلام](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>تحديد الأعمدة في Power BI

إذا واجهت أي إشارة من الإشارات التي ورد ذكرها سابقًا تتعلق ببطء الأداء عند إنشاء تقرير Power BI في مقابل جدول ظاهري في Dataverse، يمكنك تحسين الأداء باستبعاد أعمدة المفاتيح الخارجية من الأعمدة المحددة من الجدول للتقرير. على سبيل المثال، إذا كنت تستخدم Power BI Desktop لإنشاء تقرير في مقابل الكيان **mshr_hcmworkerbaseentity**، فيمكنك استخدام الخطوات التالية لتحديد الأعمدة التي تريد تضمينه في استعلام التقرير.

1. في Power BI Desktop، حدد **المزيد...** من القائمة المنسدلة **إحضار البيانات** على شريط الإجراء.
2. في نافذة **إحضار البيانات**، أدخل **Common Data Service** في مربع البحث، وحدد موصل **Common Data Service**، وحدد **اتصال**.
3. في حقل **Url‏‎ الخادم** في نافذة Common Data Service، أدخل URI المؤسسة لبيئة Dataverse وحدد **موافق**.
  
   ![أدخل URI لبيئة Dataverse الخاصة بك.](./media/PowerBIDataverseURLSetup.png)
  
4. في نافذة المتصفح، قم بتوسيع عقدة **الكيانات**.
5. في مربع البحث، أدخل **mshr_hcmworkerbaseentity**، وحدد الكيان.
6. حدد **تحويل البيانات**.
7. في نافذة Power Query Editor، حدد **المحرر المتقدم**.
8. في نافذة **المحرر المتقدم**، حدّث الاستعلام بحيث يبدو مماثلاً لما يلي، مع إضافة أعمدة إلى الصفيف أو إزالتها منه حسب الحاجة.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![حدّث الاستعلام في المحرر المتقدم في Power Query Editor.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. حدد **تم**.

   > [!NOTE]
   > إذا تلقيت في السابق خطأ من النوع 429 من الاستعلام قبل التحديث، فقد تحتاج إلى انتظار فترة لإعادة المحاولة قبل تحديث الاستعلام لإكماله بنجاح.

10. انقر فوق **إغلاق وتطبيق** على شريط إجراء Power Query Editor.

عندئذ يمكنك بدء بناء تقرير Power BI في مقابل الأعمدة المحددة من الجدول الظاهري.

#### <a name="selecting-columns-in-power-apps"></a>تحديد الأعمدة في Power Apps

بطريقة مماثلة لاستعلامات واجهات API الويب في Dataverse وفي Power BI، يمكنك تحسين أداء الاستعلام لتطبيقات Power Apps بالاستناد إلى الجداول الظاهرية في Dataverse باستثناء أعمدة الجداول ذات الصلة من تطبيقك. إذا تم تضمين أي أعمدة من جدول ذي صلة في صفحة، فإن عنوان URL الخاص بالطلب الذي تم إنشاؤه لإحضار البيانات سيتضمن خصائص المفاتيح الخارجية للجدول ذي الصلة. يؤدي ذلك، كما في أمثلة [تحديد الأعمدة في استعلام ODat](#selecting-columns-in-power-apps) أعلاه إلى تقليل الأداء من خلال التسبب في حدوث عمليات بحيث إضافية عن البيانات.

لحل هذه المشكلة، يمكنك التحقق من عدم تضمين حقول بيانات من الجداول ذات الصلة على أي نموذج بيانات في Power App.

1. في جزء طريقة العرض الشجرة، حدد نموذج البيانات للشاشة.
2. في جزء **الخصائص**، حدد **تحرير** على خاصية **الحقول**.
3. في جزء **البيانات**، تأكد من أن الحقول المحددة ليس حقول الجدول الظاهري لمصدر البيانات.

على سبيل المثال، إذا كان أحد حقول البيانات المضمنة في الصفحة في التطبيق يشير إلى جدول آخر، مثل **ThisItem.Worker.Name**، حيث **Worker** هو الجدول ذو الصلة، فهناك احتمال بحدوث أداء منخفض عند إحضار البيانات.

يمكنك استخدام [مراقبة Power Apps](/powerapps/maker/monitor-overview) للتأكد من تضمين فقط الأعمدة التي تحتاج إليها في الاستعلام للحصول على بيانات Power App. يمكنك عرض عنوان URL المكون لعمليات getRows للتأكد من أن الأعمدة التي حددتها لتطبيقك ستكون مثالية لاسترداد البيانات.

![استخدم مراقبة Power Apps لتحليل عملية getData.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>تصفية استعلام البيانات

هناك طريقة أخرى لتحسين أداء تنفيذ الاستعلام وهي تقييد عدد السجلات المرتجعة في نتائج الاستعلام. يمكنك القيام بذلك عن طريق تصفية النتائج كي تتلقي السجلات التي تحتاجها فقط.

راجع [تصفية النتائج](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) لمزيد من المعلومات حول تصفية بيانات الاستعلام.

### <a name="limiting-the-page-size-of-the-query"></a>تحديد حجم الصفحة للاستعلام

إذا كنت تعمل مع مجموعات بيانات كبيره ، يمكنك تقسيم نتائج الاستعلام إلى صفحات متعددة عن طريق أضافه `odata.maxpagesize`راس التفضيل إلى استعلامات البيانات.

لمزيد من المعلومات حول ترقيم الصفحات، راجع [تحديد عدد الكيانات التي سيتم إرجاعها في الصفحة](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>راجع أيضًا

- [تكوين جداول Dataverse الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md)
- [‏‫الأسئلة المتداولة حول الجداول الظاهرية في ‬‏‫Human Resources‬‏‫](hr-admin-virtual-entity-faq.md)
- [‏‫الأسئلة المتداولة حول التقييد](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
