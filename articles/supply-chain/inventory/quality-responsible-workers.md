---
title: العاملون المسؤولون عن الموافقة على حالات عدم المطابقة
description: يوضح هذا الموضوع كيفيه تكوين العمال المسؤولين عن اعتماد حالات عدم التوافق.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956537"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="d7bac-103">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7bac-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7bac-104">يوضح هذا الموضوع كيفيه تكوين العمال المسؤولين عن اعتماد حالات عدم التوافق.</span><span class="sxs-lookup"><span data-stu-id="d7bac-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="d7bac-105">يجب اعتماد عدم التوافق قبل ان يتمكن المستخدمون من البدء في إدخال التفاصيل مثل التصحيحات أو العمليات.</span><span class="sxs-lookup"><span data-stu-id="d7bac-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="d7bac-106">قبل ان يتمكن المستخدمون من اعتماد حالات عدم التوافق أو رفضها، يجب ربط معرف المستخدم (سجل المستخدم) الخاص بهم بسجل العامل.</span><span class="sxs-lookup"><span data-stu-id="d7bac-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="d7bac-107">يمكنك اختياريا تكوين العمال المسؤولين عن الجودة، ثم السماح لعامل واحد باعتماد العمل بالنيابة عن عامل آخر.</span><span class="sxs-lookup"><span data-stu-id="d7bac-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="d7bac-108">تمكين المستخدم لمعالجة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="d7bac-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="d7bac-109">قبل أن يتمكن المستخدم من قبول حالات عدم المطابقة أو رفضها، يجب عليك ربط سجل المستخدم الخاص به بسجل عامل.</span><span class="sxs-lookup"><span data-stu-id="d7bac-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="d7bac-110">ويمكن بعد ذلك تعيين حقول الاعتماد تلقائيا، ويمكن ملء المستخدم الحالي تلقائيا بالجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="d7bac-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="d7bac-111">قبل أن يتمكن المستخدم من استخدام ملاحظات المستند، يجب عليك تنشيط معالجة المستندات في خيارات المستخدم الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="d7bac-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="d7bac-112">انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="d7bac-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="d7bac-113">البحث عن وفتح المستخدم الذي يجب ان يكون قادرا علي اعتماد حالات عدم التوافق أو رفضها.</span><span class="sxs-lookup"><span data-stu-id="d7bac-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="d7bac-114">قم بتعيين حقل **الشخص** إلى اسم العامل المرتبط بسجل المستخدم الحالي.</span><span class="sxs-lookup"><span data-stu-id="d7bac-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="d7bac-115">في جزء الإجراءات، حدد **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="d7bac-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="d7bac-116">في صفحة **الخيارات** لسجل المستخدم الحالي، في علامة التبويب **التفضيلات**، قم بتعيين خيار **تمكين معالجة المستند** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="d7bac-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="d7bac-117">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="d7bac-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="d7bac-118">تحديد العاملين المسؤولين عن الجودة</span><span class="sxs-lookup"><span data-stu-id="d7bac-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="d7bac-119">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> العمال المسؤولين عن الجودة**.</span><span class="sxs-lookup"><span data-stu-id="d7bac-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="d7bac-120">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d7bac-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="d7bac-121">في حقل **العامل**، حدد العامل الذي يدخل بيانات الجودة.</span><span class="sxs-lookup"><span data-stu-id="d7bac-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="d7bac-122">في حقل **العامل المسؤول**، حدد العامل الذي يقوم العامل المحدد بإدخال العمل نيابة عنه.</span><span class="sxs-lookup"><span data-stu-id="d7bac-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="d7bac-123">وعند إنشاء حالات عدم التوافق وتحديثها، سيتم إدخال هذا العامل بشكل افتراضي في حقول **العاملين**.</span><span class="sxs-lookup"><span data-stu-id="d7bac-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7bac-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d7bac-124">Additional resources</span></span>

- [<span data-ttu-id="d7bac-125">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="d7bac-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="d7bac-126">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="d7bac-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="d7bac-127">مصاريف الجودة</span><span class="sxs-lookup"><span data-stu-id="d7bac-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="d7bac-128">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7bac-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="d7bac-129">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7bac-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="d7bac-130">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7bac-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="d7bac-131">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="d7bac-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="d7bac-132">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="d7bac-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
