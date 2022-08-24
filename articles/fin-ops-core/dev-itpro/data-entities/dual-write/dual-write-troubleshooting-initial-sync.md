---
title: استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية
description: توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها الذي يمكن أن تساعدك على إصلاح المشكلات التي قد تحدث في أثناء المزامنة الأولية.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289473"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية

[!include [banner](../../includes/banner.md)]



توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها في تكامل الكتابة المزدوجة بين تطبيقات التمويل والعمليات وDataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي تتناولها هذه المقالة إما منصب مسؤول النظام أو بيانات اعتماد مسؤول مستأجر Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>التحقق من أخطاء المزامنة الأولية في تطبيقات التمويل والعمليات

بعد تمكين قوالب التعيين، يجب أن تكون حالة المخططات **قيد التشغيل**. إذا لم تكن الحالة **قيد التشغيل**، حدثت أخطاء أثناء المزامنة الأولية. لعرض الأخطاء، حدد علامة التبويب **تفاصيل المزامنة الأولية** في صفحة **الكتابة الثنائية**.

![خطأ في علامة التبويب تفاصيل المزامنة الأولية.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>لا يمكنك إكمال المزامنة الأولية: 400 طلب غير صحيح

**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام

قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل التعيين والمزامنة الأولية:

*(\[طلب غير صحيح\]، يقوم الخادم عن بُعد بإرجاع خطأ: (400) طلب غير صحيح.)، AX صادف التصدير خطأ.*

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

1. سجل دخولك إلى الجهاز الظاهري (VM) لتطبيق التمويل والعمليات.
2. افتح وحدة التحكم بالإدارة لـ Microsoft.
3. في جزء **الخدمات**، تأكد من تشغيل خدمة إطار عمل التصدير الخاص باستيراد بيانات Microsoft Dynamics 365. وأعد تشغيلها إذا تم إيقافها، لأن المزامنة الأولية تتطلب ذلك.

## <a name="initial-synchronization-error-403-forbidden"></a>خطأ المزامنة الأولية: 403 ممنوع

قد تتلقى رسالة الخطأ التالية أثناء المزامنة الأولية:

*(\[ممنوع\]، أرجع الخادم البعيد خطأ: (403) ممنوع.)، صادف تصدير AX خطأ*

لإصلاح المشكلة، اتبع هذه الخطوات.

1. سجّل دخولك إلى تطبيق التمويل والعمليات.
2. في صفحة **تطبيقات Azure Active Directory**، احذف عميل **DtAppID**، ثم أضفه مرة أخرى.

![عميل DtAppID في قائمة تطبيقات Azure AD.](media/aad_applications.png)

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

1. في تطبيق التمويل والعمليات، احذف العمودين **PrimaryContactPersonId** و **InvoiceVendorAccountNumber** من التعيين، ثم احفظ التعيين.

    1. في صفحة تعيين الكتابة المزدوجة **Vendors V2 (msdyn\_vendors)**، على علامة تبويب **تعيينات الجدول** في عامل التصفية الأيسر، حدد **apps.Vendors V2 لتطبيقات التمويل والعمليات**. في عامل التصفية الأيمن، حدد **Sales.Vendor**
    2. ابحث عن **primarycontactperson** للعثور على العمود المصدر **PrimaryContactPersonId**.
    3. حدد **الإجراءات**، ثم حدد **حذف**.

        ![حذف العمود PrimaryContactPersonId.](media/vend_selfref3.png)

    4. كرر هذه الخطوات لحذف العمود **InvoiceVendorAccountNumber**.

        ![حذف العمود InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. احفظ التغييرات الخاصة بك للتعيين.

2. قم بإيقاف تشغيل تعقب جدول **المورّدون V2**.

    1. في مساحة عمل **إدارة بيانات**، حدد تجانب **جداول البيانات**.
    2. حدد الجدول **المورّدون V2**.
    3. في جزء الإجراء، حدد **الخيارات**، ثم حدد **تعقب التغييرات**.

        ![تحديد خيار تعقب التغييرات.](media/selfref_options.png)

    4. حدد **تعطيل تعقب التغييرات**.

        ![تحديد تعطيل تعقب التغييرات.](media/selfref_tracking.png)

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

1. في تطبيق التمويل والعمليات، احذف العمودين **ContactPersonID** و **InvoiceAccount** من التعيين **العملاء V3 (الحسابات)**، ثم احفظ التعيين.

    1. في صفحة تعيين الكتابة المزدوجة **الإصدار 3 من العملاء (الحسابات)**، وفي علامة تبويب **تعيينات الجدول**، في عامل التصفية الأيسر، حدد **app.Customers V3 للتمويل والعمليات**. في عامل التصفية الأيسر، حدد **Dataverse.Account**.
    2. ابحث عن **contactperson** للعثور على العمود المصدر **ContactPersonID**.
    3. حدد **الإجراءات**، ثم حدد **حذف**.

        ![حذف العمود ContactPersonID.](media/cust_selfref3.png)

    4. كرر هذه الخطوات لحذف العمود **‎InvoiceAccount**.

        ![حذف العمود InvoiceAccount.](media/cust_selfref4.png)

    5. احفظ التغييرات الخاصة بك للتعيين.

2. قم بإيقاف تشغيل تعقب جدول **العملاء V3**.

    1. في مساحة عمل **إدارة بيانات**، حدد تجانب **جداول البيانات**.
    2. حدد الجدول **العملاء V3**.
    3. في جزء الإجراء، حدد **الخيارات**، ثم حدد **تعقب التغييرات**.

        ![تحديد خيار تعقب التغييرات.](media/selfref_options.png)

    4. حدد **تعطيل تعقب التغييرات**.

        ![تحديد تعطيل تعقب التغييرات.](media/selfref_tracking.png)

3. قم بتشغيل المزامنة الأولية لتعيين **العملاء V3 (الحسابات)**. يجب أن تنجح المزامنة الأولية بدون حدوث أية أخطاء.
4. قم بتشغيل المزامنة الأولية لتعيين **جهات اتصال CDS V2 (جهات الاتصال)**.

    > [!NOTE]
    > هناك مخططان لهما نفس الاسم. تأكد من تحديد المخطط الذي يتضمن الوصف التالي في علامة التبويب **تفاصيل**: **قالب كتابة مزدوجة للمزامنة بين FO.CDS المورّدون جهات الاتصال V2 وCDS.Contacts. بحاجة إلى حزمة جديدة \[Dynamics365SupplyChainExtended\].**

5. أعد إضافة العمودين **InvoiceAccount** و **ContactPersonId** إلى تعيين **العملاء V3 (الحسابات)**، ثم احفظ التعيين. العمودان **InvoiceAccount** و **ContactPersonId** هما الآن عبارة عن جزء من وضع المزامنة المباشرة مرة أخرى. في الخطوة التالية، ستقوم بالمزامنة الأولية لهذه الأعمدة.
6. قم بتشغيل المزامنة الأولية مرة أخرى لتعيين **العملاء V3 (الحسابات)**. بسبب إيقاف تشغيل تعقب التغييرات، ستتم مزامنة بيانات **InvoiceAccount** و **ContactPersonId** من تطبيق التمويل والعمليات إلى Dataverse.
7. لمزامنة بيانات **InvoiceAccount** و **ContactPersonId** من Dataverse إلى تطبيق التمويل والعمليات، يجب استخدام مشروع تكامل بيانات.

    1. في Power Apps، أنشئ مشروع تكامل البيانات بين الجدولين **Sales.Account** و **التمويل والعمليات apps.Customers V3**. يجب أن يكون اتجاه البيانات من Dataverse إلى تطبيق التمويل والعمليات. لأن **InvoiceAccount** عبارة عن سمة جديدة في الكتابة المزدوجة، فقد ترغب في تخطي المزامنة الأولية لهذه السمة. للحصول على مزيد من المعلومات، راجع [دمج البيانات في Dataverse](/power-platform/admin/data-integrator).

        يوضح الرسم التوضيحي التالي مشروعًا يقوم بتحديث **CustomerAccount** و **ContactPersonId**.

        ![مشروع تكامل البيانات لتحديث CustomerAccount وCustomerAccount.](media/cust_selfref6.png)

    2. أضف معايير الشركة في عامل التصفية على جانب Dataverse، بحيث يتم تحديث فقط الصفوف التي تطابق معايير التصفية في تطبيق التمويل والعمليات. لإضافة عامل تصفية، حدد زر عامل التصفية. ثم في مربع الحوار **تحرير الاستعلام**، فإنه يمكنك إضافة استعلام عامل تصفية مثل **\_msdyn\_company\_value eq '\<guid\>'**.

        > [ملحوظة] إذا لم يكن زر عامل التصفية موجودًا، فأنشئ تذكرة دعم كي تطلب من فريق تكامل البيانات تمكين إمكانية التصفية على المستأجر.

        إذا لم تقم بإدخال استعلام عامل تصفية للقيمة **\_msdyn\_company\_value**، فستتم مزامنة جميع الصفوف.

        ![إضافة استعلام عامل تصفية.](media/cust_selfref7.png)

    يتم الآن إكمال المزامنة الأولية للصفوف.

8. في تطبيق التمويل والعمليات، قم بتشغيل تعقب التغييرات مرة أخرى لجدول **العملاء V3**.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>فشل المزامنة الأولية على الخرائط مع أكثر من 10 حقول بحث

قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل فشل مزامنة أولية على **العملاء V3 - حسابات** أو تعيينات **أوامر المبيعات** أو أي خريطة مع أكثر من 10 حقول بحث:

*CRMExport: اكتمال تنفيذ الحزمة. خطأ وصف 5 محاولات للحصول على البيانات من https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc failed.*

وبسبب قيود البحث على الاستعلام، فشل المزامنة الأولية عندما يحتوي تعيين الكيان على أكثر من 10 عمليات بحث. لمزيد من المعلومات، راجع [استرداد سجلات الجداول ذات الصلة باستخدام استعلام](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

لإصلاح هذه المشكلة، اتبع هذه الخطوات:

1. إزالة حقول البحث الاختيارية من مخطط الكيان ثنائي الكتابة بحيث يكون عدد عمليات البحث 10 أو أقل.
2. حفظ الخريطة والقيام بالمزامنة الأولية.
3. عند نجاح المزامنة الأولية للخطوة الأولى، أضف حقول البحث المتبقية وأزل حقول البحث التي قمت بمزامنتها في الخطوة الأولى. تأكد من أن عدد حقول البحث 10 أو أقل. حفظ الخريطة وتشغيل المزامنة الأولية.
4. كرر هذه الخطوات حتى تتم مزامنة كافة حقول البحث.
5. إضافة كافة حقول البحث مرة أخرى إلى الخريطة وحفظ الخريطة وتشغيل الخريطة مع **تخطي المزامنة الأولية**.

تمكن هذه العملية الخريطة لوضع المزامنة المباشرة.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>مشكلة معروفة أثناء المزامنة الأولية للعناوين البريدية للطرف والعناوين الإلكترونية للطرف

قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل syn الأولية من عناوين الطرف البريدية والعناوين الإلكترونية الطرف:

*تعذر العثور على رقم الطرف في Dataverse.*

هناك مجموعة نطاقات على **DirPartyCDSEntity** في تطبيق التمويل والعمليات يقوم بتصفية الأطراف من النوع **شخص** و **مؤسسة**. ونتيجة لذلك، لن تؤدي المزامنة الأولية لتعيين **أطراف CDS‏ - msdyn_parties** إلى مزامنة الأطراف من الأنواع الأخرى، بما في ذلك **الكيان القانوني** و **وحدة التشغيل**. عند تشغيل المزامنة الأولية **للعناوين البريدية لأطراف CDS‏ ‏(msdyn_partypostaladdresses)** أو **جهات اتصال الأطراف V3 ‏(msdyn_partyelectronicaddresses)** قد تتلقى الخطأ.

نحن نعمل على إصلاح لإزالة نطاق نوع الطرف على كيان التمويل والعمليات بحيث يمكن مزامنة الأطراف من جميع الأنواع مع Dataverse بنجاح.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>هل هناك أي مشكلات في الأداء أثناء تشغيل المزامنة الأولية لبيانات العملاء أو جهات الاتصال؟

إذا قمت بتشغيل المزامنة الأولية لبيانات **العميل** وكان لديك مخططات **العملاء** قيد التشغيل ومن ثم يتم تشغيل المزامنة الأولية لبيانات **جهات الاتصال**، قد تكون هناك مشكلات في الأداء أثناء عمليات الإدراج والتحديثات إلى جدولي **LogisticsPostalAddress** و **LogisticsElectronicAddress** لعناوين **جهات الاتصال**. يتم تعقب نفس العنوان البريدي العمومي وجداول العناوين الإلكترونية لـ **CustCustomerV3Entity** و **VendVendorV2Entity** ويحاول الكتابة المزدوجة إنشاء المزيد من الاستعلامات لكتابة البيانات إلى الجانب الآخر. إذا كنت قد قمت بتشغيل المزامنة الأولية **للعميل** بالفعل، فقم بإيقاف الخريطة المقابلة أثناء تشغيل المزامنة الأولية لبيانات **جهات الاتصال**. قم بنفس الشيء لبيانات **المورد**. عند انتهاء المزامنة الأولية، يمكنك تشغيل كافة الخرائط عن طريق تخطي المزامنة الأولية.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>لا يمكن مزامنة نوع البيانات الذي تم تعويمه والذي يحتوي علي قيمة صفرية

قد تفشل المزامنة الأولية للسجلات التي لها قيمة صفرية لحقل السعر، مثل **مبلغ الدفعة الثابتة** أو **المبلغ** بعملة الحركة. في هذه الحالة، ستتلقي رسالة خطأ مشابهة للمثال التالي:

*حدث خطأ أثناء التحقق من معلمات الإدخال: Microsoft.OData.ODataException: لا يمكن تحويل '000000' الحرفي إلى النوع المتوقع 'Edm.Decimal'، ...*

تكمن المشكلة في قيمة **اللغة المحلية** ضمن **تنسيقات بيانات المصدر** في وحدة **إدارة البيانات**. قم بتغيير قيمة حقل **اللغة المحلية** إلى **en-us**، ثم حاول مرة أخرى.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

