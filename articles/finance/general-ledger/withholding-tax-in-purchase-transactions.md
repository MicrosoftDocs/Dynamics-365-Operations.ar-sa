---
title: ضريبة الخصم في حركات الشراء
description: بالنسبة للموردين الخاضعين لضريبة الخصم، يمكنك تعيين **مجموعة ضريبة الخصم** الافتراضية في صفحة **كافة الموردين**.
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
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256657"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="f6ab1-103">ضريبة الخصم في حركات الشراء</span><span class="sxs-lookup"><span data-stu-id="f6ab1-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="f6ab1-104">بالنسبة للموردين الخاضعين لضريبة الخصم، يمكنك تعيين **مجموعة ضريبة الخصم** الافتراضية في صفحة **كافة الموردين**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="f6ab1-105">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > المورّدون > كافة المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="f6ab1-106">انقر فوق حساب المورد الخاص، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="f6ab1-107">في علامة التبويب **الفاتورة والتسليم**، قم بتعيين حقل **حساب ضريبة الخصم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f6ab1-108">لن يتم حساب ضريبة الخصم في حالة عدم تبديل **حساب ضريبة الخصم** لهذا المورد في البيانات.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="f6ab1-109">حدد مجموعة ضريبة الخصم في **مجموعة ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="f6ab1-110">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-110">Click **Save**.</span></span>

<span data-ttu-id="f6ab1-111">بالنسبة للأصناف/الخدمات الخاضعة لضريبة الخصم، يمكنك تعيين **مجموعة ضريبة خصم الصنف** الافتراضية في **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="f6ab1-112">‏‫انتقل إلى ‬**جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .</span><span class="sxs-lookup"><span data-stu-id="f6ab1-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="f6ab1-113">انقر فوق رقم الصنف الخاص، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="f6ab1-114">في علامة التبويب **الشراء**، انقر فوق **حساب ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="f6ab1-115">لن يتم حساب ضريبة الخصم في حالة عدم تعيين **حساب ضريبة الخصم** إلى **نعم** لهذا الصنف في علامة تبويب **الشراء** في صفحة **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="f6ab1-116">حدد مجموعة ضريبة خصم الصنف في قائمة **مجموعة ضريبة خصم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="f6ab1-117">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-117">Click **Save**.</span></span>

<span data-ttu-id="f6ab1-118">يمكن تعيين مجموعات ضريبة الخصم ومجموعات ضريبة خصم الصنف في الصفحات:</span><span class="sxs-lookup"><span data-stu-id="f6ab1-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="f6ab1-119">**أمر الشراء**</span><span class="sxs-lookup"><span data-stu-id="f6ab1-119">**Purchase order**</span></span>
- <span data-ttu-id="f6ab1-120">**فاتورة المورد**</span><span class="sxs-lookup"><span data-stu-id="f6ab1-120">**Vendor invoice**</span></span>
- <span data-ttu-id="f6ab1-121">**دفتر يومية الفواتير**</span><span class="sxs-lookup"><span data-stu-id="f6ab1-121">**Invoice journal**</span></span>

<span data-ttu-id="f6ab1-122">سيتم تحويل مجموعة ضريبة الخصم الافتراضية ومجموعة ضريبة خصم الصنف إلى البنود عند إنشاء **أوامر الشراء** و/أو **فواتير المورد المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="f6ab1-123">بالنسبة **لدفتر يومية فواتير المورد**، يمكنك تشغيل **حساب ضريبة الخصم** وتحديد **مجموعة ضرائب خصم الصنف** في علامة التبويب **عام** في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="f6ab1-124">يتوفر المبلغ المؤقت لضريبة الخصم في الحقل **ضريبة الخصم المعدلة** في علامة التبويب **الإجماليات** في صفحة **أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![تضمين ضريبة الخصم في أمر الشراء](media/withholding-tax-adjusted.png)

<span data-ttu-id="f6ab1-126">يتم حساب ضريبة الخصم في **دفتر يومية مدفوعات المورد**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="f6ab1-127">يمكنك تعديل أكواد ضريبة الخصم القابلة للتطبيق يدويًا بالإضافة إلى مبالغ ضريبة الخصم الفعلية في علامة التبويب **ضريبة الخصم** في صفحة **تسوية الحركات**.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![يمكن تعديل الخصم يدويًا في صفحة تسوية الحركات](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="f6ab1-129">سيتم خصم مبلغ ضريبة الخصم المشتقة من دفع المورد وترحيله إلى **حساب ضريبة الخصم** في إيصال متعلق.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![حساب ضريبة الخصم يُظهر إيصالا متعلقًا](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]