---
title: الأصول الواردة والصادرة
description: يشرح هذا الموضوع كيفية تسجيل الأصول الواردة والصادرة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847541"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="9b892-103">الأصول الواردة والصادرة</span><span class="sxs-lookup"><span data-stu-id="9b892-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9b892-104">إذا كانت شركتك تنفذ مهام إصلاح أو صيانة على أصول تتلقاها من مواقع أخرى أو عملاء أخرين، فبإمكان إدارة الأصول تتبع الأصول الواردة التي هي في طريقها إلى شركتك والأصول الصادرة التي يتم إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="9b892-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="9b892-105">إذا كنت ترغب في استخدام حالات دورة الحياة الواردة والصادرة لإدارة الأصول التي تأتي ويتم إرجاعها، يجب إعداد حالات دورة حياة طلب الصيانة ونماذج دورة الحياة لدعم هذه الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="9b892-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="9b892-106">لمزيد من المعلومات، راجع [إعداد طلبات الصيانة](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="9b892-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="9b892-107">يحدد إعداد "إدارة الأصول" ما إذا كان يمكنك العمل مع الأصول الواردة والصادرة.</span><span class="sxs-lookup"><span data-stu-id="9b892-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="9b892-108">تسجيل الأصول كواردة</span><span class="sxs-lookup"><span data-stu-id="9b892-108">Register assets as inbound</span></span>

1. <span data-ttu-id="9b892-109">حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **طلبات الصيانة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="9b892-110">حدد طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9b892-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="9b892-111">حدد **تحديث حالة طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="9b892-112">حدد **وارد** (أو حالة دورة حياة أخرى قمت بإنشائها للأصول الواردة)، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9b892-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![الشكل 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="9b892-114">تسجيل الأصول الواردة كمستلمة</span><span class="sxs-lookup"><span data-stu-id="9b892-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="9b892-115">حدد **إدارة الأصول** \> **عام** \> **وارد/صادر** \> **الأصول الواردة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="9b892-116">حدد الأصل أو طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9b892-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="9b892-117">حدد **استلام الأصول**.</span><span class="sxs-lookup"><span data-stu-id="9b892-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="9b892-118">في الحقل **مُستَلم‬**، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="9b892-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="9b892-119">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9b892-119">Then select **OK**.</span></span> <span data-ttu-id="9b892-120">يُزال السجل من صفحة‏‎ قائمة **الأصول الواردة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-120">The record is removed from the **Inbound assets** list page.</span></span>

![الشكل 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="9b892-122">تسجيل الأصول كصادرة</span><span class="sxs-lookup"><span data-stu-id="9b892-122">Register assets as outbound</span></span>

<span data-ttu-id="9b892-123">عند الانتهاء من مهمة الصيانة أو الإصلاح، يمكنك تسجيل الأصل كمرتجع.</span><span class="sxs-lookup"><span data-stu-id="9b892-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="9b892-124">حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **طلبات الصيانة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="9b892-125">حدد طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9b892-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="9b892-126">حدد **تحديث حالة طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="9b892-127">حدد **صادر** (أو حالة دورة حياة أخرى قمت بإنشائها للأصول الصادرة)، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9b892-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="9b892-128">تسجيل الأصول كمسلَّمة‬</span><span class="sxs-lookup"><span data-stu-id="9b892-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="9b892-129">حدد **إدارة الأصول** \> **عام** \> **وارد/صادر** \> **الأصول الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="9b892-130">حدد الأصل أو طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9b892-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="9b892-131">حدد **تسليم الأصول**.</span><span class="sxs-lookup"><span data-stu-id="9b892-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="9b892-132">في الحقل **مسلَّمة‬**، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="9b892-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="9b892-133">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9b892-133">Then select **OK**.</span></span> <span data-ttu-id="9b892-134">يُزال السجل من صفحة‏‎ قائمة **الأصول الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="9b892-134">The record is removed from the **Outbound assets** list page.</span></span>
