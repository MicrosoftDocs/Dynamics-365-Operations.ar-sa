---
title: استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.
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
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941045"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>التحقق من أخطاء المزامنة الأولية في تطبيق Finance and Operations

بعد تمكين قوالب التعيين، يجب أن تكون حالة المخططات **قيد التشغيل**. إذا لم تكن الحالة **قيد التشغيل**، حدثت أخطاء أثناء المزامنة الأولية. لعرض الأخطاء، حدد علامة التبويب **تفاصيل المزامنة الأولية** في صفحة **الكتابة الثنائية**.

![خطأ في علامة التبويب تفاصيل المزامنة الأولية](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>لا يمكنك إكمال المزامنة الأولية: 400 طلب غير صحيح

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل التعيين والمزامنة الأولية:

*(\[طلب غير صحيح\]، يقوم الخادم عن بُعد بإرجاع خطأ: (400) طلب غير صحيح.)، AX صادف التصدير خطأ*

فيما يلي مثال لرسالة الخطأ الكاملة.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

في حاله حدوث هذا الخطأ باستمرار، ولا يمكنك إكمال المزامنة الأولية، فاتبع هذه الخطوات لإصلاح هذه المشكلة.

1. سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.
2. افتح وحدة التحكم بالإدارة لـ Microsoft.
3. في جزء **الخدمات**، تأكد من تشغيل خدمة إطار عمل التصدير الخاص باستيراد بيانات Microsoft Dynamics 365. وأعد تشغيلها إذا تم إيقافها، لأن المزامنة الأولية تتطلب ذلك.

## <a name="initial-synchronization-error-403-forbidden"></a>خطأ المزامنة الأولية: 403 ممنوع

قد تتلقى رسالة الخطأ التالية أثناء المزامنة الأولية:

*(\[ممنوع\]، أرجع الخادم البعيد خطأ: (403) ممنوع.)، صادف تصدير AX خطأ*

لإصلاح المشكلة، اتبع هذه الخطوات.

1. قم بتسجيل الدخول إلى تطبيق Finance and Operations.
2. في صفحة **تطبيقات Azure Active Directory**، احذف عميل **DtAppID**، ثم أضفه مرة أخرى.

![عميل DtAppID في قائمة تطبيقات Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>حالات فشل المراجع الذاتية أو المراجع الدائرية أثناء المزامنة الأولية

قد تتلقى رسائل خطأ عند وجود مراجع ذاتية أو مراجع دائرية لدى أي من تعييناتك. تقع الأخطاء ضمن هذه الفئات:

- [خطأ في تعيين جدول الموردين V2–to–msdyn_vendors](#error-vendor-map)
- [خطأ في تعيين جدول العملاء V3–to–Accounts](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>حل خطأ في تعيين جدول الموردين V2–to–msdyn_vendors

قد تواجه أخطاء المزامنة الأولية لتعيين **الموردون V2** إلى **msdyn\_الموردون** إذا كانت الجداول تحتوي على صفوف حالية حيث توجد قيم في الأعمدة **PrimaryContactPersonId** و **InvoiceVendorAccountNumber**. تحدث هذه الأخطاء لأن **InvoiceVendorAccountNumber** عبارة عن عمود مرجع ذاتي و **PrimaryContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.

سيكون لرسائل الخطأ التي تتلقاها النموذج التالي.

*يتعذر حل guid الدليل للحقل: \<field\>. لم يتم العثور على قيمة البحث: \<value\>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

فيما يلي بعض الأمثلة:

- *يتعذر حل guid الدليل للحقل: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. لم يتم العثور على البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *يتعذر حل guid الدليل للحقل: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. لم يتم العثور على قيمة البحث: V24-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

إذا كانت أية صفوف في جدول مورد تتضمن قيمًا في الأعمدة **PrimaryContactPersonId** و **InvoiceVendorAccountNumber**، فاتبع هذه الخطوات لإكمال المزامنة الأولية.

1. في التطبيق Finance and Operations، احذف العمودين **PrimaryContactPersonId** و **InvoiceVendorAccountNumber** من التعيين، ثم احفظ التعيين.

    1. في صفحة تعيين الكتابة المزدوجة **Vendors V2 (msdyn\_الموردون)**، في علامة التبويب **تعيينات الجدول**، في عامل التصفية الأيسر، حدد **Finance and Operations apps.Vendors V2**. في عامل التصفية الأيمن، حدد **Sales.Vendor**
    2. ابحث عن **primarycontactperson** للعثور على العمود المصدر **PrimaryContactPersonId**.
    3. حدد **الإجراءات**، ثم حدد **حذف**.

        ![حذف العمود PrimaryContactPersonId](media/vend_selfref3.png)

    4. كرر هذه الخطوات لحذف العمود **InvoiceVendorAccountNumber**.

        ![حذف العمود InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. احفظ التغييرات الخاصة بك للتعيين.

2. قم بإيقاف تشغيل تعقب جدول **المورّدون V2**.

    1. في مساحة عمل **إدارة بيانات**، حدد تجانب **جداول البيانات**.
    2. حدد الجدول **المورّدون V2**.
    3. في جزء الإجراء، حدد **الخيارات**، ثم حدد **تعقب التغييرات**.

        ![تحديد خيار تعقب التغييرات](media/selfref_options.png)

    4. حدد **تعطيل تعقب التغييرات**.

        ![تحديد تعطيل تعقب التغييرات](media/selfref_tracking.png)

3. قم بتشغيل المزامنة الأولية لتعيين **الموردون V2 (msdyn\_الموردون)**. يجب أن تنجح المزامنة الأولية بدون حدوث أية أخطاء.
4. قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**. يجب مزامنة هذا التعيين إذا كنت ترغب في مزامنة عمود جهة الاتصال الرئيسية أو جدول الموردين، لأنه يجب إجراء مزامنة أولية لصفوف جهات الاتصال.
5. أضف الأعمدة **PrimaryContactPersonId** و **InvoiceVendorAccountNumber** إلى تعيين **الموردون V2 (msdyn\_vendors)**، ثم احفظ التعيين.
6. قم بتشغيل المزامنة الأولية مرة أخرى لتعيين **الموردون V2 (msdyn\_الموردون)**. ستتم مزامنة كافة الصفوف بسبب إيقاف تشغيل تعقب التغييرات.
7. قم بتشغيل تعقب جدول **المورّدون V2** مرة أخرى.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>حل أخطاء في تعيين جدول العملاء V3–to–Accounts

قد تواجه أخطاء المزامنة الأولية لتعيين **العملاء V3** إلى **الحسابات** إذا كانت الجداول تحتوي على صفوف حالية حيث توجد قيم في الاعمدة **ContactPersonID** و **InvoiceAccount**. يعود سبب حدوث هذه الأخطاء إلى كون **InvoiceAccount** عبارة عن عمود مرجع ذاتي و **ContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.

سيكون لرسائل الخطأ التي تتلقاها النموذج التالي.

*يتعذر حل guid الدليل للحقل: \<field\>. لم يتم العثور على قيمة البحث: \<value\>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

فيما يلي بعض الأمثلة:

- *يتعذر حل guid للحقل: primarycontactid.msdyn\_contactpersonid. لم يتم العثور على البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *يتعذر حل guid للحقل: msdyn\_billingaccount.accountnumber. لم يتم العثور على البحث: 1206-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية:`https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

إذا كانت أية صفوف في كيان العميل تتضمن قيمًا في الأعمدة **ContactPersonID** و **InvoiceAccount**، فاتبع هذه الخطوات لإكمال المزامنة الأولية. يمكنك استخدام هذا الأسلوب لأي جداول جاهزة مثل **الحسابات** و **جهات الاتصال**.

1. في التطبيق Finance and Operations، احذف العمودين **ContactPersonID** و **InvoiceAccount** من التعيين **العملاء V3 (الحسابات)** ثم احفظ التعيين.

    1. في صفحة تعيين الكتابة المزدوجة **العملاء V3 (الحسابات)**، وفي علامة تبويب **تعيينات الجدول**، في عامل التصفية الأيسر، حدد **Finance and Operations app.Customers V3**. في عامل التصفية الأيسر، حدد **Dataverse.Account**.
    2. ابحث عن **contactperson** للعثور على العمود المصدر **ContactPersonID**.
    3. حدد **الإجراءات**، ثم حدد **حذف**.

        ![حذف العمود ContactPersonID](media/cust_selfref3.png)

    4. كرر هذه الخطوات لحذف العمود **‎InvoiceAccount**.

        ![حذف العمود InvoiceAccount](media/cust_selfref4.png)

    5. احفظ التغييرات الخاصة بك للتعيين.

2. قم بإيقاف تشغيل تعقب جدول **العملاء V3**.

    1. في مساحة عمل **إدارة بيانات**، حدد تجانب **جداول البيانات**.
    2. حدد الجدول **العملاء V3**.
    3. في جزء الإجراء، حدد **الخيارات**، ثم حدد **تعقب التغييرات**.

        ![تحديد خيار تعقب التغييرات](media/selfref_options.png)

    4. حدد **تعطيل تعقب التغييرات**.

        ![تحديد تعطيل تعقب التغييرات](media/selfref_tracking.png)

3. قم بتشغيل المزامنة الأولية لتعيين **العملاء V3 (الحسابات)**. يجب أن تنجح المزامنة الأولية بدون حدوث أية أخطاء.
4. قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**.

    > [!NOTE]
    > هناك مخططان لهما نفس الاسم. تأكد من تحديد المخطط الذي يتضمن الوصف التالي في علامة التبويب **تفاصيل**: **قالب كتابة مزدوجة للمزامنة بين FO.CDS المورّدون جهات الاتصال V2 وCDS.Contacts. بحاجة إلى حزمة جديدة \[Dynamics365SupplyChainExtended\].**

5. أعد إضافة العمودين **InvoiceAccount** و **ContactPersonId** إلى تعيين **العملاء V3 (الحسابات)**، ثم احفظ التعيين. العمودان **InvoiceAccount** و **ContactPersonId** هما الآن عبارة عن جزء من وضع المزامنة المباشرة مرة أخرى. في الخطوة التالية، ستقوم بالمزامنة الأولية لهذه الأعمدة.
6. قم بتشغيل المزامنة الأولية مرة أخرى لتعيين **العملاء V3 (الحسابات)**. بسبب إيقاف تشغيل تعقب التغييرات، سيؤدي تشغيل المزامنة إلى مزامنة بيانات **InvoiceAccount** و **ContactPersonId** من التطبيق Finance and Operations إلى Dataverse.
7. لمزامنة بيانات **InvoiceAccount** و **ContactPersonId** من تطبيق Dataverse إلى Finance and Operations، فإنك تستخدم مشروع تكامل البيانات.

    1. في Power Apps، أنشئ مشروع تكامل البيانات بين الجدولين **Sales.Account** و **Finance and Operations apps.Customers V3**. يجب أن يكون اتجاه البيانات من Dataverse إلى التطبيق Finance and Operations. لأن **InvoiceAccount** عبارة عن سمة جديدة في الكتابة المزدوجة، فقد ترغب في تخطي المزامنة الأولية لهذه السمة. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Dataverse](/power-platform/admin/data-integrator).

        يوضح الرسم التوضيحي التالي مشروعًا يقوم بتحديث **CustomerAccount** و **ContactPersonId**.

        ![مشروع تكامل البيانات لتحديث CustomerAccount وCustomerAccount](media/cust_selfref6.png)

    2. أضف معايير الشركة في عامل التصفية على جانب Dataverse، لذلك فإن الصفوف التي تطابق معايير التصفية هي وحدها التي سيتم تحديثها في التطبيق Finance and Operations. لإضافة عامل تصفية، حدد زر عامل التصفية. ثم في مربع الحوار **تحرير الاستعلام**، فإنه يمكنك إضافة استعلام عامل تصفية مثل **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [ملحوظة] إذا لم يكن زر عامل التصفية موجودًا، فأنشئ تذكرة دعم كي تطلب من فريق تكامل البيانات تمكين إمكانية التصفية على المستأجر.

        إذا لم تقم بإدخال استعلام عامل تصفية للقيمة **\_msdyn\_company\_value**، فستتم مزامنة جميع الصفوف.

        ![إضافة استعلام عامل تصفية](media/cust_selfref7.png)

    يتم الآن إكمال المزامنة الأولية للصفوف.

8. في التطبيق  Finance and Operations، قم بتشغيل تعقب التغييرات مرة أخرى الجدول **العملاء V3**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]