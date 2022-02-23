---
title: تصدير البيانات من Attract وOnboard
description: تصدير البيانات من Dynamics 365 Talent - Attract وOnboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460155"
---
# <a name="export-data-from-attract-and-onboard"></a>تصدير البيانات من Attract وOnboard

[!include [banner](includes/banner.md)]

كما تم الإعلان عنه في [إيقاف العمل بتطبيقات Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)، نحن بصدد إيقاف العمل بتطبيق Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard في 1 فبراير 2022. للمساعدة في عملية الترحيل إلى منتج آخر، يوفر التطبيقان الآن قدرات تصدير البيانات.

## <a name="export-data-from-attract"></a>تصدير البيانات من Attract

يمكنك تصدير بياناتك من دون تقييد الوصول إلى بيئتك. قد ترغب في القيام بذلك لأغراض الاختبار أو لفهم بنية بياناتك. عندما تصبح جاهزًا للترحيل، قيّد الوصول إلى بيئة Attract باستخدام الإرشادات بعد هذا الاجراء. تأكد من تصدير بياناتك مرة أخرى. 

1. الانتقال إلى [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. ضمن **تصدير البيانات**، حدد **طلب تصدير البيانات**.

   ![[طلب تصدير بيانات من Attract‎](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. عند ظهور مربع الرسالة **طلبك قيد المراجعة**، حدد **موافق**. بإمكان عملية تصدير البيانات أن تستغرق 20 دقيقة 20 استنادًا إلى حجم التصدير.

4. عند اكتمال التصدير، حدد الزر **تنزيل** بجواره. 

   >[!NOTE]
   >تتوفر كافة عمليات تصدير البيانات لسبعه أيام تنتهي عندها صلاحية ارتباط **التنزيل**.</br>
   
يحتوي ارتباط التنزيل على ملف zip. مع بيانات Attract، بما في ذلك المجلدات التالية:

| اسم المجلد | ‏‏الوصف |
| --- | --- |
| إعدادات المسؤول | تكوينات مركز إدارة Attract. |
| المرشحون | جميع المرشحين الذين تمت اضافتهم إلى المهام أو تجمعات المواهب. |
| قوالب البريد الإلكتروني | جميع قوالب البريد الكتروني التي تم تكوينها للبيئة. |
| قوالب حزم عروض الوظائف | جميع قوالب حزم عروض الوظائف التي تم إنشاؤها، بالإضافة إلى التكوينات المقترنة بها. |
| مجموعات قواعد عروض الوظائف |  جميع ملفات مجموعات القواعد التي تم تحميلها لإدارة العروض. |
| قوالب عروض الوظائف | جميع قوالب مستندات عروض الوظائف التي تم إنشاؤها للبيئة. |
| فرص التوظيف | جميع الوظائف التي تم إنشاؤها. لا يتم تصدير الوظائف المحذوفة. تحتوي المجلدات الفرعية على طلب المرشحين، مع مجلدات فرعية لمرفقات طلبات المرشحين وحزم عروض الوظائف، حيث كان ذلك ممكنًا. |
| قوالب فرص التوظيف | قوالب عمليات التوظيف التي تم تكوينها للبيئة. |
| مجموعات المواهب | جميع مجموعات المواهب‬‬ التي تم إنشاؤها وقوائم المساهمين الخاصة بها وقوائم المرشحين لمجموعات المواهب. |
| العاملون | قائمة بجميع العاملين الموجودين في البيئة، بالإضافة إلى أدوارهم. |
| (المجلد الجذر) | ملف مخطط JSON يصف حقول بنية البيانات. |

### <a name="restrict-access-to-attract"></a>تقييد الوصول إلى Attract

عندما تصبح جاهزًا للترحيل، قيّد وصول الأشخاص من غير المسولين إلى بيئة Attract وتصدير بياناتك.

>[!IMPORTANT]
>يعتبر تقييد الوصول إلى بيئة Attract دائمًا ولا يمكن التراجع عنه. إذا أردت تمكين المستخدمين من غير المسؤولين من مواصلة الوصول إلى بيئتك، فعليك تخطي هذه الخطوة.

1. الانتقال إلى [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. لمنع وصول مستخدمين من غير المسؤولين إلى بيئة Attract، حدد **تقييد الوصول الآن** ضمن **تقييد الوصول إلى هذا التطبيق**. يؤدي أيضًا تقييد الوصول إلى إلغاء نشر أي وظائف نشطة تم نشرها.

   ![[تقييد وصول مستخدمين من غير المسؤولين إلى Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. عندما يظهر التحذير **هذا تغيير دائم**، حدد **تقييد الوصول** لمنع وصول مستخدمين من غير المسؤولين إلى هذه البيئة. إذا لم تكن جاهزًا لإكمال هذه الخطوة، فحدد **إلغاء**.

   ![[تحذير بأن تقييد الوصول هو تغيير دائم](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >بإمكان المسؤولين متابعة الوصول إلى صفحة تصدير البيانات وتقرير الشخص بعد تقييد الوصول إلى بيئة Attract.

## <a name="export-data-from-onboard"></a>تصدير البيانات من Onboard

عندما تصبح جاهزًا، يمكنك تحميل القوالب والأدلة وبيانات المرشحين من Onboard.

1. الانتقال إلى [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. ضمن **تصدير البيانات**، حدد **طلب تصدير البيانات**. 

   ![[طلب تصدير بيانات من Onboard‎‎](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. عند ظهور مربع الرسالة **طلبك قيد المراجعة**، حدد **موافق**. بإمكان عملية تصدير البيانات أن تستغرق 20 دقيقة 20 استنادًا إلى حجم التصدير.

4. عند اكتمال التصدير، حدد الزر **تنزيل** بجواره. 

   ![[تنزيل تصدير البيانات من Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >يتوفر تصدير البيانات لمدة سبعة أيام. بعد سبعة أيام، تنتهي صلاحية ارتباط **التنزيل**، ويجب أن تطلب عملية تصدير جديدة إذا احتجت إلى تنزيل بياناتك من جديد. عندما تبدأ عملية تصدير جديدة للبيانات، ستنتهي صلاحية التنزيلات الموجودة بعد نجاح عملية التصدير الجديدة.

ملف التنزيل عبارة عن ملف zip. يحتوي علي:

- مجلد **قوالب** يحتوي على قوالب Onboard بتنسيق مستند Word.

- مجلد **أدلة** الذي يحتوي على أدلة Onboard بتنسيق مستند Word.

## <a name="see-also"></a>راجع أيضًا

[إيقاف العمل بتطبيقات Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)