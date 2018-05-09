--- 
title: "إنشاء دفع ضريبة مبيعات"
description: "تعمل وظيفة \"تسوية ضريبة المبيعات وترحيلها‬\" على تسوية أرصدة ضريبة المبيعات على حسابات ضريبة المبيعات وتعويضها في حساب تسوية ضريبة المبيعات لفترة معينة."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 28d4b38ea2efeff5ada787e8a74b85037e6a78af
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="45ae5-103">إنشاء دفع ضريبة مبيعات</span><span class="sxs-lookup"><span data-stu-id="45ae5-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45ae5-104">تعمل وظيفة "تسوية ضريبة المبيعات وترحيلها‬" على تسوية أرصدة ضريبة المبيعات على حسابات ضريبة المبيعات وتعويضها في حساب تسوية ضريبة المبيعات لفترة معينة.</span><span class="sxs-lookup"><span data-stu-id="45ae5-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="45ae5-105">انتقل إلى الضريبة > إقرارات > ضريبة المبيعات > تسوية ضريبة المبيعات وترحيلها‬‬.</span><span class="sxs-lookup"><span data-stu-id="45ae5-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="45ae5-106">في الحقل "فترة التسوية"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="45ae5-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="45ae5-107">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="45ae5-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="45ae5-108">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="45ae5-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="45ae5-109">إذا لم يكن الخيار "تضمين التصحيحات‬" محددًا على صفحة محددات دفتر الأستاذ العام، فيمكن معالجة التسوية لإصدارات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="45ae5-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="45ae5-110">الإصدار الأصلي هو التسوية الأولى لفترة زمنية ولا يمكن معالجته إلا مرة واحدة لفترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="45ae5-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="45ae5-111">ستقوم أحدث التصحيحات بتسوية حركات ضريبة المبيعات التي تم ترحيلها بعد إنشاء الإصدار الأصلي.</span><span class="sxs-lookup"><span data-stu-id="45ae5-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="45ae5-112">في حقل "‏‫تاريخ الحركة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="45ae5-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="45ae5-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45ae5-113">Click OK.</span></span>


