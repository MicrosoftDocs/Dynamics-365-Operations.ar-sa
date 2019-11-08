---
title: تمكين حساب الضريبة المؤجل في دفاتر اليومية
description: يوضح هذا الموضوع كيفية تشغيل ميزة حساب الضرائب المؤجلة للمساعدة في تحسين أداء العمليات الحسابية الضريبية عندما يكون عدد بنود دفتر اليومية كبيرًا للغاية.
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
ms.openlocfilehash: e336be5468106007e1f5adf26bf272c88b8b413b
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2623511"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="97b32-103">تمكين حساب الضريبة المؤجل في دفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="97b32-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="97b32-104">يوضح هذا الموضوع كيف يمكنك تأجيل حساب ضريبة المبيعات في دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="97b32-105">وتساعد هذه الإمكانية علي تحسين أداء الحسابات الضريبية عند وجود العديد من بنود دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="97b32-106">بشكل افتراضي، يتم حساب مبالغ ضريبة المبيعات في بنود دفتر اليومية كلما تم تحديث الحقول المتعلقة بالضريبة.</span><span class="sxs-lookup"><span data-stu-id="97b32-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="97b32-107">تتضمن هذه الحقول الحقول الخاصة بمجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.</span><span class="sxs-lookup"><span data-stu-id="97b32-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="97b32-108">يتسبب أي تحديث لبند دفتر اليومية في إعادة حساب مبالغ الضريبة لكافة بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="97b32-109">علي الرغم من أن هذا السلوك يساعد المستخدم في رؤية مبالغ الضرائب المحسوبة في الوقت الفعلي، إلا أنه يمكن أن يؤثر أيضًا علي الأداء إذا كان عدد بنود دفتر اليومية كبيرًا جدًا.</span><span class="sxs-lookup"><span data-stu-id="97b32-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="97b32-110">تتيح لك ميزة حساب الضريبة المؤجلة إمكانية تأجيل حساب الضريبة علي دفاتر اليومية والقيام بذلك بالمساعدة علي إصلاح مشكلات الأداء.</span><span class="sxs-lookup"><span data-stu-id="97b32-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="97b32-111">عندما تكون هذه الميزة قيد التشغيل، سيتم حساب مبلغ الضريبة فقط عند قيام المستخدم بتحديد **ضريبة المبيعات** أو ترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="97b32-112">يمكنك تأجيل حساب ضرائب المبيعات علي ثلاثة مستويات:</span><span class="sxs-lookup"><span data-stu-id="97b32-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="97b32-113">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="97b32-113">Legal entity</span></span>
- <span data-ttu-id="97b32-114">اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="97b32-114">Journal name</span></span>
- <span data-ttu-id="97b32-115">رأس دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="97b32-115">Journal header</span></span>

<span data-ttu-id="97b32-116">يعطي النظام الأولوية لإعداد رأس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="97b32-117">وبشكل افتراضي، يتم الحصول على هذا الإعداد من اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="97b32-118">وبشكل افتراضي، يتم الحصول علي إعداد اسم دفتر اليومية من خلال الإعداد الموجود في صفحة **معلمات دفتر الأستاذ العام** عند إنشاء اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="97b32-119">توضح الأقسام التالية كيفية تشغيل حساب الضريبة المؤجلة للكيانات القانونية وأسماء دفاتر اليومية ورؤوس دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="97b32-120">تشغيل حساب الضريبة المؤجل علي مستوي الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="97b32-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="97b32-121">انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر الأستاذ‬ \> معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="97b32-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="97b32-122">على علامة التبويب **ضريبة المبيعات** ، على علامة التبويب السريعة **عام** ، حدد الخيار **حساب الضريبة المؤجلة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="97b32-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![صورة معلمات دفتر الأستاذ العام](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="97b32-124">تشغيل حساب الضريبة المؤجل علي مستوي اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="97b32-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="97b32-125">انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر اليومية \> أسماء دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="97b32-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="97b32-126">على علامة التبويب السريعة **عام** ، في القسم **ضريبة المبيعات** ، حدد الخيار **حساب الضريبة المؤجل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="97b32-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![صورة أسماء دفاتر اليومية](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="97b32-128">تشغيل حساب الضريبة المؤجل علي مستوي رأس دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="97b32-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="97b32-129">انتقل إلى **دفتر الأستاذ العام \> إدخالات دفتر اليومية \> دفاتر اليومية العامة**‬.</span><span class="sxs-lookup"><span data-stu-id="97b32-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="97b32-130">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="97b32-130">Select **New**.</span></span>
3. <span data-ttu-id="97b32-131">حدد اسم دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="97b32-131">Select a journal name.</span></span>
4. <span data-ttu-id="97b32-132">على علامة التبويب **إعداد** ، قم بتعيين خيار **حساب الضريبة المؤجل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="97b32-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![صورة صفحة دفتر اليومية العام](media/delayed-tax-calculation-journal-header.png)
