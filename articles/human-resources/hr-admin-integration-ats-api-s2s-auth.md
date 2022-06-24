---
title: مصادقة خادم إلى خادم لواجهة API لتكامل نظام تعقب مقدم الطلب‬ (ATS)
description: توضح هذه المقالة كيفية إعداد مصادقة خادم إلى خادم للتكاملات مقابل واجهة API لتكامل نظام تعقب مقدم الطلب‬ (ATS) في Dynamics 365 Human Resources.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: de3dc29c5366996276c02576eba27f7e831e4ccf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879355"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>مصادقة خادم إلى خادم لواجهة API لتكامل نظام تعقب مقدم الطلب‬ (ATS)


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيفية إعداد مصادقة خادم إلى خادم لتكاملات التطبيق مقابل واجهة API لتكامل نظام تعقب مقدم الطلب‬ (ATS) في Dynamics 365 Human Resources . هناك بضع طبقات من الأمان يجب إدارتها لمدير الخدمة للحصول على حق الوصول إلى جدول Microsoft Dataverse الظاهري والبيانات المرتبطة. يجب أن يتم منح المستخدم صلاحية الوصول إلى جدول Dataverse الظاهري في Microsoft Power Platform، والوصول إلى البيانات في Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>تمكين الوصول إلى جدول Dataverse الظاهري في Power Platform

