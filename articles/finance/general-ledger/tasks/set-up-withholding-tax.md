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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976735"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="a7a8a-103">إعداد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="a7a8a-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7a8a-104">يشرح هذا الموضوع كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="a7a8a-105">*ضريبة الخصم* هي ضريبة يتم احتسابها على المورّدين، والتي لا تقوم بإنشاء حركات ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="a7a8a-106">ضريبة الخصم التي يتم حسابها على مدفوعات المورّد يعد التزامًا مستحقًا.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="a7a8a-107">وبالتالي تُعد حسابات الميزانية العمومية وحسابات الالتزامات المستحقة حسابات صالحة لترحيل ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="a7a8a-108">يوضح دليل المهام هذا كيفية إعداد ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="a7a8a-109">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة الخصم > أكواد ضريبة الخصم** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes** .</span></span>
2. <span data-ttu-id="a7a8a-110">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-110">Select **New** .</span></span>
3. <span data-ttu-id="a7a8a-111">في حقل **كود ضريبة الخصم** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="a7a8a-112">في حقل **اسم ضريبة الخصم** ، أدخل اسم كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="a7a8a-113">في حقل **الحساب الرئيسي** ، حدد الحساب الرئيسي لترحيل الخضوع لضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="a7a8a-114">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-114">Select **Save** .</span></span>
7. <span data-ttu-id="a7a8a-115">حدد **القيم** وضع علامة على السجل المطلوب في القائمة.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="a7a8a-116">في حقل **القيمة** ، أدخل النسبة المئوية المستخدمة لاحتساب ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="a7a8a-117">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-117">Select **Save** .</span></span>
10. <span data-ttu-id="a7a8a-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-118">Close the page.</span></span>
11. <span data-ttu-id="a7a8a-119">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-119">Select **Save** .</span></span>
12. <span data-ttu-id="a7a8a-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-120">Close the page.</span></span>
13. <span data-ttu-id="a7a8a-121">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة الخصم > مجموعات ضريبة الخصم** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups** .</span></span>
14. <span data-ttu-id="a7a8a-122">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-122">Select **New** .</span></span>
15. <span data-ttu-id="a7a8a-123">في حقل **مجموعة ضرائب الخصم** ، أدخل معرف مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="a7a8a-124">في حقل **الوصف** ، أدخل اسم مجموعة ضرائب الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="a7a8a-125">في حقل **كود ضريبة الخصم** ، حدد كود ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="a7a8a-126">حدد **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="a7a8a-126">Select **Save** .</span></span>
19. <span data-ttu-id="a7a8a-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a7a8a-127">Close the page.</span></span>

