---
title: إنشاء أوامر خدمة يدويًا
description: يمكنك إنشاء أوامر الخدمة يدويًا باستخدام اتفاقية الخدمة أو باستخدام النموذج **أوامر الخدمة**.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 486b4a0291ca527e647c9b5a41ff2e65a7820291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817571"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="58042-103">إنشاء أوامر خدمة يدويًا</span><span class="sxs-lookup"><span data-stu-id="58042-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="58042-104">يمكنك إنشاء أوامر الخدمة يدويًا باستخدام اتفاقية الخدمة أو باستخدام النموذج **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="58042-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="58042-105">يمكنك أيضًا إنشاء أمر خدمة من أحد المشاريع.</span><span class="sxs-lookup"><span data-stu-id="58042-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="58042-106">يمكنك استخدام عمليات تلقائية لإنشاء أوامر خدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="58042-107">إنشاء أمر خدمة يدويًا من اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="58042-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="58042-108">حدد **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="58042-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="58042-109">حدد اتفاقية الخدمة أو قم بإنشاء اتفاقية خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="58042-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="58042-110">حدد علامة تبويب **تسليم** علامة التبويب وفي مجموعة **إنشاء** حدد **أوامر الخدمة المخططة** لفتح النموذج **إنشاء أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="58042-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="58042-111">إنشاء أمر الخدمة يدويًا في نموذج أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="58042-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="58042-112">حدد **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="58042-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="58042-113">حدد **جديد** لإنشاء أمر خدمة جديد.</span><span class="sxs-lookup"><span data-stu-id="58042-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="58042-114">قم بإنشاء بنود أمر الخدمة لأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="58042-115">إذا تم تحديد خانة الاختيار <STRONG>سماح بدون اتفاقية خدمات‬</STRONG> الموجودة في النموذج <STRONG>محددات إدارة الخدمة</STRONG>، يمكنك ترحيل الحركات من سطور أوامر الخدمة دون إرفاق أمر الخدمة باتفاقية خدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="58042-116">وإذا تم إلغاء تحديد مربع الاختيار، يجب إرفاق أمر الخدمة الذي تم إنشاؤه يدويًا بأحد المشروعات قبل ترحيل سطور أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="58042-117">إنشاء أمر خدمة من مشروع</span><span class="sxs-lookup"><span data-stu-id="58042-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="58042-118">انتقل إلى **إدارة المشاريع‬ والمحاسبة** \> **عام** \> **المشاريع** \> **كل المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="58042-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="58042-119">في نموذج **المشاريع** ، ومن **جزء الإجراءات**، حدد علامة التبويب **إدارة** \> حدد **خدمة** \> **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="58042-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="58042-120">اتبع الإجراء السابق لإنشاء أمر الخدمة يدويًا في نموذج **أوامر الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="58042-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="58042-121">يعرض حقل **معرف المشروع** مرجع المشروع.</span><span class="sxs-lookup"><span data-stu-id="58042-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="58042-122">إذا تم تحديد خانة الاختيار <STRONG>سماح بدون اتفاقية خدمات‬</STRONG> الموجودة في النموذج <STRONG>محددات إدارة الخدمة</STRONG>، يمكنك ترحيل الحركات من سطور أوامر الخدمة دون إرفاق أمر الخدمة باتفاقية خدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="58042-123">وإذا تم إلغاء تحديد مربع الاختيار، يجب إرفاق أمر الخدمة الذي تم إنشاؤه يدويًا بأحد المشروعات قبل ترحيل سطور أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="58042-124">إنشاء أمر خدمة من نموذج أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="58042-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="58042-125">يمكنك إنشاء أمر خدمة من نموذج **أوامر المبيعات** باستخدام المعالج **إنشاء أمر خدمة جديد استناداً إلى أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="58042-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="58042-126">انتقل إلى **المبيعات والتسويق** \> **عام** \> **أوامر المبيعات** \> **كل أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="58042-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="58042-127">افتح أمر المبيعات المتعلق.</span><span class="sxs-lookup"><span data-stu-id="58042-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="58042-128">في علامة تبويب **أمر المبيعات** ، حدد **أمر الخدمة** لبدء المعالج **إنشاء أمر خدمة جديد استنادًا إلى أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="58042-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="58042-129">حدد **التالي \>**، ثم أكمل الخطوات التالية في صفحة **تحديد اتفاقية لأمر الخدمة**:</span><span class="sxs-lookup"><span data-stu-id="58042-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="58042-130">استخدم حقل **اتفاقية الخدمة** لتحديد اتفاقية الخدمة التي يجب ربط أمر الخدمة الجديد بها.</span><span class="sxs-lookup"><span data-stu-id="58042-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="58042-131">اختياريًا: استخدم الحقل **معرف المشروع** لربط أمر الخدمة هذا بمشروع معين.</span><span class="sxs-lookup"><span data-stu-id="58042-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="58042-132">حدد **التالي \>**، ثم أكمل الخطوات التالية في صفحة **إنشاء أمر الخدمة**:</span><span class="sxs-lookup"><span data-stu-id="58042-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="58042-133">أدخل تاريخًا ووقتًا لبدء الاتصال بالخدمة في الحقل **وقت الخدمة المفضل**.</span><span class="sxs-lookup"><span data-stu-id="58042-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="58042-134">اختياريًا: قم بتعديل النص في حقل **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="58042-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="58042-135">افتراضيًا، يحتوي هذا الحقل على وصف لاتفاقية الخدمة التي قمت بتحديدها في الصفحة السابقة.</span><span class="sxs-lookup"><span data-stu-id="58042-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="58042-136">في حقل **المسؤول**، حدد معرف الموظف المسئول عن الاتفاقية، وأدخل معرف الفني المفضل لدى العميل للاتصال بالخدمة إذا كنت تعرفه.</span><span class="sxs-lookup"><span data-stu-id="58042-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="58042-137">في حقل **معرف جهة الاتصال**، حدد الشخص في شركة العميل الذي يجب الاتصال به فيما يتعلق بأمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="58042-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="58042-138">حدد **التالي \>**، ثم حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="58042-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="58042-139">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="58042-139">See also</span></span>

[<span data-ttu-id="58042-140">أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="58042-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="58042-141">إنشاء أوامر الخدمة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="58042-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="58042-142">[إنشاء أوامر خدمات (نموذج الفئة)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="58042-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]