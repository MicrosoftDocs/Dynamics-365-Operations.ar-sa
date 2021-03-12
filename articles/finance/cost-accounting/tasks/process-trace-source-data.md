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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4363a51549503327e7decccf38c82db6e75acd88
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990632"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="e2336-103">معالجة وتتبع مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="e2336-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2336-104">يتم تشغيل كافة عمليات معالجة البيانات بواسطة المهام.</span><span class="sxs-lookup"><span data-stu-id="e2336-104">All data processing is run by jobs.</span></span> <span data-ttu-id="e2336-105">لكل وظيفة وموفر بيانات، يتم إنشاء دفتر يومية لتوثيق تشغيل العملية، ومعالجة الإدخالات في الوظيفة الحالية.</span><span class="sxs-lookup"><span data-stu-id="e2336-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="e2336-106">استخدم هذا الإجراء لإعداد مصدر بيانات ثم تتبع أصل إدخال تكلفة محدد.</span><span class="sxs-lookup"><span data-stu-id="e2336-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="e2336-107">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="e2336-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="e2336-108">قبل إتمام هذه المهمة، احرص على تشغيل دلائل المهام التالية "إنشاء دفتر أستاذ محاسبة التكاليف" و"تحديد وحدات التحكم بالتكاليف" و"إدارة مصدر البيانات لدفتر أستاذ محاسبة التكاليف".</span><span class="sxs-lookup"><span data-stu-id="e2336-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="e2336-109">انتقل إلى محاسبة التكاليف > إعداد دفتر الأستاذ > دفاتر أستاذ محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="e2336-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="e2336-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e2336-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e2336-111">حدد دفتر أستاذ محاسبة التكاليف الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="e2336-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="e2336-112">انقر فوق "الإصدارات الفعلية".</span><span class="sxs-lookup"><span data-stu-id="e2336-112">Click Actual versions.</span></span>
4. <span data-ttu-id="e2336-113">في "جزء الإجراءات"، انقر فوق "معالجة البيانات المصدر".</span><span class="sxs-lookup"><span data-stu-id="e2336-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="e2336-114">انقر فوق "دفاتر يومية تحويل إدخال دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="e2336-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="e2336-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e2336-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e2336-116">انقر فوق "إدخالات دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="e2336-116">Click Journal entries.</span></span>
8. <span data-ttu-id="e2336-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e2336-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e2336-118">انقر فوق "إدخالات التكلفة".</span><span class="sxs-lookup"><span data-stu-id="e2336-118">Click Cost entries.</span></span>
10. <span data-ttu-id="e2336-119">انقر فوق "إدخال المصدر".</span><span class="sxs-lookup"><span data-stu-id="e2336-119">Click Source entry.</span></span>
11. <span data-ttu-id="e2336-120">في "جزء الإجراءات"، انقر فوق "معالجة البيانات المصدر".</span><span class="sxs-lookup"><span data-stu-id="e2336-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="e2336-121">انقر فوق "دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="e2336-121">Click General ledger.</span></span>
13. <span data-ttu-id="e2336-122">في حقل "فترة التقويم المالي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e2336-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="e2336-123">لهذا المثال، حدد المالية 2017 الفترة 9.</span><span class="sxs-lookup"><span data-stu-id="e2336-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="e2336-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e2336-124">Click OK.</span></span>

