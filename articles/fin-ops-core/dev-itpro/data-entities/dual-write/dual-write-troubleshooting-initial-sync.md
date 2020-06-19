---
title: استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.
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
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410071"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>التحقق من أخطاء المزامنة الأولية في تطبيق Finance and Operations

بعد تمكين قوالب التعيين، يجب أن تكون حالة المخططات **قيد التشغيل**. إذا لم تكن الحالة **قيد التشغيل**، حدثت أخطاء أثناء المزامنة الأولية. لعرض الأخطاء، حدد علامة التبويب **تفاصيل المزامنة الأولية** في صفحة **الكتابة الثنائية**.

![علامة التبويب تفاصيل المزامنة الأولية](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>لا يمكنك إكمال المزامنة الأولية: 400 طلب غير صحيح

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل التعيين والمزامنة الأولية:

*أرجع الخادم البعيد الخطأ: (400) طلب غير صحيح.)، صادف تصدير AX خطأ*

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

![قائمة تطبيقات Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>حالات فشل المراجع الذاتية أو المراجع الدائرية أثناء المزامنة الأولية

قد تتلقى رسائل خطأ عند وجود مراجع ذاتية أو مراجع دائرية لدى أي من تعييناتك. تقع الأخطاء ضمن هذه الفئات:

- [تعيين كيان المورّدون V2 في مقابل msdyn_vendors](#error-vendor-map)
- [تعيين كيان العملاء V3 في مقابل الحسابات](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>حل خطأ في تعيين كيان المورّدون V2 في مقابل msdyn_vendors

قد تواجه أخطاء المزامنة الأولية التالية على تعيين **المورّدون V2** في مقابل **msdyn_vendors** إذا تضمنت الكيانات سجلات موجودة لديها قيم في الحقلين **PrimaryContactPersonId** و**InvoiceVendorAccountNumber**. يعود سبب ذلك إلى كون **InvoiceVendorAccountNumber** عبارة عن حقل مرجع ذاتي و**PrimaryContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.

*تعذّر حل guid للحقل: <field>. لم يتم العثور على قيمة البحث: <value>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

فيما يلي بعض الأمثلة:

- *تعذّر حل guid للحقل: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. لم يتم العثور على قيمة البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *تعذّر حل guid للحقل: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. لم يتم العثور على قيمة البحث: V24-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

إذا كانت لديك سجلات تتضمن قيمًا في هذه الحقول في كيان المورّد، فاتبع الخطوات في القسم أدناه لإكمال المزامنة الأولية.

1. في التطبيق Finance and Operations، احذف الحقلين **PrimaryContactPersonId** و**InvoiceVendorAccountNumber** من التعيين واحفظ التغييرات.

    1. انتقل إلى صفحة تعيين الكتابة المزدوجة **المورّدون V2 (msdyn_vendors)**، وحدد علامة تبويب **تعيينات الكيان**. في عامل التصفية الأيسر، حدد **Finance and Operations apps.Vendors V2**. في عامل التصفية الأيمن، حدد **Sales.Vendor**

    2. ابحث عن **primarycontactperson** للعثور على الحقل المصدر **PrimaryContactPersonId**.
    
    3. انقر فوق زر **الإجراءات**، وحدد **حذف**.
    
        ![مرجع ذاتي أو دائري 3](media/vend_selfref3.png)
    
    4. كرر الإجراء لحذف الحقل **InvoiceVendorAccountNumber**.
    
        ![مرجع ذاتي أو دائري 4](media/vend-selfref4.png)
    
    5. احفظ تغييرات التعيين.

2. عطّل تعقب التغييرات لكيان **المورّدون V2**.

    1. انتقل إلى **إدارة البيانات \> كيانات البيانات**.
    
    2. حدد الكيان **المورّدون V2**.
    
    3. انقر فوق **خيارات** من شريط القوائم، ثم فوق **تعقب التغييرات**.
    
        ![مرجع ذاتي أو دائري 5](media/selfref_options.png)
    
    4. انقر فوق **تعطيل تعقب التغييرات**.
    
        ![مرجع ذاتي أو دائري 6](media/selfref_tracking.png)

3. قم بتشغيل المزامنة الأولية لتعيين **المورّدون V2 (msdyn_vendors)**. يجب أن تنجح المزامنة الأولية بدون حدوث أي أخطاء.

4. قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**. يجب مزامنة هذا التعيين إذا كنت ترغب في مزامنة حقل جهة الاتصال الرئيسية أو كيان الموردين لأنه يجب إجراء مزامنة أولية لسجلات جهات الاتصال.

5. أعد إضافة الحقلين **PrimaryContactPersonId** و**InvoiceVendorAccountNumber** إلى تعيين **المورّدون V2 (msdyn_vendors)** واحفظ التعيين.

6. قم بتشغيل المزامنة الأولية من جديد لتعيين **المورّدون V2 (msdyn_vendors)**. ستتم مزامنة كافة السجلات بسبب تعطيل تعقب التغييرات.

7. مكّن تعقب التغييرات لكيان **المورّدون V2**.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>حل خطأ في تعيين كيان العملاء V3 في مقابل الحسابات

قد تواجه أخطاء المزامنة الأولية التالية على تعيين **العملاء V3** في مقابل **الحسابات** إذا تضمنت الكيانات سجلات موجودة لديها قيم في الحقلين **ContactPersonID** و**InvoiceAccount**. يعود سبب ذلك إلى كون **InvoiceAccount** عبارة عن حقل مرجع ذاتي و**ContactPersonId** عبارة عن مرجع دائري في تعيين المورّد.

*تعذّر حل guid للحقل: <field>. لم يتم العثور على قيمة البحث: <value>. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *تعذّر حل guid للحقل: primarycontactid.msdyn_contactpersonid. لم يتم العثور على قيمة البحث: 000056. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *تعذّر حل guid للحقل: msdyn_billingaccount.accountnumber. لم يتم العثور على قيمة البحث: 1206-1. جرّب عنوان (عناوين) URL هذا للتأكد من وجود البيانات المرجعية: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

إذا كانت لديك سجلات تتضمن قيمًا في هذه الحقول في كيان العميل، فاتبع الخطوات في القسم أدناه لإكمال المزامنة الأولية. يمكنك استخدام هذا الأسلوب لأي كيانات جاهزة مثل الحسابات وجهات الاتصال.

1. في التطبيق Finance and Operations، احذف الحقلين **ContactPersonID** و**InvoiceAccount** من التعيين **العملاء V3 (الحسابات)** واحفظ التعيين.

    1. انتقل إلى صفحة تعيين الكتابة المزدوجة **العملاء V3 (الحسابات)**، وحدد علامة تبويب **تعيينات الكيان**. في عامل التصفية الأيسر، حدد **Finance and Operations app.Customers V3**. في عامل التصفية الأيسر، حدد **Common Data Service.Account**.

    2. ابحث عن **contactperson** للعثور على الحقل المصدر **ContactPersonID**.
    
    3. انقر فوق زر **الإجراءات**، وحدد **حذف**.
    
        ![مرجع ذاتي أو دائري 3](media/cust_selfref3.png)
    
    4. كرر الإجراء لحذف الحقل **InvoiceAccount**.
    
        ![مرجع ذاتي أو دائري](media/cust_selfref4.png)
    
    5. احفظ تغييرات التعيين.

2. عطّل تعقب التغييرات لكيان **العملاء V3**.

    1. انتقل إلى **إدارة البيانات \> كيانات البيانات**.
    
    2. حدد الكيان **العملاء V3**.
    
    3. انقر فوق **خيارات** من شريط القوائم، ثم فوق **تعقب التغييرات**.
    
        ![مرجع ذاتي أو دائري 5](media/selfref_options.png)
    
    4. انقر فوق **تعطيل تعقب التغييرات**.
    
        ![مرجع ذاتي أو دائري 6](media/selfref_tracking.png)

3. قم بتشغيل المزامنة الأولية لتعيين **العملاء V3 (الحسابات)**. يجب أن تنجح المزامنة الأولية بدون حدوث أي أخطاء.

4. قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**. هناك خريطتان بالاسم نفسه. حدد الخريطة التي تتضمن الوصف **قالب كتابة مزدوجة للمزامنة بين FO.CDS المورّدون جهات الاتصال V2 وCDS.Contacts. بحاجة إلى حزمة جديدة \[Dynamics365SupplyChainExtended\].** على علامة التبويب **تفاصيل** للخريطة.

5. أعد إضافة الحقلين **InvoiceAccount** و**ContactPersonId** إلى تعيين **العملاء V3 (الحسابات)** واحفظ التعيين. الحقلان **InvoiceAccount** و**ContactPersonId** هما الآن من جديد عبارة عن جزء من وضع المزامنة المباشرة. في الخطوة التالية، ستكمل المزامنة الأولية لهذه الحقول.

6. قم بتشغيل المزامنة الأولية من جديد لتعيين **العملاء V3 (الحسابات)**. بسبب تعطيل تعقب التغييرات، سيؤدي تشغيل المزامنة إلى مزامنة بيانات **InvoiceAccount** و**ContactPersonId** من التطبيق Finance and Operations إلى Common Data Service.

7. لمزامنة بيانات **InvoiceAccount** و**ContactPersonId** من Common Data Service إلى Finance and Operations، تستخدم مشروع تكامل البيانات.

    1. في Power Apps، أنشئ مشروع تكامل البيانات بين الكيانين **Sales.Account** و**Finance and Operations apps.Customers V3**. يجب أن يكون اتجاه البيانات من Common Data Service إلى التطبيق Finance and Operations.  لأن **InvoiceAccount** عبارة عن سمة جديدة في الكتابة المزدوجة، فقد ترغب في تخطي المزامنة الأولية لهذه السمة. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        تظهر الصورة التالية مشروعًا يقوم بتحديث **CustomerAccount** و**ContactPersonId**.

        ![مرجع ذاتي أو دائري](media/cust_selfref6.png)

    2. أضف معايير الشركة في عامل التصفية على جانب Common Data Service، لأنه السجلات التي تطابق معايير التصفية هي وحدها التي سيتم تحديثها في التطبيق Finance and Operations. لإضافة عامل تصفية، انقر فوق أيقونة التصفية. في مربع الحوار **تحرير الاستعلام**، يمكنك إضافة استعلام تصفية مثل **_msdyn_company_value eq '\<guid\>'**. إذا لم تكن أيقونة التصفية موجودة، فأنشئ تذكرة دعم كي تطلب من فريق تكامل البيانات تمكين إمكانية التصفية على المستأجر. إذا لم تقم بإدخال استعلام تصفية للقيمة **_msdyn_company_value**، فستتم مزامنة جميع السجلات.

        ![مرجع ذاتي أو دائري](media/cust_selfref7.png)

        يؤدي ذلك إلى إكمال المزامنة الأولية للسجلات.

8. مكّن تعقب التغييرات لكيان **العملاء V3** في التطبيق Finance and Operations.

