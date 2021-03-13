---
title: ضريبة الخصم في حركات المبيعات
description: يسرد هذا الموضوع الخطوات الخاصة بتجنب حساب ضريبة الخصم للعملاء المحددين. بالنسبة للعملاء الذين يحددون ضريبة الخصم في مدفوعاتهم إليك، يمكنك تعيين مجموعة ضريبة الخصم الافتراضية.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060696"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="83761-104">ضريبة الخصم في حركات المبيعات</span><span class="sxs-lookup"><span data-stu-id="83761-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="83761-105">يسرد هذا الموضوع الخطوات الخاصة بتجنب حساب ضريبة الخصم للعملاء المحددين.</span><span class="sxs-lookup"><span data-stu-id="83761-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="83761-106">بالنسبة للعملاء الذين يحددون ضريبة الخصم في مدفوعاتهم إليك، يمكنك تعيين **مجموعة ضريبة الخصم** الافتراضية في صفحة **العملاء**.</span><span class="sxs-lookup"><span data-stu-id="83761-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="83761-107">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > العملاء > كافة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="83761-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="83761-108">انقر فوق حساب العميل الخاص، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="83761-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="83761-109">في علامة التبويب **الفاتورة والتسليم**، قم بتعيين حقل **حساب ضريبة الخصم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="83761-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="83761-110">لن يتم حساب ضريبة الخصم في حالة عدم تبديل **حساب ضريبة الخصم** لهذا العميل في البيانات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="83761-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="83761-111">حدد مجموعة ضريبة الخصم في **مجموعة ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="83761-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="83761-112">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="83761-112">Click **Save**.</span></span>

<span data-ttu-id="83761-113">بالنسبة للأصناف/الخدمات، الخاضعة لضريبة الخصم، يمكنك تعيين **مجموعة ضريبة خصم الصنف** الافتراضية في **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="83761-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="83761-114">‏‫انتقل إلى ‬**جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .</span><span class="sxs-lookup"><span data-stu-id="83761-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="83761-115">انقر فوق رقم الصنف الخاص، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="83761-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="83761-116">في علامة التبويب **البيع**، انقر فوق **حساب ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="83761-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="83761-117">لن يتم حساب ضريبة الخصم في حالة عدم تعيين **حساب ضريبة الخصم** إلى **نعم** لهذا الصنف في علامة تبويب **البيع** في صفحة **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="83761-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="83761-118">حدد مجموعة ضريبة خصم الصنف في قائمة **مجموعة ضريبة خصم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="83761-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="83761-119">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="83761-119">Click **Save**.</span></span>

<span data-ttu-id="83761-120">يمكن تعيين مجموعات ضريبة الخصم ومجموعات ضريبة خصم الصنف باستخدام صفحة **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="83761-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="83761-121">سيتم استخدام مجموعة ضريبة الخصم الافتراضية ومجموعة ضريبة خصم الصنف كإدخالات افتراضية في بنود أوامر المبيعات عند إنشاء أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="83761-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="83761-122">يتم حساب ضريبة الخصم وترحيلها **بدفتر يومية مدفوعات العميل**.</span><span class="sxs-lookup"><span data-stu-id="83761-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="83761-123">يمكنك تعديل كود ضريبة الخصم القابلة للتطبيق يدويًا بالإضافة إلى مبلغ ضريبة الخصم الفعلية في علامة التبويب **ضريبة الخصم** في صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="83761-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="83761-124">سيتم خصم مبلغ ضريبة الخصم المحتسبة من دفع المورد وترحيله إلى حساب **مقاصة ضريبة الخصم** في إيصال متعلق.</span><span class="sxs-lookup"><span data-stu-id="83761-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>
