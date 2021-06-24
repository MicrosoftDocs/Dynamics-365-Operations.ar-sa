---
title: تمكين تقدير التدفق النقدي (معاينة)
description: يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222548"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="633f4-103">تمكين تقدير التدفق النقدي (معاينة)</span><span class="sxs-lookup"><span data-stu-id="633f4-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="633f4-104">يوضح هذا الموضوع كيفية تشغيل ميزة توقعات التدفق النقدي في Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="633f4-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="633f4-105">لاستخدام تنبؤات الدفع في التدفق النقدي، فإنه يجب إعداد ميزة تنبؤات الدفع الخاصة بالعميل كما هو موضح في [تمكين تنبؤات مدفوعات العميل](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="633f4-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="633f4-106">استخدم المعلومات من صفحة البيئة في Microsoft Dynamics Lifecycle Services (LCS) للاتصال بالمثيل الأساسي لـ Azure SQL لتلك البيئة.</span><span class="sxs-lookup"><span data-stu-id="633f4-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="633f4-107">قم بتشغيل الأمر Transact-SQL (T-SQL) لتشغيل إصدارات التقييم لبيئة وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="633f4-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="633f4-108">(قد تضطر إلى تشغيل الوصول إلى عنوان IP الخاص بك في LCS قبل أن تتمكن من الاتصال بخادم كائن التطبيق عن بُعد \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="633f4-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="633f4-109">تجاوز هذه الخطوة إذا كنت تستخدم الإصدار 10.0.20 أو أحدث، أو إذا كنت تستخدم عملية نشر Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="633f4-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="633f4-110">يجب أن يكون فريق Finance insights قد قام بالفعل بتشغيل إصدار التقييم.</span><span class="sxs-lookup"><span data-stu-id="633f4-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="633f4-111">إذا لم تر الميزة في مساحة عمل **إدارة الميزات**، أو إذا واجهتك مشكلات عند محاولة تشغيلها، تواصل على <fiap@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="633f4-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="633f4-112">افتح مساحة العمل **إدارة الميزات**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="633f4-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="633f4-113">حدد **التحقق من وجود تحديثات**.</span><span class="sxs-lookup"><span data-stu-id="633f4-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="633f4-114">تشغيل الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="633f4-114">Turn on the following features:</span></span>

        - <span data-ttu-id="633f4-115">عنصر تحكم شبكة جديد</span><span class="sxs-lookup"><span data-stu-id="633f4-115">New grid control</span></span>
        - <span data-ttu-id="633f4-116">تجميع في الشبكات (معاينة)</span><span class="sxs-lookup"><span data-stu-id="633f4-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="633f4-117">تنبؤات دفع العميل (معاينة)</span><span class="sxs-lookup"><span data-stu-id="633f4-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="633f4-118">تنبؤات التدفقات النقدية (معاينة)</span><span class="sxs-lookup"><span data-stu-id="633f4-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="633f4-119">انتقل إلى **إدارة النقد والبنوك \> إعداد التنبؤ بالتدفقات النقدية**، وأضف حسابات السيولة التي يجب تضمينها في التوقعات.</span><span class="sxs-lookup"><span data-stu-id="633f4-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="633f4-120">في حالة عدم إعداد حسابات السيولة، لا يمكن إنشاء التدفق النقدي.</span><span class="sxs-lookup"><span data-stu-id="633f4-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="633f4-121">انتقل إلى **إدارة النقد والبنوك \> الإعداد \> Finance Insights (معاينة) \> تقديرات التدفقات المالية (معاينة)**، واتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="633f4-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="633f4-122">في علامة التبويب **تقدير التدفقات النقدية**، حدد **تمكين الميزة**.</span><span class="sxs-lookup"><span data-stu-id="633f4-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="633f4-123">حدد **إنشاء نموذج توقع**.</span><span class="sxs-lookup"><span data-stu-id="633f4-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="633f4-124">لمزيد من المعلومات حول قدرة تقدير التدفقات النقدية، راجع [تقدير التدفقات النقدية](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="633f4-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
