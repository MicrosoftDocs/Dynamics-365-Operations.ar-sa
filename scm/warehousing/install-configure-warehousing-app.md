---
title: "تثبيت وتكوين Microsoft Dynamics 365 لعمليات & #8211؛ مستودع"
description: "يصف هذا الموضوع كيفية تثبيت وتكوين Microsoft Dynamics 365 للعمليات-التخزين."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>تثبيت وتكوين Microsoft Dynamics 365 لعمليات & #8211؛ مستودع

يصف هذا الموضوع كيفية تثبيت وتكوين Microsoft Dynamics 365 للعمليات-التخزين.

ديناميات 365 للعمليات-التخزين تطبيق متوفراً على مخزن التشغيل Google ومخزن Windows. يتم توفير هذا التطبيق للإصدار الحالي من Microsoft Dynamics 365 للعمليات، كمكون مستقل، مما يعني النشر الذاتي على الأجهزة المستخدمة لمهام المستودع. لاستخدام التطبيق في 365 الديناميات الخاصة بك لبيئة العمليات، يجب تحميل التطبيق على كل جهاز وتكوينه للاتصال الخاص بك 365 ديناميات بيئة العمليات. يصف هذا الموضوع كيفية تثبيت التطبيق على الأجهزة. وهو يوضح أيضا كيفية تكوين التطبيق للاتصال الخاص بك 365 ديناميات بيئة العمليات.

## <a name="prerequisites"></a>المتطلبات الأساسية
يتوفر التطبيق على أنظمة تشغيل Windows والروبوت. لاستخدام هذا التطبيق، يجب أن يكون لديك أحد أنظمة التشغيل التالية المعتمدة المثبتة على الأجهزة. يجب عليك أيضا أحد الإصدارات التالية من 365 ديناميات عمليات. استخدام المعلومات في الجدول التالي لتقييم حالة جاهزة لدعم التثبيت بيئة المعدات والبرامجيات الحاسوبية.

| النظام الأساسي                    | ‏‏الإصدار                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| الروبوت                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | 10 Windows (كافة الإصدارات)                                                                                                                                                   |
| ديناميكيات 365 للعمليات | تحديث Microsoft Dynamics 365 لعمليات الإصدار 1611-أو-إصدار Microsoft Dynamics Dynamics AX 7.0/7.0.1 والنظام الأساسي Microsoft Dynamics AX 2 بالإصلاح العاجل 3210014 كيلو بايت |

