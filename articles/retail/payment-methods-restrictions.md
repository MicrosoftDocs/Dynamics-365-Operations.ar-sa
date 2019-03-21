---
title: تقييد طرق الدفع للمرتجعات من دون إيصال
description: يصف هذا الموضوع كيف يمكن تقييد بعض أنواع الدفع لتلقي المبالغ المستردة إذا تم إجراء عمليات الإرجاع من دون إيصال.
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/05/2019
ms.locfileid: "777167"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="426ca-103">تقييد طرق الدفع للمرتجعات من دون إيصال</span><span class="sxs-lookup"><span data-stu-id="426ca-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="426ca-104">يجب أن يتم تكوين كل نوع دفع يقبله بائع التجزئة عند إعداد النظام.</span><span class="sxs-lookup"><span data-stu-id="426ca-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="426ca-105">يصف هذا الموضوع كيف يمكن تقييد بعض أنواع الدفع لتلقي المبالغ المستردة إذا تم إجراء عمليات الإرجاع من دون إيصال.</span><span class="sxs-lookup"><span data-stu-id="426ca-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="426ca-106">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="426ca-106">Set up payment methods</span></span>

<span data-ttu-id="426ca-107">لإعداد طرق الدفع، يجب إكمال المهام التالية.</span><span class="sxs-lookup"><span data-stu-id="426ca-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="426ca-108">أنشئ طرق الدفع التي تم قبولها من قِبل المؤسسة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="426ca-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="426ca-109">‏‫أنشئ أنواع البطاقات وأرقام البطاقات على مستوى المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="426ca-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="426ca-110">وإذا تم قبول بطاقات الدائن أو بطاقات المدين، فيجب إنشاء طريقة دفع واحدة للبطاقات، ثم إنشاء أنواع البطاقات وأرقام البطاقات على مستوى المؤسسة.‬</span><span class="sxs-lookup"><span data-stu-id="426ca-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="426ca-111">قم بإعداد طرق الدفع في المتجر.</span><span class="sxs-lookup"><span data-stu-id="426ca-111">Set up store payment methods.</span></span> <span data-ttu-id="426ca-112">اربط طرق الدفع بكل متجر، ثم قم بإدخال الإعدادات الخاصة بالمتجر لكل طريقة دفع.</span><span class="sxs-lookup"><span data-stu-id="426ca-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="426ca-113">‏‫قم بإعداد طرق الدفع للمتاجر.</span><span class="sxs-lookup"><span data-stu-id="426ca-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="426ca-114">وللحصول على أيٍّ من طرق الدفع بالبطاقة التي يقبلها المتجر، استكمل إعداد البطاقة.‬</span><span class="sxs-lookup"><span data-stu-id="426ca-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="426ca-115">![إعداد متجر البيع بالتجزئة](media/NoReceiptReturns1.png "إعداد متجر البيع بالتجزئة")</span><span class="sxs-lookup"><span data-stu-id="426ca-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="426ca-116">تقييد طرق الدفع للمرتجعات من دون إيصال</span><span class="sxs-lookup"><span data-stu-id="426ca-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="426ca-117">لكل طريقة دفع في المتجر، في صفحة **إدارة متجر البيع بالتجزئة**، ضمن **مرتجعات من دون إيصال**، عيّن الخيار **تقييد المبالغ المستردة من دون إيصال** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="426ca-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="426ca-118">القيمة الافتراضية لمفتاح التبديل هي **لا**، مما يضمن السماح لطريقة الدفع باسترداد المبلغ المدفوع.</span><span class="sxs-lookup"><span data-stu-id="426ca-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="426ca-119">عند تعيين الخيار **تقييد المبالغ المستردة من دون إيصال** إلى **نعم**، لن يُسمح لطريقة الدفع باسترداد المبلغ المدفوع.</span><span class="sxs-lookup"><span data-stu-id="426ca-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="426ca-120">![طريقة الدفع في متجر البيع بالتجزئة](media/NoReceiptReturns3.png "طريقة الدفع في متجر البيع بالتجزئة")</span><span class="sxs-lookup"><span data-stu-id="426ca-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="426ca-121">عندما يحدد أمين الصندوق طريقة دفع تم فيها تقييد المبالغ المستردة من دون إيصال، تظهر رسالة للتحقق من طرق الدفع المقبولة.</span><span class="sxs-lookup"><span data-stu-id="426ca-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="426ca-122">![طرق الدفع المقبولة](media/NoReceiptReturns4.png "طرق الدفع المقبولة")</span><span class="sxs-lookup"><span data-stu-id="426ca-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="426ca-123">إذا تضمنت حركة ما عملية إرجاع مع إيصال وعملية إرجاع من دون إيصال، فلن تُفرض شروط التقييد لأن الحركة ستكون عبارة عن سير عمل إرجاع مع إيصال.</span><span class="sxs-lookup"><span data-stu-id="426ca-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

