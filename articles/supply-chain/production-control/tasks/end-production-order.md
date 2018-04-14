---
title: "إنهاء أمر إنتاج"
description: "يوضح هذا الإجراء كيفية إنهاء أمر إنتاج."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9cb20294e4abbccd0016e7188a2610796e75b26
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="end-a-production-order"></a><span data-ttu-id="3c880-103">إنهاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="3c880-103">End a production order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c880-104">يوضح هذا الإجراء كيفية إنهاء أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="3c880-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="3c880-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="3c880-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3c880-106">هذا هو الإجراء النهائي من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3c880-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="3c880-107">إنهاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="3c880-107">End a production order</span></span>
1. <span data-ttu-id="3c880-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3c880-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3c880-109">حدد أمر إنتاج يكون في الحالة "تم الإبلاغ عنه كمنتهٍ".</span><span class="sxs-lookup"><span data-stu-id="3c880-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="3c880-110">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="3c880-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3c880-111">انقر فوق "إنهاء".</span><span class="sxs-lookup"><span data-stu-id="3c880-111">Click End.</span></span>
    * <span data-ttu-id="3c880-112">في هذه الصفحة، يمكنك تأكيد رغبتك في إنهاء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3c880-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="3c880-113">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="3c880-113">Click the General tab.</span></span>
5. <span data-ttu-id="3c880-114">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3c880-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="3c880-115">في الحقل "أسلوب الخردة"، حدد "تخصيص".</span><span class="sxs-lookup"><span data-stu-id="3c880-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="3c880-116">عند تحديد طريقة التخصيص، تتم إضافة التكاليف من مواد الخردة إلى البضائع المنتهية.</span><span class="sxs-lookup"><span data-stu-id="3c880-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="3c880-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3c880-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="3c880-118">التحقق من صحة نتائج الحساب</span><span class="sxs-lookup"><span data-stu-id="3c880-118">Validate calculation results</span></span>
1. <span data-ttu-id="3c880-119">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="3c880-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="3c880-120">انقر فوق "عرض مقارنة التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3c880-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="3c880-121">بعد إنهاء أمر الإنتاج، يمكنك مقارنة سعر التكلفة المقدر مقابل سعر التكلفة المحقق للحصول على نظرة عامة حول نسب الفرق في الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3c880-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  

