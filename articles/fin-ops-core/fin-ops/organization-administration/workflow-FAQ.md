---
title: الأسئلة المتداولة حول سير العمل
description: يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل.
author: ChrisGarty
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdddd26a662e9334f6d3c9806871df5b58ec03c7
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934899"
---
# <a name="workflow-faq"></a><span data-ttu-id="13692-103">الأسئلة المتداولة حول سير العمل</span><span class="sxs-lookup"><span data-stu-id="13692-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13692-104">يجيب هذا الموضوع عن الأسئلة المتداولة حول نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13692-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="13692-105">لماذا أتلقى إخطارات متعددة عند رفض عنصر عمل؟</span><span class="sxs-lookup"><span data-stu-id="13692-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="13692-106">عند رفض عنصر عمل، يتم إكمال هذا العنصر كعنصر مرفوض.</span><span class="sxs-lookup"><span data-stu-id="13692-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="13692-107">ويتم إنشاء عنصر عمل آخر وتعيينه إلى المنشئ.</span><span class="sxs-lookup"><span data-stu-id="13692-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="13692-108">وهذا يعني إرسال إخطار إلى المنشئ يتعلق بعنصر العمل المرفوض وإخطار منفصل إلى المستخدم المعيّن إلى عنصر العمل الجديد "التغيير المطلوب‬".</span><span class="sxs-lookup"><span data-stu-id="13692-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="13692-109">يتعلق كل إخطار بعنصر عمل مختلف، ولكن التشابه قد يسبب الإرباك.</span><span class="sxs-lookup"><span data-stu-id="13692-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="13692-110">نحن بصدد البحث عن طرق لتحسين هذا الأمر في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="13692-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="13692-111">لماذا يفشل تصدير عمليات سير العمل؟</span><span class="sxs-lookup"><span data-stu-id="13692-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="13692-112">يوجد حاليًا قيد في ميزة تصدير عمليات سير العمل يمنع تجاوز أسماء عمليات سير العمل 48 حرفًا.</span><span class="sxs-lookup"><span data-stu-id="13692-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="13692-113">قد يؤدي استخدام اسم أطول من 48 حرفًا إلى ظهور الخطأ "فشل الخادم في مصادقة الطلب" و/أو منع تصدير ملف بدون نوع ملف.</span><span class="sxs-lookup"><span data-stu-id="13692-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="13692-114">يوفر منشور المدونة التالي المزيد من التفاصيل [استكشاف أخطاء تصدير سير العمل وإصلاحها](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="13692-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="13692-115">هل يمكن لمرسل سير عمل القيام أيضًا الموافقة على سير العمل؟</span><span class="sxs-lookup"><span data-stu-id="13692-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="13692-116">نعم، يمكن أيضًا لمرسل سير عمل الموافقة على سير العمل إذا تم تكوينه بهذه الطريقة.</span><span class="sxs-lookup"><span data-stu-id="13692-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="13692-117">لمنع حدوث مثل هذا السلوك، عيِّن **إدارة النظام > سير العمل > معلمات سير العمل > عام > المعتمد > عدم السماح للمرسِل بالموافقة‬** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="13692-117">To prevent this behavior, set **System administration > Workflow > Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="13692-118">هل يمكنني إضافة تنبيهات إلى مهام سير العمل لتوفير إخطارات للمستخدمين؟</span><span class="sxs-lookup"><span data-stu-id="13692-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="13692-119">فيما يلي بعض المناطق الأساسية لملاحظة إضافة تنبيهات إلى مهام سير العمل لتوفير إخطارات:</span><span class="sxs-lookup"><span data-stu-id="13692-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="13692-120">التنبيهات مقابل آليات إخطار سير العمل</span><span class="sxs-lookup"><span data-stu-id="13692-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="13692-121">يمكن إعداد التنبيهات لتغييرات السجلات.</span><span class="sxs-lookup"><span data-stu-id="13692-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="13692-122">تغير مهام سير العمل السجلات، لذا من الممكن إعداد تنبيه مرتبط بتغيير سجل يحدث بسبب سير عمل.</span><span class="sxs-lookup"><span data-stu-id="13692-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="13692-123">ولكن نظرًا لوجود خيارات إخطار مضمنة مختلفة لمهام سير العمل، لا يعد استخدام التنبيهات مثاليًا.</span><span class="sxs-lookup"><span data-stu-id="13692-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="13692-124">إخطارات قياسية من مهام سير العمل</span><span class="sxs-lookup"><span data-stu-id="13692-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="13692-125">توجد إخطارات بريد إلكتروني مضمنة ف مهام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="13692-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="13692-126">يمكن للعميل تكوين الإخطارات بحيث يتم إرسال رسائل بريد إلكتروني إلى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="13692-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="13692-127">لا تؤدي هذه الإخطارات إلى إرسال رسائل مركز الإجراءات للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="13692-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="13692-128">في أحد التحديثات المستقبلية ستتم إضافة رسالة مركز الإجراءات حتى يتم تعيين عنصر عمل سير العمل إلى المستخدم.</span><span class="sxs-lookup"><span data-stu-id="13692-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="13692-129">إضافة إخطارات لمهام سير العمل</span><span class="sxs-lookup"><span data-stu-id="13692-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="13692-130">يمكن إنشاء رسائل مركز الإجراءات لمستخدمين محددين، مثل رسالة تم إنشاؤها من سير عمل في X++.</span><span class="sxs-lookup"><span data-stu-id="13692-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="13692-131">[تحتوي مهام سير العمل علي أحداث أعمال](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) يمكن للعميل استخدامها لتشغيل المهام ذات الإشعارات التي يبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="13692-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="13692-132">وفي الملخص، في حالة عدم حصول المستخدم على الإخطار المناسب من مركز الإجراءات عند تعيين عنصر عمل لسير العمل، قم بزيادة [أحداث أعمال سير العمل](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) مع Microsoft Power Automate لتوفير إخطارات إضافية أو مختلفة.</span><span class="sxs-lookup"><span data-stu-id="13692-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Power Automate to provide additional or different notifications.</span></span>

## <a name="workflow-editor-has-trouble-starting-under-adfs"></a><span data-ttu-id="13692-133">يواجه محرر سير العمل مشكلة في بدء التشغيل ضمن ADFS</span><span class="sxs-lookup"><span data-stu-id="13692-133">Workflow editor has trouble starting under ADFS</span></span> 
<span data-ttu-id="13692-134">عند التشغيل ضمن ‏‫خدمات الأمان المشترك لـ Active Directory (AD FS)‬ في بيئة تمت ترقيتها، فقد يواجه محرر سير العمل مشكلة في بدء التشغيل.</span><span class="sxs-lookup"><span data-stu-id="13692-134">When running under Active Directory Federation Services (AD FS) in an upgraded environment, the workflow editor may have trouble starting.</span></span> <span data-ttu-id="13692-135">إذا كان الأمر كذلك ، تأكد من إضافة عنوان URL "https://dynamicsaxworkfloweditor/" إلى الخاصية **Microsoft Dynamics 365 for Operations محلي - سير العمل - التطبيق الأصلي** في إعدادات ADFS.</span><span class="sxs-lookup"><span data-stu-id="13692-135">If it does, make sure that the URL "https://dynamicsaxworkfloweditor/" is added to the property **Microsoft Dynamics 365 for Operations On-premises - Workflow - Native application** in the ADFS settings.</span></span>
