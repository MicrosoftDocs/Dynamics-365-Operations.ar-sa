---
title: إنشاء ملف تعريف للموقع
description: يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع، على سبيل المثال، ما إذا كان الموقع يسمح بأصناف مختلطة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847317"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="93bd8-103">إنشاء ملف تعريف للموقع</span><span class="sxs-lookup"><span data-stu-id="93bd8-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93bd8-104">يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع، على سبيل المثال، ما إذا كان الموقع يسمح بأصناف مختلطة.</span><span class="sxs-lookup"><span data-stu-id="93bd8-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="93bd8-105">في هذا الإجراء سوف نقوم بإنشاء ملف تعريف لموقع لا يتطلب التحكم بواسطة لوحة الترخيص‬.</span><span class="sxs-lookup"><span data-stu-id="93bd8-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="93bd8-106">سنقوم بتمكين الأصناف المختلطة وحالات المخزون مختلطة، ونسمح بالجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="93bd8-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="93bd8-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="93bd8-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="93bd8-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="93bd8-108">Click New.</span></span>
2. <span data-ttu-id="93bd8-109">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="93bd8-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="93bd8-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="93bd8-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="93bd8-111">في الحقل "تنسيق الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="93bd8-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="93bd8-112">في الحقل "نوع الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="93bd8-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="93bd8-113">في الحقل "‏‫‏‫معرف ملف تعريف إدارة المساحات‬ "، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="93bd8-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="93bd8-114">حدد "نعم" في حقل "‏‫‏‫السماح بالأصناف المختلطة".</span><span class="sxs-lookup"><span data-stu-id="93bd8-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="93bd8-115">حدد "نعم" في حقل "‏‫‏‫السماح بحالات المخزون المختلطة".</span><span class="sxs-lookup"><span data-stu-id="93bd8-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="93bd8-116">حدد "نعم" في حقل "‏‫السماح بالجرد الدوري‬".</span><span class="sxs-lookup"><span data-stu-id="93bd8-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="93bd8-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="93bd8-117">Click Save.</span></span>
11. <span data-ttu-id="93bd8-118">انتقل إلى إدارة المستودعات‬ > إعداد > المستودع > ملفات تعريف الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="93bd8-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

