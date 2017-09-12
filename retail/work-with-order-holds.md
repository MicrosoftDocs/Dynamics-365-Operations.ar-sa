---
title: "تعليقات الأمر"
description: "يصف هذا الموضوع تعليقات الأوامر باستخدام Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="order-holds"></a><span data-ttu-id="bad71-103">تعليقات الأمر</span><span class="sxs-lookup"><span data-stu-id="bad71-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bad71-104">يصف هذا الموضوع تعليقات الأوامر باستخدام Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="bad71-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="bad71-105">يمكن وضع أمر قيد الانتظار لأسباب مختلفة.</span><span class="sxs-lookup"><span data-stu-id="bad71-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="bad71-106">على سبيل المثال، قد تضع أمر قيد الانتظار حتى يمكن التحقق من أسلوب الدفع أو عنوان عميل أو حتى يقوم مدير بمراجعة حد الائتمان الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="bad71-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="bad71-107">أثناء عملية المبيعات، هناك أوقات يجب عندها وضع أوامر المبيعات قيد الانتظار.</span><span class="sxs-lookup"><span data-stu-id="bad71-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="bad71-108">على سبيل المثال، قد يتم وضع أمر المبيعات قيد الانتظار بسبب مشاكل في دفع عميل، بسبب احتيال مشكوك فيه أو لأنه يجب على المدير مراجعة الأمر.</span><span class="sxs-lookup"><span data-stu-id="bad71-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="bad71-109">عندما يتم وضع أمر المبيعات قيد الانتظار، يتم تعيين رمز تعليق لأمر إلى أمر المبيعات للإشارة إلى سبب التعليق.</span><span class="sxs-lookup"><span data-stu-id="bad71-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="bad71-110">يتم تكوين رموز تعليق أمر المبيعات في **المبيعات والتسويق** &gt; **الإعداد** &gt; **أوامر المبيعات** &gt; **رموز تعليقات الأمر**.</span><span class="sxs-lookup"><span data-stu-id="bad71-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="bad71-111">ويمكن وضع أمر مبيعات قيد الانتظار يدوياً في وقت إنشاء الأمر أو لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="bad71-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="bad71-112">بالإضافة إلى ذلك، يمكن وضع أمر قيد الانتظار تلقائياً، وفقًا لقواعد الاحتيال.</span><span class="sxs-lookup"><span data-stu-id="bad71-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="bad71-113">وأثناء وضع أمر مبيعات قيد الانتظار، قد تحتاج إلى تحديثه بمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="bad71-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="bad71-114">وبدلاً من ذلك، قد تحتاج إلى التحقق من أمر المبيعات عند مواصلة العمل فيه.</span><span class="sxs-lookup"><span data-stu-id="bad71-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="bad71-115">ويمكنك سحب أمر مبيعات، وإدراجه مرة أخرى، وحتى تجاوز سحب مستخدم آخر باستخدام منضدة تعليق الأوامر (**البيع بالتجزئة** &gt; **العملاء‏‎** &gt; **تعليقات الأمر**).</span><span class="sxs-lookup"><span data-stu-id="bad71-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="bad71-116">عندما يكون أمر ما جاهز للاكتمال، يجب إزالة الوضع قيد الانتظار قبل إتمام عملية الأمر.</span><span class="sxs-lookup"><span data-stu-id="bad71-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




