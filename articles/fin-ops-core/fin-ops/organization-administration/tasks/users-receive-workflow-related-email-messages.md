---
title: قم بتمكين المستخدمين من تلقي رسائل البريد الإلكتروني المرتبطة بسير العمل
description: يمكنك تكوين النظام لإرسال رسائل إلكترونية إلى المستخدمين عند وقوع أحداث مرتبطة بسير العمل.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3207727c8deba97eebfd7516e9600238e5e79b3d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747239"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="09cae-103">قم بتمكين المستخدمين من تلقي رسائل البريد الإلكتروني المرتبطة بسير العمل</span><span class="sxs-lookup"><span data-stu-id="09cae-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09cae-104">يمكنك تكوين النظام لإرسال رسائل إلكترونية إلى المستخدمين عند وقوع أحداث مرتبطة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="09cae-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="09cae-105">على سبيل المثال، يمكن إرسال رسائل البريد الإلكتروني للمستخدمين عندما يتم تعيين المستندات إليهم للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="09cae-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="09cae-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="09cae-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="09cae-107">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النظام > المستخدمون > المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="09cae-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="09cae-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="09cae-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="09cae-109">في **جزء الإجراءات**، انقر فوق **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="09cae-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="09cae-110">انقر فوق علامة‏‎ التبويب **سير العمل**. تأكد من توسيع قسم **الإخطارات‏‎**.</span><span class="sxs-lookup"><span data-stu-id="09cae-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="09cae-111">في قسم **الإخطارات**، يمكنك تحديد كيف تريد أن يتم إعلام المستخدم بالأحداث المرتبطة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="09cae-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="09cae-112">في الحقل **نوع إخطار سير العمل لعنصر البند**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="09cae-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="09cae-113">مجمَّع‬ – يتم تجميع الإخطارات لأصناف البنود في رسالة بريد إلكتروني واحدة.</span><span class="sxs-lookup"><span data-stu-id="09cae-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="09cae-114">فردي - يتم إرسال رسالة بريد إلكتروني لكل صنف بند.</span><span class="sxs-lookup"><span data-stu-id="09cae-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="09cae-115">إذا أردت أن يتلقى المستخدم الإخطارات في العميل، فحدد خانة الاختيار **إرسال إخطارات بالبريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="09cae-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="09cae-116">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="09cae-116">Click **Save**.</span></span>
7. <span data-ttu-id="09cae-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="09cae-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="09cae-118">يتم توريد قوالب البريد الإلكتروني لسير العمل من قوالب البريد الإلكتروني للنظام أو قوالب البريد الإلكتروني للمؤسسة استنادًا إلى ما إذا كان سير العمل هو سير عمل على مستوى النظام (غير خاص بالشركة) أو سير عمل على مستوي مستوى (خاص بالشركة).</span><span class="sxs-lookup"><span data-stu-id="09cae-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]