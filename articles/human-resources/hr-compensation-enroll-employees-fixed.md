---
title: تسجيل موظف في خطة تعويض ثابتة
description: بإمكان مدير التعويضات والميزات‬ تعيين الموظفين لخطط التعويض الثابتة لإدارة راتبهم الأساسي.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3029e52a7cc1fb6dfda390f5d892c89f1eda8509
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417092"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="ea36b-103">تسجيل موظف في خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="ea36b-103">Enroll an employee in a fixed compensation plan</span></span>

<span data-ttu-id="ea36b-104">بإمكان مدير التعويضات والميزات‬ تعيين الموظفين لخطط التعويض الثابتة لإدارة راتبهم الأساسي.</span><span class="sxs-lookup"><span data-stu-id="ea36b-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="ea36b-105">يفترض هذا الإجراء أنه قد تم إنشاء خطة ثابتة وهي نشطة، وأنه قد تم تعيين قواعد الأهلية للخطة.</span><span class="sxs-lookup"><span data-stu-id="ea36b-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="ea36b-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="ea36b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ea36b-107">لبدء الإجراء، انتقل إلى الموارد البشرية > العاملون > الموظفون > التعويض > خطة ثابتة</span><span class="sxs-lookup"><span data-stu-id="ea36b-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="ea36b-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ea36b-108">Click New.</span></span>
2. <span data-ttu-id="ea36b-109">في الحقل "الإجراء‬"، حدد "إجراء التعويض الثابت‬" من النوع "توظيف/إعادة توظيف‬" لوصف التغيير في تعويض الموظف.</span><span class="sxs-lookup"><span data-stu-id="ea36b-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="ea36b-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea36b-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ea36b-111">في الحقل "المنصب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ea36b-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ea36b-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea36b-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea36b-113">المستوى المعروض هو من "مستوى التعويض" للوظيفة في المنصب.</span><span class="sxs-lookup"><span data-stu-id="ea36b-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="ea36b-114">يجب تعيين مستوى الوظيفة قبل أن يتم تعيين التعويض إلى الموظف.</span><span class="sxs-lookup"><span data-stu-id="ea36b-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="ea36b-115">في الحقل "الخطة"، حدد خطة التعويض الثابت للموظف.</span><span class="sxs-lookup"><span data-stu-id="ea36b-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="ea36b-116">يتم تصفية بحث الخطة لإظهار فقط الخطط التي يتأهل الموظف لها استنادًا إلى قواعد الأهلية.</span><span class="sxs-lookup"><span data-stu-id="ea36b-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="ea36b-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="ea36b-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ea36b-118">تأتي تاريخي السريان وانتهاء الصلاحية للتعويض بشكل افتراضي من تاريخي البدء والانتهاء لتعيين منصب العامل.</span><span class="sxs-lookup"><span data-stu-id="ea36b-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="ea36b-119">يمكنك تعديل هذه التواريخ حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="ea36b-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="ea36b-120">إذا كانت خطة التعويض الثابت خطة خطوة، فحدد الخطوة التي تتضمن معدل الدفع الصحيح للموظف.</span><span class="sxs-lookup"><span data-stu-id="ea36b-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="ea36b-121">وإذا كانت خطة التعويض الثابت خطة نطاق أو درجة، فأدخل معدل الدفع الصحيح للموظف.</span><span class="sxs-lookup"><span data-stu-id="ea36b-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="ea36b-122">وسيتم التحقق من معدل الدفع مقابل إعدادات التفاوت للخطة، ونقاط مرجعية الحد الأدنى والحد الأقصى لمستوى التعويض لهذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="ea36b-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="ea36b-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ea36b-123">Click OK.</span></span>

