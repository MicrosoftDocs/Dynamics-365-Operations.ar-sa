---
title: تكامل الأصول الثابتة
description: يمكن تكامل الأصول الثابتة مع دفتر الأستاذ العام وإدارة المخزون وكذلك الحسابات المدينة والدائنة. كما يمكن إعداد أصول ثابتة بحيث تتكامل مع أوامر الشراء.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb1348a3a3c47e5fd7df46d9ce4af3725d8896b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176211"
---
# <a name="fixed-assets-integration"></a><span data-ttu-id="eadf2-104">تكامل الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="eadf2-104">Fixed assets integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eadf2-105">يمكن تكامل الأصول الثابتة مع دفتر الأستاذ العام وإدارة المخزون وكذلك الحسابات المدينة والدائنة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-105">Fixed assets can be integrated with General ledger, Inventory management, Accounts receivable, and Accounts payable.</span></span> <span data-ttu-id="eadf2-106">كما يمكن إعداد أصول ثابتة بحيث تتكامل مع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="eadf2-106">You can also set up Fixed assets so that it is integrated with purchase orders.</span></span>

<a name="general-ledger"></a><span data-ttu-id="eadf2-107">دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="eadf2-107">General ledger</span></span>
--------------

<span data-ttu-id="eadf2-108">في دفتر الأستاذ العام، يتم عادةً تلخيص قيمة كافة الأصول الثابتة في حسابات رئيسية متعددة مطلوبة للتقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="eadf2-108">In General ledger, the value of all fixed assets is typically summarized in multiple main accounts that are required for financial reporting.</span></span> <span data-ttu-id="eadf2-109">ومع ذلك، يمكنك إنشاء الكثير من سجلات الأصول الثابتة في صفحة **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-109">However, on the **Fixed assets** page, you can create many fixed asset records.</span></span> <span data-ttu-id="eadf2-110">يمكن أن تتضمن هذه السجلات معلومات مثل سعر الامتلاك والإهلاك والتقييم.</span><span class="sxs-lookup"><span data-stu-id="eadf2-110">These records can include information such as the acquisition price, depreciation, and valuation.</span></span> <span data-ttu-id="eadf2-111">ويتم تحديث الحسابات الرئيسية المناسبة في كل مرة تقوم فيها بترحيل حركة لأصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="eadf2-111">Each time that you post a transaction for a fixed asset, the appropriate main accounts are updated.</span></span> <span data-ttu-id="eadf2-112">ودائمًا ما تقوم الحسابات الرئيسية الخاصة بالأصول الثابتة بعرض القيمة المحدثة للأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-112">The main accounts for fixed assets always show the updated value of the fixed assets.</span></span>

<span data-ttu-id="eadf2-113">في صفحة **ملفات تعريف ترحيل الأصول الثابتة**، يمكنك تحديد الحسابات الرئيسية التي يتم ترحيل حركات دفتر الأصول الثابتة إليها.</span><span class="sxs-lookup"><span data-stu-id="eadf2-113">On the **Fixed asset posting profiles** page, you define the main accounts that fixed asset book transactions are posted to.</span></span> <span data-ttu-id="eadf2-114">يمكنك أيضًا تحديد أنواع حركات الأصول الثابتة التي يتم ترحيلها إلى الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="eadf2-114">You also specify the types of fixed asset transactions that are posted to each main account.</span></span> <span data-ttu-id="eadf2-115">ويمكنك إنشاء مجموعات متنوعة من حسابات الرئيسية للأصول الثابتة وذلك وفقًا لمستوى التفاصيل المطلوب للأصول الثابتة في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="eadf2-115">You can create various combinations of main accounts for fixed assets, depending on the level of detail that you want for fixed assets in the general ledger.</span></span> <span data-ttu-id="eadf2-116">بإمكان الحسابات الرئيسية أن تستند إلى أنواع الحركات والدفاتر وحسابات رئيسية أخرى.</span><span class="sxs-lookup"><span data-stu-id="eadf2-116">Main accounts can be based on transaction types, books, and other main accounts.</span></span>

