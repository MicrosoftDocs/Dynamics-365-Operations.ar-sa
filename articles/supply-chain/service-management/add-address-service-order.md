---
title: إضافة عنوان لأمر الخدمة
description: يصف هذا الموضوع كيفية إضافة عنوان عميل إلى أمر خدمة.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570355"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="7da71-103">إضافة عنوان لأمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="7da71-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7da71-104">يصف هذا الموضوع كيفية إضافة عنوان عميل إلى أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="7da71-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="7da71-105">عند إنشاء أمر خدمة، يتم تحويل معلومات العنوان من المشروع المرفق به أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7da71-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="7da71-106">ومع ذلك، يمكنك تحديد موقع بديل من العناوين التي تم إدخالها مسبقًا في Microsoft Dynamics AX للعملاء والموردين والمواقع والمستودعات وأوامر الخدمة والمشاريع.</span><span class="sxs-lookup"><span data-stu-id="7da71-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="7da71-107">كما يمكن إنشاء عنوان جديد.</span><span class="sxs-lookup"><span data-stu-id="7da71-107">You can also create a new address.</span></span> <span data-ttu-id="7da71-108">بشكل افتراضي، يتم تحويل العنوان الجديد للمشروع.</span><span class="sxs-lookup"><span data-stu-id="7da71-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="7da71-109">ومع ذلك، يمكنك تحديد أن العنوان الجديد مناسبًا فقط لهذا المثيل من الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7da71-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="7da71-110">إذا قمت بذلك، لا يتم تحويل العنوان الجديد للمشروع.</span><span class="sxs-lookup"><span data-stu-id="7da71-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="7da71-111">إنشاء عنوان العميل لأوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="7da71-111">Create a customer address for a service order</span></span>

<span data-ttu-id="7da71-112">لإضافة عنوان إلى أمر خدمة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="7da71-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="7da71-113">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="7da71-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="7da71-114">افتح أمر الخدمة الذي تريد إنشاء عنوان له.</span><span class="sxs-lookup"><span data-stu-id="7da71-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="7da71-115">في **جزء الإجراء**، انقر فوق **تحرير**، ثم انقر فوق **عرض الرأس**.</span><span class="sxs-lookup"><span data-stu-id="7da71-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="7da71-116">في علامة التبويب السريعة **عنوان**، انقر فوق **إضافة عنوان**.</span><span class="sxs-lookup"><span data-stu-id="7da71-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="7da71-117">في النموذج **عنوان جديد**، أدخل اسمًا فريدًا للعنوان وأكمل الحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="7da71-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="7da71-118">إذا قمت بإدخال نفس الاسم كعنوان موجود، ستستبدل المعلومات التي يتم إدخالها في الحقول المتبقية معلومات العنوان الموجودة.</span><span class="sxs-lookup"><span data-stu-id="7da71-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="7da71-119">انقر فوق **موافق** لنسخ عنوان جديد إلى أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7da71-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="7da71-120">تحديد عنوان بديل على أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="7da71-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="7da71-121">لإضافة عنوان بديل إلى أمر خدمة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="7da71-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="7da71-122">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="7da71-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="7da71-123">افتح أمر الخدمة الذي تريد إدخال عنوان بديل له.</span><span class="sxs-lookup"><span data-stu-id="7da71-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="7da71-124">في **جزء الإجراء**، انقر فوق **تحرير**، ثم انقر فوق **عرض الرأس**.</span><span class="sxs-lookup"><span data-stu-id="7da71-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="7da71-125">في علامة التبويب السريعة **عنوان**، انقر فوق **عنوان آخر**.</span><span class="sxs-lookup"><span data-stu-id="7da71-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="7da71-126">في نموذج **تحديد العنوان** في حقل **نوع سجل**، حدد **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="7da71-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="7da71-127">حدد عنوانًا ثم انقر فوق **موافق** لنسخه إلى أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="7da71-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


