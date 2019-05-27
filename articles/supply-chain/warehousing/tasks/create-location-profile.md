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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bc7705b7db46af8fbe8bf9e78a878a53249b452
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560884"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="6d87a-103">إنشاء ملف تعريف للموقع</span><span class="sxs-lookup"><span data-stu-id="6d87a-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d87a-104">يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع، على سبيل المثال، ما إذا كان الموقع يسمح بأصناف مختلطة.</span><span class="sxs-lookup"><span data-stu-id="6d87a-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="6d87a-105">في هذا الإجراء سوف نقوم بإنشاء ملف تعريف لموقع لا يتطلب التحكم بواسطة لوحة الترخيص‬.</span><span class="sxs-lookup"><span data-stu-id="6d87a-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="6d87a-106">سنقوم بتمكين الأصناف المختلطة وحالات المخزون مختلطة، ونسمح بالجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="6d87a-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="6d87a-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="6d87a-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="6d87a-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6d87a-108">Click New.</span></span>
2. <span data-ttu-id="6d87a-109">في الحقل "معرف ملف تعريف الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6d87a-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="6d87a-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="6d87a-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6d87a-111">في الحقل "تنسيق الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d87a-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="6d87a-112">في الحقل "نوع الموقع‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d87a-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="6d87a-113">في الحقل "‏‫‏‫معرف ملف تعريف إدارة المساحات‬ "، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d87a-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="6d87a-114">حدد "نعم" في حقل "‏‫‏‫السماح بالأصناف المختلطة".</span><span class="sxs-lookup"><span data-stu-id="6d87a-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="6d87a-115">حدد "نعم" في حقل "‏‫‏‫السماح بحالات المخزون المختلطة".</span><span class="sxs-lookup"><span data-stu-id="6d87a-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="6d87a-116">حدد "نعم" في حقل "‏‫السماح بالجرد الدوري‬".</span><span class="sxs-lookup"><span data-stu-id="6d87a-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="6d87a-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="6d87a-117">Click Save.</span></span>
11. <span data-ttu-id="6d87a-118">انتقل إلى إدارة المستودعات‬ > إعداد > المستودع > ملفات تعريف الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="6d87a-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

