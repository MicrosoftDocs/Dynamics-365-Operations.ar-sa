---
title: استكشاف المشاكل وإصلاحها في المزامنة المباشرة
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 60839bbd1b3ae642cdd419c7df2388292776a461
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172727"
---
# <a name="troubleshoot-live-synchronization-issues"></a>استكشاف المشاكل وإصلاحها في المزامنة المباشرة

[!include [banner](../../includes/banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service. على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح مشكلات المزامنة المباشرة.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>تطرح المزامنة المباشرة خطأ ممنوع 403 عند إنشاء سجل في تطبيق Finance and Operations

قد تظهر رسالة الخطأ التالية عند إنشاء سجل في تطبيق Finance and Operations:

*\[{\\"الخطأ\\":{\\"الكود\\":\\"0x80072560\\"،\\"الرسالة\\":\\"المستخدم ليس عضوا في المؤسسة.\\"}}\]، أرجع الخادم البعيد الخطأ: (403) ممنوع."}}".*

لإصلاح هذه المشكلة، اتبع الخطوات الموجودة في [متطلبات النظام والمتطلبات الأساسية](requirements-and-prerequisites.md). لإكمال هذه الخطوات، يجب أن يكون لدى مستخدمي تطبيق الكتابة الثنائية الذين تم إنشاؤهم في Common Data Service دور مسؤول النظام. يجب أن يكون لدى الفريق المالك الافتراضي دور مسؤول النظام أيضًا.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>تطرح المزامنة المباشرة لأي كيان باستمرار خطأ مشابهًا عند إنشاء سجل في تطبيق Finance and Operations

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تتلقى رسالة خطأ مثل الرسالة التالية في كل مرة تحاول فيها حفظ بيانات الكيان في تطبيق Finance and Operations:

*لا يمكن حفظ التغييرات التي تم اجراؤها علي قاعده البيانات. ولا يمكن لوحدة العمل تنفيذ الحركة. وتتعذر كتابة البيانات إلى وحدات قياس الكيانات. وفشلت عمليات الكتابة إلى UnitOfMeasureEntity مع ظهور رسالة الخطأ "تتعذر المزامنة مع وحدات قياس الكيانات.*

لإصلاح المشكلة، يجب التأكد من وجود بيانات مرجع المتطلبات الأساسية في كل من تطبيق Finance and Operations وCommon Data Service. علي سبيل المثال، إذا كان العميل الموجود في تطبيق Finance and Operationsينتمي إلى مجموعة عملاء محددة، فتأكد من وجود مجموعة العملاء في Common Data Service.

في حالة وجود بيانات على كلا الجانبين، وقمت بالتأكد من أن المشكلة غير مرتبطة بالبيانات، فاتبع الخطوات التالية.

1. أوقف الكيان المرتبط.
2. قم بتسجيل الدخول إلى تطبيق Finance and Operations، وتأكد من أن السجلات الخاصة بالكيان الفاشل موجودة في الجدولين DualWriteProjectConfiguration وDualWriteProjectFieldConfiguration. على سبيل المثال، فيما يلي ما يبدو عليه الاستعلام في حالة فشل كيان **العملاء**.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. في حالة وجود سجلات للكيان الفاشل حتى بعد إيقاف تعيين الكيان، فاحذف السجلات المرتبطة بالكيان الفاشل. دوّن ملاحظm عن العمود **projectname** في جدول DualWriteProjectConfiguration، ثم قم بإحضار السجل في الجدول DualWriteProjectFieldConfiguration باستخدام اسم المشروع لحذف السجل.
4. ابدأ تعيين الكيان. تحقق مما إذا كانت ستتم مزامنة البيانات دون أي مشكلات.

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

4. قم بتعيين الدور الذي يحتوي على امتياز القراءة/الكتابة للكيانات ذات الصلة، ثم حدد **موافق**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>إصلاح مشكلات المزامنة في بيئة تحتوي على بيئة Common Data Service تم تغييرها مؤخرًا

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تظهر رسالة الخطأ التالية عند إنشاء البيانات في تطبيق Finance and Operations:

*{"entityName":"CustCustomerV3Entity"،"executionStatus":2,"fieldResponses":\[\]،"recordResponses":\[{"errorMessage":"**يتعذر إنشاء الحمولة للكيان CustCustomerV3Entity**فشل إنشاء logDateTime":"2019-08-27T18:51:52.5843124Z"،"verboseError":"Payload"،" مع ظهور الخطأ عنوان URL غير صالح: عنوان URI فارغ."}\]،"isErrorCountUpdated":true}*

فيما يلي النمط الذي يبدو عليه الخطأ في التطبيق المستند إلى النموذج في Dynamics 365:

*حدث خطأ غير متوقع من كود ISV. ‏(ErrorType = ClientError) استثناء غير متوقع من المكون الإضافي (التنفيذ): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: فشل معالجة حساب الكيان-(فشلت محاولة الاتصال بسبب عدم استجابه الجهة المتصلة بشكل صحيح بعد فترة من الوقت، أو فشل تأسيس الاتصال بسبب فشل المضيف المتصل في الاستجابة*

يحدث هذا الخطأ عند إعادة تعيين بيئة Common Data Service بشكل غير صحيح في نفس الوقت الذي تحاول فيه إنشاء البيانات في تطبيق Finance and Operations.

لإصلاح المشكلة، اتبع هذه الخطوات.

1. قم بتسجيل الدخول إلى الجهاز الظاهري لـ Finance and Operations، وافتح SQL Server Management STUDIO (ssms) ، وابحث عن السجلات في الجدول DUALWRITEPROJECTCONFIGURATIONENTITY حيث **internalentityname** يساوي **العملاء V3** و**externalentityname** يساوي **الحسابات**. فيما يلي الشكل الذي يبدو عليه الاستعلام.

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

3. تأكد من أن العمود **externalenvironmentURL** على عنوان URL الصحيح للتطبيق أو Common Data Service. احذف أي سجلات مكررة تشير إلى عنوان URL غير الصحيح لـ Common Data Service. احذف السجلات المقابلة في جدولي DUALWRITEPROJECTFIELDCONFIGURATION وDUALWRITEPROJECTCONFIGURATION.
4. أوقف تعيين الكيان، ثم أعد تشغيله
