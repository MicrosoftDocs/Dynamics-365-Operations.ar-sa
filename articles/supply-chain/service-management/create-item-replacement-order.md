---
title: إنشاء أمر استبدال صنف
description: يتم عادة إنشاء أوامر استبدال الأصناف بعد إرجاع أحد المنتجات وفحصه.
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 784a2522c27e8131f211ffc52319552b3b928cc3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "355002"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="fb247-103">إنشاء أمر استبدال صنف</span><span class="sxs-lookup"><span data-stu-id="fb247-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fb247-104">يتم عادة إنشاء أوامر استبدال الأصناف بعد إرجاع أحد المنتجات وفحصه.</span><span class="sxs-lookup"><span data-stu-id="fb247-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="fb247-105">لكن عندما يجب استبدال صنف قبل إرجاعه أو في حالة عدم إرجاع الصنف الأصلي، فإنه يمكن إنشاء أمر استبدال صنف فورًا بعد إنشاء أمر إرجاع.</span><span class="sxs-lookup"><span data-stu-id="fb247-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="fb247-106">إنشاء أمر استبدال بعد استلام صنف مرتجع</span><span class="sxs-lookup"><span data-stu-id="fb247-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="fb247-107">انقر فوق **المبيعات والتسويق** \> **عام** \> **أوامر الإرجاع** \> **كل أوامر الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="fb247-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="fb247-108">نشئ أمر إرجاع جديدًا أو حدد أمرًا مرتجعًا من القائمة لفتح النموذج **أمر الإرجاع - ‏‫رقم ترخيص المواد المسترجعة‬: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="fb247-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="fb247-109">انقر فوق **سطر الإرجاع**، ثم قم بتحديد **صنف الاستبدال**.</span><span class="sxs-lookup"><span data-stu-id="fb247-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="fb247-110">حدد الصنف لاستبدال الصنف المرتجع به.</span><span class="sxs-lookup"><span data-stu-id="fb247-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="fb247-111">أدخل مواصفات الصنف ثم انقر فوق **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="fb247-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="fb247-112">انقر فوق **إيصال التعبئة** لإنشاء إيصال التعبئة لأمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="fb247-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="fb247-113">يتم إنشاء أمر مبيعات لصنف الاستبدال الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="fb247-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="fb247-114">بعد إنشاء أمر المبيعات لصنف الاستبدال، يتم البحث في اتفاقيات المبيعات تلقائيًا وفي حالة وجود اتفاقية بيع قابلة للتطبيق، يتم تطبيقها على أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="fb247-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="fb247-115">إنشاء أمر استبدال قبل استلام صنف مرتجع</span><span class="sxs-lookup"><span data-stu-id="fb247-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="fb247-116">انقر فوق **المبيعات والتسويق** \> **عام** \> **أوامر الإرجاع** \> **كل أوامر الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="fb247-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="fb247-117">نشئ أمر إرجاع جديدًا أو حدد أمر إرجاع من القائمة لفتح النموذج **أمر الإرجاع - ‏‫رقم ترخيص المواد المسترجعة‬: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="fb247-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="fb247-118">انقر فوق **بحث عن أوامر المبيعات** إذا كنت تريد تحديد أمر المبيعات للصنف المرتجع.</span><span class="sxs-lookup"><span data-stu-id="fb247-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="fb247-119">أكمل النموذج **العثور على أمر المبيعات** ثم انقر فوق **موافق‏‎** لإغلاق النموذج والرجوع إلى النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="fb247-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="fb247-120">يتم نسخ بند أمر المبيعات للصنف المرتجع إلى أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="fb247-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="fb247-121">انقر فوق **أمر استبدال** لفتح نموج **إنشاء أمر مبيعات**.</span><span class="sxs-lookup"><span data-stu-id="fb247-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="fb247-122">حدد خانة الاختيار **نسخ بنود أمر الإرجاع** لنقل التفاصيل من أمر الإرجاع المحدد في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2** إلى أمر المبيعات هذا.</span><span class="sxs-lookup"><span data-stu-id="fb247-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="fb247-123">قم بإدخال التفاصيل أو تعديلها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="fb247-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="fb247-124">إذا قمت بتحديد أمر المبيعات في الخطوة 3، وإذا تم ربط بند أمر المبيعات للصنف المرتجع باتفاقية بيع، فسيتم عرض المعرف لاتفاقية البيع القابلة للتطبيق لأمر استبدال الصنف تلقائيًا في الحقل **معرف اتفاقية المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="fb247-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="fb247-125">انقر فوق **موافق** لإغلاق نموذج **إنشاء أمر مبيعات** وفتح النموذج **أمر المبيعات**، حيث يمكنك متابعة إدخال المعلومات لأمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="fb247-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="fb247-126">سيتم نسخ أي بنود أمر إرجاع قابلة للتطبيق إلى أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="fb247-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="fb247-127">إذا تم عرض معرف اتفاقية البيع تلقائيًا في الحقل **معرف اتفاقية المبيعات**، فهذا يعني أنه تم ربط اتفاقية البيع برأس أمر المبيعات لأمر استبدال الصنف.</span><span class="sxs-lookup"><span data-stu-id="fb247-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="fb247-128">وفي حالة وجود التزام قابل للتطبيق في اتفاقية البيع لم يتم الوفاء به بعد، يتم إنشاء أمر المبيعات قبل انتهاء صلاحية اتفاقية البيع كما يتم إنشاء ارتباط بين بند اتفاقية البيع وبند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="fb247-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="fb247-129">وبناءًا على ذلك، يتم نسخ المعلومات من اتفاقية البيع، مثل سعر الصنف، إلى بند أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="fb247-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


