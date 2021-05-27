---
title: أنواع التشخيص لحالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه استخدام وإنشاء أنواع التشخيصات التي يمكن استخدامها مع حالات عدم التوافق.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022266"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="60c30-103">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="60c30-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60c30-104">يوضح هذا الموضوع كيفيه استخدام وإنشاء أنواع التشخيصات التي يمكن استخدامها مع حالات عدم التوافق.</span><span class="sxs-lookup"><span data-stu-id="60c30-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="60c30-105">يمكنك استخدام صفحة **أنواع التشخيص** لتحديد تصنيف إجراءات التشخيص.</span><span class="sxs-lookup"><span data-stu-id="60c30-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="60c30-106">وبعد ذلك، عندما تقوم بإنشاء تصحيح لعدم توافق، فانك تقوم بتحديد تشخيص.</span><span class="sxs-lookup"><span data-stu-id="60c30-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="60c30-107">يحدد التصحيح نوع إجراء التشخيص الذي ينبغي القيام به لحالة عدم مطابقة معتمدة، وكذلك الشخص الذي ينبغي عليه القيام بالإجراء.</span><span class="sxs-lookup"><span data-stu-id="60c30-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="60c30-108">ويحدد أيضًا تاريخ الاكتمال المطلوب وتاريخ الاكتمال المخطط له.</span><span class="sxs-lookup"><span data-stu-id="60c30-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="60c30-109">أمثلة على أنواع التشخيص</span><span class="sxs-lookup"><span data-stu-id="60c30-109">Examples of diagnostic types</span></span>

<span data-ttu-id="60c30-110">لقد قمت بالعمل لشركه تصنيع، وإذا فشلت العديد من الأصناف في اختبارات جوده فاشله.</span><span class="sxs-lookup"><span data-stu-id="60c30-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="60c30-111">يتم نقل هذه الأصناف إلى منطقه الفحص وتمييزها كمنتجات غير متوافقة.</span><span class="sxs-lookup"><span data-stu-id="60c30-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="60c30-112">يتم إنشاء سجل عدم توافق في Microsoft Dynamics 365 Supply Chain Management لتتبع التفاصيل من خلال حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="60c30-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="60c30-113">في هذه الحالة، تحدث مشكلات الجودة بسبب بيرينجس في الجهاز والتي اختفت في حزم الأصناف وأوفيرهياتينجها.</span><span class="sxs-lookup"><span data-stu-id="60c30-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="60c30-114">والتصحيح الخاص بهذه المشكلة هو استبدال الأجزاء الموجودة في الجهاز.</span><span class="sxs-lookup"><span data-stu-id="60c30-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="60c30-115">عند تكوين أنواع التشخيص، يمكنك إنشاء سجلات متعددة، يمثل كل منها نوعا مختلفا من المشكلات التي قد يمتلكها الجهاز.</span><span class="sxs-lookup"><span data-stu-id="60c30-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="60c30-116">بدلا من ذلك، يمكنك إنشاء نوع تشخيص عام واحد يمثل إصلاح الجهاز.</span><span class="sxs-lookup"><span data-stu-id="60c30-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="60c30-117">إنشاء نوع تشخيص</span><span class="sxs-lookup"><span data-stu-id="60c30-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="60c30-118">انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> أنواع التشخيص**.</span><span class="sxs-lookup"><span data-stu-id="60c30-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="60c30-119">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="60c30-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="60c30-120">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="60c30-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="60c30-121">**التشخيص** – أدخل معرفًا فريدًا أو اسمًا لنوع التشخيص.</span><span class="sxs-lookup"><span data-stu-id="60c30-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="60c30-122">**الوصف** - أدخل وصفًا مفصلاً لنوع التشخيص.</span><span class="sxs-lookup"><span data-stu-id="60c30-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="60c30-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="60c30-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60c30-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="60c30-124">Additional resources</span></span>

- [<span data-ttu-id="60c30-125">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="60c30-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="60c30-126">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="60c30-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="60c30-127">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="60c30-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="60c30-128">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="60c30-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="60c30-129">أنواع المشكلات لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="60c30-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="60c30-130">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="60c30-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="60c30-131">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="60c30-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="60c30-132">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="60c30-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
