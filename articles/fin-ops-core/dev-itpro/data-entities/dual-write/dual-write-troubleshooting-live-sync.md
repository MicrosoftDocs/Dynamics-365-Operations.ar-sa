---
title: استكشاف المشاكل وإصلاحها في المزامنة المباشرة
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748887"
---
# <a name="troubleshoot-live-synchronization-issues"></a>استكشاف المشاكل وإصلاحها في المزامنة المباشرة

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse. على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>تطرح المزامنة المباشرة خطأ ممنوع 403 عند إنشاء صف في تطبيق Finance and Operations

قد تظهر رسالة الخطأ التالية عند إنشاء صف في تطبيق Finance and Operations:

*\[{\\"الخطأ\\":{\\"الكود\\":\\"0x80072560\\"،\\"الرسالة\\":\\"المستخدم ليس عضوا في المؤسسة.\\"}}\]، أرجع الخادم البعيد الخطأ: (403) ممنوع."}}".*

لإصلاح هذه المشكلة، اتبع الخطوات الموجودة في [متطلبات النظام والمتطلبات الأساسية](requirements-and-prerequisites.md). لإكمال هذه الخطوات، يجب أن يكون لدى مستخدمي تطبيق الكتابة الثنائية الذين تم إنشاؤهم في Dataverse دور مسؤول النظام. يجب أن يكون لدى الفريق المالك الافتراضي دور مسؤول النظام أيضًا.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>تطرح المزامنة المباشرة لأي جدول باستمرار خطأ مشابهًا عند إنشاء صف في تطبيق Finance and Operations

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تتلقى رسالة خطأ مثل الرسالة التالية في كل مرة تحاول فيها حفظ بيانات الجدول في تطبيق Finance and Operations:

*لا يمكن حفظ التغييرات التي تم اجراؤها علي قاعده البيانات. ولا يمكن لوحدة العمل تنفيذ الحركة. وتتعذر كتابة البيانات إلى وحدات قياس الكيانات. وفشلت عمليات الكتابة إلى UnitOfMeasureEntity مع ظهور رسالة الخطأ "تتعذر المزامنة مع وحدات قياس الكيانات.*

لإصلاح المشكلة، يجب التأكد من وجود بيانات مرجع المتطلبات الأساسية في كل من تطبيق Finance and Operations وDataverse. علي سبيل المثال، إذا كان العميل الموجود في تطبيق Finance and Operationsينتمي إلى مجموعة عملاء محددة، فتأكد من وجود مجموعة العملاء في Dataverse.

في حالة وجود بيانات على كلا الجانبين، وقمت بالتأكد من أن المشكلة غير مرتبطة بالبيانات، فاتبع الخطوات التالية.

1. أوقف الجدول المرتبط.
2. قم بتسجيل الدخول إلى تطبيق Finance and Operations، وتأكد من أن الصفوف الخاصة بالجدول الفاشل موجودة في الجدولين DualWriteProjectConfiguration وDualWriteProjectFieldConfiguration. على سبيل المثال، فيما يلي ما يبدو عليه الاستعلام في حالة فشل جدول **العملاء**.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. في حالة وجود صفوف للجدول الفاشل حتى بعد إيقاف تعيين الجدول، فاحذف الصفوف المرتبطة بالجدول الفاشل. دوّن ملاحظة عن العمود **projectname** في جدول DualWriteProjectConfiguration، ثم قم بإحضار صف في الجدول DualWriteProjectFieldConfiguration باستخدام اسم المشروع لحذف الصف.
4. ابدأ تعيين الجدول. تحقق مما إذا كانت ستتم مزامنة البيانات دون أي مشكلات.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>معالجة أخطاء امتيازات القراءة أو الكتابة عند إنشاء بيانات في تطبيق Finance and Operations

قد تظهر رسالة الخطأ "طلب غير صحيح" المشابهة للمثال التالي عند إنشاء بيانات في تطبيق Finance and Operations.

