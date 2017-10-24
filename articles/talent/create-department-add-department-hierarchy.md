---
title: "إنشاء قسم وربطه بالتدرج الهرمي للأقسام"
description: "القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي في المؤسسة. والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية. ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية. قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: adf3dbf8b7ffa906c872a6b66d9cb43eb8e02805
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="ff2da-106">إنشاء قسم وربطه بالتدرج الهرمي للأقسام</span><span class="sxs-lookup"><span data-stu-id="ff2da-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ff2da-107">القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="ff2da-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="ff2da-108">والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="ff2da-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="ff2da-109">ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="ff2da-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="ff2da-110">قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="ff2da-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="ff2da-111">قد يتضمن القسم مجموعة من مراكز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ff2da-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="ff2da-112">ويمكن تعيين مناصب للأقسام.</span><span class="sxs-lookup"><span data-stu-id="ff2da-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="ff2da-113">لإنشاء قسم، انقر فوق **الموارد البشرية** &gt; **الأقسام** &gt; **القسم**.</span><span class="sxs-lookup"><span data-stu-id="ff2da-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="ff2da-114">يصف الجدول التالي الحقول المتوفرة.‬</span><span class="sxs-lookup"><span data-stu-id="ff2da-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="ff2da-115">الحقل</span><span class="sxs-lookup"><span data-stu-id="ff2da-115">Field</span></span>               | <span data-ttu-id="ff2da-116">الوصف</span><span class="sxs-lookup"><span data-stu-id="ff2da-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2da-117">الاسم</span><span class="sxs-lookup"><span data-stu-id="ff2da-117">Name</span></span>                | <span data-ttu-id="ff2da-118">أدخل اسمًا للقسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ff2da-119">رقم القسم</span><span class="sxs-lookup"><span data-stu-id="ff2da-119">Department number</span></span>   | <span data-ttu-id="ff2da-120">قد يتم إنشاء قيمة افتراضية تلقائيًا في حالة تعيين كود تسلسل رقمي لمرجع **رقم المؤسسة** في صفحة **المسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="ff2da-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="ff2da-121">اسم البحث</span><span class="sxs-lookup"><span data-stu-id="ff2da-121">Search name</span></span>         | <span data-ttu-id="ff2da-122">أدخل اسمًا أو اختصارًا يمكن استخدامه في البحث عن القسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="ff2da-123">مذكرة</span><span class="sxs-lookup"><span data-stu-id="ff2da-123">Memo</span></span>                | <span data-ttu-id="ff2da-124">أدخل أي معلومات إضافية هنا.</span><span class="sxs-lookup"><span data-stu-id="ff2da-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="ff2da-125">في تدرج هرمي</span><span class="sxs-lookup"><span data-stu-id="ff2da-125">In hierarchy</span></span>        | <span data-ttu-id="ff2da-126">تشير خانة الاختيار المحددة إلى ما إذا كان القسم مضمنًا في التدرج الهرمي للأقسام أو لا.</span><span class="sxs-lookup"><span data-stu-id="ff2da-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="ff2da-127">لمزيد من المعلومات حول كيفية إضافة قسم إلى التدرج الهرمي للأقسام، راجع المعلومات لاحقاً في هذه المقالة.</span><span class="sxs-lookup"><span data-stu-id="ff2da-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="ff2da-128">رقم نظام الترقيم العالمي للبيانات</span><span class="sxs-lookup"><span data-stu-id="ff2da-128">DUNS number</span></span>         | <span data-ttu-id="ff2da-129">يشير الاختصار DUNS إلى نظام الترقيم العالمي للبيانات.</span><span class="sxs-lookup"><span data-stu-id="ff2da-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="ff2da-130">هذا هو رقم مكون من تسعة أرقام تصدره Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="ff2da-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="ff2da-131">المدير</span><span class="sxs-lookup"><span data-stu-id="ff2da-131">Manager</span></span>             | <span data-ttu-id="ff2da-132">أدخل الشخصية التي تدير القسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="ff2da-133">العناوين</span><span class="sxs-lookup"><span data-stu-id="ff2da-133">Addresses</span></span>           | <span data-ttu-id="ff2da-134">أضف معلومات العنوان الخاصة بالقسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-134">Add the address information for the department.</span></span> <span data-ttu-id="ff2da-135">على سبيل المثال، أضف العنوان البريدي للمبنى حيث يوجد القسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="ff2da-136">معلومات جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="ff2da-136">Contact information</span></span> | <span data-ttu-id="ff2da-137">أضف معلومات الاتصال الخاصة بالقسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-137">Add contact information for the department.</span></span> <span data-ttu-id="ff2da-138">على سبيل المثال، أضف رقم هاتف لمكتب الخدمة في القسم.</span><span class="sxs-lookup"><span data-stu-id="ff2da-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="ff2da-139">لإضافة قسم إلى التردج الهرمي للأقسا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ff2da-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="ff2da-140">انقر فوق **الموارد البشرية** &gt; **الأقسام** &gt; **التدرج الهرمي للأقسام**.</span><span class="sxs-lookup"><span data-stu-id="ff2da-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="ff2da-141">انقر فوق **تحرير**، ثم حدد المؤسسة التي يجب أن تكون المؤسسة ضمنها.</span><span class="sxs-lookup"><span data-stu-id="ff2da-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="ff2da-142">انقر فوق **إدراج**، وحدد **قسم** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="ff2da-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="ff2da-143">في قائمة الأقسام التي تظهر، حدد القسم لإضافته إلى التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="ff2da-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="ff2da-144">‏‏قم بحفظ التغييرات التي قمت بإجرائها.</span><span class="sxs-lookup"><span data-stu-id="ff2da-144">Save your changes.</span></span> <span data-ttu-id="ff2da-145">وتظهر لك رسالة تفيد بأنه قد تم إنشاء نسخة مسودة من التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="ff2da-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="ff2da-146">‏‫وعندما تكون جاهزاً، انقر فوق **نشر‬‏‫** في مصمم التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="ff2da-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="ff2da-147">ويمكنك إدخال تاريخ سريان يشير إلى متى يجب نشر التدرج الهرمي.‬</span><span class="sxs-lookup"><span data-stu-id="ff2da-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="ff2da-148">على سبيل المثال، لإضافة قسم جديد في بداية السنة التقويمية التالية، قم بتعيين تاريخ السريان إلى 1 كانون الثاني/يناير من السنة التقويمية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="ff2da-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="ff2da-149">وستصبح التغييرات على التدرج الهرمي نافذة المفعول في ذلك التاريخ.</span><span class="sxs-lookup"><span data-stu-id="ff2da-149">The changes to the hierarchy will take effect on that date.</span></span>





