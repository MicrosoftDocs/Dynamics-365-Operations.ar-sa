---
title: "تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations &#8211; التخزين"
description: "يصف هذا الموضوع كيفية تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations - التخزين"
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 608543c9cfd93c4772e93089e1d174312d8b23a6
ms.openlocfilehash: 411bb28668f5aa9d07774211814da4e9757ac43c
ms.contentlocale: ar-sa
ms.lasthandoff: 03/06/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations &#8211; التخزين

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> 
> يوضح هذا الموضوع كيفية تكوين التخزين لعمليات توزيع المجموعة. إذا كنت تبحث عن كيفية تكوين التخزين لعمليات التوزيع المحلي، فيُرجى مراجعة [التخزين لعمليات التوزيع المحلية](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


يصف هذا الموضوع كيفية تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations - التخزين

إن Finance and Operations - التخزين عبارة عن تطبيق يتوفر على Google Play Store ومتجر Windows. بالنسبة إلى الإصدار الحالي من Finance and Operations، يتوفر هذا التطبيق كمكون مستقل، مما يعني النشر الذاتي على الأجهزة المستخدمة لمهام المستودع. لاستخدام التطبيق في بيئة Finance and Operations، يجب تنزيل التطبيق على كل جهاز وتكوينه للاتصال ببيئة Finance and Operations. يصف هذا الموضوع كيفية تثبيت التطبيق على الأجهزة. وهو يوضح أيضًا كيفية تكوين التطبيق للاتصال ببيئة Finance and Operations.

## <a name="prerequisites"></a>المتطلبات الأساسية
يتوفر التطبيق على أنظمة تشغيل Windows وAndroid. لاستخدام هذا التطبيق، يجب أن يكون أحد أنظمة التشغيل التالية المعتمدة مثبتة على أجهزتك. ويجب أن يتوفر لديك أيضًا أحد الإصدارات المعتمدة التالية من Finance and Operations. استخدم المعلومات في الجدول التالي لتقييم جهوزية بيئة الأجهزة والبرامج لديك لدعم عملية التثبيت.

| النظام الأساسي                    | ‏‏الإصدار                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows ‏(UWP)               | Windows 10 (كل الإصدارات)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations، الإصدار 1611 <br>-أو - <br>الإصدار 7.0/7.0.1 من Microsoft Dynamics AX وتحديث النظام الأساسي لـ Dynamics AX 2 مع الإصلاح العاجل KB 3210014 |

## <a name="get-the-app"></a>الحصول على التطبيق
-   Windows ‏(UWP)
     - [Finance and Operations - التخزين في متجر Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - التخزين على Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - التخزين على Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>إنشاء تطبيق خدمة ويب في Azure Active Directory
لتمكين التطبيق من التفاعل مع خادم Finance and Operations معين، يجب عليك تسجيل تطبيق خدمة ويب في Azure Active Directory لمستأجر Finance and Operations. لأسباب تتعلق بالأمان، نوصي بإنشاء تطبيق خدمة ويب لكل جهاز تستخدمه. لإنشاء تطبيق خدمة ويب في Azure Active Directory (Azure AD)، أكمل الخطوات التالية:

1.  في مستعرض ويب، انتقل إلى <https://portal.azure.com>.
2.  أدخل اسم المستخدم وكلمة المرور لمستخدم له حق الوصول إلى اشتراك Azure.
3.  في مدخل Azure، في جزء التنقل الأيمن، انقر فوق **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  تأكد من أن مثيل Active Directory هو المثيل الذي يتم استخدامه بواسطة Finance and Operations.
5.  في القائمة، انقر فوق **عمليات تسجيل التطبيق**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  في الجزء العلوي، انقر فوق **تسجيل تطبيق جديد**. يبدأ تشغيل معالج **إضافة تطبيق**.
7.  أدخل اسمًا للتطبيق وحدد **تطبيق ويب/web API**. أدخل عنوان URL لتسجيل الدخول، وهو عنوان URL لتطبيق ويب. عنوان URL هذا هو نفسه عنوان URL للنشر، ولكن مع إضافة oauth في نهايته. انقر فوق **إنشاء**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  حدد التطبيق الجديدة في القائمة. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  تذكر **"معرف تطبيق"**، أنك ستحتاجه فيما بعد. ستتم الإشارة إلى **معرف التطبيق** لاحقًا باعتباره **معرف العميل**.
10. انقر فوق **مفاتيح** في **جزء الإعدادات**. أنشئ مفتاحًا عن طريق إدخال وصف مفتاح وفترة زمنية في قسم **كلمات المرور**. 
11. انقر فوق **حفظ** وانسخ المفتاح. سيُشار إلى هذا المفتاح لاحقًا على أنه **سر العميل**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>إنشاء وتكوين حساب مستخدم في Finance and Operations
لتمكين Finance and Operations لاستخدام تطبيق Azure AD، تحتاج إلى إكمال خطوات التكوين التالية:

1.  أنشئ حساب مستخدم جديدًا في Active Directory لمستأجر Finance and Operations. الغرض من حساب المستخدم هذا هو الوصول إلى الخدمة المخصصة المعينة لتطبيق التخزين، والتي يعرضها خادم Finance and Operations. بعد إكمال هذه الخطوة، سيكون لديك بيانات اعتماد مستخدم WMDP، التي تتكون من عنوان بريد إلكتروني WMDP وكلمة مرور WMDP. للتعرف على الخطوات الأساسية لإضافة مستخدمين إلى Azure AD وFinance and Operations، يمكنك مراجعة هذا البرنامج التعليمي: [التسجيل للحصول على اشتراك في Finance and Operations](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  أنشئ مستخدم Finance and Operations يتطابق مع بيانات اعتماد مستخدم تطبيق التخزين.
    1.  في Finance and Operations، انتقل إلى **إدارة النظام** &gt; **عام** &gt; **المستخدمون**.
    2.  أنشئ مستخدمًا جديدًا.
    3.  عيّن مستخدم الجهاز المحمول للمستودع‬، كما هو موضح في لقطة الشاشة التالية. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  قم بإقران تطبيق Azure Active Directory بمستخدم تطبيق تخزين.
    1.  في Finance and Operations، انتقل إلى **إدارة النظام** &gt; **الإعداد** &gt; **تطبيقات Azure Active Directory**.
    2.  قم بإنشاء بند جديد.
    3.  أدخل **"معرف العميل"** (الذي تم الحصول عليه في القسم الأخير)، وأدخل اسمًا له، وحدد المستخدم الذي أنشأته في وقت سابق. نوصي بتمييز كل أجهزتك بحيث يمكنك أن تزيل بسهولة حق وصولها إلى Finance and Operations من هذه الصفحة في حال فقدانها. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>تكوين التطبيق
يجب عليك تكوين التطبيق على الجهاز للاتصال بخادم Finance and Operations من خلال تطبيق Azure AD. ولإجراء ذلك، أكمل الخطوات التالية.

1.  في التطبيق، انتقل إلى **إعدادات الاتصال**.
2.  انقر فوق حقل **وضع العرض التوضيحي**. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  أدخل المعلومات التالية: 
    + **معرف عميل Azure Active Directory** - يتم الحصول على معرف العميل في الخطوة 9 "إنشاء تطبيق خدمة ويب في Active Directory". 
    + **سر عميل Azure Active Directory** - يتم الحصول على سر العميل في الخطوة 11 "إنشاء تطبيق خدمة ويب في Active Directory". 
    + **مورد Azure Active Directory** - يمثّل مورد Azure Active Directory عنوان URL الجذر لـ Finance and Operations. **ملاحظة**: لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل. 
    + **مستأجر Azure Active Directory** - مستأجر دليل Azure AD المستخدم مع خادم Finance and Operations: `https://login.windows.net/your-AD-tenant-ID`. على سبيل المثال: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**ملاحظة**: لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل. 
    + **الشركة** -أدخل الكيان القانوني في Finance and Operations الذي تريد أن يتصل به التطبيق. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  حدد زر **السابق** في الزاوية العلوية اليمنى من التطبيق. سيتصل الآن التطبيق بخادم Finance and Operations وستظهر شاشة تسجيل الدخول لعامل المستودع. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

للحصول على المزيد من المعلومات حول كيفية إعداد Dynamics 365 for Finance and Operations – Warehousing لمسح الأكواد الشريطية باستخدام كاميرا جهاز محمول، راجع [مسح الأكواد الشريطية باستخدام كاميرا في Dynamics 365 for Finance and Operations – Warehousing](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>إزالة حق الوصول لجهاز
عند فقدان جهاز أو تعرضه للاختراق، يجب إزالة حق الوصول إلى Finance and Operations للجهاز. تصف الخطوات التالية العملية الموصى بها لإزالة حق الوصول.

1.  في Finance and Operations، انتقل إلى **إدارة النظام** &gt; **الإعداد** &gt; **تطبيقات Azure Active Directory**.
2.  احذف السطر الذي يتوافق مع الجهاز الذي تريد إزالة حق الوصول الممنوح له. تذكر **معرف العميل** المستخدم للجهاز الذي تمت إزالته، أنك ستحتاجه فيما بعد.
3.  سجل الدخول إلى مدخل Azure على العنوان <https://portal.azure.com>.
4.  انقر فوق رمز **Active Directory** في القائمة اليسرى، وتأكد من أنك في الدليل الصحيح.
5.  في القائمة، انقر فوق **عمليات تسجيل التطبيقات**، ثم انقر فوق التطبيق الذي تريد تكوينه. ستظهر صفحة **الإعدادات** مع معلومات التكوين.
6.  تأكد من أن **معرف العميل** هو نفسه كما هو موضح في الخطوة 2 في هذا القسم.
7.  انقر فوق الزر **حذف** في الجزء العلوي.
8.  انقر فوق **نعم** في رسالة التأكيد.

