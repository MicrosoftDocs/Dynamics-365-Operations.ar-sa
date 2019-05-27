---
title: إعداد ضريبة الخصم
description: ضريبة الخصم هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشا حركات ضرائب المبيعات.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562778"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="9859e-103">إعداد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="9859e-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9859e-104">ضريبة الخصم هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشا حركات ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="9859e-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="9859e-105">ضريبة الخصم التي يتم حسابها على مدفوعات المورّد يعد التزامًا مستحقًا.</span><span class="sxs-lookup"><span data-stu-id="9859e-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="9859e-106">وبالتالي تُعد حسابات الميزانية العمومية وحسابات الالتزامات المستحقة حسابات صالحة لترحيل ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="9859e-107">يوضح دليل المهام هذا كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="9859e-108">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة الخصم > أكواد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="9859e-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9859e-109">Click New.</span></span>
3. <span data-ttu-id="9859e-110">في الحقل "كود ضريبة الخصم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9859e-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="9859e-111">في الحقل "اسم ضريبة الخصم"، أدخل اسمًا لكود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="9859e-112">في حقل "الحساب الرئيسي"، حدد الحساب الرئيسي لترحيل الخضوع لضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="9859e-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9859e-113">Click Save.</span></span>
7. <span data-ttu-id="9859e-114">انقر فوق "القيم‬".</span><span class="sxs-lookup"><span data-stu-id="9859e-114">Click Values.</span></span>
8. <span data-ttu-id="9859e-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9859e-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9859e-116">في حقل "القيمة"، أدخل النسبة المئوية المستخدمة لاحتساب ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="9859e-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9859e-117">Click Save.</span></span>
11. <span data-ttu-id="9859e-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9859e-118">Close the page.</span></span>
12. <span data-ttu-id="9859e-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9859e-119">Click Save.</span></span>
13. <span data-ttu-id="9859e-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9859e-120">Close the page.</span></span>
14. <span data-ttu-id="9859e-121">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة الخصم‬ > مجموعات ضرائب الخصم‬.</span><span class="sxs-lookup"><span data-stu-id="9859e-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="9859e-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9859e-122">Click New.</span></span>
16. <span data-ttu-id="9859e-123">في الحقل "مجموعة ضرائب الخصم"، أدخل معرف مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="9859e-124">في الحقل "الوصف"، أدخل اسم مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="9859e-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9859e-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="9859e-126">في الحقل "كود ضريبة الخصم"، حدد كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="9859e-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="9859e-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9859e-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="9859e-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9859e-128">Click Save.</span></span>

