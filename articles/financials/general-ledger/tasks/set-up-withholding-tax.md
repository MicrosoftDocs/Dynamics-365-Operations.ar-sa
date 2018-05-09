--- 
title: "إعداد ضريبة الخصم"
description: "ضريبة الخصم هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشا حركات ضرائب المبيعات."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 39ebd6a1a326b0ff2943957c9606e91852d524ce
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="d2e3d-103">إعداد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="d2e3d-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2e3d-104">ضريبة الخصم هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشا حركات ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="d2e3d-105">ضريبة الخصم التي يتم حسابها على مدفوعات المورّد يعد التزامًا مستحقًا.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="d2e3d-106">وبالتالي تُعد حسابات الميزانية العمومية وحسابات الالتزامات المستحقة حسابات صالحة لترحيل ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="d2e3d-107">يوضح دليل المهام هذا كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="d2e3d-108">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة الخصم > أكواد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="d2e3d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-109">Click New.</span></span>
3. <span data-ttu-id="d2e3d-110">في الحقل "كود ضريبة الخصم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="d2e3d-111">في الحقل "اسم ضريبة الخصم"، أدخل اسمًا لكود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="d2e3d-112">في حقل "الحساب الرئيسي"، حدد الحساب الرئيسي لترحيل الخضوع لضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="d2e3d-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-113">Click Save.</span></span>
7. <span data-ttu-id="d2e3d-114">انقر فوق "القيم‬".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-114">Click Values.</span></span>
8. <span data-ttu-id="d2e3d-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d2e3d-116">في حقل "القيمة"، أدخل النسبة المئوية المستخدمة لاحتساب ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="d2e3d-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-117">Click Save.</span></span>
11. <span data-ttu-id="d2e3d-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-118">Close the page.</span></span>
12. <span data-ttu-id="d2e3d-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-119">Click Save.</span></span>
13. <span data-ttu-id="d2e3d-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-120">Close the page.</span></span>
14. <span data-ttu-id="d2e3d-121">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة الخصم‬ > مجموعات ضرائب الخصم‬.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="d2e3d-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-122">Click New.</span></span>
16. <span data-ttu-id="d2e3d-123">في الحقل "مجموعة ضرائب الخصم"، أدخل معرف مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="d2e3d-124">في الحقل "الوصف"، أدخل اسم مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="d2e3d-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="d2e3d-126">في الحقل "كود ضريبة الخصم"، حدد كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="d2e3d-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d2e3d-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="d2e3d-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d2e3d-128">Click Save.</span></span>


