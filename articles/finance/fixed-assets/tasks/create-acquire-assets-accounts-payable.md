---
title: إنشاء والحصول على الأصول من الحسابات الدائنة
description: سينقلك دليل المهمة هذا عبر عملية إنشاء أصل ثابت والاستحواذ عليه بواسطة عملية الشراء.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b27ccc3b4c4f5470d3a5b8ed7347e269c6793b87
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976031"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="d0f46-103">إنشاء والحصول على الأصول من الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="d0f46-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0f46-104">سينقلك دليل المهمة هذا عبر عملية إنشاء أصل ثابت والاستحواذ عليه بواسطة عملية الشراء.</span><span class="sxs-lookup"><span data-stu-id="d0f46-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="d0f46-105">إنه يستخدم دور المحاسب وموظفي الحسابات الدائنة وشركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d0f46-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="d0f46-106">تعيين محددات الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="d0f46-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="d0f46-107">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الإعداد > محددات الأصول الثابتة‬**‬.</span><span class="sxs-lookup"><span data-stu-id="d0f46-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="d0f46-108">قم بتوسيع علامة التبويب السريعة **أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="d0f46-109">حدد خانة الاختيار **السماح بالحصول على الأصل من الشراء‬**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="d0f46-110">حدد خانة الاختيار **إنشاء أصل أثناء ترحيل إيصال استلام المنتجات أو الفاتورة‬**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="d0f46-111">إنشاء فاتورة مورّد جديدة</span><span class="sxs-lookup"><span data-stu-id="d0f46-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="d0f46-112">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > مساحات العمل > إدخال فاتورة المورّد**‬.</span><span class="sxs-lookup"><span data-stu-id="d0f46-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="d0f46-113">انقر فوق **فاتورة مورّد جديدة**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="d0f46-114">في الحقل **حساب الفاتورة**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d0f46-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d0f46-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d0f46-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d0f46-116">في حقل **الرقم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d0f46-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="d0f46-117">في الحقل **تاريخ الترحيل**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="d0f46-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="d0f46-118">انقر فوق **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-118">Click **Add line**.</span></span>
8. <span data-ttu-id="d0f46-119">في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d0f46-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="d0f46-120">يمكن استخدام الأصناف غير المخزنة أو فئات التدبير للاستحواذ على الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="d0f46-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="d0f46-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d0f46-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d0f46-122">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d0f46-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="d0f46-123">سينشئ بند فاتورة واحد أصلاً ثابتًا واحدًا فقط، بغض النظر عن الكمية.</span><span class="sxs-lookup"><span data-stu-id="d0f46-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="d0f46-124">سيتم نقل قيمة حقل كمية الفاتورة إلى كمية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="d0f46-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="d0f46-125">في حقل **سعر الوحدة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d0f46-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="d0f46-126">قم بتوسيع علامة التبويب السريعة **تفاصيل البند**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="d0f46-127">انقر فوق علامة التبويب **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="d0f46-128">حدد خانة الاختيار **إنشاء أصل ثابت جديد‬**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="d0f46-129">في الحقل **مجموعة الأصول الثابتة‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d0f46-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d0f46-130">في القائمة، حدد مجموعة الأصول الثابتة التي سيتم استخدامها عند إنشاء الأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="d0f46-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="d0f46-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d0f46-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d0f46-132">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="d0f46-132">Click **Post**.</span></span> <span data-ttu-id="d0f46-133">سيتم إنشاء الأصل الثابت والاستحواذ عليه عند ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d0f46-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

