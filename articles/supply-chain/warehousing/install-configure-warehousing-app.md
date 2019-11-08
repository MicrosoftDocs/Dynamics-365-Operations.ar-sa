---
title: نظرة عامة على تثبيت وتكوين تطبيق التخزين
description: يصف هذا الموضوع كيفية تثبيت وتكوين Dynamics 365 for Finance and Operations - تطبيق التخزين.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f629fffc5c424c244a25bb8faef0435814398ee1
ms.sourcegitcommit: 4aac45c84b87f463b22b318f5f6f729f8d737090
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2548958"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>نظرة عامة على تثبيت وتكوين تطبيق التخزين

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> يوضح هذا الموضوع كيفية تكوين التخزين لعمليات توزيع المجموعة. إذا كنت تبحث عن كيفية تكوين التخزين لعمليات التوزيع المحلي، فيُرجى مراجعة [التخزين لعمليات التوزيع المحلية](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


يصف هذا الموضوع كيفية تثبيت وتكوين Dynamics 365 for Finance and Operations - تطبيق التخزين.

يتوفر تطبيق التخزين في متجر Google Play وMicrosoft Store. بالنسبة إلى الإصدار الحالي من Dynamics 365 Supply Chain Management، يتوفر هذا التطبيق كمكون مستقل، مما يعني النشر الذاتي على الأجهزة المستخدمة لمهام المستودع. لاستخدام التطبيق، يجب تنزيل التطبيق على كل جهاز وتكوينه للاتصال ببيئة Supply Chain Management. يصف هذا الموضوع كيفية تثبيت التطبيق على الأجهزة. وهو يوضح أيضًا كيفية تكوين التطبيق للاتصال ببيئة Supply Chain Management.

## <a name="prerequisites"></a>المتطلبات الأساسية
يتوفر التطبيق على أنظمة تشغيل Android وWindows. لاستخدام هذا التطبيق، يجب أن يكون أحد أنظمة التشغيل التالية المعتمدة مثبتة على أجهزتك. يجب أن يتوفر لديك أحد الإصدارات التالية المعتمدة. استخدم المعلومات في الجدول التالي لتقييم جهوزية بيئة الأجهزة والبرامج لديك لدعم عملية التثبيت.

| النظام الأساسي                    | الإصدار                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4، 5.0، 6.0، 7.0، 8.0، 9.0                                                                                                                                                     |
| Windows ‏(UWP)               | Windows 10 (كل الإصدارات)                                                                                                                                                   |
| Finance and Operations | الإصدار 1611 من Microsoft Dynamics 365 for Operations <br>-أو - <br>الإصدار 7.0/7.0.1 من Microsoft Dynamics AX وMicrosoft Dynamics AX platform update 2 مع الإصلاح العاجل KB 3210014 |

## <a name="get-the-app"></a>الحصول على التطبيق
-   Windows ‏(UWP)
     - [Finance and Operations - التخزين في متجر Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - التخزين على Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> تم إيقاف Zebra App Gallery عن العمل، مما يعني أن تطبيق التخزين لن يعود متوفرًا لتنزيله من هذا الموقع.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>إنشاء تطبيق خدمة ويب في Azure Active Directory
لتمكين التطبيق من التفاعل مع خادم Supply Chain Management معين، يجب عليك تسجيل تطبيق خدمة ويب في Azure Active Directory لمستأجر Supply Chain Management. لأسباب تتعلق بالأمان، نوصي بإنشاء تطبيق خدمة ويب لكل جهاز تستخدمه. لإنشاء تطبيق خدمة ويب في Azure Active Directory (Azure AD)، أكمل الخطوات التالية:

1.  في مستعرض ويب، انتقل إلى <https://portal.azure.com>.
2.  أدخل اسم المستخدم وكلمة المرور لمستخدم له حق الوصول إلى اشتراك Azure.
3.  في مدخل Azure، في جزء التنقل الأيمن، انقر فوق **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  تأكد من أن مثيل Active Directory هو المثيل الذي يتم استخدامه بواسطة Supply Chain Management.
5.  في القائمة، انقر فوق **عمليات تسجيل التطبيق**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  في الجزء العلوي، انقر فوق **تسجيل جديد**. يبدأ تشغيل **معالج تسجيل تطبيق**.
7.  ادخل اسمًا للتطبيق وحدد **حسابات في هذا الدليل التنظيمي فقط**. انقر فوق **تسجيل**.  [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  يفتح تسجيل التطبيق الجديد. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  تذكر **"معرف تطبيق"**، أنك ستحتاجه فيما بعد. ستتم الإشارة إلى **معرف التطبيق** لاحقًا باعتباره **معرف العميل**.
10. انقر فوق **الشهادة والأسرار** في الجزء **إدارة**. انقر فوق **سر عميل جديد**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. أنشئ مفتاحًا عن طريق إدخال وصف مفتاح وفترة زمنية في قسم **كلمات المرور**. انقر فوق **إضافة** وانسخ المفتاح. سيُشار إلى هذا المفتاح لاحقًا على أنه **سر العميل**. [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>إنشاء وتكوين حساب مستخدم في Supply Chain Management
لتمكين Supply Chain Management لاستخدام تطبيق Azure AD، تحتاج إلى إكمال خطوات التكوين التالية:

1.  أنشئ مستخدمًا يتطابق مع بيانات اعتماد مستخدم تطبيق التخزين.
    1.  انتقل إلى **إدارة النظام** &gt; **عام** &gt; **المستخدمون**.
    2.  أنشئ مستخدمًا جديدًا.
    3.  عيّن مستخدم الجهاز المحمول للمستودع‬، كما هو موضح في لقطة الشاشة التالية. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  قم بإقران تطبيق Azure Active Directory بمستخدم تطبيق التخزين.
    1.  في Supply Chain Management، انتقل إلى **إدارة النظام** &gt; **الإعداد‏‎** &gt; **تطبيقات Azure Active Directory**.
    2.  قم بإنشاء بند جديد.
    3.  أدخل **"معرف العميل"** (الذي تم الحصول عليه في القسم الأخير)، وأدخل اسمًا له، وحدد المستخدم الذي أنشأته في وقت سابق. نوصي بتمييز كل أجهزتك بحيث يمكنك أن تزيل بسهولة حق وصولها إلى Supply Chain Management من هذه الصفحة في حال فقدانها. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>تكوين التطبيق
يجب عليك تكوين التطبيق على الجهاز للاتصال بخادم Supply Chain Management من خلال تطبيق Azure AD. ولإجراء ذلك، أكمل الخطوات التالية.

1.  في التطبيق، انتقل إلى **إعدادات الاتصال**.
2.  انقر فوق حقل **وضع العرض التوضيحي**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  أدخل المعلومات التالية: 
    + **معرف عميل Azure Active Directory** - يتم الحصول على معرف العميل في الخطوة 9 "إنشاء تطبيق خدمة ويب في Active Directory". 
    + **سر عميل Azure Active Directory** - يتم الحصول على سر العميل في الخطوة 11 "إنشاء تطبيق خدمة ويب في Active Directory". 
    + **مورد Azure Active Directory** - يمثل مورد Azure AD Directory‏‎ عنوان URL الجذر لـ Supply Chain Management. **ملاحظة**: لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل. 
    + **مستأجر Azure Active Directory** - مستأجر Azure AD Directory‏‎ المستخدم مع خادم Supply Chain Management: `https://login.windows.net/your-AD-tenant-ID`. على سبيل المثال: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**ملاحظة**: لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل. 
    + **الشركة** - أدخل الكيان القانوني في Supply Chain Management الذي تريد أن يتصل به التطبيق. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  حدد زر **السابق** في الزاوية العلوية اليمنى من التطبيق. سيتصل الآن التطبيق بخادم Supply Chain Management وستظهر شاشة تسجيل الدخول لعامل المستودع. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

لمزيد من المعلومات حول كيفية إعداد تطبيق التخزين لمسح الأكواد الشريطية باستخدام كاميرا على جهاز محمول، راجع [مسح الأكواد الشريطية باستخدام كاميرا في Dynamics 365 for Finance and Operations – التخزين](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>إزالة حق الوصول لجهاز
عند فقدان جهاز أو تعرضه للاختراق، يجب إزالة حق الوصول إلى Supply Chain Management للجهاز. تصف الخطوات التالية العملية الموصى بها لإزالة حق الوصول.

1.  انتقل إلى **إدارة النظام** &gt; **الإعداد** &gt; **تطبيقات Azure Active Directory**.
2.  احذف السطر الذي يتوافق مع الجهاز الذي تريد إزالة حق الوصول الممنوح له. تذكر **معرف العميل** المستخدم للجهاز الذي تمت إزالته، أنك ستحتاجه فيما بعد.
3.  سجل الدخول إلى مدخل Azure على العنوان <https://portal.azure.com>.
4.  انقر فوق رمز **Active Directory** في القائمة اليسرى، وتأكد من أنك في الدليل الصحيح.
5.  في القائمة، انقر فوق **عمليات تسجيل التطبيقات**، ثم انقر فوق التطبيق الذي تريد تكوينه. ستظهر صفحة **الإعدادات** مع معلومات التكوين.
6.  تأكد من أن **معرف العميل** هو نفسه كما هو موضح في الخطوة 2 في هذا القسم.
7.  انقر فوق الزر **حذف** في الجزء العلوي.
8.  انقر فوق **نعم** في رسالة التأكيد.
