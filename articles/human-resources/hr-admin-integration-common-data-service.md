---
title: تكوين تكامل Dataverse
description: يُمكنك تشغيل التكامل بين Microsoft Dataverse وDynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة جدول للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111382"
---
# <a name="configure-dataverse-integration"></a>تكوين تكامل Dataverse

يُمكنك تشغيل التكامل بين Microsoft Dataverse وDynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة جدول للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.

> [!NOTE]
> لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

عند إيقاف تشغيل التكامل، يُمكن للمستخدمين إجراء تغييرات في Human Resources أو Dataverse، ولكن لا تتم مزامنة هذه التغييرات بين البيئتين.

بشكل افتراضي، يكون التكامل بين Human Resources وDataverse متوقفًا عن التشغيل.

قد ترغب في إيقاف تشغيل التكامل في هذه الحالات:

- تقوم بتعبئة البيانات من خلال Data Management Framework ويجب عليك استيراد البيانات عدة مرات للوصول إلى حالة صحيحة.

- توجد مشاكل في البيانات إما في Human Resources أو Dataverse. إذا قمت بإيقاف تشغيل التكامل، يُمكنك حذف سجل في إحدى البيئات دون حذفه في الآخر. عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة السجل الموجود في البيئة التي لم يتم حذفه فيها مرة أخرى إلى البيئة التي تم حذفه فيها. تبدأ المزامنة في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Dataverse المفقود**.

> [!WARNING]
> عند إيقاف تشغيل تكامل البيانات، تأكد من أنك لم تقم بتحرير نفس السجل في كلتا البيئتين. عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة آخر سجل قمت بتحريره. وبالتالي، إذا لم تقم بإجراء نفس التغييرات على السجل في كلا البيئتين، فقد يؤدي ذلك إلى فقد البيانات.

## <a name="access-the-dataverse-integration-page"></a>الوصول إلى صفحة تكامل Dataverse

1. في مثيل Human Resources الذي ترغب في عرض أو تكوين إعدادات للتكامل مع Dataverse فيه، حدد التجانب **إدارة النظام**.

    [![تجانب إدارة النظام](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. حدد علامة التبويب **الارتباطات**.

    [![علامة التبويب ارتباطات](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. تحت **عمليات التكامل**، حدد **تكوين Dataverse**.

    [![ارتباط تكوين Dataverse ](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>تشغيل تكامل البيانات بين Human Resources و Dataverse أو إيقاف تشغيله.

- لتشغيل التكامل، قم بتعيين خيار **تمكين تكامل Dataverse** إلى  إلى **نعم** في صفحة **تكامل Microsoft Dataverse**.

    > [!NOTE]
    > عند تشغيل التكامل، سوف تتم مزامنة البيانات في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Dataverse المفقود**. يجب أن تكون كافة البيانات متاحة بعد اكتمال الوظيفة الدفعية.

- لإيقاف تشغيل التكامل، قم بتعيين الخيار إلى **لا**.

[![تشغيل تكامل Dataverse أو إيقاف تشغيله](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> نوصي بضرورة إيقاف تشغيل تكامل Dataverse أثناء تنفيذ مهام ترحيل البيانات. بإمكان تحميلات البيانات الكبيرة أن تؤثر على الأداء بشكل ملحوظ. على سبيل المثال، قد يستغرق تحميل 2000 عامل ساعات متعددة عند تمكين التكامل، وأقل من ساعة عند تعطيله. الأرقام المتوفرة في هذا المثال هي لأغراء العرض التوضيحي فقط. يمكن أن يختلف مقدار الوقت الدقيق الذي تستغرقه عملية استيراد السجلات بشكل كبير استنادًا إلى العديد من العوامل.

## <a name="view-data-integration-details"></a>عرض تفاصيل تكامل البيانات

في علامة التبويب السريعة **الإدارة** في صفحة **تكامل Microsoft Dataverse**، يُمكنك رؤية كيف ترتبط البنود ببعضها بين Human Resources وDataverse.

- لعرض الصفوف الخاصة بأحد الجداول، حدد الجدول في حقل **جدول Dataverse** تعرض الشبكة كافة الصفوف المرتبطة بالجدول المُحدد.

> [!NOTE]
> حاليًا، لا يتم سرد كافة جداول Dataverse. تظهر فقط الجداول التي تدعم استخدام الحقول المخصصة في الشبكة. تتوفر الجداول الجديدة من خلال الإصدارات المستمرة لـ Human Resources.

تتضمن الشبكة الحقول التالية:

- **جدول Dataverse** – اسم الجدول في Dataverse.
- **مرجع جدول Dataverse** – المعرف الذي يستخدمه Dataverse لتعريف سجل. تُكافئ هذه القيمة قيمة **RecId** لـ Human Resourcesـ. يُمكنك العثور على المُعرف عندما تقوم بفتح جدول Dataverse في Microsoft Excel.
- **اسم كيان Human Resources** - آخر كيان Human Resources تمت مزامنة بياناته إلى Dataverse. يمكن أن يكون للكيان إما بادئة Dataverse أو بادئة أخرى.
- **مرجع Human Resources** - قيمة **RecId** المقترنة بالسجل في Human Resources.
- **محذوف من Dataverse** – قيمة تشير إلى ما إذا كان الصف قد تم حذفه من Dataverse أم لا.

> [!NOTE]
> السجلات في Human Resources التي تتوافق مع الصفوف في Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>إزالة اقتران سجل Human Resources من صف Dataverse

إذا واجهت مشاكل خلال مزامنة البيانات بين Human Resources و Dataverse، فقد تكون قادرًا على حلها عن طريق مسح التعقب والسماح بإعادة مزامنة جدول التعقب. إذا قمت بإزالة الاقتران، ثم قمت بتغيير صف أو حذفه في Dataverse، فلن تتم مزامنة التغييرات مع Human Resources. إذا قمت بإجراء تغييرات في Human Resources، يتم إنشاء سجل تعقب جديد، ويتم تحديث الصف في Dataverse.

- لإزالة اقتران سجل Human Resources و صف Dataverse، حدد الجدول في حقل **جدول Dataverse**، ثم حدد **مسح معلومات التعقب**.

[![مسح معلومات التعقب](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

لتشغيل مزامنة كاملة على الجدول بعد مسح التتبع، راجع الإجراء التالي.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>مزامنة جدول بين Human Resources وDataverse

استخدم هذا الإجراء في الحالات التالية:

- يستغرق ظهور التغييرات من Dataverse في Human Resources وقتًا طويلاً.

- يجب تحديث جدول التعقب بعد مسح التعقب.

لتشغيل مزامنة كاملة على جدول بين Human Resources وDataverse:

1. حدد نوع الجدول في الحقل **جدول Dataverse**.

2. حدد **المزامنة الآن**.

[![تشغيل مزامنة كاملة](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>راجع أيضًا

[جداول Dataverse](hr-developer-entities.md)<br>
[تكوين جداول Dataverse الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[الأسئلة المتداولة حول الجداول الظاهرية في Human Resources](hr-admin-virtual-entity-faq.md)<br>
[ما هو Microsoft Dataverse؟](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[تحديثات المصطلحات](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
