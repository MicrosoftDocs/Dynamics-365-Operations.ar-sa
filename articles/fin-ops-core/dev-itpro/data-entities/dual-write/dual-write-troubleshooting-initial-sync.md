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
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="b5db6-103">استكشاف المشاكل وإصلاحها أثناء المزامنة الأولية</span><span class="sxs-lookup"><span data-stu-id="b5db6-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b5db6-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="b5db6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b5db6-105">على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="b5db6-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="b5db6-106">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="b5db6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b5db6-107">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="b5db6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="b5db6-108">التحقق من أخطاء المزامنة الأولية في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b5db6-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="b5db6-109">بعد تمكين قوالب التعيين، يجب أن تكون حالة المخططات **قيد التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="b5db6-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="b5db6-110">إذا لم تكن الحالة **قيد التشغيل**، حدثت أخطاء أثناء المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="b5db6-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="b5db6-111">لعرض الأخطاء، حدد علامة التبويب **تفاصيل المزامنة الأولية** في صفحة **الكتابة الثنائية**.</span><span class="sxs-lookup"><span data-stu-id="b5db6-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![علامة التبويب تفاصيل المزامنة الأولية](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="b5db6-113">لا يمكنك إكمال المزامنة الأولية: 400 طلب غير صحيح</span><span class="sxs-lookup"><span data-stu-id="b5db6-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="b5db6-114">**الدور المطلوب لإصلاح المشكلة:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="b5db6-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b5db6-115">قد تتلقى رسالة الخطأ التالية عند محاولة تشغيل التعيين والمزامنة الأولية:</span><span class="sxs-lookup"><span data-stu-id="b5db6-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="b5db6-116">*أرجع الخادم البعيد الخطأ: (400) طلب غير صحيح.)، صادف تصدير AX خطأ*</span><span class="sxs-lookup"><span data-stu-id="b5db6-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="b5db6-117">فيما يلي مثال لرسالة الخطأ الكاملة.</span><span class="sxs-lookup"><span data-stu-id="b5db6-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="b5db6-118">في حاله حدوث هذا الخطأ باستمرار، ولا يمكنك إكمال المزامنة الأولية، فاتبع هذه الخطوات لإصلاح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="b5db6-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="b5db6-119">سجل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5db6-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b5db6-120">افتح وحدة التحكم بالإدارة لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b5db6-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="b5db6-121">في جزء **الخدمات**، تأكد من تشغيل خدمة إطار عمل التصدير الخاص باستيراد بيانات Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b5db6-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="b5db6-122">وأعد تشغيلها إذا تم إيقافها، لأن المزامنة الأولية تتطلب ذلك.</span><span class="sxs-lookup"><span data-stu-id="b5db6-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="b5db6-123">خطأ المزامنة الأولية: 403 ممنوع</span><span class="sxs-lookup"><span data-stu-id="b5db6-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="b5db6-124">قد تتلقى رسالة الخطأ التالية أثناء المزامنة الأولية:</span><span class="sxs-lookup"><span data-stu-id="b5db6-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="b5db6-125">*(\[ممنوع\]، أرجع الخادم البعيد خطأ: (403) ممنوع.)، صادف تصدير AX خطأ*</span><span class="sxs-lookup"><span data-stu-id="b5db6-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="b5db6-126">لإصلاح المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b5db6-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b5db6-127">قم بتسجيل الدخول إلى تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5db6-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="b5db6-128">في صفحة **تطبيقات Azure Active Directory**، احذف عميل **DtAppID**، ثم أضفه مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="b5db6-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![قائمة تطبيقات Azure AD](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="b5db6-130">حالات فشل المراجع الذاتية أثناء المزامنة الأولية</span><span class="sxs-lookup"><span data-stu-id="b5db6-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="b5db6-131">قد تظهر رسالة خطأ مشابهه للمثال التالي إذا كان لأي من التعيينات الخاصة بك مراجع ذاتية:</span><span class="sxs-lookup"><span data-stu-id="b5db6-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="b5db6-132">*بالنسبة للموردين V2، الخطأ التالي: معرف السجل: سجل جديد، ErrorMessage: تعذر حل معرف guid للحقل: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. لم يتم العثور على قيمة البحث: CN-001. جرب عناوين URL هذه للتحقق مما إذا كانت البيانات المرجعية موجودة: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="b5db6-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="b5db6-133">يحدث هذا النوع من الأخطاء أثناء المزامنة الأولية للتعيينات التي لها مراجع ذاتية.</span><span class="sxs-lookup"><span data-stu-id="b5db6-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="b5db6-134">في المثال السابق، يشير حساب فاتورة الحقل إلى كيان المورد.</span><span class="sxs-lookup"><span data-stu-id="b5db6-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="b5db6-135">لإصلاح هذه المشكلة، قد تضطر إلى تشغيل التعيين مرتين قبل نجاح المزامنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="b5db6-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

