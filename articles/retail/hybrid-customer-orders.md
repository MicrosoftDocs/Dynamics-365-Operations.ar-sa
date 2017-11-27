---
title: "أوامر العملاء المختلطة"
description: "أمر العميل المختلط هو أمر واحد يحتوي على المنتجات التي يمكن تلبيتها من المتجر للعميل، بالإضافة إلى المنتجات التي سيتم انتقاؤها أو شحنها لاحقاً."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed5d403c1321e2573df38d60956e6f89282b3de8
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="hybrid-customer-orders"></a><span data-ttu-id="20dbf-103">أوامر العملاء المختلطة</span><span class="sxs-lookup"><span data-stu-id="20dbf-103">Hybrid customer orders</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="20dbf-104">أمر العميل المختلط هو أمر واحد يحتوي على المنتجات التي يمكن تلبيتها من المتجر للعميل، بالإضافة إلى المنتجات التي سيتم انتقاؤها أو شحنها لاحقاً.</span><span class="sxs-lookup"><span data-stu-id="20dbf-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="20dbf-105">في Microsoft Dynamics 365 for Retail، يمكنك تحديد إما تلبية كافة المنتجات أو تلبية منتجات محددة من أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="20dbf-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="20dbf-106">تتم تلقائيًا فوترة بنود المنتجات التي يُوضع عليها علامة التنفيذ بعد إنشاء الأمر، وبالمثل يكون هذا هو الحال نفسه مع أمر مقرر انتقاؤه لتنفيذه بعد إنشاء الأمر.</span><span class="sxs-lookup"><span data-stu-id="20dbf-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="20dbf-107">يتحدد المبلغ المستحق للأوامر المختلطة عبر إضافة نسبة الوديعة على الانتقاء وشحن بنود المنتجات إلى المبلغ الكامل لتنفيذ البنود.</span><span class="sxs-lookup"><span data-stu-id="20dbf-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="20dbf-108">بالنسبة للأوامر المختلطة، يقوم النظام بالتبديل بين وضع أمر العميل ووضع الدفع والتسليم كما يلي:</span><span class="sxs-lookup"><span data-stu-id="20dbf-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

-   <span data-ttu-id="20dbf-109">إذا تم تعيين كافة المنتجات في السلة إلى **تنفيذ التسليم**، فسيتم التعامل مع الأمر كحركة دفع وتسليم.</span><span class="sxs-lookup"><span data-stu-id="20dbf-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
-   <span data-ttu-id="20dbf-110">إذا تم تعيين أي أو جميع البنود في السلة إما إلى **انتقاء** أو **شحن التسليم**، فسيتم التعامل مع الأمر كحركة أمر عميل.</span><span class="sxs-lookup"><span data-stu-id="20dbf-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="20dbf-111">إذا تم تحديد أحد بنود السلة وتم **تحديد الانتقاء** أو **تحديد الشحن** أو **تحديد التنفيذ**، فلن يتم تعيين غير بند السلة المحدد لطريقة التسليم هذه.</span><span class="sxs-lookup"><span data-stu-id="20dbf-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="20dbf-112">في هذه الحالة، يستمر تدفق المراحل النهائية من العملية كالمعتاد.</span><span class="sxs-lookup"><span data-stu-id="20dbf-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="20dbf-113">مع ذلك، إذا تم **تحديد الانتقاء** أو **تحديد الشحن** أو **تحديد التنفيذ** دون تحديد بند من السلة، فسيتم فتح صفحة جديدة تسرد كافة بنود السلة.</span><span class="sxs-lookup"><span data-stu-id="20dbf-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="20dbf-114">في هذه الشاشة، يمكنك تحديد بنود متعددة دفعة واحدة لتعيين طريقة التسليم.</span><span class="sxs-lookup"><span data-stu-id="20dbf-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="20dbf-115">عند استخدام هذه الطريقة لتحديد البنود، سيتم تجاوز أي طريقة تسليم سابقة تم تعيينها إلى البند.</span><span class="sxs-lookup"><span data-stu-id="20dbf-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

<a name="see-also"></a><span data-ttu-id="20dbf-116">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="20dbf-116">See also</span></span>
--------

[<span data-ttu-id="20dbf-117">نظرة عامة حول أوامر العميل</span><span class="sxs-lookup"><span data-stu-id="20dbf-117">Customer orders overview</span></span>](customer-orders-overview.md)




