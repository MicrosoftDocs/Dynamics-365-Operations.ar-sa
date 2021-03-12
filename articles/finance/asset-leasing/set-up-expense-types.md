---
title: إعداد أنواع المصروفات
description: يشرح هذا الموضوع كيفية إعداد أنواع المصروفات في تأجير الأصول.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3ab31b16c6ae07466d7655832701e71092064fe1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969493"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="489e0-103">إعداد أنواع المصروفات</span><span class="sxs-lookup"><span data-stu-id="489e0-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="489e0-104">يشرح هذا الموضوع كيفية إعداد أنواع المصروفات في تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="489e0-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="489e0-105">تعرف التكاليف التي لا يتم تمثيلها بجدول الدفع باسم *تكاليف المصروفات*.</span><span class="sxs-lookup"><span data-stu-id="489e0-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="489e0-106">تشتمل أمثلة على هذه التكاليف على ضرائب الخصائص وتكاليف صيانة المنطقة الشائعة ومصروفات التأمين.</span><span class="sxs-lookup"><span data-stu-id="489e0-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="489e0-107">إضافة نوع مصروفات إدارية</span><span class="sxs-lookup"><span data-stu-id="489e0-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="489e0-108">انتقل إلى **تأجير الأصول \> الضبط \> أنواع المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="489e0-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="489e0-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="489e0-109">Select **New**.</span></span>
3. <span data-ttu-id="489e0-110">في الحقول المناسبة، أدخل نوع المصروفات الجديد والوصف.</span><span class="sxs-lookup"><span data-stu-id="489e0-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="489e0-111">تعيين حسابات إلى تكاليف إدارية</span><span class="sxs-lookup"><span data-stu-id="489e0-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="489e0-112">بعد ذلك، يجب إقران الحسابات بأنواع المصروفات.</span><span class="sxs-lookup"><span data-stu-id="489e0-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="489e0-113">سيتم خصم هذه الحسابات عند ترحيل إدخالات جدول المصروفات.</span><span class="sxs-lookup"><span data-stu-id="489e0-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="489e0-114">يتم تحديد الحساب المقابل في البنود **جدول دفع تكلفة تنفيذ العقد** في كل إيجار.</span><span class="sxs-lookup"><span data-stu-id="489e0-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="489e0-115">انتقل إلى **تأجير الأصول‬ \> الإعداد‬ \> معلمات تأجير الأصول**.</span><span class="sxs-lookup"><span data-stu-id="489e0-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="489e0-116">من علامة التبويب **الحساب** في علامة التبويب السريعة **تكاليف تنفيذ العقد**، في الحقل **نوع المصروفات**، حدد نوع المصروفات.</span><span class="sxs-lookup"><span data-stu-id="489e0-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="489e0-117">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="489e0-117">Select **Add**.</span></span>
4. <span data-ttu-id="489e0-118">في الحقل **نوع الدفتر**، حدد نوع الدفتر للارتباط بالتكاليف الإدارية.</span><span class="sxs-lookup"><span data-stu-id="489e0-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="489e0-119">يمكن ربط أنواع الدفاتر المتعددة بحساب المصروفات نفسه.</span><span class="sxs-lookup"><span data-stu-id="489e0-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="489e0-120">في الحقل **كود الحساب**، حدد أي العقود التي يجب تطبيق الدفتر عليها:</span><span class="sxs-lookup"><span data-stu-id="489e0-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="489e0-121">**الكل** – قم بتطبيق الدفتر على جميع عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="489e0-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="489e0-122">**المجموعة** – تطبيق الدفتر على مجموعة معينة من عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="489e0-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="489e0-123">**الجدول** – قم بتطبيق الدفتر على عقود إيجار محددة.</span><span class="sxs-lookup"><span data-stu-id="489e0-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="489e0-124">إذا قمت بتحديد **المجموعة** أو **الجدول** في الحقل **كود الحساب**، حدد رقم الحساب أو رقم المجموعة في الحقل **رقم الحساب/المجموعة** .</span><span class="sxs-lookup"><span data-stu-id="489e0-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="489e0-125">في الحقول المناسبة، حدد الحساب الرئيسي لعقد الإيجار التمويلي والحساب الرئيسي للتأجير التشغيلي.</span><span class="sxs-lookup"><span data-stu-id="489e0-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="489e0-126">عند إكمالك لهذه الخطوات، يمكنك إضافة مصروفات عبر بنود **جدول دفع تكلفة تنفيذ العقد** في الصفحة **تفاصيل عقد الإيجار** لعقد إيجار محدد.</span><span class="sxs-lookup"><span data-stu-id="489e0-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="489e0-127">وبدلاً من ذلك، يمكنك إضافة المصروفات عندما تقوم بإنشاء عقد إيجار جديد.</span><span class="sxs-lookup"><span data-stu-id="489e0-127">Alternatively, you can add expenses when you create a new lease.</span></span>