## <a name="inventory-management"></a><span data-ttu-id="eadf2-117">إدارة المخزون</span><span class="sxs-lookup"><span data-stu-id="eadf2-117">Inventory management</span></span>
<span data-ttu-id="eadf2-118">في دفتر يومية المخزون للأصول الثابتة، يمكنك إدخال قيمة امتلاك الأصول الثابتة التي تم إنتاجها الكيان القانوني أو إنشائها لصالحها.</span><span class="sxs-lookup"><span data-stu-id="eadf2-118">In the inventory journal for fixed assets, you can enter the acquisition of fixed assets that the legal entity has produced or constructed for itself.</span></span> <span data-ttu-id="eadf2-119">ثم يمكنك نقل أصناف المخزون إلى الأصول الثابتة كامتلاك أو كجزء من عملية امتلاك.</span><span class="sxs-lookup"><span data-stu-id="eadf2-119">You can then transfer inventory items to fixed assets either as an acquisition or as part of an acquisition.</span></span> 

<span data-ttu-id="eadf2-120">ويمكن كذلك الحصول على أصول باستخدام أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="eadf2-120">You can also acquire assets by using purchase orders.</span></span> <span data-ttu-id="eadf2-121">وعندما تحتوي أوامر الشراء على أصناف المخزون التي تم تعيينها كأصول ثابتة، فإن إعداد الخيار **السماح بالحصول على الأصل من الشراء‬** في صفحة **محددات الأصول الثابتة‬** يحدد ما إذا كان سيتم ترحيل استحواذ للأصل الثابت عند ترحيل الفاتورة أم لا.</span><span class="sxs-lookup"><span data-stu-id="eadf2-121">When purchase orders contain inventory items that are designated as fixed assets, the setting of the **Allow asset acquisition from Purchasing** option on the **Fixed assets parameters** page determines whether an acquisition is posted for the fixed asset when the invoice is posted.</span></span> <span data-ttu-id="eadf2-122">سينشئ بند شراء واحد أصلاً ثابتًا واحدًا فقط، بغض النظر عن الكمية.</span><span class="sxs-lookup"><span data-stu-id="eadf2-122">One purchasing line will create one fixed asset, regardless of the quantity.</span></span> <span data-ttu-id="eadf2-123">يعتمد تأثير امتلاك أصول ثابتة تحتوي على المخزون على الإعداد للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="eadf2-123">The effect that the acquisition of fixed assets has on inventory depends on the setup of the legal entity.</span></span> 

<span data-ttu-id="eadf2-124">عندما يصبح أحد أصناف المخزون جزءًا من عملية الاستحواذ على أصول ثابتة من خلال دفتر يومية المخزون أو أمر شراء أو مقترح استحواذ‬، يتم إنشاء حركة استحواذ‬ دفتر الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-124">When an inventory item becomes a fixed asset acquisition through the inventory journal, a purchase order, or an acquisition proposal, a fixed asset book acquisition transaction is created.</span></span> <span data-ttu-id="eadf2-125">وإذا تضمن استحواذ الدفتر دفترًا مشتقًا، فسيتم أيضًا إنشاء حركة استحواذ الدفتر المشتق.</span><span class="sxs-lookup"><span data-stu-id="eadf2-125">If a book acquisition includes a derived book, the derived book acquisition transaction is also created.</span></span> 

<span data-ttu-id="eadf2-126">إن قواعد الترحيل التي تم إعدادها في صفحة **الترحيل** في إدارة المخزون تتحكم في خفض المخزون عند ترحيل عملية استحواذ.</span><span class="sxs-lookup"><span data-stu-id="eadf2-126">Posting rules that are set up on the **Posting** page in Inventory management control the decrease in inventory when an acquisition is posted.</span></span> <span data-ttu-id="eadf2-127">ومع ذلك، فأنت لا تعمل دائمًا على خفض المخزون عند ترحيل فواتير مرتبطة بأصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-127">However, you don’t always decrease inventory when you post invoices that are related to fixed assets.</span></span> <span data-ttu-id="eadf2-128">في بعض الحالات، قد يتم شراء الأصول الثابتة للاستخدام الداخلي.</span><span class="sxs-lookup"><span data-stu-id="eadf2-128">In some cases, the fixed assets might be purchased for internal use.</span></span> <span data-ttu-id="eadf2-129">من الأمثلة على ذلك، شراء كمبيوتر محمول لقسم المبيعات.</span><span class="sxs-lookup"><span data-stu-id="eadf2-129">An example is a laptop that is purchased for the sales department.</span></span> <span data-ttu-id="eadf2-130">وعند التعامل مع أوامر الشراء، يمكنك استخدام الأصناف التي تم إعدادها لإعادة البيع والاستخدام الداخلي معًا.</span><span class="sxs-lookup"><span data-stu-id="eadf2-130">When you work with purchase orders, you can use items that are set up for both resale and internal use.</span></span> 

