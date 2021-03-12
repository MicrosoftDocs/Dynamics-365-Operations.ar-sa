---
title: " تكوينات الدفع لكشوف حساب Retail"
description: يوضح هذا الإجراء تكوينات لطرق الدفع في متاجر Commerce، والتي تؤثر على كيفية إنشاء كشوفات الحساب وترحيلها.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b1fc042bff4d801ae893b0370b67cd8e11ba95f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982298"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="3a1ca-103"> تكوينات الدفع لكشوف حساب Retail</span><span class="sxs-lookup"><span data-stu-id="3a1ca-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a1ca-104">يوضح هذا الإجراء تكوينات لطرق الدفع في متاجر Commerce، والتي تؤثر على كيفية إنشاء كشوفات الحساب وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="3a1ca-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="3a1ca-106">انتقل إلى Retail and Commerce > القنوات > المتاجر > جميع المتاجر.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="3a1ca-107">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3a1ca-108">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3a1ca-109">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="3a1ca-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="3a1ca-110">انقر فوق طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-110">Click Payment methods.</span></span>
6. <span data-ttu-id="3a1ca-111">قم بتوسيع قسم الترحيل أو طيه.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="3a1ca-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="3a1ca-112">Click Edit.</span></span>
    * <span data-ttu-id="3a1ca-113">حدد ما إذا كان ينبغي ترحيل المبالغ المستلمة لطريقة الدفع هذه لحساب دفتر الأستاذ أو حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="3a1ca-114">حدد الحساب الذي ينبغي ترحيل المبالغ المستلمة لطريقة الدفع هذه له.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="3a1ca-115">حدد حسابًا لترحيل الاختلافات المحتملة بين ‏‫إجمالي مبلغ الحركة المستلم والمبلغ المحتسب لطريقة الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="3a1ca-116">في هذا الحقل، يمكنك إدخال مبلغ للتحكم في التوقيت الذي ينبغي فيه ترحيل مبلغ الفرق إلى حساب فرق آخر.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="3a1ca-117">يمكنك استخدام هذا لتعقب الاختلافات الكبيرة.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="3a1ca-118">حدد حسابًا لترحيل الاختلافات المحتملة بين إجمالي مبلغ الحركة المستلم والمبلغ المحتسب، عندما يتجاوز القيمة المحددة في حقل "الحد الأقصى لمبلغ الفرق".</span><span class="sxs-lookup"><span data-stu-id="3a1ca-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="3a1ca-119">حدد "نعم" لترحيل مبالغ الإيداع البنكي إلى حساب منفصل.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="3a1ca-120">في هذا الحقل، يمكنك تحديد ما إذا كان ينبغي ترحيل مبالغ الإيداع البنكي إلى حساب دفتر الأستاذ أو حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="3a1ca-121">حدد الحساب لترحيل مبالغ الإيداع البنكي إليه.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="3a1ca-122">حدد نوع الحركة البنكية المراد استخدامها عند ترحيل مبالغ الإيداع البنكي للحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="3a1ca-123">حدد "نعم" لترحيل مبالغ الإيداع بالخزينة إلى حساب منفصل.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="3a1ca-124">حدد ما إذا كان ينبغي ترحيل مبالغ الإيداع بالخزينة إلى حساب دفتر الأستاذ أو الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="3a1ca-125">حدد الحساب الذي سيتم ترحيل مبالغ الإيداع بالخزينة إليه.</span><span class="sxs-lookup"><span data-stu-id="3a1ca-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="3a1ca-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3a1ca-126">Click Save.</span></span>

