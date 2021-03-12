---
title: تعديلات الأسعار والخصومات
description: توفر هذه المقالة معلومات حول الخصومات وتعديلات الأسعار في Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f29e90e1c61792c70d4d6eaeee7758676bf193b2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972470"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="8dd34-103">تعديلات الأسعار والخصومات</span><span class="sxs-lookup"><span data-stu-id="8dd34-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8dd34-104">توفر هذه المقالة معلومات حول الخصومات وتعديلات الأسعار في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8dd34-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8dd34-105">في Commerce، يمكنك إجراء تعديلات الأسعار على المنتجات، ويمكنك أيضًا إعداد الخصومات التي يتم تطبيقها على صنف أو حركة في نقطة البيع، أو في أمر مبيعات مركز اتصال أو أمر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="8dd34-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="8dd34-106">يمكن ربط كلٍّ من تعديلات الأسعار والخصومات بمجموعات الأسعار.</span><span class="sxs-lookup"><span data-stu-id="8dd34-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="8dd34-107">ولتعديل الأسعار والخصومات، يمكنك تحديد تاريخ بدء واحد وتاريخ انتهاء أو فترة تكرار، وكود خصم، وبعض السمات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="8dd34-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="8dd34-108">يمكن تطبيق تعديلات الأسعار والخصومات للمنتجات أو متغيرات أو الفئات.</span><span class="sxs-lookup"><span data-stu-id="8dd34-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="8dd34-109">وإذا كان يُطبق أكثر من خصم واحد على منتج، قد يتلقي عميل أحد الخصومات أو خصمًا مدمجًا، اعتماداً إلى تكوين الخصم.</span><span class="sxs-lookup"><span data-stu-id="8dd34-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="8dd34-110">يطبّق Commerce تلقائيًا الخصم أو مجموعة الخصومات التي تقدم السعر الأفضل للعميل.</span><span class="sxs-lookup"><span data-stu-id="8dd34-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="8dd34-111">وعند إعداد تعديل سعر أو خصم، تأكد من تعيين مجموعات السعر التي يتم تعيينها للقنوات الصحيحة أو الكتالوجات أو التبعيات أو برامج الولاء الذي تريده تطبيق الخصم عليه.</span><span class="sxs-lookup"><span data-stu-id="8dd34-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="8dd34-112">بالإضافة إلى ذلك، إذا كنت تريد إنشاء معرف الخصم تلقائيًا، فقم بإعداد المسلسلات الرقمية في صفحة **معلمات Commerce** قبل تحديد خصم أو تعديل سعر جديد.</span><span class="sxs-lookup"><span data-stu-id="8dd34-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="8dd34-113">يمكنك حذف تعديل سعر أو خصم.</span><span class="sxs-lookup"><span data-stu-id="8dd34-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="8dd34-114">ومع ذلك، سيتم فقدان المعلومات الإحصائية.</span><span class="sxs-lookup"><span data-stu-id="8dd34-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="8dd34-115">أنواع الخصومات</span><span class="sxs-lookup"><span data-stu-id="8dd34-115">Types of discounts</span></span>

<span data-ttu-id="8dd34-116">هناك أنواع عديدة من الخصومات:</span><span class="sxs-lookup"><span data-stu-id="8dd34-116">There are many types of discounts:</span></span>

- <span data-ttu-id="8dd34-117">**خصم بسيط** – نسبة مئوية واحدة أو مبلغ.</span><span class="sxs-lookup"><span data-stu-id="8dd34-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="8dd34-118">**خصم الكمية** – خصم يتم تطبيقه عند شراء اثنين أو أكثر من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="8dd34-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="8dd34-119">**خصم المنتجات المختلفة‬** – خصم يتم تطبيقه عند شراء مجموعة محددة من المنتجات.</span><span class="sxs-lookup"><span data-stu-id="8dd34-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="8dd34-120">**خصم الحد** – خصم يتم تطبيقه عندما يكون إجمالي الحركة أكبر من مبلغ محدد.</span><span class="sxs-lookup"><span data-stu-id="8dd34-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="8dd34-121">**‏‫الخصومات المستندة إلى طريقة الدفع‬‬** - الخصم الذي يتم تطبيقه عندما يكون إجمالي الحركة أكثر من مبلغ محدد ويتم استخدام نوع دفع محدد (على سبيل المثال، نقدًا أو بطاقة ائتمان أو بطاقة خصم) للدفع.</span><span class="sxs-lookup"><span data-stu-id="8dd34-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="8dd34-122">**خصم الشحن** – الخصم الذي يتم تطبيقه عندما يكون إجمالي الحركة أكثر من مبلغ محدد ويتم استخدام طريقة محددة للتسليم (على سبيل المثال، شحن ليومين أو شحن طوال الليل) في الأمر.</span><span class="sxs-lookup"><span data-stu-id="8dd34-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="8dd34-123">يمكن ربط كلٍّ من تعديلات الأسعار والخصومات بمجموعات الأسعار.</span><span class="sxs-lookup"><span data-stu-id="8dd34-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="8dd34-124">ويمكن فيما بعد ربط مجموعات الأسعار بالقنوات، والكتالوجات، والتبعيات، وبرامج الولاء.</span><span class="sxs-lookup"><span data-stu-id="8dd34-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
