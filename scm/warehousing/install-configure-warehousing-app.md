---
title: "تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations &#8211; التخزين"
description: "يصف هذا الموضوع كيفية تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations - التخزين"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 2e6b0fb81396eef945dbce3be8aee17c9fd455bc
ms.contentlocale: ar-sa
ms.lasthandoff: 06/13/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations &#8211; التخزين

[!include[banner](../includes/banner.md)]


يصف هذا الموضوع كيفية تثبيت وتكوين Microsoft Dynamics 365 for Finance and Operations - التخزين

إن Finance and Operations - التخزين عبارة عن تطبيق يتوفر على Google Play Store ومتجر Windows. بالنسبة إلى الإصدار الحالي من Finance and Operations، يتوفر هذا التطبيق كمكون مستقل، مما يعني النشر الذاتي على الأجهزة المستخدمة لمهام المستودع. لاستخدام التطبيق في بيئة Finance and Operations، يجب تنزيل التطبيق على كل جهاز وتكوينه للاتصال ببيئة Finance and Operations. يصف هذا الموضوع كيفية تثبيت التطبيق على الأجهزة. وهو يوضح أيضًا كيفية تكوين التطبيق للاتصال ببيئة Finance and Operations.

## <a name="prerequisites"></a>المتطلبات الأساسية
يتوفر التطبيق على أنظمة تشغيل Windows وAndroid. لاستخدام هذا التطبيق، يجب أن يكون أحد أنظمة التشغيل التالية المعتمدة مثبتة على أجهزتك. ويجب أن يتوفر لديك أيضًا أحد الإصدارات المعتمدة التالية من Finance and Operations. استخدم المعلومات في الجدول التالي لتقييم جهوزية بيئة الأجهزة والبرامج لديك لدعم عملية التثبيت.

| النظام الأساسي                    | ‏‏الإصدار                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4 و5.0 و6.0                                                                                                                                                               |
| Windows ‏(UWP)               | Windows 10 (كل الإصدارات)                                                                                                                                                   |
| Finance and Operations | الإصدار 1611 من Microsoft Finance and Operations <br>-أو - <br>الإصدار 7.0/7.0.1 من Microsoft Dynamics AX وتحديث النظام الأساسي لـ Dynamics AX 2 مع الإصلاح العاجل KB 3210014 |

