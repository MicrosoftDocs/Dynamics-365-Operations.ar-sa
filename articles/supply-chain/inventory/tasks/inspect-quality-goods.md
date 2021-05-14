---
title: فحص جودة البضائع
description: يصف هذا الموضوع كيفية معالجة أوامر الجودة.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956124"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="bc9d2-103">فحص جودة البضائع</span><span class="sxs-lookup"><span data-stu-id="bc9d2-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc9d2-104">يصف هذا الموضوع كيفية معالجة أوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="bc9d2-105">عادة ما يتم إجراء عمليات فحص الجودة بواسطة موظف الجودة.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="bc9d2-106">إذا تم تثبيت بيانات العرض التوضيحي القياسية، يمكنك استخدامها لإكمال الإجراءات في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="bc9d2-107">لاستخدام بيانات العرض التوضيحي، حدد الكيان القانوني *USMF* قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="bc9d2-108">يجب عليك بعد ذلك تأكيد أمر الشراء *000016* وترحيل إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="bc9d2-109">يتم إنشاء أمر الجودة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="bc9d2-110">الخطوة 1: تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="bc9d2-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="bc9d2-111">لتحديد أمر جودة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="bc9d2-112">انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="bc9d2-113">حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="bc9d2-114">الخطوة 2: تسجيل نتائج الاختبار</span><span class="sxs-lookup"><span data-stu-id="bc9d2-114">Step 2: Record test results</span></span>

<span data-ttu-id="bc9d2-115">لتسجيل نتائج الاختبار، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="bc9d2-116">حدد **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-116">Select **Results**.</span></span>
1. <span data-ttu-id="bc9d2-117">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-117">Select **Edit**.</span></span>
1. <span data-ttu-id="bc9d2-118">في الحقل **كمية النتائج‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="bc9d2-119">في حقل **النتيجة**، حدد السجل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="bc9d2-120">في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="bc9d2-121">عادة، سوف تسجل نتيجة اختبار أكثر تحديدًا، مثل الحجم أو البعد الآخر.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="bc9d2-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-122">Select **Save**.</span></span>
1. <span data-ttu-id="bc9d2-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="bc9d2-124">الخطوة 3: التحقق من صحة أمر الجودة</span><span class="sxs-lookup"><span data-stu-id="bc9d2-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="bc9d2-125">للتحقق من صحة أمر الجودة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="bc9d2-126">حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-126">Select **Validate**.</span></span>
1. <span data-ttu-id="bc9d2-127">في حقل **تم التحقق بواسطة**، حدد المستخدم الذي يقوم بالفحص.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="bc9d2-128">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-128">Select **Select**.</span></span>
1. <span data-ttu-id="bc9d2-129">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-129">Select **OK**.</span></span>
1. <span data-ttu-id="bc9d2-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bc9d2-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
