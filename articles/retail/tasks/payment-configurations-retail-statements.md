--- 
title: " تكوينات الدفع لكشوف حساب Retail"
description: "يوضح هذا الإجراء تكوينات لطرق الدفع في متاجر البيع بالتجزئة، والتي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f12d8ac9be11b92eaef4acce094ae183906278d4
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="b1820-103"> تكوينات الدفع لكشوف حساب Retail</span><span class="sxs-lookup"><span data-stu-id="b1820-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b1820-104">يوضح هذا الإجراء تكوينات لطرق الدفع في متاجر البيع بالتجزئة، والتي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="b1820-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="b1820-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="b1820-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="b1820-106">انتقل إلى البيع بالتجزئة والتجارة > القنوات > متاجر البيع بالتجزئة > جميع متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="b1820-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="b1820-107">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b1820-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b1820-108">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b1820-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b1820-109">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="b1820-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="b1820-110">انقر فوق طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="b1820-110">Click Payment methods.</span></span>
6. <span data-ttu-id="b1820-111">قم بتوسيع قسم الترحيل أو طيه.</span><span class="sxs-lookup"><span data-stu-id="b1820-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="b1820-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b1820-112">Click Edit.</span></span>
    * <span data-ttu-id="b1820-113">حدد ما إذا كان ينبغي ترحيل المبالغ المستلمة لطريقة الدفع هذه لحساب دفتر الأستاذ أو حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="b1820-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="b1820-114">حدد الحساب الذي ينبغي ترحيل المبالغ المستلمة لطريقة الدفع هذه له.</span><span class="sxs-lookup"><span data-stu-id="b1820-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="b1820-115">حدد حسابًا لترحيل الاختلافات المحتملة بين ‏‫إجمالي مبلغ الحركة المستلم والمبلغ المحتسب لطريقة الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="b1820-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="b1820-116">في هذا الحقل، يمكنك إدخال مبلغ للتحكم في التوقيت الذي ينبغي فيه ترحيل مبلغ الفرق إلى حساب فرق آخر.</span><span class="sxs-lookup"><span data-stu-id="b1820-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="b1820-117">يمكنك استخدام هذا لتعقب الاختلافات الكبيرة.</span><span class="sxs-lookup"><span data-stu-id="b1820-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="b1820-118">حدد حسابًا لترحيل الاختلافات المحتملة بين إجمالي مبلغ الحركة المستلم والمبلغ المحتسب، عندما يتجاوز القيمة المحددة في حقل "الحد الأقصى لمبلغ الفرق".</span><span class="sxs-lookup"><span data-stu-id="b1820-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="b1820-119">حدد "نعم" لترحيل مبالغ الإيداع البنكي إلى حساب منفصل.</span><span class="sxs-lookup"><span data-stu-id="b1820-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="b1820-120">في هذا الحقل، يمكنك تحديد ما إذا كان ينبغي ترحيل مبالغ الإيداع البنكي إلى حساب دفتر الأستاذ أو حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="b1820-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="b1820-121">حدد الحساب لترحيل مبالغ الإيداع البنكي إليه.</span><span class="sxs-lookup"><span data-stu-id="b1820-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="b1820-122">حدد نوع الحركة البنكية المراد استخدامها عند ترحيل مبالغ الإيداع البنكي للحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="b1820-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="b1820-123">حدد "نعم" لترحيل مبالغ الإيداع بالخزينة إلى حساب منفصل.</span><span class="sxs-lookup"><span data-stu-id="b1820-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="b1820-124">حدد ما إذا كان ينبغي ترحيل مبالغ الإيداع بالخزينة إلى حساب دفتر الأستاذ أو الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="b1820-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="b1820-125">حدد الحساب الذي سيتم ترحيل مبالغ الإيداع بالخزينة إليه.</span><span class="sxs-lookup"><span data-stu-id="b1820-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="b1820-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b1820-126">Click Save.</span></span>

