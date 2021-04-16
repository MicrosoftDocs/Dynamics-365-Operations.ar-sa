---
title: استكشاف أخطاء مكون المنتج وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع مكوِّن المنتج.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841541"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="f22e3-103">استكشاف أخطاء مكون المنتج وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="f22e3-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="f22e3-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع مكوِّن المنتج.</span><span class="sxs-lookup"><span data-stu-id="f22e3-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="f22e3-105">تتم الكتابة فوق نص الصنف عند تكوين منتج في بند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f22e3-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f22e3-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f22e3-106">Issue description</span></span>

<span data-ttu-id="f22e3-107">تحدث هذه المشكلة عند إنشاء بند أمر المبيعات لصنف قابل للتكوين ثم تعديل نص الصنف.</span><span class="sxs-lookup"><span data-stu-id="f22e3-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="f22e3-108">عند تكوين الصنف ثم تحديد **موافق**، تتم الكتابة فوق النص بالنص القياسي.</span><span class="sxs-lookup"><span data-stu-id="f22e3-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f22e3-109">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f22e3-109">Issue resolution</span></span>

<span data-ttu-id="f22e3-110">هذا السلوك متوقع.</span><span class="sxs-lookup"><span data-stu-id="f22e3-110">This behavior is expected.</span></span> <span data-ttu-id="f22e3-111">يتضمن حقل النص اسم المتغير ، والذي يتم ملؤه فقط بعد تكوين البند.</span><span class="sxs-lookup"><span data-stu-id="f22e3-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="f22e3-112">التالي ، يجب تغيير النص بعد تكوين البند ، وليس قبل ذلك.</span><span class="sxs-lookup"><span data-stu-id="f22e3-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="f22e3-113">تم تقريب سمات الاعداد الصحيحة بشكل غير صحيح عند حساب نماذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="f22e3-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f22e3-114">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f22e3-114">Issue description</span></span>

<span data-ttu-id="f22e3-115">يمكن ان تحدث هذه المشكلة عند تنفيذ السلسلة التالية من الإجراءات:</span><span class="sxs-lookup"><span data-stu-id="f22e3-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="f22e3-116">قم باعداد السمات التالية في أحد نماذج تكوين الإنتاج:</span><span class="sxs-lookup"><span data-stu-id="f22e3-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="f22e3-117">إدخال (عدد صحيح)</span><span class="sxs-lookup"><span data-stu-id="f22e3-117">Input (integer)</span></span>
    - <span data-ttu-id="f22e3-118">بالمائة (عشري)</span><span class="sxs-lookup"><span data-stu-id="f22e3-118">Percent (decimal)</span></span>
    - <span data-ttu-id="f22e3-119">النتيجة (عدد صحيح)</span><span class="sxs-lookup"><span data-stu-id="f22e3-119">Result (integer)</span></span>

2. <span data-ttu-id="f22e3-120">قم بإنشاء عملية حسابية تتضمن التعبير التالي:</span><span class="sxs-lookup"><span data-stu-id="f22e3-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="f22e3-121">*النتيجة* = *الإدخال* × *النسبة المئوية* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="f22e3-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="f22e3-122">في هذه الحالة ، لا تكون نتيجة العدد الصحيح مقربه دائما بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="f22e3-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="f22e3-123">علي سبيل المثال ، يكون الإدخال 1,000 ، والنسبة المئوية هي 2.40.</span><span class="sxs-lookup"><span data-stu-id="f22e3-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="f22e3-124">التالي ، فانك تتوقع ان تكون النتيجة الصحيحة هي 24 ، لان 2.40 بالمائة من 1,000 هي 24 (أو 24.00 بشكل عشري).</span><span class="sxs-lookup"><span data-stu-id="f22e3-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="f22e3-125">بدلا من ذلك ، يتم عرض النتيجة 23.</span><span class="sxs-lookup"><span data-stu-id="f22e3-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="f22e3-126">ومع ذلك ، عندما تكون النسبة المئوية 2.39 ، يتم تقريب الحساب إلى 24 بدلا من 23.</span><span class="sxs-lookup"><span data-stu-id="f22e3-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="f22e3-127">عندما تكون النسبة المئوية 2.50، يتم تقريب الحساب إلى 25 كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="f22e3-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f22e3-128">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f22e3-128">Issue resolution</span></span>

<span data-ttu-id="f22e3-129">تحدث هذه المشكلة بسبب الطريقة التي تستخدمها Microsoft Solver Foundation لتمثيل الأرقام داخليًا باستخدام الكسور.</span><span class="sxs-lookup"><span data-stu-id="f22e3-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="f22e3-130">بالنسبة للمثال السابق ، يتم تمثيل نتيجة عمليه الحساب التي تكون النسبة المئوية فيها 2.40 كما 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="f22e3-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="f22e3-131">عندما يقوم .NET بتحويل هذه القيمة إلى عدد صحيح ، سيتم إرجاع 23.</span><span class="sxs-lookup"><span data-stu-id="f22e3-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="f22e3-132">لن يتم تغيير هذا السلوك ، لان السيناريوهات الأخرى تعتمد عليه.</span><span class="sxs-lookup"><span data-stu-id="f22e3-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="f22e3-133">بالنسبة للمثال السابق ، يمكنك إصلاح المشكلة من خلال تقديم سمه عشريه اضافيه وعمليه حسابيه.</span><span class="sxs-lookup"><span data-stu-id="f22e3-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="f22e3-134">على سبيل المثال، يمكنك اعداد السمات التالية في أحد نماذج تكوين الإنتاج:</span><span class="sxs-lookup"><span data-stu-id="f22e3-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="f22e3-135">إدخال (عدد صحيح)</span><span class="sxs-lookup"><span data-stu-id="f22e3-135">Input (integer)</span></span>
- <span data-ttu-id="f22e3-136">بالمائة (عشري)</span><span class="sxs-lookup"><span data-stu-id="f22e3-136">Percent (decimal)</span></span>
- <span data-ttu-id="f22e3-137">ResultDecimal (عشري)</span><span class="sxs-lookup"><span data-stu-id="f22e3-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="f22e3-138">ResultInteger (عدد صحيح)</span><span class="sxs-lookup"><span data-stu-id="f22e3-138">ResultInteger (integer)</span></span>

<span data-ttu-id="f22e3-139">يمكنك أيضًا إضافة العمليات الحسابية التالية:</span><span class="sxs-lookup"><span data-stu-id="f22e3-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="f22e3-140">*ResultDecimal* = *إدخال* × *النسبة المئوية* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="f22e3-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="f22e3-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="f22e3-141">*ResultInteger* = *ResultDecimal*</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]