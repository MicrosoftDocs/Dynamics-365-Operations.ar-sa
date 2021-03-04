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
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529842"
---
# <a name="understand-date-and-time-fields"></a>فهم حقول التاريخ والوقت

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تعد حقول **التاريخ والوقت** مفهومًا أساسيًا في Dynamics 365 Human Resources. من الضروري فهم كيفية التعامل مع بيانات **التاريخ والوقت** في نماذج Dynamics 365 Human Resources، وCommon Data Service، والمصادر الخارجية.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>فهم الفرق بين أنواع بيانات حقل التاريخ والتاريخ والوقت

تحتوي حقول **التاريخ والوقت** على معلومات المنطقة الزمنية، بينما لا تحتوي حقول **التاريخ** على مثل هذه المعلومات. تعرض حقول **التاريخ** نفس المعلومات في أي موقع. عند إدخال تاريخ في حقل **التاريخ**، يكتب Human Resources نفس التاريخ في قاعدة البيانات.

عند عرض البيانات في حقل **التاريخ والوقت**، يقوم Human Resources بضبط التاريخ والوقت استنادًا إلى المنطقة الزمنية للمستخدم المعينة في نموذج **خيارات المستخدم** (**عام > الإعداد > خيارات المستخدم**). قد لا تكون معلومات التاريخ والوقت التي تقوم بإدخالها في الحقل هي نفسها المعلومات التي تمت كتابتها في قاعدة البيانات.

[![نموذج خيارات المستخدم](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>فهم حقول التاريخ والوقت في النماذج 

عند إدخال البيانات في حقل **التاريخ والوقت**، لا تكون البيانات المعروضة على الشاشة هي نفس البيانات المخزنة في قاعدة البيانات إذا لم يتم تعيين المنطقة الزمنية للمستخدم إلى التوقيت العالمي المتفق عليه (UTC). يتم دائمًا تخزين البيانات في حقول **التاريخ والوقت** بالتوقيت العالمي UTC.

[![نموذج العامل](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>فهم حقول التاريخ والوقت في قاعدة البيانات 

عندما يقوم Human Resources بكتابة قيمة **التاريخ والوقت** في قاعدة البيانات، فإنه يُخزّن البيانات بالتوقيت العالمي UTC. ويسمح ذلك للمستخدمين برؤية أي بيانات في حقل **التاريخ والوقت** بالنسبة إلى المنطقة الزمنية المحددة في خيارات المستخدم الخاصة بهم.
 
في المثال المبين أعلاه، وقت البدء هو نقطة زمنية، وليس تاريخًا محددًا. بتغيير المنطقة الزمنية للمستخدم المسجل دخوله من GMT + 12:00 إلى GMT UTC، يعرض نفس السجل الذي تم إنشاؤه 04/30/2019 12:00:00 بدلا من 05/01/2019 12:00:00.
  
في المثال المبين أدناه، أصبح توظيف الموظف 000724 نشطًا في نفس الوقت بغض النظر عن المنطقة الزمنية. سيكون الموظف نشطًا في 04/30/2019 في المنطقة الزمنية GMT، وهو نفسه 05/01/2019 في المنطقة الزمنية GMT + 12:00. يشير كل منهما إلى نفس النقطة في الوقت وليس كتاريخ معين. 

[![نموذج العامل](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>بيانات التاريخ والوقت في Data Management Framework، وExcel، وCommon Data Service، وPower BI 

تم تصميم كافة تقارير Data Management Framework، ووظائف Excel الإضافية، وCommon Data Service، وPower BI بحيث تتفاعل مع البيانات مباشرة على مستوى قاعدة البيانات. نظرًا لعدم وجود عميل لتعديل بيانات **التاريخ والوقت** إلى المنطقة الزمنية للمستخدم، تكون كافة قيم **التاريخ والوقت** بالتوقيت العالمي (UTC)، مما قد يؤدي إلى بعض الافتراضات غير الصحيحة عند إدخال البيانات أو عرضها.  
 
يتم افتراض بيانات **التاريخ والوقت** التي تم إرسالها من خلال DMF، أو Excel، أو Common Data Service على أنها بالتوقيت العالمي (UTC) من قِبل قاعدة البيانات. قد يتسبب هذا في حدوث التباس عند عدم عرض قيمة **التاريخ والوقت** المرسلة كما هو متوقع لأن المستخدم الذي يعرض البيانات ليس لديه المنطقة الزمنية للمستخدم المرسل للبيانات والمعينة بالتوقيت العالمي (UTC). 
 
يمكن أن يحدث نفس الشيء بالعكس عند تصدير البيانات. ويمكن أن تكون بيانات **التاريخ والوقت** الموجودة في كيان DMF الذي تم تصديره مختلفة عما يتم عرضه في عميل Dynamics. 
 
عند استخدام مصادر خارجية مثل DMF لعرض البيانات أو تأليفها، فإنه من الضروري الأخذ بالحسبان أن قيم **التاريخ والوقت** تعتبر افتراضيًا بالتوقيت العالمي (UTC) بغض النظر عن المنطقة الزمنية في كمبيوتر المستخدم أو إعدادات المنطقة الزمنية للمستخدم الحالي الخاصة بتلك البيانات. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>أمثلة عن نفس السجل الذي يتم عرضه في مناطق منتج مختلفة 

**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي (UTC)**

[![نموذج العامل](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي GMT +12:00** 

[![نموذج العامل](./media/worker-form4.png)](./media/worker-form4.png)

**Excel عبر OData**

[![Excel عبر OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**التشغيل المرحلي في DMF**

[![التشغيل المرحلي في DMF](./media/DMFStaging.png)](./media/DMFStaging.png)

**تصدير DMF**

[![التشغيل المرحلي في DMF](./media/DMFexport.png)](./media/DMFexport.png)

**Excel عبر Common Data Service**

[![Excel عبر Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>راجع أيضًا

[بيانات التاريخ والوقت](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[المناطق الزمنية المفضلة للمستخدم](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]