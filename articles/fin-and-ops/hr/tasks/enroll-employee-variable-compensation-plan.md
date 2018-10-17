--- 
title: "تسجيل موظف في خطة التعويض المتغيرة"
description: "بإمكان مدير التعويضات والميزات‬ تسجيل الموظفين في خطط التعويض المتغيرة لحساب المكافآت النقدية وغير النقدية للموظفين."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 6ab2533293b5c8cb37953427893b75a98ddf3976
ms.contentlocale: ar-sa
ms.lasthandoff: 09/17/2018

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="6642e-103">تسجيل موظف في خطة التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="6642e-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6642e-104">بإمكان مدير التعويضات والميزات‬ تسجيل الموظفين في خطط التعويض المتغيرة لحساب المكافآت النقدية وغير النقدية للموظفين.</span><span class="sxs-lookup"><span data-stu-id="6642e-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="6642e-105">يفترض هذا الإجراء أنه قد تم إنشاء خطة تعويض متغيرة مع تعيين الحقل "تمكين التسجيل" إلى "نعم"، وأنه قد تم إنشاء قواعد الأهلية لخطة التعويض المتغيرة هذه.</span><span class="sxs-lookup"><span data-stu-id="6642e-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="6642e-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="6642e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6642e-107">لبدء هذا الإجراء، انتقل إلى الموارد البشرية > العاملون‬ > الموظفون > التعويض > تسجيل الخطة المتغيرة</span><span class="sxs-lookup"><span data-stu-id="6642e-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="6642e-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6642e-108">Click New.</span></span>
2. <span data-ttu-id="6642e-109">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6642e-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6642e-110">يتم تصفية بحث الخطة لإظهار فقط خطط التعويض المتغيرة التي يتأهل الموظف لها استنادًا إلى قواعد الأهلية.</span><span class="sxs-lookup"><span data-stu-id="6642e-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="6642e-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6642e-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6642e-112">بدّل توسيع المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="6642e-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="6642e-113">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="6642e-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="6642e-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6642e-114">Click Save.</span></span>
7. <span data-ttu-id="6642e-115">بدّل توسيع المقطع "التجاوزات‬".</span><span class="sxs-lookup"><span data-stu-id="6642e-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="6642e-116">بشكل اختياري، يمكن تعيين تاريخ قاعدة توظيف لتجاوز تاريخ التوظيف لموظف عند تحديد "النسبة‬" لقاعدة التوظيف المحددة للخطة المتغيرة المحددة.</span><span class="sxs-lookup"><span data-stu-id="6642e-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="6642e-117">إذا كانت الخطة المتغيرة عبارة عن نسبة من الخطة الأساسية، فيمكن تجاوز النسبة المئوية لمكافأة الموظف.</span><span class="sxs-lookup"><span data-stu-id="6642e-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="6642e-118">أما إذا كانت خطة التعويض المتغيرة عبارة عن عدد من وحدات الخطة، فيمكن تجاوز عدد الوحدات للموظف.</span><span class="sxs-lookup"><span data-stu-id="6642e-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="6642e-119">إذا كان يجب تقديم مبلغ أساسي للموظف كمكافأة، فيمكن تعيين المبلغ هنا.</span><span class="sxs-lookup"><span data-stu-id="6642e-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="6642e-120">بدّل توسيع المقطع "التجاوزات التنظيمية‬".</span><span class="sxs-lookup"><span data-stu-id="6642e-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="6642e-121">إذا كان يتعين على أداء الموظف أن يأخذ في الاعتبار أداء أقسام مختلفة أو أداء قسم آخر غير القسم المعين إلى منصف الموظف، فيمكن تجاوز القسم.</span><span class="sxs-lookup"><span data-stu-id="6642e-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="6642e-122">يجب أن يساوي إجمالي عمود "النسبة" 100.</span><span class="sxs-lookup"><span data-stu-id="6642e-122">The Percent column should total 100.</span></span>  


