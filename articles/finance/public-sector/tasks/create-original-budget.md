---
title: إنشاء موازنة أصلية ثم إلغاء إدخالات الموازنة الأولية في القطاع العام
description: عند إنشاء إدخال موازنة أصلية واستخدام قيم البعد ونموذج الموازنة التي تتضمن مبالغ الموازنة الأولية، يمكن إلغاء مبالغ الموازنة الأولية.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32d89216d49a743729de8910f738276cbddcd8bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440040"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="1d033-103">إنشاء موازنة أصلية ثم إلغاء إدخالات الموازنة الأولية في القطاع العام</span><span class="sxs-lookup"><span data-stu-id="1d033-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d033-104">عند إنشاء إدخال موازنة أصلية واستخدام قيم البعد ونموذج الموازنة التي تتضمن مبالغ الموازنة الأولية، يمكن إلغاء مبالغ الموازنة الأولية.</span><span class="sxs-lookup"><span data-stu-id="1d033-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="1d033-105">تم إنشاء هذا الإجراء باستخدام شركة بيانات العرض التوضيحي PSUS في قسم القطاع العام.</span><span class="sxs-lookup"><span data-stu-id="1d033-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="1d033-106">انتقل إلى إعداد الموازنة > إدخالات سجل الموازنة.</span><span class="sxs-lookup"><span data-stu-id="1d033-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="1d033-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1d033-107">Click New.</span></span>
3. <span data-ttu-id="1d033-108">في حقل "‏‫نموذج الموازنة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d033-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1d033-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d033-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1d033-110">في حقل "‏‫كود الموازنة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d033-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1d033-111">في القائمة، انقر فوق "الموازنة الأصلية".</span><span class="sxs-lookup"><span data-stu-id="1d033-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="1d033-112">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="1d033-112">Click Save.</span></span>
8. <span data-ttu-id="1d033-113">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="1d033-113">Click Add line.</span></span>
9. <span data-ttu-id="1d033-114">اختياري: إذا أردت تغيير التاريخ الموجود في رأس الصفحة، أدخل تاريخًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="1d033-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="1d033-115">يحدد هذا التاريخ الفترة المالية التي سيتم تسجيل الموازنة بها.</span><span class="sxs-lookup"><span data-stu-id="1d033-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="1d033-116">في الحقل "بنية الحساب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d033-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="1d033-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d033-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="1d033-118">في حقل "‏‫قيم الأبعاد‬"، حدد القيم المرغوب فيها.</span><span class="sxs-lookup"><span data-stu-id="1d033-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="1d033-119">في حقل "المبلغ"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1d033-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="1d033-120">في الحقل "العملة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d033-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="1d033-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d033-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="1d033-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1d033-122">Click Save.</span></span>
17. <span data-ttu-id="1d033-123">انقر فوق تحديث أرصدة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="1d033-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="1d033-124">اختياري: يمكنك تحديد خيار "إلغاء الموازنة الأولية".</span><span class="sxs-lookup"><span data-stu-id="1d033-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="1d033-125">لاحظ أنه يمكنك إلغاء كافة إدخالات الموازنة الأولية، أو إدخالات الموازنة الأولية التي لها رمز موازنة تحدده فقط.</span><span class="sxs-lookup"><span data-stu-id="1d033-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="1d033-126">لإجراء تحديدات الاختيارية، انقر فوق رمز "إلغاء التأمين" أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1d033-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="1d033-127">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="1d033-127">Click Update.</span></span>

