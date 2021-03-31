---
title: استكشاف أخطاء ‏‫عمليات المستودعات الصادرة‬‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الصادرة في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1344a1c16bf72b31f7aaf18aaeb6e08c7bc9d87e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223256"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="bb938-103">استكشاف أخطاء ‏‫عمليات المستودعات الصادرة‬‬ وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="bb938-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb938-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الصادرة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bb938-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="bb938-105">أتلقى رسالة الخطا التالية: "تعذر إصدار أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="bb938-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bb938-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="bb938-106">Issue description</span></span>

<span data-ttu-id="bb938-107">قد تحدث هذه المشكلة لأسباب عديده.</span><span class="sxs-lookup"><span data-stu-id="bb938-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="bb938-108">علي سبيل المثال ، يكون الأمر في انتظار أداره الائتمان ، ولا يمكن إنشاء إيه شحنات حتى يتم إدخال عنوان بريدي صالح لكافة بنود المبيعات المرتبطة بامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bb938-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="bb938-109">وبدلا من ذلك ، هناك قائمه احتجاز يجب معالجتها قبل التمكن من إصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="bb938-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="bb938-110">وقد تكون قائمه الاحتجاز هذه خاصه بالطلب ، أو قد تكون موجودة في حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="bb938-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bb938-111">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="bb938-111">Issue resolution</span></span>

<span data-ttu-id="bb938-112">قم باضافه العنوان أو تحديثه علي بنود أمر المبيعات والأمر ، ثم قم بتحرير الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="bb938-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="bb938-113">يمكن إصدار الأوامر إلى المستودع فقط إذا كان لديها عنوان تسليم صالح (لكل اعداد تنسيق العنوان في الوحدة النمطية **أداره المؤسسة**).</span><span class="sxs-lookup"><span data-stu-id="bb938-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="bb938-114">التحقق من احتجاز الأمر ومعالجه المشكلات.</span><span class="sxs-lookup"><span data-stu-id="bb938-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="bb938-115">ثم قم بازاله التعليق من الأمر أو العميل ، ثم قم بإصدار الأمر إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="bb938-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="bb938-116">أتلقى الرسالة التالية: "تم تاكيد الشحنة الخاصة بالتحميل 1%."</span><span class="sxs-lookup"><span data-stu-id="bb938-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="bb938-117">ومع ذلك ، لا يتم ترحيل إيه بنود.</span><span class="sxs-lookup"><span data-stu-id="bb938-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bb938-118">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="bb938-118">Issue description</span></span>

<span data-ttu-id="bb938-119">تم تاكيد الشحن علي الحمل ، لكن لم يتم اجراء ترحيل آخر.</span><span class="sxs-lookup"><span data-stu-id="bb938-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bb938-120">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="bb938-120">Issue resolution</span></span>

<span data-ttu-id="bb938-121">لا يؤثر تاكيد الشحن علي الترحيل.</span><span class="sxs-lookup"><span data-stu-id="bb938-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="bb938-122">وهي تقوم فقط بتحديث الشحنة وحاله التحميل.</span><span class="sxs-lookup"><span data-stu-id="bb938-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="bb938-123">يجب ان تحدث عمليه الترحيل في عمليه منفصلة.</span><span class="sxs-lookup"><span data-stu-id="bb938-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="bb938-124">أتلقى رسالة الخطا التالية: "التسليم المباشر غير قادر علي معالجه المستودع 1% نظرا لأنه يحتوي علي أداره مستودع ممكنة.</span><span class="sxs-lookup"><span data-stu-id="bb938-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="bb938-125">الرجاء تحديد مستودع آخر غير ممكن لأداره المستودعات. "</span><span class="sxs-lookup"><span data-stu-id="bb938-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bb938-126">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="bb938-126">Issue description</span></span>

<span data-ttu-id="bb938-127">تتم أضافه صنف إلى بند مبيعات للتسليم المباشر من مستودع يتم تمكينه لأداره المستودعات (WMS).</span><span class="sxs-lookup"><span data-stu-id="bb938-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="bb938-128">تظهر رسالة الخطا هذه عند تحديث بند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bb938-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="bb938-129">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="bb938-129">Issue resolution</span></span>

<span data-ttu-id="bb938-130">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه.</span><span class="sxs-lookup"><span data-stu-id="bb938-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="bb938-131">حاليا ، لا يدعم WMS التسليم المباشر.</span><span class="sxs-lookup"><span data-stu-id="bb938-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="bb938-132">التالي ، لاستخدام التسليم المباشر ، يجب تحديد صنف ومستودع غير WMS.</span><span class="sxs-lookup"><span data-stu-id="bb938-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]