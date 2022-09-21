---
title: معاينة الإصدار 10.0.30 من Dynamics 365 Supply Chain Management (نوفمبر 2022)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في 10.0.30. Microsoft Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429113"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>معاينة الإصدار 10.0.30 من Dynamics 365 Supply Chain Management (نوفمبر 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا المقال الميزات الجديدة أو المتغيرة في إصدار المعاينة 10.0.30 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.1362، وهو يتوفر وفق الجدول التالي:

- **معاينة الإصدار:** سبتمبر 2022
- **التوفر العام للإصدار (تحديث ذاتي):** أكتوبر 2022
- **التوفر العام للإصدار (تحديث تلقائي):** نوفمبر 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تمت إضافتها إلى البنية بعد نشر هذا الموضوع.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| التصنيع | [مراقبه المعدات باستخدام معلومات الاستشعار لمستشعر](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [الصفحة الرئيسية لذكاء بيانات الاستشعار](../sensor-data-intelligence/sdi-home-page.md) | إدارة الميزات:<br>*الوظيفة الإضافية Sensor Data Intelligence (إصدار أولي)* |
| Warehouse management | عمليات الالتفاف متعدد المستويات لتطبيق Warehouse Management للأجهزة المحمولة <!-- KFM: Add link when RP updates --> | [تكوين منحنيات للخطوات في عناصر قائمه الجهاز المحمول](../warehousing/warehouse-app-detours.md) | إدارة الميزات:<br>*عمليات الالتفاف متعدد المستويات لتطبيق Warehouse Management للأجهزة المحمولة* |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. وتوفر كل واحدة منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطة الإصدار](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك).

إذا كنت ترغب في تشغيل أي من هذه الميزات أو إيقاف تشغيلها، فيجب عليك القيام بذلك في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | اسم الميزة في إدارة الميزات | معلومات إضافية |
|---|---|---|
| التحكم بالإنتاج | المعلومات المتاحة في صفحة "أوامر الإنتاج للإصدار‬" | يضيف عمودًا لكمية المخزون الفعلي للبند في قسم البنود في **إصدار أوامر الإنتاج** الصفحة. |
| إدارة النقل | تعيين الشحنات إلى أجزاء المسارات ذات الصلة | تعمل هذه الميزة علي تمكين النظام لأبورتيون تكاليف شحن الشحن بشكل أكثر دقه ، بما في ذلك التحميلات مع الشحنات المتعددة التي يتم تسليمها إلى وجات القطع المتنوعة عبر المسار الواحد. حيث يقوم بتعيين كل شحنه إلى جزء المسار الأكثر ملاءمة بناء علي عناوين الوجهة الخاصة بالشحنة والشريحة. وتقوم هذه الميزة بعد ذلك بحساب تكلفه شحن كل شحنه كنسبه إجمالي تكلفه الشحن الإجمالي ، استنادا إلى الوزن النسبي للشحنة والحجم والترافيليد والكمية والمسافة. تنطبق هذه الميزة فقط علي الشحنات المدارة باستخدام الوحدة النمطية لأداره النقل (TMS). |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.30 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.30 من تطبيقات التمويل والعمليات (نوفمبر 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من نسخة 10.0.29، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 1 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022](/dynamics365-release-plan/2022wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح المقال [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
