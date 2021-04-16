---
title: البحث عن الأسعار والخصومات السارية
description: يوضح هذا الإجراء كيفية البحث عن السعر و/أو الخصم لمنتج صالح لعميل معين حاليًا، دون إنشاء أمر مبيعات.
author: omulvad
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50d7cf7b765c27db5aa9ea50c8593132c68c850a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824836"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="b11ed-103">البحث عن الأسعار والخصومات السارية</span><span class="sxs-lookup"><span data-stu-id="b11ed-103">Look up applicable prices and discounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b11ed-104">يوضح هذا الإجراء كيفية البحث عن السعر و/أو الخصم لمنتج صالح لعميل معين حاليًا، دون إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="b11ed-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="b11ed-105">ويوضح الإجراء مثالاً محددًا، وأنت بحاجة إلى متابعة المثال باستخدام شركة العرض التقديمي USMF لتحديد القيم الضرورية.</span><span class="sxs-lookup"><span data-stu-id="b11ed-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="b11ed-106">البحث عن السعر القابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="b11ed-106">Find the applicable price</span></span>
1. <span data-ttu-id="b11ed-107">انتقل للمبيعات والتسويق > الأسعار والخصومات > البحث عن الأسعار.</span><span class="sxs-lookup"><span data-stu-id="b11ed-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="b11ed-108">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b11ed-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b11ed-109">في القائمة، ابحث عن العميل الولايات المتحدة-001 وحدده.</span><span class="sxs-lookup"><span data-stu-id="b11ed-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="b11ed-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b11ed-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b11ed-111">في الحقل "رقم الصنف، اكتب "T0004".</span><span class="sxs-lookup"><span data-stu-id="b11ed-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="b11ed-112">بشكل افتراضي، يتم تعيين الحقل "الكمية" على 1.</span><span class="sxs-lookup"><span data-stu-id="b11ed-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="b11ed-113">ومع ذلك، إذا كنت تعرف حجم الأمر الذي يريد العميل إدخاله للمنتج المعني، فأدخل هذه القيمة بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="b11ed-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="b11ed-114">هذه المعلومات ملاءمة إذا كانت اتفاقيات التجارة مع العميل بها فواصل كمية، أي أن سعر المنتج يعتمد على الحد الأدنى للكمية التي تم شراؤها.</span><span class="sxs-lookup"><span data-stu-id="b11ed-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="b11ed-115">في الحقل "التاريخ"، أدخل تاريخاً لما يتوقع العميل إدخال أمر به.</span><span class="sxs-lookup"><span data-stu-id="b11ed-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="b11ed-116">يمكن أن يكون التاريخ هو تاريخ اليوم أو تاريخ الغد أو أي تاريخ يُحدد في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="b11ed-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="b11ed-117">يُرجع النظام الآن السعر الصالح للمنتج المحدد عند شراءه بواسطة العميل المحدد في التاريخ المحدد بكمية محددة.</span><span class="sxs-lookup"><span data-stu-id="b11ed-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="b11ed-118">في هذا المثال، إذا اشترى العميل الولايات المتحدة-001 وحدة واحدة من المنتج T0004 اليوم، سيتحمل تكلفة 350 دولاراً للوحدة.</span><span class="sxs-lookup"><span data-stu-id="b11ed-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="b11ed-119">يأتي هذا السعر من اتفاقية تجارة قائمة ونشطة مع العميل.</span><span class="sxs-lookup"><span data-stu-id="b11ed-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="b11ed-120">توفر حقول أخرى في الصفحة تفاصيل إضافية حول سعر المنتج وتكلفة المنتج (إذا تم الإعداد بأصل المنتج)، والربحية المحسوبة.</span><span class="sxs-lookup"><span data-stu-id="b11ed-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="b11ed-121">إذا تم تحديد خيار إظهار متغيرات المنتج ذات الصلة، فهذا يعني وجود اتفاقيات تجارة إضافية لمتغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="b11ed-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="b11ed-122">انقر فوق خانة الاختيار "إظهار المتغيرات المتعلقة بالمنتج".</span><span class="sxs-lookup"><span data-stu-id="b11ed-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="b11ed-123">وتُعرض قائمة بمتغيرات المنتج، مع معلومات عن أبعادها.</span><span class="sxs-lookup"><span data-stu-id="b11ed-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="b11ed-124">في القائمة، ضع علامة تميز بها البند الذي يمثل اللون الأبيض.</span><span class="sxs-lookup"><span data-stu-id="b11ed-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="b11ed-125">لاحظ أن سعر المنتج الآن مختلف عن السعر الذي تم عرضه مسبقاً عندما لم يكن محددًا لكل بعد.</span><span class="sxs-lookup"><span data-stu-id="b11ed-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="b11ed-126">انقر فوق "عرض أسعار المبيعات".</span><span class="sxs-lookup"><span data-stu-id="b11ed-126">Click View sales prices.</span></span>
    * <span data-ttu-id="b11ed-127">تعرض الصفحة (المبيعات) جميع اتفاقيات التجارة القابلة للتطبيق للمنتج، بما في ذلك متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="b11ed-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="b11ed-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b11ed-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="b11ed-129">البحث عن الخصم القابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="b11ed-129">Find the applicable discount</span></span>
<span data-ttu-id="b11ed-130">تأكد من أن الحقل "حساب العميل" يحتوي على رقم العميل الولايات المتحدة-001 </span><span class="sxs-lookup"><span data-stu-id="b11ed-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="b11ed-131">في الحقل "رقم الصنف، اكتب "T0012".</span><span class="sxs-lookup"><span data-stu-id="b11ed-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="b11ed-132">تأكد من تعيين الحقل "الكمية" على 1.</span><span class="sxs-lookup"><span data-stu-id="b11ed-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="b11ed-133">ترد تفاصيل التسعير التالية للمنتج T0012 من اتفاقية تجارة واحدة أو أكثر: سعر الوحدة هو 1000 دولار كندي ونسبة الخصم المئوية هي 5.</span><span class="sxs-lookup"><span data-stu-id="b11ed-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="b11ed-134">تعيين الكمية إلى "20".</span><span class="sxs-lookup"><span data-stu-id="b11ed-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="b11ed-135">تؤدي زيادة كمية الأمر إلى خصم البند الذي سيتم تقديمه للعميل لتغييره من 5 في المائة إلى 7 في المائة.</span><span class="sxs-lookup"><span data-stu-id="b11ed-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="b11ed-136">يتم حساب المبلغ الصافي استنادًا إلى سعر الوحدة والخصم وإجمالي الكمية.</span><span class="sxs-lookup"><span data-stu-id="b11ed-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="b11ed-137">انقر فوق "عرض خصم البند".</span><span class="sxs-lookup"><span data-stu-id="b11ed-137">Click View line discount.</span></span>
    * <span data-ttu-id="b11ed-138">هناك اتفاقيتا خصم بنود للمنتج T0012، تحددان خصمًا قدره 5 في المائة لكمية بنود أمر من 1 إلى 10 وخصمًا 7 بالمائة لكميات أمر أكبر من 10.</span><span class="sxs-lookup"><span data-stu-id="b11ed-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="b11ed-139">لاحظ أنه يتم تطبيق الخصومات على مجموعة من المنتجات، وفي هذا المثال، رمز المجموعة 01، الذي يمثل المنتج T0012 عضوًا منها.</span><span class="sxs-lookup"><span data-stu-id="b11ed-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="b11ed-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b11ed-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]