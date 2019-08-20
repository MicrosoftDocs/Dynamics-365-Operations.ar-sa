---
title: معالجة وتتبع مصدر البيانات
description: يتم تشغيل كافة عمليات معالجة البيانات بواسطة المهام.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6e913f3630862ba07718592cdd039940c5d40b8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841119"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="92bbf-103">معالجة وتتبع مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="92bbf-103">Process and trace source data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92bbf-104">يتم تشغيل كافة عمليات معالجة البيانات بواسطة المهام.</span><span class="sxs-lookup"><span data-stu-id="92bbf-104">All data processing is run by jobs.</span></span> <span data-ttu-id="92bbf-105">لكل وظيفة وموفر بيانات، يتم إنشاء دفتر يومية لتوثيق تشغيل العملية، ومعالجة الإدخالات في الوظيفة الحالية.</span><span class="sxs-lookup"><span data-stu-id="92bbf-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="92bbf-106">استخدم هذا الإجراء لإعداد مصدر بيانات ثم تتبع أصل إدخال تكلفة محدد.</span><span class="sxs-lookup"><span data-stu-id="92bbf-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="92bbf-107">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="92bbf-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="92bbf-108">قبل إتمام هذه المهمة، احرص على تشغيل دلائل المهام التالية "إنشاء دفتر أستاذ محاسبة التكاليف" و"تحديد وحدات التحكم بالتكاليف" و"إدارة مصدر البيانات لدفتر أستاذ محاسبة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="92bbf-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="92bbf-109">انتقل إلى محاسبة التكاليف > إعداد دفتر الأستاذ > دفاتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="92bbf-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="92bbf-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="92bbf-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="92bbf-111">حدد دفتر أستاذ محاسبة التكاليف الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="92bbf-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="92bbf-112">انقر فوق "الإصدارات الفعلية".</span><span class="sxs-lookup"><span data-stu-id="92bbf-112">Click Actual versions.</span></span>
4. <span data-ttu-id="92bbf-113">في "جزء الإجراءات"، انقر فوق "معالجة البيانات المصدر".</span><span class="sxs-lookup"><span data-stu-id="92bbf-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="92bbf-114">انقر فوق "دفاتر يومية تحويل إدخال دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="92bbf-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="92bbf-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="92bbf-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="92bbf-116">انقر فوق "إدخالات دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="92bbf-116">Click Journal entries.</span></span>
8. <span data-ttu-id="92bbf-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="92bbf-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="92bbf-118">انقر فوق "إدخالات التكلفة".</span><span class="sxs-lookup"><span data-stu-id="92bbf-118">Click Cost entries.</span></span>
10. <span data-ttu-id="92bbf-119">انقر فوق "إدخال المصدر".</span><span class="sxs-lookup"><span data-stu-id="92bbf-119">Click Source entry.</span></span>
11. <span data-ttu-id="92bbf-120">في "جزء الإجراءات"، انقر فوق "معالجة البيانات المصدر".</span><span class="sxs-lookup"><span data-stu-id="92bbf-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="92bbf-121">انقر فوق "دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="92bbf-121">Click General ledger.</span></span>
13. <span data-ttu-id="92bbf-122">في حقل "فترة التقويم المالي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="92bbf-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="92bbf-123">لهذا المثال، حدد المالية 2017 الفترة 9.</span><span class="sxs-lookup"><span data-stu-id="92bbf-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="92bbf-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="92bbf-124">Click OK.</span></span>