<span data-ttu-id="eadf2-131">إذا كنت تستخدم حسابات إيصالات وصرف محددة للأصول الثابتة الخاصة بمجموعات الأصناف، فيمكنك استخدام نفس صنف المخزون للمشتريات الداخلية وكمخزون لإعادة البيع.</span><span class="sxs-lookup"><span data-stu-id="eadf2-131">If you use specific receipt and issue accounts on item groups for fixed assets, you can use the same inventory item both for internal purchases and as stock for resale.</span></span> 

<span data-ttu-id="eadf2-132">يتم إعداد الأصول الثابتة المخصصة للاستخدام الداخلي بحيث يكون لديها حساب من النوع **استلام الأصل الثابت‬**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-132">Fixed assets that are for internal use are set up so that they have an account type of **Fixed asset receipt**.</span></span> <span data-ttu-id="eadf2-133">يتم استخدام نوع الحساب هذا لتعقب استلام الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="eadf2-133">This account type is used to track the receipt of the fixed asset.</span></span> <span data-ttu-id="eadf2-134">عندما تقوم بترحيل فاتورة مورد، فقم باستخدام حساب إيصال الأصول الثابتة إذا تحققت أي من الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="eadf2-134">When you post a vendor invoice, use the fixed asset receipt account if any of the following conditions is true:</span></span>

-   <span data-ttu-id="eadf2-135">بند فاتورة تتضمن أصل ثابت موجود لأغراض داخلية.</span><span class="sxs-lookup"><span data-stu-id="eadf2-135">The invoice line contains an existing fixed asset for internal purposes.</span></span>
-   <span data-ttu-id="eadf2-136">تم تحديد خانة الاختيار **أصل ثابت جديد؟** لبند إيصال استلام المنتجات التي تم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="eadf2-136">The **New fixed asset?** check box is selected for the product receipt line that is posted.</span></span>
-   <span data-ttu-id="eadf2-137">تم تحديد خانة الاختيار **إنشاء أصل ثابت جديد‬** لبند فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="eadf2-137">The **Create a new fixed** asset check box is selected for the vendor invoice line.</span></span>

<span data-ttu-id="eadf2-138">يكون هذا الحساب عادة حساب مصروفات.</span><span class="sxs-lookup"><span data-stu-id="eadf2-138">Typically, this account is an expense account.</span></span> <span data-ttu-id="eadf2-139">يمكنك إعداد نوع حساب **استلام الأصل الثابت** لمجموعة أصناف أو صنف فردي عن طريق استخدام علامة التبويب **أمر الشراء** في صفحة **مجموعة الأصناف** أو صفحة **الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-139">You can set up the **Fixed asset receipt** account type for either an item group or an individual item by using the **Purchase order** tab on the **Item group** or **Posting** page.</span></span>

<span data-ttu-id="eadf2-140">بطريقة مماثلة، يمكن إعداد الأصول الثابتة المخصصة للاستخدام الداخلي بحيث يكون لديها حساب من النوع **صرف أصل ثابت‬**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-140">Similarly, fixed assets that are for internal use can be set up so that they have an account type of **Fixed asset issue**.</span></span> <span data-ttu-id="eadf2-141">يتم استخدام نوع الحساب هذا لإصدار الأصل الثابت إلى المستلم.</span><span class="sxs-lookup"><span data-stu-id="eadf2-141">This account type is used to track the issuing of the fixed asset to the recipient.</span></span> <span data-ttu-id="eadf2-142">وعند الحصول على أحد الأصول باستخدام أمر شراء، فإن حساب إصدار الأصل الثابت سيعادل حساب الأصل الثابت المدين.</span><span class="sxs-lookup"><span data-stu-id="eadf2-142">When an asset is acquired by using a purchase order, the fixed asset issue account offsets the fixed asset debit account.</span></span> <span data-ttu-id="eadf2-143">يمكن ترحيل الاستحواذ على الأصول إما عند ترحيل فاتورة مورّد أو عند ترحيل الاستحواذ على الأصول في دفتر اليومية الأصول الثابتة، باستخدام مقترح استحواذ على الأرجح.</span><span class="sxs-lookup"><span data-stu-id="eadf2-143">The asset acquisition can be posted either when you post a vendor invoice or when you post the asset acquisition in the Fixed assets journal, possibly by using an acquisition proposal.</span></span> <span data-ttu-id="eadf2-144">ويمكنك إعداد نوع الحساب **صرف أصل ثابت** لمجموعة أصناف أو صنف فردي عن طريق استخدام علامة التبويب **المخزون** في صفحة **مجموعة الأصناف** أو صفحة **ترحيل الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-144">You can set up the **Fixed asset issue** account type for either an item group or an individual item by using the **Inventory** tab on the **Item group** or **Item posting** page.</span></span> 