## <a name="get-the-app"></a>الحصول على التطبيق
-   Windows (UWP)- [Dynamics 365 للعمليات-التخزين على مخزن Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   الروبوت- [Dynamics 365 للعمليات-التخزين على مخزن التشغيل جوجل](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>إنشاء تطبيق خدمة ويب في "Active Directory"
لتمكين التطبيق للتفاعل مع 365 Dynamics محددة لعمليات الخادم، يجب عليك تسجيل تطبيق خدمة ويب في أزور Active Directory ل 365 Dynamics للمستأجر العمليات. لأسباب تتعلق بالأمان، نوصي بإنشاء تطبيق خدمة ويب لكل الجهاز الذي تستخدمه. لإنشاء تطبيق خدمة ويب في "خدمة active Directory" (Azure AD) أزور، أكمل الخطوات التالية:

1.  في مستعرض ويب، انتقل إلى <https://manage.windowsazure.com>.
2.  أدخل اسم وكلمة مرور لمستخدم له حق الوصول إلى اشتراك Azure.
3.  موقع أزور، في جزء التنقل الأيمن، انقر فوق **Active Directory**. [](./media/wh-01-active-directory-example.png)[![م-01-نشط-دليل-مثال](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  في الشبكة، حدد مثيل "خدمة active Directory" التي يستخدمها 365 ديناميات عمليات.
5.  على شريط الأدوات العلوي، انقر فوق **تطبيقات**. [![م-02-نشط-دليل-تطبيقات](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  في الجزء السفلي، انقر فوق **إضافة**. **إضافة تطبيق** بدء تشغيل المعالج.
7.  أدخل اسماً للتطبيق وتحديد **تطبيق ويب و/أو الويب API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  أدخل URL الدخول وهو عنوان URL للتطبيق في المستأجر، عمليات URL الجذر. URL الدخول لا بنشاط يستخدم حاليا في مصادقة التطبيق، ولكن حقل إلزامي. أدخل URL نفسه في مجال تطبيق معرف URI. [![م-04-الإعلان-إضافة-خصائص](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  انتقل إلى **تكوين** علامة التبويب. [![م-05-الإعلان-تكوين-التطبيق](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. قم بالتمرير لأسفل حتى تشاهد **الأذونات لتطبيقات أخرى** المقطع. انقر فوق **إضافة تطبيق**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. حدد **Microsoft Dynamics ERP** في القائمة. انقر فوق **إكمال التحقق من** الزر في الزاوية اليمنى من الصفحة. [![م-07-الإعلان-حدد-أذونات](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. في **"أذونات التفويض"** ، حدد كافة خانات الاختيار. Click **Save**. [![م-08-الإعلان--أذونات التفويض](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. دون ملاحظة عن المعلومات التالية:
    -   **معرف العميل** -أثناء قيامك بالتمرير أعلى الصفحة، سترى **"معرف العميل"** عرض.
    -   **مفتاح** - **مفاتيح** المقطع وإنشاء مفتاح بتحديد مدة نسخ المفتاح. هذا المفتاح سيتم لاحقاً أن يشار إلى **عميل سري**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>إنشاء وتكوين حساب مستخدم في ديناميات 365 للعمليات
لتمكين 365 ديناميات عمليات استخدام التطبيق إعلانية Azure، تحتاج إلى إكمال خطوات التكوين التالية:

1.  إنشاء حساب مستخدم جديد في "Active Directory أزور" ل 365 Dynamics للمستأجر العمليات. كان الغرض من هذا الحساب المستخدم للوصول إلى خدمة معينة مخصصة لتطبيق التخزين، و 365 Dynamics لملقم عمليات الكشف عن. بعد إكمال هذه الخطوة، سيكون لديك ومدب بيانات اعتماد المستخدم، التي تتكون من عنوان بريد إلكتروني ومدب وكلمة مرور ومدب. للتعرف على الخطوات الأساسية لإضافة مستخدمين إلى إعلان الﻻزوردية وديناميات 365 للعمليات، تشير إلى هذا البرنامج التعليمي: [التسجيل Microsoft Dynamics 365 للاشتراك في عمليات](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  إنشاء 365 Dynamics للمستخدم عمليات يقابل التطبيق تخزين بيانات اعتماد المستخدم.
    1.  في ديناميات 365 للعمليات، انتقل إلى **إدارة النظام**&gt;**العامة**&gt;**المستخدمين**.
    2.  إنشاء مستخدم جديد.
    3.  تعيين مستخدم جهاز محمول المستودع، كما هو موضح في الصورة التالية. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  إقران تطبيق Azure Active Directory الخاص بك المستخدم التطبيق التخزين.
    1.  في ديناميات 365 للعمليات، انتقل إلى **إدارة النظام**&gt;**الإعداد**&gt;**تطبيقات Azure Active Directory**.
    2.  قم بإنشاء بند جديد.
    3.  أدخل **"معرف العميل"** (التي تم الحصول عليها في المقطع الأخير)، إعطاء اسم، وحدد المستخدم التي تم إنشاؤها مسبقاً. نوصي بتمييز كل الأجهزة الخاصة بك حيث يمكنك بسهولة إزالة وصولهم إلى 365 ديناميات عمليات من هذه الصفحة في حالة فقدان. [![م-10-الإعلان-التطبيقات-النموذج](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>تكوين التطبيق
يجب عليك تكوين التطبيق للاتصال إلى 365 Dynamics لملقم العمليات من خلال تطبيق Azure الإعلان على الجهاز. لإجراء ذلك، أكمل الخطوات التالية.

1.  في التطبيق، انتقل إلى **إعدادات الاتصال**.
2.  مسح **طريقة العرض** الحقل. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  أدخل المعلومات التالية:- **معرف العميل الدليل النشط Azure** -العميل الحصول على معرف في الخطوة 13 "إنشاء تطبيق ويب خدمة في خدمة active Directory". - **سري العميل الدليل النشط azure** -سر العميل التي يتم الحصول عليها في الخطوة 13 "إنشاء تطبيق ويب خدمة في خدمة active Directory". - **الموارد الدليل النشط azure** -يصف الموارد الدليل الإعلان Azure Dynamics 365 ل URL الجذر العمليات. **ملاحظة**: لا ينتهي هذا الحقل باستخدام حرف الخط مائل للأمام (/). - **المستأجر الدليل النشط azure** -المستأجر الدليل الإعلان Azure استخدام Dynamics 365 لملقم العمليات: https://login.windows.net/&lt;الخاص بك--المستأجر-معرف الإعلان&gt;. على سبيل المثال: https://login.windows.net/contosooperations.onmicrosoft.com. 
**ملاحظة**: لا ينتهي هذا الحقل باستخدام حرف الخط مائل للأمام (/). - **شركة** -إدخال الكيان القانوني في ديناميات 365 للعمليات التي تريد التطبيق للاتصال. [![م-12-التطبيق--إعدادات الاتصال](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  حدد **السابق** الزر في الزاوية العلوية اليمنى من التطبيق. التطبيق سيتصل الآن 365 الديناميات الخاصة بك لملقم العمليات وسيتم عرض شاشة تسجيل الدخول للعامل المستودع. [![م-13--شاشة الدخول](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>إزالة الوصول لجهاز
في حالة جهاز مفقود أو المساس بها، يجب إزالة الوصول إلى Dynamics 365 للعمليات الخاصة بالجهاز. تصف الخطوات التالية العملية الموصى بها لإزالة حق الوصول.

1.  في ديناميات 365 للعمليات، انتقل إلى **إدارة النظام**&gt;**الإعداد**&gt;**تطبيقات Azure Active Directory**.
2.  حذف السطر الذي يتوافق مع الجهاز الذي تريد إزالة الوصول. يدون **"معرف العميل"** المستخدمة لإزالة الجهاز.
3.  تسجيل في مدخل Azure التقليدية في <https://manage.windowsazure.com>.
4.  انقر فوق **Active Directory** رمز في القائمة اليسرى، ثم انقر فوق الدليل المطلوب.
5.  في الأعلى، انقر فوق **تطبيقات**، ثم انقر فوق التطبيق الذي تريد تكوينه. **"البدء السريع"** ستظهر الصفحة باستخدام تسجيل الدخول الأحادي ومعلومات التكوين الأخرى.
6.  انقر فوق **تكوين** علامة التبويب، قم بالتمرير لأسفل والتأكد من أن **"معرف العميل"** التطبيق هي نفسها كما في الخطوة 2 في هذا القسم.
7.  انقر فوق **حذف** زر في شريط الأوامر.
8.  انقر فوق **نعم** في رسالة التأكيد.



