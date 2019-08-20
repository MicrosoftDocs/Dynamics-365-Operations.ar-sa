---
title: إعداد ضريبة الخصم
description: يشرح هذا الموضوع كيفية إعداد ضريبة الخصم.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834724"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="66e7f-103">إعداد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="66e7f-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66e7f-104">يشرح هذا الموضوع كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="66e7f-105">*ضريبة الخصم* هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشاء حركات ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="66e7f-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="66e7f-106">ضريبة الخصم التي يتم حسابها على مدفوعات المورّد يعد التزامًا مستحقًا.</span><span class="sxs-lookup"><span data-stu-id="66e7f-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="66e7f-107">وبالتالي تُعد حسابات الميزانية العمومية وحسابات الالتزامات المستحقة حسابات صالحة لترحيل ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="66e7f-108">يوضح دليل المهام هذا كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="66e7f-109">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة الخصم > أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="66e7f-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-110">Select **New**.</span></span>
3. <span data-ttu-id="66e7f-111">في حقل **كود ضريبة الخصم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66e7f-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="66e7f-112">في حقل **اسم ضريبة الخصم**، أدخل اسم كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="66e7f-113">في حقل **الحساب الرئيسي**، حدد الحساب الرئيسي لترحيل الخضوع لضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="66e7f-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-114">Select **Save**.</span></span>
7. <span data-ttu-id="66e7f-115">حدد **القيم** وضع علامة على السجل المطلوب في القائمة.</span><span class="sxs-lookup"><span data-stu-id="66e7f-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="66e7f-116">في حقل **القيمة**، أدخل النسبة المئوية المستخدمة لاحتساب ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="66e7f-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-117">Select **Save**.</span></span>
10. <span data-ttu-id="66e7f-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66e7f-118">Close the page.</span></span>
11. <span data-ttu-id="66e7f-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-119">Select **Save**.</span></span>
12. <span data-ttu-id="66e7f-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66e7f-120">Close the page.</span></span>
13. <span data-ttu-id="66e7f-121">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة الخصم > مجموعات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="66e7f-122">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-122">Select **New**.</span></span>
15. <span data-ttu-id="66e7f-123">في حقل **مجموعة ضرائب الخصم**، أدخل معرف مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="66e7f-124">في حقل **الوصف**، أدخل اسم مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="66e7f-125">في حقل **كود ضريبة الخصم**، حدد كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="66e7f-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="66e7f-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="66e7f-126">Select **Save**.</span></span>
19. <span data-ttu-id="66e7f-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66e7f-127">Close the page.</span></span>

