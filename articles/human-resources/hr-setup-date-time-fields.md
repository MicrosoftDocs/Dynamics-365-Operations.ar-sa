---
title: فهم حقول التاريخ والوقت
description: يشرح هذا الموضوع ما يمكن توقعه عند استخدام حقلي التاريخ والوقت في Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c81155f0c5150af44982f224c8eca2026a78ee7
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060879"
---
# <a name="understand-date-and-time-fields"></a>فهم حقول التاريخ والوقت

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



حقول **التاريخ والوقت** عبارة عن مفهوم أساسي في Microsoft Dynamics 365 Human Resources. من المهم أن تفهم كيفية التعامل مع بيانات **التاريخ والوقت** على الصفحات، في Dataverse، وفي المصادر الخارجية.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>فهم الفرق بين أنواع بيانات حقل التاريخ والتاريخ والوقت

تحتوي حقول **التاريخ والوقت** على معلومات المنطقة الزمنية، بينما لا تحتوي حقول **التاريخ** على مثل هذه المعلومات. تعرض حقول **التاريخ** نفس المعلومات في أي موقع. عند إدخال تاريخ في حقل **التاريخ**، تتم كتابة نفس التاريخ في قاعدة البيانات.

عند عرض البيانات في حقل **التاريخ والوقت**، يتم ضبط التاريخ والوقت بناءً على المنطقة الزمنية للمستخدم التي تم تحديدها في صفحة **خيارات المستخدم** (**عام \> إعداد \> خيارات المستخدم**). قد لا تكون معلومات التاريخ والوقت التي تدخلها في الحقل هي نفسها المعلومات المكتوبة في قاعدة البيانات.

[![صفحة خيارات المستخدم.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>فهم حقول التاريخ والوقت في الصفحات 

لا تكون بيانات **التاريخ والوقت** المعروضة على الشاشة هي نفس البيانات المخزنة في قاعدة البيانات إذا لم يتم تعيين المنطقة الزمنية للمستخدم إلى التوقيت العالمي المتفق عليه (UTC). يتم دائمًا تخزين البيانات في حقول **التاريخ والوقت** بالتوقيت العالمي UTC.

[![صفحه العمال UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>فهم حقول التاريخ والوقت في قاعدة البيانات 

عندما تتم كتابة قيمة **التاريخ والوقت** في قاعدة البيانات، فإنه يتم تخزين البيانات كـ UTC. ولذلك، يمكن للمستخدمين رؤية أي بيانات **تاريخ ووقت** بالنسبة إلى المنطقة الزمنية المحددة في خيارات المستخدم الخاصة بهم.
 
في المثال المبين أعلاه، وقت البدء هو نقطة زمنية، وليس تاريخًا محددًا. بتغيير المنطقة الزمنية للمستخدم المسجل دخوله من GMT + 12:00 إلى GMT UTC، يعرض نفس السجل 04/30/2019 12:00:00 بدلا من 05/01/2019 12:00:00.

في المثال المبين أدناه، أصبح توظيف الموظف 000724 نشطًا في نفس الوقت بغض النظر عن المنطقة الزمنية. سيكون الموظف نشطًا في 04/30/2019 في المنطقة الزمنية GMT، وهو نفسه 05/01/2019 في المنطقة الزمنية GMT + 12:00. يشير كل منهما إلى نفس النقطة في الوقت وليس كتاريخ معين. 

[![صفحه العمال GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>بيانات التاريخ والوقت في Data Management Framework، وExcel، وDataverse، وPower BI 

تم تصميم كافة تقارير Data Management Framework ‏(DMF)، ووظائف Excel الإضافية، وDataverse، وPower BI بحيث تتفاعل مع البيانات مباشرة على مستوى قاعدة البيانات. نظرًا لعدم وجود عميل لتعديل بيانات **التاريخ والوقت** إلى المنطقة الزمنية للمستخدم، تكون كافة قيم **التاريخ والوقت** بالتوقيت العالمي (UTC)، مما قد يؤدي إلى بعض الافتراضات غير الصحيحة عند إدخال البيانات أو عرضها.
 
عند إرسال بيانات **التاريخ والوقت** من خلال DMF، أو Excel، أو Dataverse، تفترض قاعدة البيانات أنها بتوقيت UTC. ومع ذلك، إذا لم يكن المستخدمون الذين يعرضون البيانات قد تم تعيين المنطقة الزمنية للمستخدم الخاصة بهم إلى UTC، فلن تظهر قيمة **التاريخ والوقت** بالشكل المتوقع، وقد يصاب المستخدمون بالارتباك. 
 
يمكن أن يحدث نفس الشيء بالعكس عند تصدير البيانات. ويمكن أن تكون بيانات **التاريخ والوقت** الموجودة في كيان DMF الذي تم تصديره مختلفة عن ما يتم عرضه في عميل Dynamics. 
 
عند استخدام مصادر خارجية مثل DMF لعرض البيانات أو تأليفها، خذ بالحسبان أن قيم **التاريخ والوقت** تعتبر افتراضيًا بالتوقيت العالمي (UTC) بغض النظر عن المنطقة الزمنية في كمبيوتر المستخدم أو إعدادات المنطقة الزمنية للمستخدم الحالي الخاصة بتلك البيانات. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>أمثلة عن نفس السجل الذي يتم عرضه في مناطق منتج مختلفة 

**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي (UTC)**

[![تعيين صفحة العامل إلى UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources مع منطقة زمنية للمستخدم معينة بالتوقيت العالمي GMT +12:00** 

[![تعيين صفحة العامل إلى GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel عبر OData**

[![Excel عبر OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**التشغيل المرحلي في DMF**

[![التشغيل المرحلي في DMF.](./media/DMFStaging.png)](./media/DMFStaging.png)

**تصدير DMF**

[![تصدير DMF.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel عبر Dataverse**

[![Excel عبر Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>راجع أيضًا

[بيانات التاريخ والوقت](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[المناطق الزمنية المفضلة للمستخدم](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
