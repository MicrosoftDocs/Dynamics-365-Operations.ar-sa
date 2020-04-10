---
title: قم بتمكين المستخدمين من تلقي رسائل البريد الإلكتروني المرتبطة بسير العمل
description: يمكنك تكوين النظام لإرسال رسائل إلكترونية إلى المستخدمين عند وقوع أحداث مرتبطة بسير العمل.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4c9f2f22bc4b5ca5b4351f7956ad2eb6d3b903d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140411"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="38056-103">قم بتمكين المستخدمين من تلقي رسائل البريد الإلكتروني المرتبطة بسير العمل</span><span class="sxs-lookup"><span data-stu-id="38056-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38056-104">يمكنك تكوين النظام لإرسال رسائل إلكترونية إلى المستخدمين عند وقوع أحداث مرتبطة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="38056-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="38056-105">على سبيل المثال، يمكن إرسال رسائل البريد الإلكتروني للمستخدمين عندما يتم تعيين المستندات إليهم للموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="38056-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="38056-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="38056-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="38056-107">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النظام > المستخدمون > المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="38056-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="38056-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="38056-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="38056-109">في **جزء الإجراءات**، انقر فوق **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="38056-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="38056-110">انقر فوق علامة‏‎ التبويب **سير العمل**. تأكد من توسيع قسم **الإخطارات‏‎**.</span><span class="sxs-lookup"><span data-stu-id="38056-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="38056-111">في قسم **الإخطارات**، يمكنك تحديد كيف تريد أن يتم إعلام المستخدم بالأحداث المرتبطة بسير العمل.</span><span class="sxs-lookup"><span data-stu-id="38056-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="38056-112">في الحقل **نوع إخطار سير العمل لعنصر البند**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="38056-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="38056-113">مجمَّع‬ – يتم تجميع الإخطارات لأصناف البنود في رسالة بريد إلكتروني واحدة.</span><span class="sxs-lookup"><span data-stu-id="38056-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="38056-114">فردي - يتم إرسال رسالة بريد إلكتروني لكل صنف بند.</span><span class="sxs-lookup"><span data-stu-id="38056-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="38056-115">إذا أردت أن يتلقى المستخدم الإخطارات في العميل، فحدد خانة الاختيار **إرسال إخطارات بالبريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="38056-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="38056-116">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="38056-116">Click **Save**.</span></span>
7. <span data-ttu-id="38056-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="38056-117">Close the page.</span></span>

