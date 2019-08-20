---
title: فحص جودة البضائع
description: يشرح هذا الموضوع كيفية معالجة أمر جودة.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855676"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="3fdc7-103">فحص جودة البضائع</span><span class="sxs-lookup"><span data-stu-id="3fdc7-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3fdc7-104">يشرح هذا الموضوع كيفية معالجة أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="3fdc7-105">يمكنك تنفيذ هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="3fdc7-106">قبل بدء هذا الإجراء المستخدم كمثال، تحتاج إلى تأكيد أمر الشراء "000016" وترحيل إيصال استلام منتجات.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="3fdc7-107">سيؤدي ذلك إلى إنشاء أمر جودة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-107">This will automatically create a quality order.</span></span> <span data-ttu-id="3fdc7-108">عادة ما يتم تنفيذ عمليات فحص الجودة من قِبل موظف التحكم في الجودة‬.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="3fdc7-109">تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="3fdc7-109">Select a quality order</span></span>
1. <span data-ttu-id="3fdc7-110">في جزء التنقل، انتقل إلى **الوحدات النمطية >‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="3fdc7-111">حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="3fdc7-112">تسجيل نتائج الاختبار</span><span class="sxs-lookup"><span data-stu-id="3fdc7-112">Record test results</span></span>
1. <span data-ttu-id="3fdc7-113">حدد **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-113">Select **Results**.</span></span>
2. <span data-ttu-id="3fdc7-114">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-114">Select **Edit**.</span></span>
3. <span data-ttu-id="3fdc7-115">في الحقل **كمية النتائج‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="3fdc7-116">في حقل **النتيجة**، حدد السجل المطلوب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="3fdc7-117">في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="3fdc7-118">يمكنك عادة تسجيل نتيجة اختبار أكثر تحديدًا، على سبيل المثال، حجم أو أبعاد أخرى.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="3fdc7-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-119">Select **Save**.</span></span>
6. <span data-ttu-id="3fdc7-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="3fdc7-121">التحقق من صحة أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="3fdc7-121">Validate the quality order</span></span>
1. <span data-ttu-id="3fdc7-122">حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-122">Select **Validate**.</span></span>
2. <span data-ttu-id="3fdc7-123">في الحقل **تم التحقق من الصحة بواسطة‬**، حدد المستخدم الذي يقوم بإجراء الفحص من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="3fdc7-124">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-124">Click **Select**.</span></span>
4. <span data-ttu-id="3fdc7-125">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-125">Select **OK**.</span></span>
5. <span data-ttu-id="3fdc7-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3fdc7-126">Close the page.</span></span>