![مثال لرسالة الخطأ "طلب غير صحيح"](media/error_record_id_source.png)

لإصلاح هذه المشكلة، يجب عليك تعيين دور الأمان الصحيح إلى فريق العمل في فريق Dynamics 365 Sales المعين أو وحدة الأعمال الخاصة بـ Dynamics 365 Customer Service لتمكين الامتيازات المفقودة.

1. في تطبيق Finance and Operations، ابحث عن وحدة الأعمال التي تم تعيينها في مجموعة اتصال تكامل البيانات.

    ![تعيين المؤسسة](media/mapped_business_unit.png)

2. قم بتسجيل الدخول إلى البيئة الموجودة في التطبيق المستند إلى النموذج في Dynamics 365، وانتقل إلى **الإعداد \>الأمان**، وابحث عن فريق وحدة الأعمال المعيّنة.

    ![فريق وحدة الأعمال المعيّنة](media/setting_security_page.png)

3. افتح الصفحة الخاصة بالفريق للتحرير، ثم حدد **إدارة الأدوار** لفتح مربع الحوار **إدارة أدوار الفريق**.

    ![الزر إدارة الأدوار](media/manage_team_roles.png)

4. قم بتعيين الدور الذي يحتوي على امتياز القراءة/الكتابة للجداول ذات الصلة، ثم حدد **موافق**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>إصلاح مشكلات المزامنة في بيئة تحتوي على بيئة Dataverse تم تغييرها مؤخرًا

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تظهر رسالة الخطأ التالية عند إنشاء البيانات في تطبيق Finance and Operations:

*{"entityName":"CustCustomerV3Entity"،"executionStatus":2,"fieldResponses":\[\]،"recordResponses":\[{"errorMessage":"**يتعذر إنشاء الحمولة للكيان CustCustomerV3Entity** فشل إنشاء logDateTime":"2019-08-27T18:51:52.5843124Z"،"verboseError":"Payload"،" مع ظهور الخطأ عنوان URL غير صالح: عنوان URI فارغ."}\]،"isErrorCountUpdated":true}*

فيما يلي النمط الذي يبدو عليه الخطأ في التطبيق المستند إلى النموذج في Dynamics 365:

*حدث خطأ غير متوقع من رمز ISV. (ErrorType = ClientError) استثناء غير متوقع من المكون الإضافي (تنفيذ): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: فشلت معالجة حساب الكيان - (فشلت محاولة الاتصال لأن الطرف المتصل لم يستجب بشكل صحيح بعد فترة من الوقت أو فشل الاتصال القائم لأن المضيف المتصل فشل في الاستجابة*

يحدث هذا الخطأ عند إعادة تعيين بيئة Dataverse بشكل غير صحيح في نفس الوقت الذي تحاول فيه إنشاء البيانات في تطبيق Finance and Operations.

لإصلاح المشكلة، اتبع هذه الخطوات.

1. قم بتسجيل الدخول إلى الجهاز الظاهري لـ Finance and Operations، وافتح SQL Server Management STUDIO (ssms) ، وابحث عن الصفوف في الجدول DUALWRITEPROJECTCONFIGURATIONENTITY حيث **internalentityname** يساوي **العملاء V3** و **externalentityname** يساوي **الحسابات**. فيما يلي الشكل الذي يبدو عليه الاستعلام.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. استخدم اسم المشروع من نتائج الاستعلام السابق لتشغيل الاستعلام التالي.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. تأكد من أن العمود **externalenvironmentURL** على عنوان URL الصحيح للتطبيق أو Dataverse. احذف أي صفوف مكررة تشير إلى عنوان URL غير الصحيح لـ Dataverse. احذف الصفوف المقابلة في جدولي DUALWRITEPROJECTFIELDCONFIGURATION وDUALWRITEPROJECTCONFIGURATION.
4. أوقف تعيين الجدول، ثم أعد تشغيله


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]