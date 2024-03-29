---
title: عرض نتائج أتمتة فاتورة المورد (معاينة)
description: توضح هذه المقالات كيفية عرض حالة فواتير المورد الموجودة في عملية الإرسال إلى سير العمل التلقائية.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895156"
---
# <a name="view-vendor-invoice-automation-results"></a>عرض نتائج التنفيذ التلقائي لفاتورة المورد

[!include [banner](../includes/banner.md)]

توضح هذه المقالات كيفية عرض حالة فواتير المورد الموجودة في عملية الإرسال إلى سير العمل التلقائية. ويتم الاحتفاظ بتفاصيل محفوظات الأتمتة لكل فاتورة مورد مستورده. وفقا للعمليات التجارية التي قمت بتنفيذها تلقائيا، تعرض صفحه **فواتير المورد المعلقة** قيمتي **حاله مطابقه الإيصال التلقائية** و **حالة الإرسال التلقائي إلى سير العمل**. يمكنك عرض التفاصيل وتقديم خطه للتركيز علي الفواتير التي فشلت في تنفيذ خطوه تلقائية. وبعد ذلك ، بعد تصحيح المشكلة، يمكنك استئناف العملية التلقائية للفاتورة التي تم استيرادها.

قبل ان تتمكن من تحرير فاتورة تم تسليمها، يجب إيقاف المعالجة التلقائية مؤقتا. إذا كان يجب إيقاف فاتورة في عمليه الإرسال إلى سير العمل تلقائيا، قم بتعيين **حقل تضمين في المعالجة التلقائية** إلى **لا** في الصفحة **فواتير الموردين**. وبعد ذلك لن يتم تشغيل الأتمتة حتى يتم تعيين **التضمين في المعالجة التلقائية** إلى **نعم**. يمكن إيقاف الفاتورة مؤقتا من الأتمتة إذا لم تكن في نظام سير العمل كما انها لا تستخدم من قبل العملية التلقائية.

إذا كانت الفاتورة المستوردة خاضعه لعمليه الإرسال إلى سير العمل، فيمكنك عرض قيمه **حاله الأتمتة** في الصفحة **فواتير المورد**. يتم تعقب الحالات التالية:

- **مضمن** – يتم تشغيل العمليات التلقائية التي تم تحديدها في الصفحة **محددات الحسابات الدائنة** بشكل صحيح ولكن لم يتم إكمالها بعد.
- **متوقف مؤقتا** – تم تشغيل العمليات التلقائية التي تم تحديدها في الصفحة **معلمات الحسابات الدائنة**، ولكن توجد خطوه واحده علي الأقل في العملية. يتم تطبيق الحالة **تم الإيقاف المؤقت** أيضا إذا تم تعيين الحقل **تضمين في المعالجة التلقائية** إلى **لا**. يمكنك عرض حالات الفشل عن طريق تحديد **عرض أحدث النتائج**.
- **في سير العمل** – تم إرسال الفاتورة المستوردة إلى نظام سير العمل، سواء كانت بواسطة عمليه الإرسال إلى سير العمل التلقائية أو يدويا.
- **إكمال سير العمل** – تم إكمال عمليه سير العمل للفاتورة التي تم استيرادها.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
