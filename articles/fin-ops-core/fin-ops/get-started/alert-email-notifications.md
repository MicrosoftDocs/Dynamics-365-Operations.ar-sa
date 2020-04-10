---
title: إخطارات تنبيه‬ العميل بالبريد الإلكتروني
description: يوفر هذا الموضوع معلومات حول كيفية إعداد القواعد التي ترسل إخطارات بالبريد الإلكتروني عند وقوع أحداث معرّفة مسبقًا.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a0cf8037ba151bb4e68da1cf4609fb2e4806303a
ms.sourcegitcommit: b952b9f9066a5317259b8344db4c5d99eab4bf3c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/25/2020
ms.locfileid: "3165765"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="b73f1-103">إخطارات تنبيه‬ العميل بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="b73f1-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b73f1-104">يمكنك تحديد قواعد تنبيهات مخصصة تراقب طرق العرض المصفاة للبيانات وترسل إخطارات بالبريد الإلكتروني بشكل تلقائي عند وقوع أحداث معرّفة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="b73f1-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="b73f1-105">ويتوفر خيار إرسال إخطارات بالبريد الإلكتروني لكافة أنواع التنبيهات المدعومة ويمكن أيضًا تشغيله لقواعد التنبيه الموجودة.</span><span class="sxs-lookup"><span data-stu-id="b73f1-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="b73f1-106">يمكنك استخدام عناصر تحكم مضمنة لإنشاء قواعد التنبيه التي تراقب طرق العرض المصفاة لوظائف النظام الدُفعية.</span><span class="sxs-lookup"><span data-stu-id="b73f1-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="b73f1-107">ومن خلال مراقبة قيمة حقل **الحالة**، يمكنك أيضًا تكوين قواعد التنبيه التي ترسل رسالة بريد إلكتروني عند فشل وظيفة دُفعية.</span><span class="sxs-lookup"><span data-stu-id="b73f1-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="b73f1-108">بعد إنشاء قواعد التنبيه هذه، لن تحتاج إلى التدقيق في التقارير بحثًا عن التغييرات في بيانات العمل.</span><span class="sxs-lookup"><span data-stu-id="b73f1-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="b73f1-109">بدلاً من ذلك، يمكنك أن تسمح للخدمة الذكية للكشف عن التغييرات بإجراء عملية المراقبة بالنيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="b73f1-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="b73f1-110">تتوقف تنبيهات العميل على النظام الفرعي للبريد الإلكتروني المتوفر من خلال التكامل مع Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="b73f1-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="b73f1-111">نحن ننصحك باستخدام موفر البرتوكول البسيط لنقل رسائل البريد (SMTP)، بحيث لا يعتمد توزيع البريد الإلكتروني على عميل بريد محلي.</span><span class="sxs-lookup"><span data-stu-id="b73f1-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="b73f1-112">لإرسال الإخطارات بالبريد الإلكتروني، يجب على العملاء تكوين خدمات البريد الإلكتروني المتكاملة.</span><span class="sxs-lookup"><span data-stu-id="b73f1-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="b73f1-113">ويتم إرسال الإخطارات بالبريد الإلكتروني إلى المستلمين نيابة عن مالكي التنبيه.</span><span class="sxs-lookup"><span data-stu-id="b73f1-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="b73f1-114">للحصول على مزيد من المعلومات حول كيفية تكوين البريد الإلكتروني، راجع [تكوين وإرسال البريد الإلكتروني](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="b73f1-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="b73f1-115">تُظهر الصورة التالية مربع الحوار **إنشاء قاعدة تنبيه**، الذي يتضمن الآن الخيار **إرسال بريد إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="b73f1-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="b73f1-116">[![مربع الحوار "إنشاء قاعدة تنبيه"، حيث تم تعيين الخيار "إرسال بريد إلكتروني" إلى "نعم"](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="b73f1-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b73f1-117">عند تعيين الخيار **إرسال بريد إلكتروني** إلى **نعم**، سيستمر تسليم الإخطارات بالبريد الإلكتروني من مركز الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="b73f1-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="b73f1-118">قوالب البريد الإلكتروني لإخطارات التنبيه</span><span class="sxs-lookup"><span data-stu-id="b73f1-118">Alert notification email templates</span></span>

<span data-ttu-id="b73f1-119">ترسل الخدمة إخطارات بالبريد الإلكتروني باستخدام قوالب بريد إلكتروني معرفة مسبقًا توفر تفاصيل أساسية حول إخطار التنبيه.</span><span class="sxs-lookup"><span data-stu-id="b73f1-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="b73f1-120">تُظهر الصورة التالية بنية إخطارات التنبيه عند استلامها بالبريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="b73f1-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="b73f1-121">[![إخطارات تنبيه تستند إلى قوالب لإنشاء السجلات وإجراء تغييرات في الحقول وحذف القوالب](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="b73f1-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
