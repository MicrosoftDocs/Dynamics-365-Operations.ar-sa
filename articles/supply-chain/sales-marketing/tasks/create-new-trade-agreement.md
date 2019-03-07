---
title: إنشاء اتفاقية تجارية جديدة
description: يوضح لك هذا الإجراء كيفية إنشاء اتفاقية تجارة يتم فيها تسجيل منتج سعر جديد لمبيعات المنتجات اتفقتَ عليه مع عميل معين.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323492"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="4b4cc-103">إنشاء اتفاقية تجارية جديدة</span><span class="sxs-lookup"><span data-stu-id="4b4cc-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b4cc-104">يوضح لك هذا الإجراء كيفية إنشاء اتفاقية تجارة يتم فيها تسجيل منتج سعر جديد لمبيعات المنتجات اتفقتَ عليه مع عميل معين.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="4b4cc-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4b4cc-106">إذا كنت تستخدم البيانات الخاصة بك، قبل أن تبدأ استخدام هذا الدليل فأنت بحاجة إلى أن تتأكد من وجود اسم لدفتر يومية اتفاقيات التجارة حيث يتم تعيين العلاقة الافتراضية إلى "السعر (مبيعات)".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="4b4cc-107">قم بإنشاء دفتر يومية جديد لاتفاقيات التجارة وترحيله</span><span class="sxs-lookup"><span data-stu-id="4b4cc-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="4b4cc-108">انتقل للمبيعات والتسويق > الأسعار والخصومات > دفاتر يوميات اتفاقيات التجارة.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="4b4cc-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-109">Click New.</span></span>
3. <span data-ttu-id="4b4cc-110">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4b4cc-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4b4cc-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4b4cc-113">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-113">Click Lines.</span></span>
7. <span data-ttu-id="4b4cc-114">في الحقل "رمز الحساب" حدد "الجدول".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="4b4cc-115">في هذا المثال، تقومُ بتحديث السعر لعميل معين، وهو ما يعني أنك تحتاج إلى اختيار الجدول.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="4b4cc-116">إذا كنت تحدث سعر قائمة المنتجات، يمكنك تحديد "الكل"، بحيث يكون السعر الجديد صالحاً لجميع العملاء.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="4b4cc-117">إذا كنت تميز الأسعار بين قطاعات مختلفة من العملاء، يمكنك تحديد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="4b4cc-118">لتحديد مجموعة، يجب أن تقوم بإعداد مجموعات أسعار العملاء أولاً.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="4b4cc-119">في الحقل "اختيار الحساب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4b4cc-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4b4cc-121">في الحقل "رمز الصنف"، حدد "الجدول".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="4b4cc-122">عند إبرام اتفاقية تجارة من نوع "السعر (مبيعات)"، يجب عليك تحديد "جدول" فقط في رمز الصنف.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="4b4cc-123">وهذا لأن السعر يمثل قيمة مطلقة ولا يمكن أن يتكرر مع جميع المنتجات أو مجموعة من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="4b4cc-124">في الحقل "علاقة الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="4b4cc-125">في القائمة، حدد المنتج الذي تريد تضمينه في الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="4b4cc-126">قم بتدوين ملاحظة بالمنتج الذي حددتَه.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="4b4cc-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="4b4cc-128">في الحقل "من"، أدخل حدًا أدنى للكمية.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="4b4cc-129">إذا كان العميل ملزمًا بطلب حد أدنى من كمية قبل أن يستطيع التأهل للسعر الجديد، فستحتاج إلى تحديد تلك الكمية هنا.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="4b4cc-130">أدخل قيمة في الحقل "إلى" لتحديد الحد الأقصى للكمية الذي لا تُعتبر الاتفاقية صالحة إذا تجاوزتْه.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="4b4cc-131">إذا قمت بتقديم الأسعار والخصومات استناداً إلى فواصل كميات متعددة، فقم بتحديد كل قوس كمية كزوج من الحد الأدنى والحد الأقصى للكمية في الحقلين 'من' و'إلى' على التوالي.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="4b4cc-132">في الحقل "المبلغ بالعملة"، أدخل سعراً.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="4b4cc-133">في الحقل "من تاريخ"، أدخل تاريخًا ستكون الاتفاقية صالحة بدءًا منه.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="4b4cc-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-134">Click Save.</span></span>
18. <span data-ttu-id="4b4cc-135">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-135">Click Validate.</span></span>
19. <span data-ttu-id="4b4cc-136">انقر فوق "التحقق من صحة البنود المحددة".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="4b4cc-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-137">Click OK.</span></span>
21. <span data-ttu-id="4b4cc-138">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-138">Click Post.</span></span>
22. <span data-ttu-id="4b4cc-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="4b4cc-140">عرض اتفاقيات التجارة لأحد المنتجات</span><span class="sxs-lookup"><span data-stu-id="4b4cc-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="4b4cc-141">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4b4cc-142">في القائمة، ابحث عن المنتج الذي قمت بتحديث سعره للتو ثم حدده.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="4b4cc-143">في جزء الإجراءات، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="4b4cc-144">انقر فوق "عرض اتفاقيات التجارة".</span><span class="sxs-lookup"><span data-stu-id="4b4cc-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="4b4cc-145">راجع تفاصيل اتفاقية التجارة للسعر التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="4b4cc-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b4cc-147">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4b4cc-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="4b4cc-148">مدونات المجتمعات</span><span class="sxs-lookup"><span data-stu-id="4b4cc-148">Community blogs</span></span>
- [<span data-ttu-id="4b4cc-149">أسعار المبيعات في Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b4cc-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
