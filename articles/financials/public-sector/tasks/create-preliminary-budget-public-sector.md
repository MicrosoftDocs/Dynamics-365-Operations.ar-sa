--- 
title: "إنشاء موازنة أولية للقطاع العام"
description: "يمكنك إنشاء إدخالات سجل موازنة أولية لقيم البعد ونموذج موازنة محدد."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 98968b0025ff5c3b9723dc6cc8a8eae799a4eb43
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="cd203-103">إنشاء موازنة أولية للقطاع العام</span><span class="sxs-lookup"><span data-stu-id="cd203-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd203-104">يمكنك إنشاء إدخالات سجل موازنة أولية لقيم البعد ونموذج موازنة محدد.</span><span class="sxs-lookup"><span data-stu-id="cd203-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="cd203-105">وبعد الموافقة على الموازنة الفعلية، يمكنك إنشاء إدخالات سجل الموازنة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="cd203-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="cd203-106">تم إنشاء هذا الإجراء باستخدام شركة بيانات العرض التوضيحي PSUS في قسم القطاع العام.</span><span class="sxs-lookup"><span data-stu-id="cd203-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="cd203-107">انتقل إلى إعداد الموازنة > إدخالات سجل الموازنة.</span><span class="sxs-lookup"><span data-stu-id="cd203-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="cd203-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cd203-108">Click New.</span></span>
3. <span data-ttu-id="cd203-109">في حقل "‏‫نموذج الموازنة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cd203-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cd203-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cd203-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cd203-111">في حقل "‏‫كود الموازنة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cd203-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="cd203-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cd203-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cd203-113">في الحقل "‏‫كود السبب‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cd203-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cd203-114">في القائمة، انقر فوق السجل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="cd203-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="cd203-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cd203-115">Click Save.</span></span>
10. <span data-ttu-id="cd203-116">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="cd203-116">Click Add line.</span></span>
    * <span data-ttu-id="cd203-117">اختياري: إذا أردت تغيير التاريخ الموجود في رأس الصفحة، أدخل تاريخًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="cd203-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="cd203-118">يحدد هذا التاريخ الفترة المالية التي سيتم تسجيل الموازنة بها.</span><span class="sxs-lookup"><span data-stu-id="cd203-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="cd203-119">عند عرض دليل المهمة، ولتعبئة الحقول الأخرى، انقر فوق "إلغاء التأمين" في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd203-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="cd203-120">في الحقل "بنية الحساب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cd203-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="cd203-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cd203-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="cd203-122">في حقل "‏‫قيم الأبعاد‬"، حدد القيم المرغوب فيها.</span><span class="sxs-lookup"><span data-stu-id="cd203-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="cd203-123">في حقل "المبلغ"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cd203-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="cd203-124">يمكنك أيضًا إدخال نوع المبلغ.</span><span class="sxs-lookup"><span data-stu-id="cd203-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="cd203-125">في الحقل "العملة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cd203-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="cd203-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cd203-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="cd203-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cd203-127">Click Save.</span></span>
18. <span data-ttu-id="cd203-128">انقر فوق تحديث أرصدة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="cd203-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="cd203-129">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="cd203-129">Click Update.</span></span>
    * <span data-ttu-id="cd203-130">للاطلاع على نتائج التحديث، انقر فوق "تفاصيل الرسالة" على الشريط الأزرق.</span><span class="sxs-lookup"><span data-stu-id="cd203-130">To see the results of the update, click Message details on the blue bar.</span></span>  


