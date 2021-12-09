---
title: تكوين Finance Insights
description: يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.
author: ShivamPandey-msft
ms.date: 11/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6183e8a7500e9deff0ebf6b5dec8842ad4ca94cb
ms.sourcegitcommit: 6a9f068b59b62c95a507d1cc18b23f9fd80a859b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/20/2021
ms.locfileid: "7827018"
---
# <a name="configuration-for-finance-insights"></a>تكوين Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

تضم Finance insights الوظيفة من Microsoft Dynamics 365 Finance مع Dataverse وAzure و AI Builder لتوفير أدوات التنبؤ القوية لمؤسستك. يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights. لإكمال الإجراءات الواردة في هذا الموضوع بنجاح، يجب أن يكون لديك وصول مسؤول النظام ومخصص النظام في [مركز إدارة Power Portal](https://admin.powerplatform.microsoft.com/)، ووصول مسؤول النظام في Dynamics 365 Finance، والوصول لإنشاء البيئات في Microsoft Dynamics ‏Lifecycle Services ‏(LCS).

> [!NOTE]
> الإجراءات التالية لإعداد Finance Insights صالحة لإصدارات Dynamics 365 Finance، الإصدار 10.0.21، وإصدار أحدث.

## <a name="deploy-dynamics-365-finance"></a>نشر Dynamics 365 Finance

اتبع هذه الخطوات لنشر البيئات.

1. في LCS، أنشئ بيئة Dynamics 365 Finance أو قم بتحديثها. تتطلب البيئة تطبيق الإصدار 10.0.21 أو إصدار أحدث.

    > [!NOTE]
    > يجب أن تكون البيئة بيئة عالية التوافر (HA). (يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. إذا كنت تقوم بتكوين Finance Insights في بيئة وضع حماية، فقد تضطر إلى نسخ بيانات الإنتاج إلى تلك البيئة قبل أن تنجح التوقعات. يستخدم نموذج التنبؤ سنوات متعددة من البيانات لبناء التوقعات. لا تحتوي بيانات العرض التوضيحي لشركة Contoso على بيانات تاريخية كافية لتدريب نموذج التنبؤ بشكل مناسب. 

## <a name="configure-your-azure-ad-tenant"></a>تكوين المستأجر Azure AD الخاص بك

يجب تكوين Azure Active Directory (Azure AD) بحيث يمكن استخدام من خلال Dataverse وتطبيقات Microsoft Power Platform. يتطلب هذا التكوين إما أن يتم تعيين الدور **مالك المشروع** أو الدور **مدير البيئة** إلى المستخدم في الحقل **دور أمان المشروع** في LCS.

تحقق من اكتمال الإعداد التالي:

- لديك حق الوصول بصفة **مسؤول النظام** و **مخصص النظام** في مركز إدارة Power Portal.
- يتم تطبيق Dynamics 365 Finance أو الترخيص المكافئ على المستخدم الذي يقوم بتثبيت الوظيفة الإضافية في Finance insights.

يتم تسجيل تطبيقات Azure AD التالية في Azure AD.

|  استمارة التقديم                             | معرف التطبيق                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>تكوين Dataverse

استخدم هذه الخطوات لتكوين Dataverse لـ Finance Insights.

- في LCS، افتح صفحة البيئة، وتحقق من أن قسم **تكامل Power Platform** تم إعداده بالفعل.

    - في حالة إعداد Dataverse بالفعل، يجب إدراج اسم بيئة Dataverse المرتبط ببيئة Finance.
    - في حالة عدم إعداد Dataverse بعد، حدد **إعداد**. يمكن أن يستغرق إعداد بيئة Dataverse ما يصل إلى ساعة واحدة. عندما يتم اكتمال الإعداد بنجاح، يجب إدراج اسم بيئة Dataverse المرتبط ببيئة Finance.
    - في حالة إعداد هذا التكامل مع بيئة Microsoft Power Platform موجودة، اتصل بالمسؤول الخاص بك للتأكد من أن البيئة المرتبطة ليست في حالة التعطيل.

        وللحصول على المزيد من المعلومات، راجع [تمكين تكامل Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        للوصول إلى موقع المسؤول الخاص بـ Microsoft Power Platform، انتقل إلى <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>تكوين ‏الوظيفة الإضافية Finance insights

إذا كنت قد قمت بتثبيت الوظيفة الإضافية Finance Insights مسبقًا، فقم بإزالة تثبيتها قبل إكمال الإجراء التالي.

> [!NOTE]
> إذا قمت بالفعل بتثبيت الوظيفة الإضافية لبحيرة البيانات في LCS، فسيستخدمها Finance Insights لحفظ البيانات المطلوبة للتنبؤات. إذا لم تكن قد قمت بتثبيت الوظيفة الإضافية مستودع البيانات في LCS، فستقوم الوظيفة الإضافية Finance Insights بإنشاء مستودع بيانات مُدار لك.

اتبع الخطوات التالية لتثبيت الوظيفة الإضافية لـ Finance insights.

1. قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.
2. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
3. حدد الوظيفة الإضافية **Finance insights**.
4. وافق على البنود والشروط، ثم حدد **تثبيت**.

قد تستغرق الوظيفة الإضافية عدة دقائق لتثبيتها.

## <a name="one-last-thing"></a>يوجد شيء أخير...

بعد تثبيت الوظيفة الإضافية بنجاح، قد يستغرق الأمر ما يصل إلى ساعة قبل أن تتمكن من تمكين ميزات Finance Insights في مساحة عمل **إدارة الميزات** في Dynamics 365 Finance. إذا كنت لا تريد الانتظار كل هذا الوقت، يمكنك يدويًا تشغيل عملية **التحقق من حالة توفير Insights**. 

1. في Dynamics 365 Finance، انتقل إلى **إدارة النظام \> الإعداد \> التنفيذ التلقائي للعمية**.
2. في علامة التبويب **العمليات الخلفية**، ابحث عن **التحقق من حالة توفير Insights‬‏‫**، وحدد **تحرير**.
3. قم بتعيين حقل **التنفيذ التالي** إلى 30 دقيقة قبل الوقت الحالي.

   يجب أن يفرض هذا التغيير عملية **التحقق من حالة توفير Insights** للتشغيل على الفور.

   بعد عملية **التحقق من حالة توفير Insights** بنجاح، يمكنك تمكين ميزات Finance Insights في مساحة عمل **إدارة الميزات**.

## <a name="feedback-and-support"></a>الملاحظات والدعم

إذا كنت مهتمًا بتقديم الملاحظات أو تحتاج إلى الدعم، أرسل بريد إلكتروني إلى [‏‫Finance Insights (إصدار أولي)](mailto:fiap@microsoft.com)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
