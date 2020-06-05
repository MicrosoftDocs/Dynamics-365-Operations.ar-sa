---
title: المصروفات المشتركة بين الشركات الشقيقة
description: قد يقوم عامل تم توظيفه بواسطة كيان قانوني في مؤسسة بتنفيذ عمل لكيان قانوني آخر في المؤسسة نفسها. في هذه الحالة، يمكنك استخدام ميزة المصروفات بين الشركات الشقيقة لتعيين مصروفات العامل إلى الكيان القانوني الذي تم تنفيذ العمل له.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390874"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="fbd4d-104">المصروفات المشتركة بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="fbd4d-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbd4d-105">قد يقوم عامل تم توظيفه بواسطة كيان قانوني في مؤسسة بتنفيذ عمل لكيان قانوني آخر في المؤسسة نفسها.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="fbd4d-106">في هذه الحالة، يمكنك استخدام ميزة المصروفات بين الشركات الشقيقة لتعيين مصروفات العامل إلى الكيان القانوني الذي تم تنفيذ العمل له.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="fbd4d-107">يسمى الكيان القانوني الذي يوظف العامل الكيان القانوني المقرض.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="fbd4d-108">أما الكيان القانوني الذي يتكبد العامل مصروفات له فيسمى الكيان القانوني المقترض.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="fbd4d-109">قبل أن يتمكن العامل من إنشاء وإرسال مصروفات العمل الذي تم تنفيذه لكيان قانوني مختلف، في الكيان القانوني المقرض، في صفحة **معلمات إدارة المصروفات**، حدد الخيار **السماح ببنود المصروفات بين الشركات الشقيق**.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="fbd4d-110">ترحيل الضريبة للمصروفات بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="fbd4d-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbd4d-111">إذا كنت تريد استخدام مجموعات الضرائب المقترنة بالكيان القانوني للإقراض (المصدر) بدلا من الكيان القانوني للاقتراض (الوجهة) في تقرير المصروفات، فستحتاج إلى تكوين هذا في الإعداد الخاص بضريبة مبيعات دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="fbd4d-112">عند تعيين معلمة دفتر الأستاذ العام، يتم تعيين **الكيان القانوني لترحيل الضريبة بين الشركات الشقيقة** إلى **المصدر** وتعيين **تطبيق قواعد فرض ضرائب على المبيعات** إلى **لا**، سيتم استخدام توليفة ضريبية للكيان القانوني إقراض.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="fbd4d-113">عند تعيين نفس المعلمة إلى **الوجهة**، سيتم استخدام التوليفة الضريبية للكيان القانوني اقتراض.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="fbd4d-114">بالنسبة للكيانات القانونية في الولايات المتحدة، عند تعيين المعلمة إلى **المصدر**، يجب أيضًا تكوين حقل **ضريبة مبيعات قابلة للاسترداد** في صفحة **مجموعات ترحيل دفتر الأستاذ** الجديدة.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="fbd4d-115">سيستخدم محرك المحاسبة معلومات من هذا الحقل للإدخال المحاسبي المتعلق بالضريبة.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="fbd4d-116">ويكون السلوك متسقًا لبنود المصروفات التي تم ترحيلها مع مشروع أو بدونه.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
