---
title: إنشاء موازنات الصيانة
description: يشرح هذا الموضوع كيفية إنشاء موازنة الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2aaba8794bf0025f0449509752e4f197d3bf3db4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889687"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="a1e68-103">إنشاء موازنات الصيانة</span><span class="sxs-lookup"><span data-stu-id="a1e68-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="a1e68-104">تستخدم موازنات الصيانة لتقديم نظرة عامة حول التكاليف المتوقعة للصيانة الوقائية.</span><span class="sxs-lookup"><span data-stu-id="a1e68-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="a1e68-105">يتم حساب بنود الموازنة استنادًا إلى بنود جدول الصيانة التي لديها تاريخ بدء متوقع أثناء فترة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="a1e68-106">تعتمد موازنات الصيانة على أنواع التكلفة المستخدمة في إدارة الأصول: **وقائية** و**تصحيحية** و**استثمارية**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="a1e68-107">يتم تضمين تكاليف الموازنة لصيانة الاستثمار للأصول النشطة التي لها تاريخ استبدال أثناء فترة الموازنة وقيمة بديلة مرتبطة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="a1e68-108">ويتم تضمين تكاليف الموازنة للصيانة التصحيحية إذا تم تضمين تاريخ تصحيحي سابق في حساب الموازنة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="a1e68-109">وفي هذه الحالة، يتم حساب التكاليف التصحيحية من فترة سابقة لنفس الفترة المستقبلية التي تقوم بحساب موازنة الصيانة لها.</span><span class="sxs-lookup"><span data-stu-id="a1e68-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="a1e68-110">إنشاء موازنة الصيانة</span><span class="sxs-lookup"><span data-stu-id="a1e68-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="a1e68-111">حدد **إدارة الأصول** \> **استعلامات** \> **موازنة‏‎ الصيانة** \> **الموازنة‏‎**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="a1e68-112">حدد **إنشاء موازنة**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="a1e68-113">في الحقل **موازنة الصيانة**، أدخل معرف موازنة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="a1e68-114">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="a1e68-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="a1e68-115">على علامة التبويب السريعة **الفترة**، في الحقلين **من تاريخ** و**إلى تاريخ**، أدخل تاريخي البدء والانتهاء لفترة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="a1e68-116">لتضمين تكاليف الموازنة التصحيحية التي يتم حسابها استنادًا إلى التكاليف الفعلية من فترة سابقة، في حقل **تصحيحية من تاريخ**، أدخل تاريخ البدء للفترة التي يجب أن يتم تضمين هذه التكاليف منها.</span><span class="sxs-lookup"><span data-stu-id="a1e68-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="a1e68-117">وفقًا لمستوى التفاصيل المطلوب في الموازنة، قم بتعيين الخيارات ذات الصلة على علامات التبويب السريعة الخمس **تجميع حسب**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="a1e68-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-118">Select **OK**.</span></span>
8. <span data-ttu-id="a1e68-119">حدد **بنود الموازنة** لفتح صفحة **بنود موازنة الصيانة**، حيث يمكنك عرض كافة بنود الموازنة التي تم إنشاؤها للفترة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="a1e68-120">لاعتماد الموازنة، حددها في صفحة **موازنات‏‎ الصيانة**، ثم حدد **اعتماد**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="a1e68-121">ثم، في مربع الحوار‏‎ **اعتماد الموازنة**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="a1e68-122">يتم إدخال اسمك في الحقل **معتمد بواسطة** في صفحة **موازنات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a1e68-123">بعد اعتماد موازنة الصيانة، لا يمكنك إعادة حساب البنود ذات الصلة أو تعديلها في صفحة **بنود موازنة الصيانة** ما لم تقم أولاً بإزالة اعتماد الموازنة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="a1e68-124">لإزالة اعتماد موازنة الصيانة، حددها في صفحة **موازنات‏‎ الصيانة**، ثم حدد **اعتماد**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="a1e68-125">ثم، في مربع الحوار‏‎ **اعتماد الموازنة**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![موازنات الصيانة](media/01-maintenance-budgets.png)

<span data-ttu-id="a1e68-127">يمكنك أيضا إنشاء موازنة صيانة جديدة من خلال نسخ موازنة موجودة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="a1e68-128">صفحة **موازنات‏‎ الصيانة**، حدد الموازنة التي تريد نسخها، ثم حدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="a1e68-129">وتعد هذه الطريقة مفيدة، إذا قمت، على سبيل المثال، بإنشاء موازنة لشهر واحد وأردت نسخها إلى أشهر أخرى.</span><span class="sxs-lookup"><span data-stu-id="a1e68-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="a1e68-130">تحسب موازنة الصيانة فقط تكاليف الموازنة استنادًا إلى بنود جدول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="a1e68-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="a1e68-131">لحساب التكاليف الفعلية لنفس الفترة، يمكنك إجراء هذا الحساب في صفحة **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="a1e68-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
