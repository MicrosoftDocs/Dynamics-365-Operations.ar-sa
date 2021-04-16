---
title: تمكين تقدير التدفق النقدي (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.
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
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818718"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="f3322-103">تمكين تقدير التدفق النقدي (معاينة)</span><span class="sxs-lookup"><span data-stu-id="f3322-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f3322-104">يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="f3322-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="f3322-105">لاستخدام تنبؤات الدفع في التدفق النقدي، فإنه يجب إعداد ميزة تنبؤات الدفع الخاصة بالعميل كما هو موضح في [تمكين تنبؤات مدفوعات العميل](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="f3322-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="f3322-106">استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة.</span><span class="sxs-lookup"><span data-stu-id="f3322-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="f3322-107">قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="f3322-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="f3322-108">(قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="f3322-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="f3322-109">إذا كان نشر Microsoft Dynamics 365 Finance عبارة عن نشر Service Fabric، فإنه يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="f3322-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="f3322-110">يجب أن يكون فريق Finance Insights قد قام بالفعل بتشغيل إصدار التقييم.</span><span class="sxs-lookup"><span data-stu-id="f3322-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="f3322-111">إذا لم تر الميزات في مساحة عمل **إدارة الميزات**، أو إذا واجهتك مشكلات عند محاولة تشغيلها، تواصل على <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="f3322-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="f3322-112">افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f3322-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="f3322-113">حدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="f3322-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="f3322-114">تشغيل الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="f3322-114">Turn on the following features:</span></span>

        - <span data-ttu-id="f3322-115">عنصر تحكم شبكة جديد</span><span class="sxs-lookup"><span data-stu-id="f3322-115">New grid control</span></span>
        - <span data-ttu-id="f3322-116">تجميع في الشبكات (معاينة)</span><span class="sxs-lookup"><span data-stu-id="f3322-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="f3322-117">تنبؤات دفع العميل (معاينة)</span><span class="sxs-lookup"><span data-stu-id="f3322-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="f3322-118">تنبؤات التدفقات النقدية (معاينة)</span><span class="sxs-lookup"><span data-stu-id="f3322-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="f3322-119">انتقل إلى **إدارة النقد والبنوك \> إعداد التنبؤ بالتدفقات النقدية**، وأضف حسابات السيولة التي يجب تضمينها في التوقعات.</span><span class="sxs-lookup"><span data-stu-id="f3322-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3322-120">في حالة عدم إعداد حسابات السيولة، لا يمكن إنشاء التدفق النقدي.</span><span class="sxs-lookup"><span data-stu-id="f3322-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="f3322-121">انتقل إلى **إدارة النقد والبنوك \> الإعداد \> Finance Insights (معاينة) \> تقديرات التدفقات المالية (معاينة)**، واتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="f3322-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="f3322-122">في علامة التبويب **تقدير التدفقات النقدية**، حدد **تمكين الميزة**.</span><span class="sxs-lookup"><span data-stu-id="f3322-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="f3322-123">حدد **إنشاء نموذج توقع**.</span><span class="sxs-lookup"><span data-stu-id="f3322-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="f3322-124">لمزيد من المعلومات حول قدرة تقدير التدفقات النقدية، راجع [تقدير التدفقات النقدية](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="f3322-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f3322-125">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="f3322-125">Privacy notice</span></span>

<span data-ttu-id="f3322-126">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="f3322-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]