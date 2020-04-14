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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172704"
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

## <a name="self-reference-failures-during-initial-synchronization"></a>حالات فشل المراجع الذاتية أثناء المزامنة الأولية

قد تظهر رسالة خطأ مشابهه للمثال التالي إذا كان لأي من التعيينات الخاصة بك مراجع ذاتية:

*بالنسبة للموردين V2، الخطأ التالي: معرف السجل: سجل جديد، ErrorMessage: تعذر حل معرف guid للحقل: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. لم يتم العثور على قيمة البحث: CN-001. جرب عناوين URL هذه للتحقق مما إذا كانت البيانات المرجعية موجودة: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

يحدث هذا النوع من الأخطاء أثناء المزامنة الأولية للتعيينات التي لها مراجع ذاتية. في المثال السابق، يشير حساب فاتورة الحقل إلى كيان المورد.

لإصلاح هذه المشكلة، قد تضطر إلى تشغيل التعيين مرتين قبل نجاح المزامنة الأولية.

