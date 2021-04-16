---
title: التسلسل الرقمي الموحد لمعرفات الوظائف
description: توفر هذه الميزة تسلسلًا رقميًا واحدًا وموحدًا يقوم بإنشاء معرفات الوظائف للتحكم في الإنتاج وتنفيذ التصنيع والوحدات للوقت والحضور.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824931"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="855c6-103">التسلسل الرقمي الموحد لمعرفات الوظائف</span><span class="sxs-lookup"><span data-stu-id="855c6-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="855c6-104">توفر هذه الميزة تسلسلًا رقميًا واحدًا وموحدًا يقوم بإنشاء معرفات الوظائف للتحكم في الإنتاج وتنفيذ التصنيع والوحدات للوقت والحضور.</span><span class="sxs-lookup"><span data-stu-id="855c6-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="855c6-105">في السابق، كنت قادرًا على اختيار تسلسل رقمي مختلف لكل من هذه الوحدات، مما قد يؤدي إلى تضارب معرفات الوظائف إذا استخدم اثنان أو أكثر من هذه التسلسلات تنسيقًا متطابقًا.</span><span class="sxs-lookup"><span data-stu-id="855c6-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="855c6-106">يمكن ان يتسبب مثل هذا التعارض في تلف البيانات.</span><span class="sxs-lookup"><span data-stu-id="855c6-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="855c6-107">تشغيل هذه الميزة في نظامك</span><span class="sxs-lookup"><span data-stu-id="855c6-107">Turn on this feature for your system</span></span>

<span data-ttu-id="855c6-108">إذا لم يتضمن نظامك الميزة الموضحة في هذا الموضوع بالفعل، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) وقم بتشغيل ميزة *التسلسل الرقمي الموحد لمعرفات الوظائف‬*.</span><span class="sxs-lookup"><span data-stu-id="855c6-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="855c6-109">إعداد التسلسل الرقمي الموحد لمعرفات الوظائف</span><span class="sxs-lookup"><span data-stu-id="855c6-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="855c6-110">بعد تمكين هذه الميزة، سيتم إهلاك إعدادات التسلسل الرقمي **تعريف الوظيفة** الموجودة في صفحات المعلمات لوحدات الوقت والحضور، وتنفيذ التصنيع، ومراقبة الإنتاج، وستتم إضافة حقل **معرف الوظيفة الموحد** جديد.</span><span class="sxs-lookup"><span data-stu-id="855c6-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="855c6-111">تتم مشاركة قيمة **معرف الوظيفة الموحد** بواسطة كافة الوحدات الثلاث، ومن ثمَّ التاكد من ان كافة الوحدات تشير إلى نفس التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="855c6-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="855c6-112">وبالتالي، ستكون معرّفات الوظائف فريدة في جميع الوحدات الثلاث ولن يحدث تعارض أبدًا.</span><span class="sxs-lookup"><span data-stu-id="855c6-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="855c6-113">لإعداد التسلسل الرقمي الموحد لمعرفات الوظائف:</span><span class="sxs-lookup"><span data-stu-id="855c6-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="855c6-114">قم بتشغيل الميزة كما هو موضح في المقطع السابق.</span><span class="sxs-lookup"><span data-stu-id="855c6-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="855c6-115">قم بتحديد التسلسل الرقمي الذي ترغب في استخدامه لمعرفات الوظيفة الموحدة، أو قم بإنشاء معرفات جديده.</span><span class="sxs-lookup"><span data-stu-id="855c6-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="855c6-116">لمزيد من المعلومات، راجع [مراجعة عامة حول التسلسلات الرقمية](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="855c6-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="855c6-117">انتقل إلى صفحة **معلمات مراقبة الإنتاج** أو **معلمات تنفيذ التصنيع** أو **معلمات الوقت والحضور**.</span><span class="sxs-lookup"><span data-stu-id="855c6-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="855c6-118">لا يهم أي واحد تختاره لأنه عند إجراء هذا الإعداد على أي من هذه الصفحات، سيتم تحديث جميع الصفحات الأخرى تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="855c6-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="855c6-119">افتح علامة التبويب **التسلسلات الرقمية** على صفحة المعلمات المحددة.</span><span class="sxs-lookup"><span data-stu-id="855c6-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="855c6-120">قم بتعيين **رمز التسلسل الرقمي** الذي قمت بتحديده مسبقا لصف **معرفات الوظائف الموحدة** الخاصة بالشبكة.</span><span class="sxs-lookup"><span data-stu-id="855c6-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
