---
title: تقارير المصروفات والمعتمدون المتعددون
description: يوفر هذا الموضوع معلومات حول تقارير المصروفات التي تتطلب الموافقة بواسطة أكثر من شخص واحد.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176225"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="f3257-103">تقارير المصروفات والمعتمدون المتعددون</span><span class="sxs-lookup"><span data-stu-id="f3257-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3257-104">استنادًا إلى سياسات الموافقة على المصروفات الخاصة بمؤسستك، قد يكون لديك أكثر من شخص للموافقة على تقرير النفقات المُقدم بواسطة أحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="f3257-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="f3257-105">عند إعداد عملية سير العمل للموافقة على تقرير مصروفات، يمكنك إضافة عناصر سير العمل التي تحتوي على مهام أو خطوات لواحد أو أكثر من معتمدي تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f3257-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="f3257-106">على سبيل المثال، قد تطلب اعتماد كافة تقارير المصروفات أولًا بواسطة مدير الموظف الذي قدم التقرير، ثم بواسطة منسق الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="f3257-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="f3257-107">إذا قررت طلب عدة معتمدين لتقارير المصروفات، يمكنك إضافة عناصر سير العمل بأي من الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="f3257-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="f3257-108">إضافة عنصر اعتماد واحد يحتوي على خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f3257-108">Add one approval element that has one step.</span></span> <span data-ttu-id="f3257-109">على سبيل المثال، قد تتطلب الخطوة تعيين تقرير المصروفات إلى مجموعة مستخدمين، وقد يتطلب اعتماده بواسطة 50% من أعضاء مجموعة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="f3257-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="f3257-110">إضافة عنصر اعتماد واحد يحتوي على عدة خطوات.</span><span class="sxs-lookup"><span data-stu-id="f3257-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="f3257-111">على سبيل المثال، قد يحتوي عنصر الاعتماد على الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f3257-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="f3257-112">يعتمد مدير الموظف الذي قدم تقرير المصروفات هذا التقرير.</span><span class="sxs-lookup"><span data-stu-id="f3257-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="f3257-113">يقوم موظف الحسابات الدائنة بالتحقق من عمليات الاستلام وبنود تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f3257-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="f3257-114">يعتمد مالك الموازنة تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f3257-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="f3257-115">قم بإضافة عناصر اعتماد متعددة، كل منها يحتوي على خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="f3257-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="f3257-116">على سبيل المثال، يمكنك إضافة عنصر اعتماد نفصل لكل خطوة من الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f3257-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="f3257-117">يعتمد مدير الموظف تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f3257-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="f3257-118">يعتمد مالك الموازنة تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f3257-118">The budget owner approves the expense report.</span></span>
