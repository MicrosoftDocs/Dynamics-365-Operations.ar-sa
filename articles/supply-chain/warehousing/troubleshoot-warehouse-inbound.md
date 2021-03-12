---
title: استكشاف أخطاء ‏‫عمليات المستودعات الواردة‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الواردة في Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970226"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="de1c0-103">استكشاف أخطاء ‏‫عمليات المستودعات الواردة‬ وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="de1c0-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de1c0-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الواردة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="de1c0-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="de1c0-105">أتلقى رسالة الخطا التالية: "تم إنشاء أمر الجودة %1.</span><span class="sxs-lookup"><span data-stu-id="de1c0-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="de1c0-106">تعذر العثور على ملف تعريف نظام المجموعة، فيُرجى التحقق من التكوين."</span><span class="sxs-lookup"><span data-stu-id="de1c0-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="de1c0-107">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="de1c0-107">Issue description</span></span>

<span data-ttu-id="de1c0-108">ترتبط رسالة الخطا هذه بعمليه استلام يتم فيها تشغيل أداره الجودة (QMS).</span><span class="sxs-lookup"><span data-stu-id="de1c0-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="de1c0-109">استنادا إلى التكوينات الموجودة في البيئة الخاصة بك ، قد تساعدك التفاصيل الاضافيه حول العملية التي تقوم بإنشاء رسالة الخطا علي إصلاح المشكلة.</span><span class="sxs-lookup"><span data-stu-id="de1c0-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de1c0-110">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="de1c0-110">Issue resolution</span></span>

<span data-ttu-id="de1c0-111">أولا ، قم بمراجعه [اعداد انتقاء الكتلة](set-up-cluster-picking.md)، وتاكد من اعداد ملفات تعريف المجموعة بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="de1c0-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="de1c0-112">لا يمكنك استخدام عنصر قائمه جهاز المحمول لانتقاء نظام المجموعة ما لم يتم اعداد ملفات تعريف نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="de1c0-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="de1c0-113">اعتمادا علي البيئة الخاصة بك ، قد يتوجب عليك أيضا مراجعه التكوينات الأخرى ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="de1c0-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="de1c0-114">لا يعمل استلام لوحه الترخيص المختلط لأي كود ترتيب باستثناء الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="de1c0-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de1c0-115">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="de1c0-115">Issue description</span></span>

<span data-ttu-id="de1c0-116">عند تعيين حقل **الاجراء** الخاص بكود الترتيب إلى *دائن* أو *خردة*، يمكنك استخدام العنصر الموجود في قائمه [استلام لوح الترخيص المختلط ](mixed-license-plate-receiving.md) لمعالجه الأصناف المرتجعة فقط.</span><span class="sxs-lookup"><span data-stu-id="de1c0-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de1c0-117">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="de1c0-117">Issue resolution</span></span>

<span data-ttu-id="de1c0-118">قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه.</span><span class="sxs-lookup"><span data-stu-id="de1c0-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="de1c0-119">حاليا، [يتم دعم أكواد الترتيب](../service-management/set-up-disposition-codes.md) فقط حيث تم تعيين حقل **الاجراء** إلى *دائن* أو *الخردة* لاستلام لوحه الترخيص المختلط.</span><span class="sxs-lookup"><span data-stu-id="de1c0-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="de1c0-120">عند تشغيل المهمة الدورية لتحديث إيصالات استلام المنتجات ، يتم تاكيد أوامر الشراء غير المؤكدة.</span><span class="sxs-lookup"><span data-stu-id="de1c0-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de1c0-121">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="de1c0-121">Issue description</span></span>

<span data-ttu-id="de1c0-122">بعد تشغيل المهمة الدورية *تحديث إيصالات استلام المنتجات*، يقوم النظام تلقائيا بتاكيد أوامر الشراء غير المؤكدة التي لها حاله حركه المخزون *المسجلة*.</span><span class="sxs-lookup"><span data-stu-id="de1c0-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de1c0-123">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="de1c0-123">Issue resolution</span></span>

<span data-ttu-id="de1c0-124">تعمل ميزه معالجه التحميل الواردة الجديدة، *عبر استلام كميات التحميل*، علي إصلاح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="de1c0-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="de1c0-125">لتشغيل هذه الميزة، انتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):</span><span class="sxs-lookup"><span data-stu-id="de1c0-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="de1c0-126">إقران حركات مخزون أمر الشراء بحمل العمل</span><span class="sxs-lookup"><span data-stu-id="de1c0-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="de1c0-127">استلام زائد لكميات حمل العمل</span><span class="sxs-lookup"><span data-stu-id="de1c0-127">Over receipt of load quantities</span></span>

<span data-ttu-id="de1c0-128">لمزيد من المعلومات ، راجع [ترحيل كميات المنتج المسجلة مقابل أوامر الشراء](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="de1c0-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