<span data-ttu-id="eadf2-145">في النهاية، تتحدد الحسابات الرئيسية المستخدمة للترحيل بخيارات تكامل دفتر الأستاذ التي تم تحديدها لمجموعة نموذج الصنف.</span><span class="sxs-lookup"><span data-stu-id="eadf2-145">Ultimately, the main accounts that are used for posting are determined by the options for ledger integration that are specified for the item model group.</span></span> <span data-ttu-id="eadf2-146">بالإضافة إلى ذلك، الحسابات الرئيسية المستخدمة تختلف تبعاً لما إذا كان هناك أصل معين لبند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="eadf2-146">Additionally, the main accounts that are used vary, depending on whether an asset is assigned to the purchase order line.</span></span> <span data-ttu-id="eadf2-147">ويتم اشتقاق الحسابات من ملف تعريف الترحيل لكل مجموعة أصناف.</span><span class="sxs-lookup"><span data-stu-id="eadf2-147">The accounts are derived from the posting profile for each item group.</span></span> 
<span data-ttu-id="eadf2-148">**ملاحظة:** لا يمكن تعيين أصل ثابت أو إنشاء أصل ثابت من البند، في حالة وجود حجز مخزون عند ترحيل إيصالات استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="eadf2-148">**Note:** If an inventory reservation exists when product receipts are posted, you can’t assign a fixed asset or create a fixed asset from the line.</span></span> 

<span data-ttu-id="eadf2-149">تعتمد الحسابات التي يتم ترحيل حركات الأصول الثابتة إليها على عاملين: أحد العاملين هو ما إذا كان قد تم شراء الأصول أو إنشاؤها بواسطة الكيان القانوني والعامل الثاني هو نوع حركة الأصل.</span><span class="sxs-lookup"><span data-stu-id="eadf2-149">The accounts that fixed asset transactions are posted to depend on two factors: whether the assets are purchased or constructed by the legal entity, and the transaction type of the asset.</span></span> 

<span data-ttu-id="eadf2-150">يعمل نوع الحركة على ربط العملية المخزنية بملف تعريف الترحيل في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-150">The transaction type connects the inventory transaction to the posting profile in Fixed assets.</span></span> <span data-ttu-id="eadf2-151">ونظرًا لأن ملف تعريف الترحيل في الأصول الثابتة يقوم بتعريف الحسابات التي تم تحديثها، فإن تحديد نوع حركة الأصل الثابت يعد أيضًا، بشكلٍ غير مباشر، تحديدًا للحسابات الرئيسية التي تم ترحيل الحركة إليها.</span><span class="sxs-lookup"><span data-stu-id="eadf2-151">Because the posting profile in Fixed assets defines which accounts are updated, the selection of a transaction type for a fixed asset is also, indirectly, the selection of the main accounts that the transaction is posted to.</span></span> <span data-ttu-id="eadf2-152">بالنسبة للأصول الثابتة التي تم إنشاؤها أو شراؤها، فعادةً ما يكون نوع الحركة **الاستحواذ‬** أو **تسوية الاستحواذ‬**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-152">For both constructed and purchased fixed assets, the transaction type is typically **Acquisition** or **Acquisition adjustment**.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="eadf2-153">الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="eadf2-153">Accounts receivable</span></span>
<span data-ttu-id="eadf2-154">تكامل الأصول الثابتة مع الحسابات المدينة يستخدم ملفات تعريف الترحيل التي تم إعدادها في الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-154">The integration of Fixed assets with Accounts receivable uses posting profiles that are set up in Fixed assets.</span></span> <span data-ttu-id="eadf2-155">يتم تنشيط ملفات تعريف الترحيل هذه عندما يتم تحديد أصل ثابت ودفتر ونوع حركة الأصل الثابت لفاتورة عميل قبل ترحيل فاتورة العميل.</span><span class="sxs-lookup"><span data-stu-id="eadf2-155">These posting profiles are activated when a fixed asset, book, and fixed asset transaction type are selected for a customer invoice before the customer invoice is posted.</span></span> <span data-ttu-id="eadf2-156">ولأن الأصول الثابتة لا تعتبر جزءًا من إدارة المخزون، فيجب عليك استخدام صفحة **فاتورة النص الحر** عند بيع أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="eadf2-156">Because fixed assets aren’t part of Inventory management, you must use the **Free text invoice** page when you sell a fixed asset.</span></span> 