الخطوة الأولى لتمكين الوصول إلى جداول Dataverse الظاهرية في Power Platform هي إعداد التطبيق الخاص بك في Power Platform للمصادقة مقابل نقاط نهاية جدول Dataverse الظاهري. يتم توضيح خطوات إجراء ذلك في [Microsoft Dataverseدليل المطور](/powerapps/developer/data-platform).

  - بالنسبة لتسجيلات التطبيقات أحادية المستاجر: [استخدام مصادقة خادم إلى خادم من مستاجر واحد](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - بالنسبة لتسجيلات التطبيقات متعددة المستاجرين: [استخدام مصادقة خادم إلى خادم من مستأجرين متعددين](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>إنشاء دور أمان لعمليات تكامل ATS

تتمثل إحدى الخطوات التالية بعد إنشاء مستخدم التطبيق في تعيين المستخدم إلى دور أمان والذي يحدد الوصول الذي سيحصل عليه التطبيق إلى نقاط النهاية. وهذه هي الخطوة 7 في عملية [إنشاء مستخدم التطبيق](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) لتسجيلات التطبيقات لمستأجر واحد و[إنشاء دور أمان لمستخدم التطبيق](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) للتسجيلات متعددة المستاجرين. 

يجب أن يكون للدور الذي قمت بتعيينه لمستخدم التطبيق حق الوصول إلى كيانات البيانات المستخدمة لتكامل ATS. وهذا لا يتوفر بشكل جاهز، لذلك سيلزم إنشاء دور أمان جديد. يمكن إنشاء الدور الجديد باتباع الخطوات المذكورة في [إنشاء دور أمان](/power-platform/admin/create-edit-security-role#create-a-security-role).

بالنسبة للدور الجديد، يجب تعيين الوصول المناسب إلى الكيانات التالية، بحد أدنى، في علامة التبويب **الكيانات المخصصة** للدور الجديد. لاحظ أنه قد تكون هناك كيانات إضافية قد تحتاج إلى إضافتها في حالة استخدام التكامل لبيانات تطبيقات أكثر شمولية. وبعد إنشاء الدور الجديد، يمكن تعيينه لمستخدم التطبيق.

  - العامل الأساسي (mshr)
  - المرشح المُراد توظيفه (mshr)
  - اختصاص الشهادة (mshr)
  - نوع الشهادة (mshr)
  - الشركة
  - مهمة وظيفة التعويض (mshr)
  - نوع وظيفة التعويض (mshr)
  - البلد/المناطق (mshr)
  - القسم (mshr)
  - اختصاص التعليم (mshr)
  - درجه التعليم (mshr)
  - أنظمة التعليم (mshr)
  - المتطلبات التعليمية (mshr)
  - التعريف (mshr)
  - نوع التعريف (mshr)
  - المعهد (mshr)
  - جهة الإصدار (mshr)
  - تعويض الوظيفة (mshr)
  - الوظائف (mshr)
  - مستوي التعليم (mshr)
  - جهة اتصال الطرف (mshr)
  - الأشخاص (mshr)
  - عناوين الشخص (mshr)
  - مراقبة الشخص (mshr)
  - نوع المنصب (mshr)
  - المناصب V2 (mshr)
  - اختصاص الخبرة المهنية (mshr)
  - مستوى التقييم (mshr)
  - نماذج التقييم (mshr)
  - أكواد السبب (mshr)
  - طلب التعيين (mshr)
  - موقع طلب التعيين (mshr)
  - منصب طلب التعيين (mshr)
  - مهارة طلب التعيين (mshr)
  - نوع المراقبة (mshr)
  - اختصاص المهارة (mshr)
  - المهارات (mshr)
  - المسميات الوظيفية (mshr)
  - حالة الخبير (mshr)
  - العامل (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>منح أذونات التطبيق لبيانات الموارد البشرية

الخطوة الثانية هي التأكد من منح التطبيق الأذونات المناسبة للبيانات في الموارد البشرية عن طريق ربطها بمستخدم في تطبيق الموارد البشرية. النسبة لمستخدم أحد التطبيقات، يتم إجراء مكالمات خادم إلى خادم من خلال جداول Dataverse الظاهرية في سياق هوية المستخدم (التطبيق) في Dataverse الذي يستعي الإجراء. تقوم خدمة محول الجداول الظاهرية بعد ذلك بالبحث عن المستخدم المقترن في الموارد البشرية وتشغيل الاستعلام في سياق ذلك المستخدم. وهذا يعني أنه يجب إنشاء مستخدم في الموارد البشرية مع تعيين الأدوار الصحيحة لتوفير الوصول إلى البيانات التي سيحتاجها التطبيق المتكامل.

سيحتاج مستخدم الموارد البشرية أيضًا إلى تعيين الأذونات الصحيحة للبيانات في الموارد البشرية. يتوفر دور **تطبيق التوظيف** (HcmRecruitingIntegrator) مع امتيازات إلى الكيانات الرئيسية المطلوبة للتكامل مع بيانات التوظيف. يمكن تعيين هذا الدور لمستخدم التطبيق في صفحة **المستخدمين** لمنح حق الوصول المناسب إلى البيانات. لمزيد من المعلومات حول أدوار أمان الموارد البشرية، راجع [الأمان المستند إلى الدور](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>إعداد المستخدم الجديد بالأذونات المناسبة

لإعداد المستخدم الجديد بالأذونات المناسبة، اتبع هذه الخطوات:

  1. افتح صفحة **المستخدمين** في الموارد البشرية وحدد **جديد**.
  2. أدخل **معرف المستخدم** و **اسم المستخدم** لمستخدم التطبيق الجديد. على سبيل المثال، يمكنك إدخال "RecruitingIntegration".

      > [!NOTE]
      > إذا كان التطبيق لا يحتوي على حساب مستخدم Microsoft Azure Active Directory (Azure AD) أو بريد إلكتروني، فيمكنك إضافة شيء مثل "RecruitingApp" في عنوان البريد الإلكتروني وتوفير الحقول للمستخدم.

  3. في علامة التبويب السريعة، **أدوار المستخدم**، حدد إجراء **تعيين‏‎ الأدوار**.
  4. في جزء **تعيين الأدوار إلى المستخدم**، حدد **تطبيق التوظيف**، وحدد **موافق**.
  5. قم بحفظ سجل المستخدم الجديد.

### <a name="link-the-new-human-resources-user-to-the-application"></a>ربط مستخدم الموارد البشرية الجديد بالتطبيق

بعد إنشاء المستخدم، يجب إنشاء سجل للتطبيق في نموذج **تطبيقات Azure Active Directory** لربط التطبيق بمستخدم الموارد البشرية.

  1. افتح نموذج **تطبيقات Azure Active Directory** وحدد **جديد**.
  2. في حقل **معرف العميل**، أدخل معرف العميل الخاص بمستخدم التطبيق الذي تم إنشاؤه للتطبيق.
  3. في حقل **الاسم**، أدخل اسم تطبيق التكامل.
  4. في حقل **معرف المستخدم**، حدد مستخدم الموارد البشرية الجديد الذي تم إنشاؤها لتكامل التعيين.
  5. قم بحفظ السجل الجديد.

سيقوم التطبيق بعد ذلك بالوصول إلى بيانات الموارد البشرية، محدودًا فقط بالبيانات المطلوبة لإجراء عمليات تكامل تطبيق التعيين.

## <a name="see-also"></a>راجع أيضًا

[تعيين المرشحين للوظائف](hr-personnel-recruit.md)<br>
[ما هو Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)<br>
[استخدام واجهة ويب Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)<br>
[إنشاء مجموعات الخيارات وتحديثها باستخدام واجهة الويب](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
