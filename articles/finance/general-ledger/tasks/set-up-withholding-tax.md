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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185947"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="5932e-103">إعداد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="5932e-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5932e-104">يشرح هذا الموضوع كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="5932e-105">*ضريبة الخصم* هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشاء حركات ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="5932e-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="5932e-106">ضريبة الخصم التي يتم حسابها على مدفوعات المورّد يعد التزامًا مستحقًا.</span><span class="sxs-lookup"><span data-stu-id="5932e-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="5932e-107">وبالتالي تُعد حسابات الميزانية العمومية وحسابات الالتزامات المستحقة حسابات صالحة لترحيل ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="5932e-108">يوضح دليل المهام هذا كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="5932e-109">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة الخصم > أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="5932e-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="5932e-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5932e-110">Select **New**.</span></span>
3. <span data-ttu-id="5932e-111">في حقل **كود ضريبة الخصم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5932e-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="5932e-112">في حقل **اسم ضريبة الخصم**، أدخل اسم كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="5932e-113">في حقل **الحساب الرئيسي**، حدد الحساب الرئيسي لترحيل الخضوع لضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="5932e-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5932e-114">Select **Save**.</span></span>
7. <span data-ttu-id="5932e-115">حدد **القيم** وضع علامة على السجل المطلوب في القائمة.</span><span class="sxs-lookup"><span data-stu-id="5932e-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="5932e-116">في حقل **القيمة**، أدخل النسبة المئوية المستخدمة لاحتساب ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="5932e-117">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5932e-117">Select **Save**.</span></span>
10. <span data-ttu-id="5932e-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5932e-118">Close the page.</span></span>
11. <span data-ttu-id="5932e-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5932e-119">Select **Save**.</span></span>
12. <span data-ttu-id="5932e-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5932e-120">Close the page.</span></span>
13. <span data-ttu-id="5932e-121">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة الخصم > مجموعات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="5932e-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="5932e-122">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5932e-122">Select **New**.</span></span>
15. <span data-ttu-id="5932e-123">في حقل **مجموعة ضرائب الخصم**، أدخل معرف مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="5932e-124">في حقل **الوصف**، أدخل اسم مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="5932e-125">في حقل **كود ضريبة الخصم**، حدد كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="5932e-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="5932e-126">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5932e-126">Select **Save**.</span></span>
19. <span data-ttu-id="5932e-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5932e-127">Close the page.</span></span>

