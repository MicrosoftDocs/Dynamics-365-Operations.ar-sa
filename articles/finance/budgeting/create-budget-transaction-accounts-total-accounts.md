---
title: إنشاء موازنة من حسابات الحركات والحسابات الإجمالية
description: توفر هذه المقالة نظرة عامة على عملية إنشاء موازنات بالاستناد إلى الحسابات الإجمالية. وهي تشرح أيضًا كيفية تشغيل رقابة الموازنة للحسابات الإجمالية، إذا كانت رقابة الموازنة مطلوبة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 085bc12433616d2da2bda40a8412fb88e40db3b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210183"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="22bed-104">إنشاء موازنة من حسابات الحركات والحسابات الإجمالية</span><span class="sxs-lookup"><span data-stu-id="22bed-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22bed-105">توفر هذه المقالة نظرة عامة على عملية إنشاء موازنات بالاستناد إلى الحسابات الإجمالية.</span><span class="sxs-lookup"><span data-stu-id="22bed-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="22bed-106">وهي تشرح أيضًا كيفية تشغيل رقابة الموازنة للحسابات الإجمالية، إذا كانت رقابة الموازنة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="22bed-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="22bed-107">تسمح كلُّ من خطة الموازنة ووثائق إدخال سجل الموازنة بإعداد الموازنة في الحسابات التي لها نوع حساب الرئيسي **إجمالي**.</span><span class="sxs-lookup"><span data-stu-id="22bed-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="22bed-108">ويمكن ترحيل القيم الفعلية إلى حركات الحسابات الرئيسية فقط.</span><span class="sxs-lookup"><span data-stu-id="22bed-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="22bed-109">وبالنسبة للعملية الدورية **إنشاء خطة الموازنة من دفتر الأستاذ العام**، في علامة التبويب **مصدر**، يمكنك تحديد نوع الحساب الرئيسي **إجمالي** كمعيار.</span><span class="sxs-lookup"><span data-stu-id="22bed-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="22bed-110">وفي هذه الحالة، سيتم تضمين كل حساب رئيسي إجمالي في خطة الموازنة الهدف، وسيساوي المبلغ المبلغ الإجمالي لمجموعة الحسابات الرئيسية المحددة.</span><span class="sxs-lookup"><span data-stu-id="22bed-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="22bed-111">ويمكنك تنشيط رقابة الموازنة للحسابات الرئيسية من النوع **إجمالي**.</span><span class="sxs-lookup"><span data-stu-id="22bed-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="22bed-112">ويتم اعتماد هذه الوظيفة من خلال استخدام مجموعات الموازنة.</span><span class="sxs-lookup"><span data-stu-id="22bed-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="22bed-113">بالنسبة لكل حساب رئيسي إجمالي، يجب إنشاء الموازنة التي ينبغي مراقبتها لمجموعة موازنة في صفحة **تكوين رقابة الموازنة**.</span><span class="sxs-lookup"><span data-stu-id="22bed-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="22bed-114">ويجب أن تتضمن المعايير التي تحددها الحساب الرئيسي الإجمالي ونطاق الحسابات‬.‬</span><span class="sxs-lookup"><span data-stu-id="22bed-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="22bed-115">ولتسريع عملية إنشاء مجموعات الموازنة، يمكنك الاستفادة من وحدة بيانات مجموعات رقابة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="22bed-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="22bed-116">عند استخدام موازنة في عمليات الإبلاغ، على سبيل المثال، في قائمة مالية، فإن مجموع الموازنة للحساب الإجمالي يتكون من المبالغ التالية:</span><span class="sxs-lookup"><span data-stu-id="22bed-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="22bed-117">الموازنات التي تم إنشاؤها من كل حساب لدفتر أستاذ الحركات خلال فترة الحساب الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="22bed-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="22bed-118">مبلغ الموازنة الذي تم إدخاله مباشرة على الحساب الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="22bed-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="22bed-119">وبالتالي، يمكنك إنشاء موازنات منفصلة لمعظم حسابات الحركات المهمة في فترة الحساب الإجمالي، ثم إضافة مبلغ الموازنة المتوفر إلى الحساب الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="22bed-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]