<span data-ttu-id="eadf2-157">إذا تضمن الدفتر دفترًا مشتقًا، فسيتم إنشاء حركة الدفتر المشتق عند ترحيل فاتورة العميل.</span><span class="sxs-lookup"><span data-stu-id="eadf2-157">If the book includes a derived book, the derived book transaction is created when you post the customer invoice.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="eadf2-158">حسابات دائنة</span><span class="sxs-lookup"><span data-stu-id="eadf2-158">Accounts payable</span></span>
<span data-ttu-id="eadf2-159">يتم عادة الاستحواذ على الحسابات الدائنة من موردين خارجيين.</span><span class="sxs-lookup"><span data-stu-id="eadf2-159">Typically, fixed assets are acquired from external vendors.</span></span> <span data-ttu-id="eadf2-160">يمكنك استخدام صفحة **محددات الأصول الثابتة‬** لتحديد ما إذا كان ترحيل عمليات الاستحواذ على الأصول يتم دومًا عند ترحيل فواتير المورّد أو ما إذا كان من الممكن ترحيل عمليات الاستحواذ على الأصول من الأصول الثابتة فقط.</span><span class="sxs-lookup"><span data-stu-id="eadf2-160">You can use the **Fixed assets parameters** page to specify whether asset acquisitions are always posted when you post vendor invoices, or whether asset acquisitions can be posted only from Fixed assets.</span></span> <span data-ttu-id="eadf2-161">عند تمكين بترحيل الاستحواذ على الأصول من الحسابات الدائنة، يتم تحديث حسابات الأصول الثابتة كلما تم ترحيل فاتورة مورّد لعملية استحواذ على أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="eadf2-161">If you enable asset acquisitions to be posted from Accounts payable, fixed asset accounts are updated whenever a vendor invoice for a fixed asset acquisition is posted.</span></span> 

<span data-ttu-id="eadf2-162">إذا تم إعداد النظام بحيث يتم ترحيل عملية امتلاك أصل عند ترحيل فاتورة، فسيتم ترحيل الحركة وفقًا لملفات تعريف الترحيل التي تم إعدادها في الأصول الثابتة للأنواع المتنوعة من حركات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="eadf2-162">If the system is set up to post an asset acquisition when an invoice is posted, the transaction is posted according to the posting profiles that are set up in Fixed assets for the various fixed asset transaction types.</span></span> <span data-ttu-id="eadf2-163">ويتم التحكم في الترحيل بواسطة الأصل الثابت والدفتر ونوع حركة الأصل الثابت كما تم تحديدها في صفحة **أمر الشراء** قبل ترحيل فاتورة المورّد.</span><span class="sxs-lookup"><span data-stu-id="eadf2-163">The posting is controlled by the fixed asset, book, and fixed asset transaction type that are selected on the **Purchase order** page before the vendor invoice is posted.</span></span> 

<span data-ttu-id="eadf2-164">إذا تضمن الدفتر دفترًا مشتقًا، فسيتم إنشاء حركة الدفتر المشتق عند ترحيل فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="eadf2-164">If the book includes a derived book, the derived book transaction is created when you post the vendor invoice.</span></span>

<span data-ttu-id="eadf2-165">يتم تنشيط التكامل لكل بند من بنود الأمر من علامة التبويب **الأصول الثابتة** الموجودة في علامة التبويب السريعة **تفاصيل البند** في صفحة **أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-165">The integration for each order line is activated on the **Fixed assets** tab on the **Line details** FastTab on the **Purchase order** page.</span></span> <span data-ttu-id="eadf2-166">يمكنك إرسال أمر شراء لأصل ثابت للمورد.</span><span class="sxs-lookup"><span data-stu-id="eadf2-166">You can send a purchase order for a fixed asset to the vendor.</span></span> <span data-ttu-id="eadf2-167">ومع ذلك، يتم يتم تحديث الأصول الثابتة والحسابات الرئيسية فقط عندما تقوم بترحيل فاتورة المورد استلام الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="eadf2-167">However, the fixed assets and main accounts are updated only when you post the vendor invoice after the fixed asset is received.</span></span> <span data-ttu-id="eadf2-168">ونظرًا لأن أوامر الشراء يمكن أن تتضمن أصناف المخزون فقط، فسيعتمد تأثير امتلاك الأصول الثابتة على المخزون وفقًا لإعداد الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="eadf2-168">Because purchase orders can contain only inventory items, the effect that the acquisition of fixed assets has on inventory depends on the setup of the legal entity.</span></span>

