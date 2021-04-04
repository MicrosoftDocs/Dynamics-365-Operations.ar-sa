---
title: تقييد طرق الدفع للمرتجعات من دون إيصال
description: يصف هذا الموضوع كيف يمكن تقييد بعض أنواع الدفع لتلقي المبالغ المستردة إذا تم إجراء عمليات الإرجاع من دون إيصال.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: fc087ea24ebbebd5acd1cf37fdfd5c9422d44be8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257039"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="6abfb-103">تقييد طرق الدفع للمرتجعات من دون إيصال</span><span class="sxs-lookup"><span data-stu-id="6abfb-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6abfb-104">يجب أن يتم تكوين كل نوع دفع يقبله بائع التجزئة عند إعداد النظام.</span><span class="sxs-lookup"><span data-stu-id="6abfb-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="6abfb-105">يصف هذا الموضوع كيف يمكن تقييد بعض أنواع الدفع لتلقي المبالغ المستردة إذا تم إجراء عمليات الإرجاع من دون إيصال.</span><span class="sxs-lookup"><span data-stu-id="6abfb-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="6abfb-106">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="6abfb-106">Set up payment methods</span></span>

<span data-ttu-id="6abfb-107">لإعداد طرق الدفع، يجب إكمال المهام التالية.</span><span class="sxs-lookup"><span data-stu-id="6abfb-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="6abfb-108">أنشئ طرق الدفع التي تم قبولها من قِبل المؤسسة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="6abfb-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="6abfb-109">‏‫أنشئ أنواع البطاقات وأرقام البطاقات على مستوى المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="6abfb-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="6abfb-110">وإذا تم قبول بطاقات الدائن أو بطاقات المدين، فيجب إنشاء طريقة دفع واحدة للبطاقات، ثم إنشاء أنواع البطاقات وأرقام البطاقات على مستوى المؤسسة.‬</span><span class="sxs-lookup"><span data-stu-id="6abfb-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="6abfb-111">قم بإعداد طرق الدفع في المتجر.</span><span class="sxs-lookup"><span data-stu-id="6abfb-111">Set up store payment methods.</span></span> <span data-ttu-id="6abfb-112">اربط طرق الدفع بكل متجر، ثم قم بإدخال الإعدادات الخاصة بالمتجر لكل طريقة دفع.</span><span class="sxs-lookup"><span data-stu-id="6abfb-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="6abfb-113">‏‫قم بإعداد طرق الدفع للمتاجر.</span><span class="sxs-lookup"><span data-stu-id="6abfb-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="6abfb-114">وللحصول على أيٍّ من طرق الدفع بالبطاقة التي يقبلها المتجر، استكمل إعداد البطاقة.‬</span><span class="sxs-lookup"><span data-stu-id="6abfb-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="6abfb-115">![إعداد المتجر](media/NoReceiptReturns1.png "إعداد متجر البيع بالتجزئة")</span><span class="sxs-lookup"><span data-stu-id="6abfb-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="6abfb-116">تقييد طرق الدفع للمرتجعات من دون إيصال</span><span class="sxs-lookup"><span data-stu-id="6abfb-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="6abfb-117">لكل طريقة دفع في المتجر، في صفحة **إدارة المتاجر**، ضمن **مرتجعات من دون إيصال**، عيّن الخيار **تقييد المبالغ المستردة من دون إيصال** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="6abfb-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="6abfb-118">القيمة الافتراضية لمفتاح التبديل هي **لا**، مما يضمن السماح لطريقة الدفع باسترداد المبلغ المدفوع.</span><span class="sxs-lookup"><span data-stu-id="6abfb-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="6abfb-119">عند تعيين الخيار **تقييد المبالغ المستردة من دون إيصال** إلى **نعم**، لن يُسمح لطريقة الدفع باسترداد المبلغ المدفوع.</span><span class="sxs-lookup"><span data-stu-id="6abfb-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="6abfb-120">![طريقة الدفع بالمتجر](media/NoReceiptReturns3.png "طريقة الدفع في متجر البيع بالتجزئة")</span><span class="sxs-lookup"><span data-stu-id="6abfb-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="6abfb-121">عندما يحدد أمين الصندوق طريقة دفع تم فيها تقييد المبالغ المستردة من دون إيصال، تظهر رسالة للتحقق من طرق الدفع المقبولة.</span><span class="sxs-lookup"><span data-stu-id="6abfb-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="6abfb-122">![طرق الدفع المقبولة](media/NoReceiptReturns4.png "طرق الدفع المقبولة")</span><span class="sxs-lookup"><span data-stu-id="6abfb-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="6abfb-123">إذا تضمنت حركة ما عملية إرجاع مع إيصال وعملية إرجاع من دون إيصال، فلن تُفرض شروط التقييد لأن الحركة ستكون عبارة عن سير عمل إرجاع مع إيصال.</span><span class="sxs-lookup"><span data-stu-id="6abfb-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]