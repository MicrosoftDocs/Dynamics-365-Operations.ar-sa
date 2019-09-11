---
title: إنشاء ملف تعريف للموقع
description: يشرح هذا الموضوع كيفية إنشاء ملف تعريف الموقع في Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866969"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="9aa25-103">إنشاء ملف تعريف للموقع</span><span class="sxs-lookup"><span data-stu-id="9aa25-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9aa25-104">يشرح هذا الموضوع كيفية إنشاء ملف تعريف الموقع في Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9aa25-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9aa25-105">يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع، على سبيل المثال، ما إذا كان الموقع يسمح بأصناف مختلطة.</span><span class="sxs-lookup"><span data-stu-id="9aa25-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="9aa25-106">في هذا الإجراء سوف نقوم بإنشاء ملف تعريف لموقع لا يتطلب التحكم بواسطة لوحة الترخيص‬.</span><span class="sxs-lookup"><span data-stu-id="9aa25-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="9aa25-107">سنقوم بتمكين الأصناف المختلطة وحالات المخزون مختلطة، ونسمح بالجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="9aa25-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="9aa25-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="9aa25-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="9aa25-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المستودعات > الإعداد > المستودع > ملفات تعريف الموقع**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="9aa25-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-110">Select **New**.</span></span>
3. <span data-ttu-id="9aa25-111">في الحقل **معرف ملف تعريف الموقع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9aa25-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="9aa25-112">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9aa25-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9aa25-113">أدخل قيمة أو حددها في الحقل **تنسيق الموقع**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="9aa25-114">أدخل قيمة أو حددها في الحقل **نوع الموقع‬**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="9aa25-115">أدخل قيمة أو حددها في الحقل في الحقل **‏‫‏‫معرف ملف تعريف إدارة المساحات‬**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="9aa25-116">حدد **نعم** في حقل **السماح بالأصناف المختلطة**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="9aa25-117">حدد **نعم** في حقل **السماح بحالات المخزون المختلطة**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="9aa25-118">حدد **نعم** في حقل **السماح بالجرد الدوري**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="9aa25-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9aa25-119">Select **Save**.</span></span>