## <a name="get-the-app"></a>الحصول على التطبيق
-   Windows (UWP): [Finance and Operations - التخزين على متجر Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations - التخزين على Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - التخزين على Zebra App Gallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>إنشاء تطبيق خدمة ويب في Active Directory
لتمكين التطبيق من التفاعل مع خادم Finance and Operations معين، يجب عليك تسجيل تطبيق خدمة ويب في Azure Active Directory لمستأجر Finance and Operations. لأسباب تتعلق بالأمان، نوصي بإنشاء تطبيق خدمة ويب لكل جهاز تستخدمه. لإنشاء تطبيق خدمة ويب في Azure Active Directory (Azure AD)، أكمل الخطوات التالية:

1.  في مستعرض ويب، انتقل إلى <https://manage.windowsazure.com>.
2.  أدخل اسم المستخدم وكلمة المرور لمستخدم له حق الوصول إلى اشتراك Azure.
3.  في مدخل Azure Portal، في جزء التنقل الأيمن، انقر فوق **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  في الشبكة، حدد مثيل Active Directory الذي سيتم استخدامه من قِبل Finance and Operations.
5.  على شريط الأدوات العلوي، انقر فوق **التطبيقات**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  في الجزء السفلي، انقر فوق **إضافة**. يبدأ تشغيل معالج **إضافة تطبيق**.
7.  أدخل اسمًا للتطبيق وحدد **تطبيق ويب و/أو web API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  أدخل عنوان URL لتسجيل الدخول، وهو عنوان URL لتطبيق ويب. عنوان URL هذا هو نفسه عنوان URL للنشر، ولكن مع إضافة oauth في نهايته. أدخل URI لمعرف تطبيق، هذه القيمة إلزامية، لكنها غير مطلوبة من أجل المصادقة. تأكد من أن URI معرف التطبيق هذا عبارة عن URI وهمي مثل https://contosooperations/wmapp، لأن URL الخاص بعملية النشر قد يتسبب في حدوث مشكلات في تسجيل الدخول في تطبيقات AAD أخرى، مثل وظيفة Excel الإضافية. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  انتقل إلى علامة التبويب **تكوين**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. قم بالتمرير لأسفل حتى تشاهد المقطع **أذونات لتطبيقات أخرى**. انقر فوق **إضافة تطبيق**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. حدد **Microsoft Dynamics ERP** في القائمة. انقر فوق الزر **اكتمال التحقق** في الركن العلوي الأيسر من الصفحة. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. في **"أذونات المفوضين"**، حدد كافة خانات الاختيار. انقر فوق **حفظ**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. سجّل ملاحظة حول المعلومات التالية:
    -   **معرف العميل** -أثناء التمرير لأعلى على الصفحة، سترى **"معرف العميل"**.
    -   **المفتاح** - في مقطع **المفاتيح**، أنشئ مفتاحًا بتحديد المدة، وانسخ المفتاح. سيُشار إلى هذا المفتاح لاحقًا على أنه **سر العميل**.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>إنشاء وتكوين حساب مستخدم في Finance and Operations
لتمكين Finance and Operations لاستخدام تطبيق Azure AD، تحتاج إلى إكمال خطوات التكوين التالية:

1.  أنشئ حساب مستخدم جديدًا في Active Directory لمستأجر Finance and Operations. الغرض من حساب المستخدم هذا هو الوصول إلى الخدمة المخصصة المعينة لتطبيق التخزين، والتي يعرضها خادم Finance and Operations. بعد إكمال هذه الخطوة، سيكون لديك بيانات اعتماد مستخدم WMDP، التي تتكون من عنوان بريد إلكتروني WMDP وكلمة مرور WMDP. للتعرف على الخطوات الأساسية لإضافة مستخدمين إلى Azure AD وFinance and Operations، يمكنك مراجعة هذا البرنامج التعليمي: [التسجيل للحصول على اشتراك في Finance and Operations](/dynamics365/unified-operations/dev-itpro/dev-tools/sign-up-preview-subscription).
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
    + **معرف عميل Azure Active Directory** - يتم الحصول على معرف العميل في الخطوة 13 "إنشاء تطبيق خدمة ويب في Active Directory". 
    + **سر عميل Azure Active Directory** - يتم الحصول على سر العميل في الخطوة 13 "إنشاء تطبيق خدمة ويب في Active Directory". 
    + **مورد Azure Active Directory** - يمثّل مورد Azure Active Directory عنوان URL الجذر لـ Finance and Operations. **ملاحظة**: لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل. 
    + **مستأجر Azure Active Directory** - مستأجر Azure Active Directory المستخدم مع خادم Finance and Operations server: https://login.windows.net/your-AD-tenant-ID. على سبيل المثال: https://login.windows.net/contosooperations.onmicrosoft.com. 
    <br>**ملاحظة**: لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل. 
    + **الشركة** -أدخل الكيان القانوني في Finance and Operations الذي تريد أن يتصل به التطبيق. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  حدد زر **السابق** في الزاوية العلوية اليمنى من التطبيق. سيتصل الآن التطبيق بخادم Finance and Operations وستظهر شاشة تسجيل الدخول لعامل المستودع. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>إزالة حق الوصول لجهاز
عند فقدان جهاز أو تعرضه للاختراق، يجب إزالة حق الوصول إلى Finance and Operations للجهاز. تصف الخطوات التالية العملية الموصى بها لإزالة حق الوصول.

1.  في Finance and Operations، انتقل إلى **إدارة النظام** &gt; **الإعداد** &gt; **تطبيقات Azure Active Directory**.
2.  احذف السطر الذي يتوافق مع الجهاز الذي تريد إزالة حق الوصول الممنوح له. دوّن **"معرف العميل"** المستخدم للجهاز الذي تمت إزالته.
3.  سجل دخولك إلى مدخل Azure التقليدي في <https://manage.windowsazure.com>.
4.  انقر فوق أيقونة **Active Directory** في القائمة اليمنى، ثم انقر فوق الدليل المطلوب.
5.  في القائمة العلوية، انقر فوق **التطبيقات**، ثم انقر فوق التطبيق الذي تريد تكوينه. سوف تظهر صفحة **"البدء السريع"** مع إمكانية تسجيل دخول أحادي ومعلومات تكوين أخرى.
6.  انقر فوق علامة التبويب **تكوين**، وقم بالتمرير لأسفل وتأكد من أن **"معرف العميل"** للتطبيق هو نفسها كما في الخطوة 2 في هذا القسم.
7.  انقر فوق الزر **حذف** في شريط الأدوات.
8.  انقر فوق **نعم** في رسالة التأكيد.





