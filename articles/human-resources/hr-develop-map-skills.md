---
title: تعيين المهارات
description: يمكنك إنشاء بحث تعيين المهارة للعثور على شخص مؤهل في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076575"
---
# <a name="map-skills"></a><span data-ttu-id="29b1e-103">تعيين المهارات</span><span class="sxs-lookup"><span data-stu-id="29b1e-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="29b1e-104">يمكنك إنشاء بحث تعيين المهارة للعثور على شخص مؤهل في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="29b1e-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="29b1e-105">تقوم عمليات البحث بتعيين المهارات بإرجاع نتائج للمعايير التي قمت بإدخالها بالنظر إلى المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="29b1e-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="29b1e-106">المهارات</span><span class="sxs-lookup"><span data-stu-id="29b1e-106">Skills</span></span>
- <span data-ttu-id="29b1e-107">التعليم</span><span class="sxs-lookup"><span data-stu-id="29b1e-107">Education</span></span>
- <span data-ttu-id="29b1e-108">الشهادات</span><span class="sxs-lookup"><span data-stu-id="29b1e-108">Certificates</span></span>
- <span data-ttu-id="29b1e-109">المناصب‬</span><span class="sxs-lookup"><span data-stu-id="29b1e-109">Positions</span></span>
- <span data-ttu-id="29b1e-110">خبرة المشروع</span><span class="sxs-lookup"><span data-stu-id="29b1e-110">Project experience</span></span>

<span data-ttu-id="29b1e-111">على سبيل المثال، يمكنك العثور على أشخاص في المؤسسة التي حصلت على CPA.</span><span class="sxs-lookup"><span data-stu-id="29b1e-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="29b1e-112">‏‫تتيح لك ملفات تعريف تعيين المهارات إمكانية البحث عن الموظفين أو المرشحين الحاليين ذوي المؤهلات التي تتوافق مباشرةً مع احتياجات العمل.</span><span class="sxs-lookup"><span data-stu-id="29b1e-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="29b1e-113">سيتم فقط عرض العاملين ومقدمي الطلبات وجهات الاتصال المدرجين في عمليات بحث تعيين المهارة في قائمة نتائج تعيين المهارة أو تضمينهم في ملف تعريف مهارة.</span><span class="sxs-lookup"><span data-stu-id="29b1e-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="29b1e-114">ولتضمين عامل أو مقدم طلب أو شخص جهة الاتصال في عمليات البحث عن تعيين المهارات، قم بتعيين تحديد **تضمين في تعيين المهارات** إلى **نعم** في الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="29b1e-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="29b1e-115">العامل</span><span class="sxs-lookup"><span data-stu-id="29b1e-115">Worker</span></span><br>
> - <span data-ttu-id="29b1e-116">موظف</span><span class="sxs-lookup"><span data-stu-id="29b1e-116">Employee</span></span><br>
> - <span data-ttu-id="29b1e-117">مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="29b1e-117">Applicant</span></span><br>
> - <span data-ttu-id="29b1e-118">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="29b1e-118">Contacts</span></span><br>

<span data-ttu-id="29b1e-119">لإنشاء تعيين مهارة، انتقل إلى **تطوير الموظفين > الارتباطات > تعيين المهارات**.</span><span class="sxs-lookup"><span data-stu-id="29b1e-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="29b1e-120">لإنشاء ملف تعريف تعيين مهارة، انتقل إلى **تطوير الموظفين > الارتباطات > ملفات تعريف تعيين المهارات**.</span><span class="sxs-lookup"><span data-stu-id="29b1e-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="29b1e-121">تحليلات المهارات المفقودة وتحليلات ملف تعريف المهارات</span><span class="sxs-lookup"><span data-stu-id="29b1e-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="29b1e-122">يمكنك إنشاء تحليل ملف تعريف المهارات لعرض قائمة باختصاصات الشخص.</span><span class="sxs-lookup"><span data-stu-id="29b1e-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="29b1e-123">يمكنك إنشاء تحليل فروق المهارات لمقارنة مهارات الشخص بالمهارات المطلوبة لوظيفة.</span><span class="sxs-lookup"><span data-stu-id="29b1e-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="29b1e-124">لإنشاء تحليل الفروق، انتقل إلى **تطوير الموظف > الارتباطات > وظيفة تحليل مهارات مفقودة - شخص**.</span><span class="sxs-lookup"><span data-stu-id="29b1e-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="29b1e-125">لإنشاء تحليل ملف تعريف تعيين مهارة، انتقل إلى **تطوير الموظفين > الارتباطات > تحليل ملف تعريف المهارة**.</span><span class="sxs-lookup"><span data-stu-id="29b1e-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="29b1e-126">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="29b1e-126">See also</span></span>

[<span data-ttu-id="29b1e-127">تكوين المهارات</span><span class="sxs-lookup"><span data-stu-id="29b1e-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="29b1e-128">إدخال المهارات</span><span class="sxs-lookup"><span data-stu-id="29b1e-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]