---
title: إدارة مصدر بيانات لدفتر أستاذ محاسبة التكاليف
description: استخدم هذا الإجراء لإدارة مصدر بيانات دفتر الأستاذ العام لدفتر أستاذ محاسبة التكاليف.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f53101d73bc69199fafb00de0fa1759d59ea4ce8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "319306"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="3c3c8-103">إدارة مصدر بيانات لدفتر أستاذ محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="3c3c8-103">Manage a data source for the cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c3c8-104">استخدم هذا الإجراء لإدارة مصدر بيانات دفتر الأستاذ العام لدفتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="3c3c8-105">قبل إتمام هذه المهمة، احرص على تشغيل دلائل المهام "إنشاء دفتر أستاذ محاسبة التكاليف" و"تحديد وحدات التحكم بالتكاليف".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="3c3c8-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="3c3c8-107">انتقل إلى محاسبة التكاليف > إعداد دفتر الأستاذ > دفاتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="3c3c8-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3c3c8-109">انقر فوق "الإصدارات الفعلية".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-109">Click Actual versions.</span></span>
4. <span data-ttu-id="3c3c8-110">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="3c3c8-111">انقر فوق "دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-111">Click General ledger.</span></span>
6. <span data-ttu-id="3c3c8-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-112">Click New.</span></span>
7. <span data-ttu-id="3c3c8-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="3c3c8-114">في الحقل "موفر البيانات"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="3c3c8-115">لهذا المثال، حدد Dynamics 365 for Finance and Operations - إدخالات دفتر الأستاذ العام .</span><span class="sxs-lookup"><span data-stu-id="3c3c8-115">For this example, select Dynamics 365 for Finance and Operations - General ledger entries.</span></span>  
9. <span data-ttu-id="3c3c8-116">في الحقل "بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="3c3c8-117">بالنسبة إلى هذا المثال، حدد "عناصر التكلفة".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="3c3c8-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-118">Click Save.</span></span>
11. <span data-ttu-id="3c3c8-119">انقر فوق "تكوين موفر البيانات".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="3c3c8-120">في الحقل "الكيان القانوني"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="3c3c8-121">في هذا المثال، حدد USP2.</span><span class="sxs-lookup"><span data-stu-id="3c3c8-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="3c3c8-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-122">Click New.</span></span>
14. <span data-ttu-id="3c3c8-123">في حقل "طبقة الترحيل"، حدد "حالي".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="3c3c8-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3c3c8-124">Click OK.</span></span>

