---
title: تعديل علاقات التقارير لمنصب
description: يوضح هذا الإجراء كيفية تغيير علاقة التقارير لأحد الموظفين.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a1afd2c1cdc2ebaa303030d01b3bbe5fd2af44f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507649"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="10e7f-103">تعديل علاقات التقارير لمنصب</span><span class="sxs-lookup"><span data-stu-id="10e7f-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10e7f-104">يوضح هذا الإجراء كيفية تغيير علاقة التقارير لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="10e7f-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="10e7f-105">يمكن استخدام علاقة التقارير لتوجيه المستندات من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="10e7f-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="10e7f-106">كما يوضح الإجراء كيفية تعيين الموظف لتدرجات هرمية إضافية.</span><span class="sxs-lookup"><span data-stu-id="10e7f-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="10e7f-107">على سبيل المثال، قد يكون أحد الموظفين جزءًا من فريق المشروع بعلاقة تقارير غير رسمية لمشرف المشروع.</span><span class="sxs-lookup"><span data-stu-id="10e7f-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="10e7f-108">ويمكن تعريف علاقات التقارير الإضافية على المنصب لاستيعاب مختلف سيناريوهات المشروع أو المصفوفة.</span><span class="sxs-lookup"><span data-stu-id="10e7f-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="10e7f-109">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="10e7f-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="10e7f-110">انتقل إلى الموارد البشرية > المناصب > المناصب.</span><span class="sxs-lookup"><span data-stu-id="10e7f-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="10e7f-111">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="10e7f-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="10e7f-112">على سبيل المثال، قم بإجراء التصفية على حقل "المنصب" بقيمة "000091".</span><span class="sxs-lookup"><span data-stu-id="10e7f-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="10e7f-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10e7f-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="10e7f-114">قم بتوسيع التقارير لقسم المنصب.</span><span class="sxs-lookup"><span data-stu-id="10e7f-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="10e7f-115">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="10e7f-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="10e7f-116">في حقل "‏‫رفع التقارير إلى"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="10e7f-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="10e7f-117">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="10e7f-117">Click Create.</span></span>
8. <span data-ttu-id="10e7f-118">قم بتوسيع مقطع العلاقات.</span><span class="sxs-lookup"><span data-stu-id="10e7f-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="10e7f-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="10e7f-119">Click Add.</span></span>
10. <span data-ttu-id="10e7f-120">حدد خانة الاختيار الموجودة على يسار الشبكة.</span><span class="sxs-lookup"><span data-stu-id="10e7f-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="10e7f-121">في حقل "‏‫اسم التدرج الهرمي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="10e7f-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="10e7f-122">مثال: مشروع</span><span class="sxs-lookup"><span data-stu-id="10e7f-122">Example: Project</span></span>  
12. <span data-ttu-id="10e7f-123">في حقل "‏‫رفع التقارير إلى منصب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="10e7f-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="10e7f-124">على سبيل المثال: 000437</span><span class="sxs-lookup"><span data-stu-id="10e7f-124">Example:  000437</span></span>
13. <span data-ttu-id="10e7f-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="10e7f-125">Click Save.</span></span>

