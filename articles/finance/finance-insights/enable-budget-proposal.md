---
title: تمكين مقترحات الموازنة (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل ميزة مقترح الموازنة في Finance Insights.
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818694"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="aa262-103">تمكين مقترحات الموازنة (معاينة)</span><span class="sxs-lookup"><span data-stu-id="aa262-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="aa262-104">يوضح هذا الموضوع كيفية تشغيل ميزة مقترح الموازنة في Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="aa262-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="aa262-105">استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة.</span><span class="sxs-lookup"><span data-stu-id="aa262-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="aa262-106">قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="aa262-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="aa262-107">(قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="aa262-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="aa262-108">إذا كان نشر Microsoft Dynamics 365 Finance عبارة عن نشر Service Fabric، فإنه يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="aa262-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="aa262-109">يجب أن يكون فريق Finance Insights قد قام بالفعل بتشغيل إصدار التقييم.</span><span class="sxs-lookup"><span data-stu-id="aa262-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="aa262-110">في حالة عدم رؤية الميزة في مساحة العمل **إدارة الميزات** أو في حالة مواجهة مشكلات عند محاولة تشغيلها، قم بإرسال بريد إلكتروني إلى [فريق معاينه تطبيق Finance Insights](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="aa262-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="aa262-111">افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="aa262-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="aa262-112">حدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="aa262-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="aa262-113">ابحث عن **مقترح الموازنة** وقم بتشغيل تلك الميزة.</span><span class="sxs-lookup"><span data-stu-id="aa262-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="aa262-114">انتقل إلى **إعداد الموازنة \> الإعداد \> إعداد الموازنة الأساسية \> مقترح الموازنة (معاينة)**، وحدد **تمكين الميزة**.</span><span class="sxs-lookup"><span data-stu-id="aa262-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="aa262-115">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="aa262-115">Privacy notice</span></span>
<span data-ttu-id="aa262-116">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="aa262-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]