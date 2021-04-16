---
title: إضافة عنوان لأمر الخدمة
description: يصف هذا الموضوع كيفية إضافة عنوان عميل إلى أمر خدمة.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a54ec439fc88dc9688bbb3d6b833b5d80482f024
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824644"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="b2ed7-103">إضافة عنوان لأمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="b2ed7-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b2ed7-104">يصف هذا الموضوع كيفية إضافة عنوان عميل إلى أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="b2ed7-105">عند إنشاء أمر خدمة، يتم تحويل معلومات العنوان من المشروع المرفق به أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="b2ed7-106">ومع ذلك، يمكنك تحديد موقع بديل من العناوين التي تم إدخالها مسبقًا في Microsoft Dynamics AX للعملاء والموردين والمواقع والمستودعات وأوامر الخدمة والمشاريع.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="b2ed7-107">كما يمكن إنشاء عنوان جديد.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-107">You can also create a new address.</span></span> <span data-ttu-id="b2ed7-108">بشكل افتراضي، يتم تحويل العنوان الجديد للمشروع.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="b2ed7-109">ومع ذلك، يمكنك تحديد أن العنوان الجديد مناسبًا فقط لهذا المثيل من الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="b2ed7-110">إذا قمت بذلك، لا يتم تحويل العنوان الجديد للمشروع.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="b2ed7-111">إنشاء عنوان العميل لأوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="b2ed7-111">Create a customer address for a service order</span></span>

<span data-ttu-id="b2ed7-112">لإضافة عنوان إلى أمر خدمة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b2ed7-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="b2ed7-113">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b2ed7-114">افتح أمر الخدمة الذي تريد إنشاء عنوان له.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="b2ed7-115">في **جزء الإجراء**، انقر فوق **تحرير**، ثم انقر فوق **عرض الرأس**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="b2ed7-116">في علامة التبويب السريعة **عنوان**، انقر فوق **إضافة عنوان**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="b2ed7-117">في النموذج **عنوان جديد**، أدخل اسمًا فريدًا للعنوان وأكمل الحقول المتبقية.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="b2ed7-118">إذا قمت بإدخال نفس الاسم كعنوان موجود، ستستبدل المعلومات التي يتم إدخالها في الحقول المتبقية معلومات العنوان الموجودة.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="b2ed7-119">انقر فوق **موافق** لنسخ عنوان جديد إلى أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="b2ed7-120">تحديد عنوان بديل على أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="b2ed7-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="b2ed7-121">لإضافة عنوان بديل إلى أمر خدمة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b2ed7-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="b2ed7-122">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b2ed7-123">افتح أمر الخدمة الذي تريد إدخال عنوان بديل له.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="b2ed7-124">في **جزء الإجراء**، انقر فوق **تحرير**، ثم انقر فوق **عرض الرأس**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="b2ed7-125">في علامة التبويب السريعة **عنوان**، انقر فوق **عنوان آخر**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="b2ed7-126">في نموذج **تحديد العنوان** في حقل **نوع سجل**، حدد **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="b2ed7-127">حدد عنوانًا ثم انقر فوق **موافق** لنسخه إلى أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b2ed7-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]