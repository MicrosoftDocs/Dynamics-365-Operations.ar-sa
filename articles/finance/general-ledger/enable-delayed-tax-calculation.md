---
title: تمكين حساب الضريبة المؤجل في دفتر اليومية
description: يوضح هذا الموضوع كيفية استخدام ميزة **تمكين حساب الضريبة المؤجل في دفتر اليومية‬** لتحسين أداء حساب الضريبة عندما يكون حجم بنود دفتر اليومية ضخمًا.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176188"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="be158-103">تمكين حساب الضريبة المؤجل في دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="be158-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="be158-104">يوضح هذا الموضوع كيفية استخدام ميزة **تمكين حساب الضريبة المؤجل في دفتر اليومية‬** لتحسين أداء حساب الضريبة عندما يكون حجم بنود دفتر اليومية ضخمًا.</span><span class="sxs-lookup"><span data-stu-id="be158-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="be158-105">يتم تشغيل سلوك حساب ضريبة المبيعات الحالي في الوقت الحقيقي على دفتر اليومية عندما يقوم المستخدم بتحديث حقول الضرائب ذات الصلة، على سبيل المثال، مجموعة ضريبة المبيعات/مجموعة ضريبة مبيعات الأصناف.</span><span class="sxs-lookup"><span data-stu-id="be158-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="be158-106">سيقوم أي تحديث على مستوى بنود دفتر اليومية بإعادة حساب مبلغ الضريبة في كافة بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="be158-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="be158-107">من شأن ذلك أن يساعد المستخدم علي رؤية مبلغ الضريبة المحسوب في الوقت الحقيقي، ولكنه قد يؤدي أيضًا إلى حدوث مشكلة في الأداء إذا كان حجم بنود دفتر اليومية ضخمًا.</span><span class="sxs-lookup"><span data-stu-id="be158-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="be158-108">توفر هذه الميزة خيارًا لتأجيل حساب الضريبة لحل مشكلة الأداء.</span><span class="sxs-lookup"><span data-stu-id="be158-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="be158-109">إذا كان هذه الميزة قيد التشغيل، سيتم حساب مبلغ الضريبة فقط عند قيام المستخدم بالنقر فوق الأمر "ضريبة المبيعات" أو ترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="be158-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="be158-110">بإمكان المستخدم تشغيل/إيقاف تشغيل المعلمة على ثلاثة مستويات:</span><span class="sxs-lookup"><span data-stu-id="be158-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="be158-111">بواسطة الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="be158-111">By legal entity</span></span>
- <span data-ttu-id="be158-112">حسب اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="be158-112">By journal name</span></span>
- <span data-ttu-id="be158-113">حسب رأس دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="be158-113">By journal header</span></span>

<span data-ttu-id="be158-114">سيعتبر النظام قيمة المعلمة في رأس دفتر اليومية قيمة نهائية.</span><span class="sxs-lookup"><span data-stu-id="be158-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="be158-115">ستكون قيمة المعلمة على رأس دفتر اليومية بشكل افتراضي القيمة من اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="be158-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="be158-116">ستكون قيمة المعلمة على اسم دفتر اليومية بشكل افتراضي القيمة من معلمة دفتر الأستاذ العام عند إنشاء اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="be158-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="be158-117">سيتم إخفاء الحقلين "مبلغ ضريبة المبيعات الفعلي" و"مبلغ ضريبة المبيعات المحسوب" على دفتر اليومية في حالة تشغيل هذه المعلمة.</span><span class="sxs-lookup"><span data-stu-id="be158-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="be158-118">الغرض ليس إرباك المستخدم لأن قيمة هذين الحقلين ستعرض دائمًا 0 قبل ان يقوم المستخدم بتشغيل حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="be158-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="be158-119">تمكين حساب الضريبة المؤجل حسب الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="be158-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="be158-120">انتقل إلى **دفتر الأستاذ العام > إعداد دفتر الأستاذ‬ > معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="be158-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="be158-121">انقر فوق علامة التبويب **ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="be158-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="be158-122">ضمن علامة‏‎ التبويب السريعة **عام**، ابحث عن المعلمة **حساب الضريبة المؤجل**، وقم بتشغيلها/إيقاف تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="be158-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="be158-123">تمكين حساب الضريبة المؤجل حسب اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="be158-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="be158-124">انتقل إلى **دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="be158-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="be158-125">ضمن علامة‏‎ التبويب السريعة **عام**، ابحث عن المعلمة **حساب الضريبة المؤجل**، وقم بتشغيلها/إيقاف تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="be158-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="be158-126">تمكين حساب الضريبة المؤجل حسب دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="be158-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="be158-127">انتقل إلى **دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة**‬</span><span class="sxs-lookup"><span data-stu-id="be158-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="be158-128">انقر فوق **جديد**</span><span class="sxs-lookup"><span data-stu-id="be158-128">Click **New**</span></span>
3. <span data-ttu-id="be158-129">حدد اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="be158-129">Select a journal name</span></span>
4. <span data-ttu-id="be158-130">انقر فوق **الإعداد**</span><span class="sxs-lookup"><span data-stu-id="be158-130">Click **Setup**</span></span>
5. <span data-ttu-id="be158-131">ابحث عن المعلمة **حساب الضريبة المؤجل**، وقم بتشغيلها/إيقاف تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="be158-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
