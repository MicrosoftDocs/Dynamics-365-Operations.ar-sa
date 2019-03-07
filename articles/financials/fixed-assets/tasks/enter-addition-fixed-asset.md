---
title: إدخال إضافة إلى الأصول الثابتة
description: يوضح هذا الإجراء كيفية زيادة إضافة إلى أصل ثابت موجود.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "324412"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="404d4-103">إدخال إضافة إلى الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="404d4-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="404d4-104">يوضح هذا الإجراء كيفية زيادة إضافة إلى أصل ثابت موجود.</span><span class="sxs-lookup"><span data-stu-id="404d4-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="404d4-105">غرض إضافات الأصول الثابتة هو تعقب إضافات الأصناف أو صيانة الأصل أو التحسينات التي تم إدخالها عليه، وهو إعلامي فقط.</span><span class="sxs-lookup"><span data-stu-id="404d4-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="404d4-106">يجب إجراء أية تغييرات على قيمة الأصول الثابتة أو مدة خدمتها بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="404d4-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="404d4-107">يستخدم هذا الإجراء دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="404d4-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="404d4-108">انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="404d4-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="404d4-109">في القائمة، ابحث عن الأصل الثابت المراد إضافته وحدده.</span><span class="sxs-lookup"><span data-stu-id="404d4-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="404d4-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="404d4-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="404d4-111">في جزء الإجراءات، انقر فوق "أصل ثابت".</span><span class="sxs-lookup"><span data-stu-id="404d4-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="404d4-112">انقر فوق "إضافات الأصل الثابت".</span><span class="sxs-lookup"><span data-stu-id="404d4-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="404d4-113">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="404d4-113">Click New.</span></span>
7. <span data-ttu-id="404d4-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="404d4-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="404d4-115">عيّن تاريخ شراء الإضافة أو الخدمة.</span><span class="sxs-lookup"><span data-stu-id="404d4-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="404d4-116">أدخل تكلفة الصنف أو الصيانة أو التحسينات الأخرى التي تمت على الأصل.</span><span class="sxs-lookup"><span data-stu-id="404d4-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="404d4-117">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="404d4-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="404d4-118">لن يكون لإجمال التكلفة أي تأثير على قيمة الأصل الثابت وهو يستخدم لأغراض التعقب وأغراض إعلامية فقط.</span><span class="sxs-lookup"><span data-stu-id="404d4-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="404d4-119">إذا كانت ستتم رسملة التكلفة، فيجب ترحيل حركة تسوية الشطب بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="404d4-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="404d4-120">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="404d4-120">Click the General tab.</span></span>
    * <span data-ttu-id="404d4-121">حدد "زيادة مدة الخدمة" إذا كانت الإضافة ستزيد مدة خدمة الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="404d4-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="404d4-122">هذا الحقل للأغراض المعلوماتية فقط.</span><span class="sxs-lookup"><span data-stu-id="404d4-122">This field is informational only.</span></span> <span data-ttu-id="404d4-123">لزيادة مدة الخدمة، قم بتعديل مدة الخدمة على نماذج القيمة و/أو دفاتر الإهلاك للأصل.</span><span class="sxs-lookup"><span data-stu-id="404d4-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

