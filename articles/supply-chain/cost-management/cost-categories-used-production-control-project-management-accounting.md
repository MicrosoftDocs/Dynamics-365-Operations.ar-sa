---
title: فئات التكلفة المستخدمة في التحكم بالإنتاج ومحاسبة إدارة المشروع
description: يمكن تطبيق بعض أنواع الإنتاج على تقديرات وقت المشروع وإعداد التقارير. توفر هذه المقالة معلومات حول فئات التكلفة التي يجب تحديدها لأنواع عمل الإنتاج هذه لأغراض الإنتاج والمشروع.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26f4ce073528bf102a951d6fa002aeb0da9e380c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201906"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="a0b8a-104">فئات التكلفة المستخدمة في التحكم بالإنتاج ومحاسبة إدارة المشروع</span><span class="sxs-lookup"><span data-stu-id="a0b8a-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0b8a-105">يمكن تطبيق بعض أنواع الإنتاج على تقديرات وقت المشروع وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="a0b8a-106">توفر هذه المقالة معلومات حول فئات التكلفة التي يجب تحديدها لأنواع عمل الإنتاج هذه لأغراض الإنتاج والمشروع.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="a0b8a-107">يمكن تطبيق بعض أنواع الإنتاج على تقديرات وقت المشروع وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="a0b8a-108">في هذه الحالة، تكون فئة التكلفة مطلوبة لأغراض الإنتاج والمشروع.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="a0b8a-109">عند استخدام فئة تكلفة في الإنتاج والمشاريع، يجب تحديد معلومات إضافية متعلقة بالمشروع.‬</span><span class="sxs-lookup"><span data-stu-id="a0b8a-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="a0b8a-110">على سبيل المثال، قد تختلف التكاليف في الساعة المرتبطة بالمشاريع عن التكاليف في الساعة المرتبطة بالإنتاج.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="a0b8a-111">يمكنك استخدام صفحة **فئات التكلفة** لتعريف فئة تكلفة يتم استخدامها في التحكم بالإنتاج ومحاسبة إدارة المشروع.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="a0b8a-112">**ملاحظة:** تتضمن محاسبة التكاليف صفحة **فئات المشروع**، ولكن هذه الصفحة ليس لها أي علاقة بالوظيفة التي تم وصفها في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="a0b8a-113">عندما تستخدم فئة تكلفة في المشاريع، فإن صفحة **فئات التكلفة** تتضمن علامات تبويب إضافية تعرض معلومات إضافية متعلقة بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="a0b8a-114">تتضمن هذه المعلومات مجموعة فئات وخاصية بند وحسابات دفتر الأستاذ التي تم تعيينها لفئة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="a0b8a-115">يجب أن تكون فئة التكلفة معينة إلى مجموعات فئات تدعم نوع الحركة **الساعات**.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="a0b8a-116">تشير خاصية البند إلى معلومات افتراضية حول كيفية تحميل المشروع تكلفة الوقت الذي تم الإعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="a0b8a-117">يتم عادةً تحديد حسابات دفتر الأستاذ المرتبطة بالتكاليف والمبيعات لمجموعة الفئات المعيّنة لفئة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="a0b8a-118">ومع ذلك، يمكن تعريف حسابات معينة لفئة تكلفة فردية.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="a0b8a-119">تسمح لك الأزرار الإضافية على صفحة **فئات التكلفة** الوصول إلى المعلومات المرتبطة بالمشروع حول فئة تكلفة محددة.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="a0b8a-120">على سبيل المثال، يمكنك عرض الحركات المرتبطة بالمشروع وتعريف الموظفين أو المشاريع وتحديد التكاليف في الساعة وأسعار المبيعات وعرض التقارير.</span><span class="sxs-lookup"><span data-stu-id="a0b8a-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>



