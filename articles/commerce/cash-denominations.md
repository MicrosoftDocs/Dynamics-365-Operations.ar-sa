---
title: تكوين الفئات النقدية‬ لنقطة البيع (POS)
description: يمكن تكوين فئات العملة‬ للأوراق النقدية والعملات المعدنية في مكتب الخدمة لكي يتم استخدامها من قِبل موظفي الكاشير وشركاء المبيعات‬ والمدراء في المتجر من خلال نقطة البيع.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e3a5f9a73bdee50e3e7c68125144c3b43305efa8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961549"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="b1f0c-103">تكوين الفئات النقدية‬ لنقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="b1f0c-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1f0c-104">يمكن تكوين فئات العملة‬ للأوراق النقدية والعملات المعدنية في مكتب الخدمة لكي يتم استخدامها من قِبل موظفي الكاشير وشركاء المبيعات‬ والمدراء في المتجر من خلال نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="b1f0c-105">يمكن استخدام هذه الفئات للمساعدة في حساب النقدية لإقرارات الدفع في نهاية اليوم أو تحديد دفع عملية بيع بسرعة.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="b1f0c-106">تحديد فئات العملة</span><span class="sxs-lookup"><span data-stu-id="b1f0c-106">Define denominations</span></span>

<span data-ttu-id="b1f0c-107">يتم إعداد فئات الأوراق النقدية لكل متجر في الخيار **إعداد** \> **خيار إقرار النقدية‬** من ثصفحة موقع المتجر.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![خيار إقرار النقدية](./media/image1-denomination.png)

<span data-ttu-id="b1f0c-109">لتحديد فئة عملة:</span><span class="sxs-lookup"><span data-stu-id="b1f0c-109">To define a denomination:</span></span>

1. <span data-ttu-id="b1f0c-110">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-110">Click **New**.</span></span>
1. <span data-ttu-id="b1f0c-111">حدد النوع (نقود معدنية أو عملات ورقية).</span><span class="sxs-lookup"><span data-stu-id="b1f0c-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="b1f0c-112">حدد المبلغ (القيمة).</span><span class="sxs-lookup"><span data-stu-id="b1f0c-112">Specify the amount (value).</span></span>

![صفحة فئات إقرار النقدية](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="b1f0c-114">تكوين ملف تعريف الوظائف</span><span class="sxs-lookup"><span data-stu-id="b1f0c-114">Configure the functionality profile</span></span>

<span data-ttu-id="b1f0c-115">عند الدفع نقدًا في نقطة البيع، يمكن للمستخدم استخدام فئات الأوراق النقدية لإدخال المبلغ المدفوع من قبل العميل بسرعة.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="b1f0c-116">في ملف تعريف الوظائف، يمكنك تكوين خيارين لإظهار الفئة في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="b1f0c-117">**أكبر من أو يساوي المبلغ المستحق** – بشكل افتراضي، سوف تعرض نقطة البيع فقط فئات الأوراق النقدية الأكبر من المبلغ المستحق، مما يسمح بالدفع بلمسة واحدة.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="b1f0c-118">على سبيل المثال، إذا كان المبلغ المستحق 7.50 دولار، فستعرض نقطة البيع الفئات التالية: 10 دولارات و20 دولارًا و50 دولارًا و100 دولار.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="b1f0c-119">سيؤدي لمس أي واحد من هذه المبالغ إلى دفع قيمة البيع بهذا المبلغ.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="b1f0c-120">لا تظهر الأوراق النقدية من دولار وخمس دولارات لأن هذه المبالغ هي أقل من المبلغ المستحق.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="b1f0c-121">**جميع الفئات** – حدد هذا الخيار لإظهار دومًا كافة فئات الأوراق النقدية في نقطة البيع، بغض النظر عن المبلغ المستحق.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="b1f0c-122">وهذا يعني أنه باستطاعة المستخدم استخدام مجموعة من الأوراق النقدية للوصول إلى المبلغ المستحق.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="b1f0c-123">على سبيل المثال، إذا كان المبلغ المستحق 25 دولارًا، يستطيع المستخدم اختيار 20 دولارًا و5 دولارات لإكمال عملية البيع.</span><span class="sxs-lookup"><span data-stu-id="b1f0c-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
