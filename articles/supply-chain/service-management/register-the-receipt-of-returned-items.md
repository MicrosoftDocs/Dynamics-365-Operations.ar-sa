---
title: تسجيل استلام الأصناف المرجعة
description: يمكنك تسجيل استلام الأصناف المرتجعة باستخدام النموذج نظرة عامة على الوصول أو نموذج التسجيل.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b46801ee150d1cf25d8f4c6ea9aaa8011e1cbd38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006606"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="8edd0-103">تسجيل استلام الأصناف المرجعة</span><span class="sxs-lookup"><span data-stu-id="8edd0-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8edd0-104">يوجد أسلوبان لتسجيل استلام الأصناف المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="8edd0-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="8edd0-105">الأسلوب الأول هو عملية استلام خاصة بمستودع تستخدم النموذج **نظرة عامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="8edd0-106">بينما يستخدم الأسلوب الثاني نموذج **التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="8edd0-107">تسجيل استلام الأصناف المرتجعة في نموذج نظرة عامة على الوصول</span><span class="sxs-lookup"><span data-stu-id="8edd0-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="8edd0-108">يمكنك استخدام النموذج **نظرة عامة على الوصول** لتحديد شحنة مرتجعة برقم ترخيص المواد المرتجعة (RMA) الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="8edd0-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="8edd0-109">إذا تم تحديد اسم دفتر يومية في علامة التبويب **إعداد** وكانت بنود دفتر اليومية التي تتوافق مع البنود المحددة في النموذج **نظرة عامة على الوصول** موجودة، فيتم إنشاء رأس دفتر يومية عند النقر فوق **بدء الوصول**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="8edd0-110">انقر فوق **إدارة المخزون** \> **دوري** \> **نظرة عامة على الوصول**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="8edd0-111">في حقل **اسم الإعداد**، حدد **أمر الإرجاع**، ثم انقر فوق **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="8edd0-112">يمكن استخدام حقول <STRONG>النطاق</STRONG> لتضييق نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="8edd0-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="8edd0-113">يمكن كتابة أو تحديد رقم ترخيص المواد المسترجعة في حقل <STRONG>رقم ترخيص المواد المسترجعة</STRONG> للحصول على النتيجة الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="8edd0-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="8edd0-114">لتحديد وحفظ مجموعة من عوامل التصفية التي ستقوم بتقييد عمليات الوصول الواردة التي يتم عرضها، انقر فوق علامة التبويب <STRONG>الإعداد</STRONG>. تشمل عوامل التصفية المتوفرة أنواع والمستودعات والأرصفة.</span><span class="sxs-lookup"><span data-stu-id="8edd0-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="8edd0-115">لا يمكن خلط أوامر الإرجاع بأنواع عمليات وصول أخرى في النموذج <STRONG>نظرة عامة على الوصول</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8edd0-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="8edd0-116">وبناءً على ذلك، سيكون المرجع دائمًا أمر مبيعات، ولكن لن يتم تحديد أي أمر مبيعات في رأس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="8edd0-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="8edd0-117">في الشبكة **إيصالات الاستلام**، حدد موقع البند الملائم للصنف المرتجع، ثم حدد خانة الاختيار في العمود **محدد للوصول**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="8edd0-118">عند الرغبة في استثناء بنود بعينها من عملية استلام الأصناف المرتجعة، مثل الأصناف الموجودة في الأمر الأصلي والتي لم يتم تضمينها في الشحنة المرتجعة، قم بإلغاء تحديد خانات الاختيار **محدد للوصول** ذات الصلة في الجدول **البنود** الموجود في الجزء السفلي من النموذج.</span><span class="sxs-lookup"><span data-stu-id="8edd0-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="8edd0-119">انقر فوق الزر **بدء الوصول** لإنشاء دفتر يومية وصول.</span><span class="sxs-lookup"><span data-stu-id="8edd0-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="8edd0-120">يمكن تحديد أوامر إرجاع متعددة وتضمينها في عملية وصول مفردة.</span><span class="sxs-lookup"><span data-stu-id="8edd0-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="8edd0-121">سوف يتم نسخ كل بند أمر إرجاع في بند دفتر يومية وصول الصنف المقابل.</span><span class="sxs-lookup"><span data-stu-id="8edd0-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="8edd0-122">يمكنك إنشاء دفتر يومية وصول يدويًا أو عن طريق استخدام النموذج <STRONG>وصول الصنف</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8edd0-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="8edd0-123">انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **وصول الصنف‬**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="8edd0-124">حدد دفتر يومية الوصول الذي تم إنشاؤه بالفعل ثم انقر فوق **البنود** لفتح النموذج **بنود دفتر اليومية، المواقع**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="8edd0-125">في علامة التبويب **عام**، قم بتعديل الرقم في الحقل **الكمية**، إذا كان ذلك مطلوبًا، ثم عين رمز إرجاع في الحقل **رمز الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="8edd0-126">وبدلاً عن ذلك، يمكنك تحديد خانة الاختيار **إدارة العزل** لإرسال الأصناف المرتجعة من خلال عملية فحص في سياق أمر إدخال عملية فحص.</span><span class="sxs-lookup"><span data-stu-id="8edd0-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="8edd0-127">وفي حالة إرسال الأصناف المرتجعة من خلال الفحص، لا يمكنك تحديد أمر إرجاع.</span><span class="sxs-lookup"><span data-stu-id="8edd0-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="8edd0-128">انقر فوق زر **‏‫التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="8edd0-129">إذا لم تظهر أية أخطاء في عملية التحقق من الصحة، فانقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="8edd0-130">تسجيل استلام الأصناف المرتجعة في نموذج التسجيل</span><span class="sxs-lookup"><span data-stu-id="8edd0-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="8edd0-131">كبديل لاستخدام النموذج **نظرة عامة على الوصول**، يمكنك استخدام نموذج **التسجيل** لتسجيل وصول الأصناف المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="8edd0-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="8edd0-132">انقر فوق **المبيعات والتسويق** \> **عام** \> **أوامر الإرجاع** \> **كل أوامر الإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="8edd0-133">قم بإنشاء أمر إرجاع جديد أو فتح أمر إرجاع من القائمة.</span><span class="sxs-lookup"><span data-stu-id="8edd0-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="8edd0-134">في علامة التبويب السريعة **البنود**، حدد بند أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="8edd0-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="8edd0-135">انقر فوق **تحديث البند**، ثم انقر فوق **التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="8edd0-136">قم بتعيين رمز الإرجاع في الحقل **رمز الإرجاع**، ثم انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="8edd0-137">لا يمكن إرسال الصنف للفحص كأمر إدخال مخزن فحص باستخدام نموذج <STRONG>التسجيل</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8edd0-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="8edd0-138">في شبكة **الحركات**، حدد الحركة المطلوب تسجيلها.</span><span class="sxs-lookup"><span data-stu-id="8edd0-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="8edd0-139">في شبكة **التسجيل الآن**، انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="8edd0-140">كرر الخطوتين السابقتين حتى تظهر جميع الأصناف المرتجعة في شبكة **التسجيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="8edd0-141">انقر فوق **ترحيل كل**.</span><span class="sxs-lookup"><span data-stu-id="8edd0-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8edd0-142">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="8edd0-142">See also</span></span>

<span data-ttu-id="8edd0-143">[نظرة عامة على الوصول (نموذج)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="8edd0-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  


