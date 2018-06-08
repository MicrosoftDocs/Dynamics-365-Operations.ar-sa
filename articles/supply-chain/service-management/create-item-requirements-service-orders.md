---
title: "إنشاء متطلبات صنف لأوامر الخدمة"
description: "إذا كنت تحتاج إلى حجز أصناف محددة لأمر خدمة، يمكنك إنشاء متطلبات صنف مخزون لها."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e76b0c636470a89ba2091363efe2f34eb3d58f88
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="f3ea4-103">إنشاء متطلبات صنف لأوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="f3ea4-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f3ea4-104">يمكنك إنشاء أمر خدمة لتعقب وإدارة الخدمات التي توفرها للعملاء.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="f3ea4-105">إذا كنت تحتاج إلى حجز أصناف محددة لأمر خدمة، يمكنك إنشاء متطلبات صنف مخزون لها.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="f3ea4-106">يمكن استهلاك متطلبات صنف مباشرة من المخزون أو يمكن بدء أمر إنتاج للصنف.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="f3ea4-107">باستخدام متطلب صنف بدلا من حركة صنف، يمكنك تخطيط التسليم قبل الاستخدام الفعلي للصنف، وإنشاء أمر شراء، وتضمين الصنف في إطار عمل الاتفاقية التجارية، وتضمين متطلب الصنف في تخطيط الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="f3ea4-108">تتم معالجة متطلبات الصنف لأوامر الخدمة من خلال مشروع.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="f3ea4-109">لإنشاء متطلبات صنف في أمر خدمة، يجب تعيين أمر الخدمة لمشروع.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="f3ea4-110">بعد إنشاء متطلبات صنف لأمر خدمة، يمكنك عرض متطلبات الصنف في نموذج **المشروعات** للمشروع المحدد.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="f3ea4-111">إنشاء متطلبات الصنف لأمر خدمة</span><span class="sxs-lookup"><span data-stu-id="f3ea4-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="f3ea4-112">انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f3ea4-113">حدد أمر الخدمة الذي تريد إنشاء متطلبات الصنف له.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="f3ea4-114">في **جزء الإجراءات**، بعلامة التبويب **إرسال**، انقر فوق **متطلب الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="f3ea4-115">في النموذج **متطلبات الصنف**، أدخل معلومات للصنف المطلوب.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="f3ea4-116">لمزيد من المعلومات حول حقول محددة، راجع [متطلبات الصنف (نموذج)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="f3ea4-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="f3ea4-117">إنشاء متطلبات صنف لاتفاقية خدمة</span><span class="sxs-lookup"><span data-stu-id="f3ea4-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="f3ea4-118">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="f3ea4-119">افتح اتفاقية الخدمة التي تريد إنشاء متطلبات الصنف لها.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="f3ea4-120">في علامة التبويب السريعة **البنود**، انقر فوق **إضافة** لإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="f3ea4-121"> في الحقل **نوع الحركة**، حدد **الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="f3ea4-122">في الحقل **إعداد الصنف**، حدد **متطلب الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="f3ea4-123">في الحقل **رقم الصنف**، حدد الصنف المطلوب لاتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="f3ea4-124">في علامة التبويب السريعة **تفاصيل البند**، في علامة تبويب **أبعاد المنتج**، في حقل **موقع**، حدد موقع المخزون للصنف.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="f3ea4-125">لإنشاء أمر خدمة من بند اتفاقية، في علامة التبويب السريعة **البنود**، انقر فوق **إنشاء أوامر خدمة**، ثم أدخل المعلومات المناسبة في النموذج **إنشاء أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="f3ea4-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="f3ea4-126">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f3ea4-126">See also</span></span>

<span data-ttu-id="f3ea4-127">[إنشاء أوامر الخدمة تلقائيًا](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="f3ea4-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