## <a name="project-management-and-accounting"></a><span data-ttu-id="eadf2-169">إدارة المشاريع والمحاسبة</span><span class="sxs-lookup"><span data-stu-id="eadf2-169">Project management and accounting</span></span>
<span data-ttu-id="eadf2-170">يمكنك إقران مشروع بأصل يتأثر بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="eadf2-170">You can associate a project with an asset that is affected by the project.</span></span> <span data-ttu-id="eadf2-171">كما يمكنك إقران كل مرحلة أو مهمة أو مشروع فرعي بأصل مختلف.</span><span class="sxs-lookup"><span data-stu-id="eadf2-171">You can also associate each phase, task, or subproject to a different asset.</span></span> <span data-ttu-id="eadf2-172">يمكن إقران كل سجل المشروع أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="eadf2-172">One asset can be associated with each project record.</span></span> <span data-ttu-id="eadf2-173">يمكنك إنشاء الاقتران عند إدخال رقم أصل ثابت في حقل رقم **الأصل الثابت** في صفحة **المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-173">You create the association when you enter a fixed asset number in the **Fixed asset** number field on the **Projects** page.</span></span> <span data-ttu-id="eadf2-174">يجب أن يكون المشروع من النوع **داخلي** أو **مشروع تكلفة**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-174">The project type must be either **Internal** or **Cost project**.</span></span> 

<span data-ttu-id="eadf2-175">يمكنك أيضًا استخدام صفحة **المشاريع** لعرض تفاصيل حول الأصول المقترنة بالمشاريع.</span><span class="sxs-lookup"><span data-stu-id="eadf2-175">You can also use the **Projects** page to view details about assets that are associated with projects.</span></span> <span data-ttu-id="eadf2-176">لعرض سجل الأصول الثابتة، على علامة التبويب السريعة **الإعداد**، انقر فوق ارتباط الأصل لفتح صفحة **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-176">To view the fixed asset record, on the **Setup** FastTab, click the asset link to open the **Fixed assets** page.</span></span> <span data-ttu-id="eadf2-177">ثم انقر فوق **المشاريع** &gt; **كافة المشاريع** لعرض المشاريع المقترنة بالأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="eadf2-177">Then click **Projects** &gt; **All projects** to view the projects that are associated with the fixed asset.</span></span> 

<span data-ttu-id="eadf2-178">يمكنك عادةً إقران أصول ثابتة بالمشاريع عندما تتعلق المشاريع بالعمل أو الصيانة أو إدخال تحسينات على الأصل.</span><span class="sxs-lookup"><span data-stu-id="eadf2-178">Typically, you associate fixed assets with projects when the projects are related to work, maintenance, or improvements for the asset.</span></span> <span data-ttu-id="eadf2-179">وعند اكتمال المشروع، لا يتم إنشاء تعديل بالزيادة للأصل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="eadf2-179">When the project is completed, a write-up adjustment for the asset isn’t created automatically.</span></span> <span data-ttu-id="eadf2-180">وبالتالي، يجب إنشاء التعديل بالزيادة يدويًا إذا كان مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="eadf2-180">Therefore, if a write-up adjustment is required, you must create it manually.</span></span> 

<span data-ttu-id="eadf2-181">لحذف اقتران بين مشروع وأصل، قم بإلغاء تحديد حقل **رقم الأصل الثابت** في صفحة **المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="eadf2-181">To delete the association between a project and an asset, clear the **Fixed asset number** field on the **Projects** page.</span></span> 

<span data-ttu-id="eadf2-182">يمكنك أيضًا تعيين الأصل الثابت الذي تقوم بإنشائه أو تصنيعه كجزء من مشروع تقديري.</span><span class="sxs-lookup"><span data-stu-id="eadf2-182">You can also designate a fixed asset that you’re creating or manufacturing as part of an estimate project.</span></span> <span data-ttu-id="eadf2-183">وفي نهاية المشروع التقديري، يمكنك ترحيل حركة امتلاك الأصل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="eadf2-183">At the end of an estimate project, you can automatically post an asset acquisition transaction.</span></span>

<span data-ttu-id="eadf2-184">لمزيد من المعلومات، راجع [الحصول على الأصول عن طريق التدبير‬‏‫](acquire-assets-procurement.md)</span><span class="sxs-lookup"><span data-stu-id="eadf2-184">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md)</span></span>


