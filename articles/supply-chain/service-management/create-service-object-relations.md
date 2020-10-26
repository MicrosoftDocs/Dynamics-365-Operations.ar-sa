---
title: إنشاء علاقات كائن خدمة
description: ‏‫يوضح هذا الموضوع كيفية إنشاء علاقة كائن الخدمة لاتفاقية خدمة وأمر خدمة.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 352d3b790da340102b7dbe116d9deeb2f3cbfc4e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985959"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="5e0e6-103">إنشاء علاقات كائن خدمة</span><span class="sxs-lookup"><span data-stu-id="5e0e6-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5e0e6-104">‏‫يوضح هذا الموضوع كيفية إنشاء علاقة كائن الخدمة لاتفاقية خدمة وأمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="5e0e6-105">عند قيامك بإنشاء علاقة كائن الخدمة، فأنت تقوم بإقران كائن الخدمة لاتفاقية خدمة أو أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="5e0e6-106">عندما يطلب عميل خدمة لأحد الأصناف التي تعتبر كائن خدمة، يمكنك تحديد كائن الخدمة من قائمة علاقات كائنات الخدمة.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="5e0e6-107">إنشاء علاقة كائن خدمة لاتفاقية خدمة</span><span class="sxs-lookup"><span data-stu-id="5e0e6-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="5e0e6-108">استخدم الخطوات التالية لإنشاء علاقة كائن خدمة لاتفاقية خدمة:</span><span class="sxs-lookup"><span data-stu-id="5e0e6-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="5e0e6-109">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬** .</span><span class="sxs-lookup"><span data-stu-id="5e0e6-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements** .</span></span>

2.  <span data-ttu-id="5e0e6-110">في القائمة **اتفاقيات الخدمة** ، حدد اتفاقية خدمة موجودة، أو انقر فوق **جديد** لإنشاء اتفاقية خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="5e0e6-111">في نموذج **اتفاقيات الخدمة** ، في **جزء الإجراءات** ، بعلامة تبويب **اتفاقية الخدمة** ، في مجموعة **العلاقات** ، انقر فوق **كائنات الخدمة** .</span><span class="sxs-lookup"><span data-stu-id="5e0e6-111">In the **Service agreements** form, on the **Action Pane** , on the **Service agreement** tab, in the **Relations** group, click **Service objects** .</span></span>

4.  <span data-ttu-id="5e0e6-112">في النموذج **كائنات الخدمة** ، انقر فوق **جديد** ، ثم حدد كائن خدمة لاتفاقية الخدمة هذه.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-112">In the **Service objects** form, click **New** , and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="5e0e6-113">لتعيين قالب قائمة مكونات الصنف (BOM) لاتفاقية الخدمة، انقر فوق **الوظائف** ، ثم حدد **إرفاق قائمة مكونات الصنف قالب‬** .</span><span class="sxs-lookup"><span data-stu-id="5e0e6-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions** , and then select **Attach template BOM** .</span></span> <span data-ttu-id="5e0e6-114">في النموذج **تحديد قائمة مكونات الصنف قالب‬** ، في الحقل **قائمة مكونات الصنف قالب‬** ، حدد قالبًا.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="5e0e6-115">إنشاء علاقة كائن خدمة لأمر خدمة</span><span class="sxs-lookup"><span data-stu-id="5e0e6-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="5e0e6-116">استخدم الخطوات التالية لإنشاء علاقة كائن خدمة لأمر خدمة:</span><span class="sxs-lookup"><span data-stu-id="5e0e6-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="5e0e6-117">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات** .</span><span class="sxs-lookup"><span data-stu-id="5e0e6-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders** .</span></span>

2.  <span data-ttu-id="5e0e6-118">في القائمة **أوامر الخدمة** ، حدد أمر خدمة موجود، أو قم بإنشاء أمر خدمة جديد.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="5e0e6-119">في نموذج **أوامر الخدمة** ، في **جزء الإجراءات** ، بعلامة تبويب **أمر الخدمة** ، في مجموعة **العلاقات** ، انقر فوق **كائنات الخدمة** .</span><span class="sxs-lookup"><span data-stu-id="5e0e6-119">In the **Service orders** form, on the **Action Pane** , on the **Service order** tab, in the **Relations** group, click **Service objects** .</span></span>

4.  <span data-ttu-id="5e0e6-120">في النموذج **كائنات الخدمة** ، انقر فوق **جديد** ، ثم حدد كائن خدمة لأمر الخدمة هذه.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-120">In the **Service objects** form, click **New** , and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="5e0e6-121">لتعيين قالب قائمة مكونات الصنف (BOM) لاتفاقية الخدمة، انقر فوق **الوظائف** ، ثم حدد **إرفاق قائمة مكونات الصنف قالب‬** .</span><span class="sxs-lookup"><span data-stu-id="5e0e6-121">To assign a template BOM to the service agreement, click **Functions** , and then select **Attach template BOM** .</span></span> <span data-ttu-id="5e0e6-122">في النموذج **تحديد قائمة مكونات الصنف قالب‬** ، في الحقل **قائمة مكونات الصنف قالب‬** ، حدد قالبًا.</span><span class="sxs-lookup"><span data-stu-id="5e0e6-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="5e0e6-123">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="5e0e6-123">See also</span></span>

[<span data-ttu-id="5e0e6-124">نظرة عامة على كائنات الخدمة</span><span class="sxs-lookup"><span data-stu-id="5e0e6-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="5e0e6-125">علاقات كائنات الخدمة</span><span class="sxs-lookup"><span data-stu-id="5e0e6-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="5e0e6-126">قوائم مكونات صنف القالب</span><span class="sxs-lookup"><span data-stu-id="5e0e6-126">Template BOMs</span></span>](template-boms.md)

  


