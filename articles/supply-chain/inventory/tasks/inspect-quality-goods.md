---
title: فحص جودة البضائع
description: يشرح هذا الموضوع كيفية معالجة أمر جودة.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbfb3733cc52f0f8f54ab4388764429387358ee7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011512"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="a7c3f-103">فحص جودة البضائع</span><span class="sxs-lookup"><span data-stu-id="a7c3f-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7c3f-104">يشرح هذا الموضوع كيفية معالجة أمر جودة.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="a7c3f-105">يمكنك تنفيذ هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="a7c3f-106">قبل بدء هذا الإجراء المستخدم كمثال، تحتاج إلى تأكيد أمر الشراء "000016" وترحيل إيصال استلام منتجات.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="a7c3f-107">سيؤدي ذلك إلى إنشاء أمر جودة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-107">This will automatically create a quality order.</span></span> <span data-ttu-id="a7c3f-108">عادة ما يتم تنفيذ عمليات فحص الجودة من قِبل موظف التحكم في الجودة‬.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="a7c3f-109">تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="a7c3f-109">Select a quality order</span></span>
1. <span data-ttu-id="a7c3f-110">في جزء التنقل، انتقل إلى **الوحدات النمطية >‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="a7c3f-111">حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="a7c3f-112">تسجيل نتائج الاختبار</span><span class="sxs-lookup"><span data-stu-id="a7c3f-112">Record test results</span></span>
1. <span data-ttu-id="a7c3f-113">حدد **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-113">Select **Results**.</span></span>
2. <span data-ttu-id="a7c3f-114">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-114">Select **Edit**.</span></span>
3. <span data-ttu-id="a7c3f-115">في الحقل **كمية النتائج‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="a7c3f-116">في حقل **النتيجة**، حدد السجل المطلوب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="a7c3f-117">في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="a7c3f-118">يمكنك عادة تسجيل نتيجة اختبار أكثر تحديدًا، على سبيل المثال، حجم أو أبعاد أخرى.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="a7c3f-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-119">Select **Save**.</span></span>
6. <span data-ttu-id="a7c3f-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="a7c3f-121">التحقق من صحة أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="a7c3f-121">Validate the quality order</span></span>
1. <span data-ttu-id="a7c3f-122">حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-122">Select **Validate**.</span></span>
2. <span data-ttu-id="a7c3f-123">في الحقل **تم التحقق من الصحة بواسطة‬**، حدد المستخدم الذي يقوم بإجراء الفحص من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="a7c3f-124">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-124">Click **Select**.</span></span>
4. <span data-ttu-id="a7c3f-125">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-125">Select **OK**.</span></span>
5. <span data-ttu-id="a7c3f-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a7c3f-126">Close the page.</span></span>

