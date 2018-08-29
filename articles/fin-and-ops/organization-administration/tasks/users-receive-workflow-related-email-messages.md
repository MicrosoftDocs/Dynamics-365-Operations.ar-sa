--- 
title: "تكوين النظام لإرسال بريد إلكتروني مرتبط بسير العمل إلى المستخدمين"
description: "يمكنك تكوين النظام لإرسال رسائل إلكترونية إلى المستخدمين عند وقوع أحداث مرتبطة بسير العمل."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="f5241-103">تكوين النظام لإرسال بريد إلكتروني مرتبط بسير العمل إلى المستخدمين</span><span class="sxs-lookup"><span data-stu-id="f5241-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5241-104">يمكنك تكوين النظام لإرسال رسائل إلكترونية إلى المستخدمين عند وقوع أحداث مرتبطة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="f5241-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="f5241-105">على سبيل المثال، يمكن إرسال رسائل البريد الإلكتروني للمستخدمين عندما يتم تعيين المستندات إليهم للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="f5241-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="f5241-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="f5241-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f5241-107">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f5241-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f5241-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f5241-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f5241-109">انقر فوق خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="f5241-109">Click User options.</span></span>
4. <span data-ttu-id="f5241-110">انقر فوق علامة التبويب "سير العمل".</span><span class="sxs-lookup"><span data-stu-id="f5241-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="f5241-111">تأكد من توسيع المقطع "إخطارات".</span><span class="sxs-lookup"><span data-stu-id="f5241-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="f5241-112">في المقطع "إخطارات"، يمكنك تحديد كيف تريد أن يتم إعلام المستخدم بالأحداث المرتبطة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="f5241-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="f5241-113">في الحقل "نوع إخطار سير العمل لعنصر البند‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="f5241-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="f5241-114">مجمَّع‬ – يتم تجميع الإخطارات لأصناف البنود في رسالة بريد إلكتروني واحدة.</span><span class="sxs-lookup"><span data-stu-id="f5241-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="f5241-115">فردي - يتم إرسال رسالة بريد إلكتروني لكل صنف بند.</span><span class="sxs-lookup"><span data-stu-id="f5241-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="f5241-116">إذا أردت أن يتلقى المستخدم الإخطارات في العميل ، فحدد خانة الاختيار "إرسال إخطارات بالبريد الإلكتروني‬".</span><span class="sxs-lookup"><span data-stu-id="f5241-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="f5241-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f5241-117">Click Save.</span></span>
7. <span data-ttu-id="f5241-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f5241-118">Close the page.</span></span>


