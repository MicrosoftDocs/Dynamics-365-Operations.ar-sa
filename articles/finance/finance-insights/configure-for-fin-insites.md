---
title: تكوين Finance Insights
description: تشرح هذه المقالة خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 07edea234839a477802e5cd875620509c8f92d69
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644104"
---
# <a name="configuration-for-finance-insights"></a>تكوين Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يجمع Finance insights بين وظائف من Microsoft Dynamics 365 Finance مع Dataverse وAzure وAI Builder لتوفير أدوات تنبؤ قوية لمؤسستك. تشرح هذه المقالة خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights. لإكمال الإجراءات الواردة في هذه المقالة بنجاح، يجب أن تتمتع بوصول كمسؤول النظام ومخصص النظام في [مركز إدارة Power Portal](https://admin.powerplatform.microsoft.com/)، ووصول كمسؤول النظام في Dynamics 365 Finance والوصول لإنشاء البيئات في Microsoft Dynamics ‎ Lifecycle Services‏(‏LCS‏)‎.

> [!NOTE]
> الإجراءات التالية لإعداد Finance Insights صالحة للإصدار 10.0.21 والإصدارات الأحدث من Dynamics 365 Finance.

## <a name="deploy-dynamics-365-finance"></a>نشر Dynamics 365 Finance

اتبع هذه الخطوات لنشر البيئات.

1. في LCS، قم بإنشاء أو تحديث بيئة Dynamics 365 Finance. تتطلب البيئة تطبيق الإصدار 10.0.21 أو إصدار أحدث.

    > [!NOTE]
    > يجب أن تكون البيئة بيئة عالية التوافر (HA). (يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. إذا كنت تقوم بتكوين Finance Insights في بيئة وضع حماية، فقد تضطر إلى نسخ بيانات الإنتاج إلى تلك البيئة قبل أن تنجح التوقعات. يستخدم نموذج التنبؤ سنوات متعددة من البيانات لبناء التوقعات. لا تحتوي بيانات العرض التوضيحي لشركة Contoso على بيانات تاريخية كافية لتدريب نموذج التنبؤ بشكل مناسب. 

## <a name="configure-your-azure-ad-tenant"></a>تكوين المستأجر Azure AD الخاص بك

يجب تكوين Azure Active Directory (Azure AD) بحيث يمكن استخدام من خلال Dataverse وتطبيقات Microsoft Power Platform. يتطلب هذا التكوين إما أن يتم تعيين الدور **مالك المشروع** أو الدور **مدير البيئة** إلى المستخدم في الحقل **دور أمان المشروع** في LCS.

تحقق من اكتمال الإعداد التالي:

- لديك حق الوصول بصفة **مسؤول النظام** و **مخصص النظام** في مركز إدارة Power Portal.
- يتم تطبيق ترخيص Dynamics 365 Finance أو ترخيص مكافئ على المستخدم الذي يقوم بتثبيت الوظيفة الإضافية Finance insights.
- يتم تسجيل تطبيقات Azure AD التالية في Azure AD.

    |  استمارة التقديم                             | معرف التطبيق                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    للتحقق من تسجيل التطبيق في Azure AD ، تحقق من **قائمه كافة التطبيقات**. لمزيد من التفاصيل ، راجع [عرض تطبيقات المؤسسة](/azure/active-directory/manage-apps/view-applications-portal).
  
    إذا لم يكن التطبيق مسجلا في Azure AD ، اتصل بالدعم.
  
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

1. في Dynamics 365 Finance.، انتقل إلى **إدارة النظام \> الإعداد \> التنفيذ التلقائي للعملية**.
2. في علامة التبويب **العمليات الخلفية**، ابحث عن **التحقق من حالة توفير Insights‬‏‫**، وحدد **تحرير**.
3. قم بتعيين حقل **التنفيذ التالي** إلى 30 دقيقة قبل الوقت الحالي.

   يجب أن يفرض هذا التغيير عملية **التحقق من حالة توفير Insights** للتشغيل على الفور.

   بعد عملية **التحقق من حالة توفير Insights** بنجاح، يمكنك تمكين ميزات Finance Insights في مساحة عمل **إدارة الميزات**.

> [!NOTE]
> إذا لم تعمل عملية **التحقق من حالة توفير Insights**، فانتقل إلى **إدارة النظام** > **الاستعلامات** > **الوظائف الدُفعية**. في الحقل **وظيفة نظام الاقتراع لأتمتة العملية**، قم بتغيير القيمة إلى **انتظار** لبدء العملية. 
> 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
