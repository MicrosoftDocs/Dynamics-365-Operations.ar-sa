---
title: إعداد أكواد السبب
description: يستخدم Dynamics 365 Human Resources رموز السبب لتوضيح سبب تغيير ميزات الموظف.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056338"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="78ea9-103">إعداد أكواد السبب</span><span class="sxs-lookup"><span data-stu-id="78ea9-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="78ea9-104">يستخدم Dynamics 365 Human Resources رموز السبب لتوضيح سبب تغيير ميزات الموظف.</span><span class="sxs-lookup"><span data-stu-id="78ea9-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="78ea9-105">اعتبارا من يناير 2021، يتم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** بدلا من مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="78ea9-106">لمزيد من المعلومات، راجع [ترحيل أكواد السبب يدويًا إلى إدارة العاملين](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="78ea9-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="78ea9-107">إنشاء أكواد سبب</span><span class="sxs-lookup"><span data-stu-id="78ea9-107">Create reason codes</span></span>

1. <span data-ttu-id="78ea9-108">في مساحة عمل **إدارة العاملين** (أو مساحة عمل **إدارة الميزات** إذا لم يتم ترحيل أكواد السبب الخاصة بك بعد) ، حدد **الارتباطات**، ثم حدد **أكواد السبب**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="78ea9-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-109">Select **New**.</span></span>

3. <span data-ttu-id="78ea9-110">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="78ea9-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="78ea9-111">الحقل</span><span class="sxs-lookup"><span data-stu-id="78ea9-111">Field</span></span> | <span data-ttu-id="78ea9-112">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="78ea9-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="78ea9-113">**رمز السبب**</span><span class="sxs-lookup"><span data-stu-id="78ea9-113">**Reason code**</span></span> | <span data-ttu-id="78ea9-114">اسم فريد لتحديد السبب الذي من أجله قام الموظف بتغيير تسجيل خطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="78ea9-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="78ea9-115">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="78ea9-115">**Description**</span></span> | <span data-ttu-id="78ea9-116">وصف كود السبب.</span><span class="sxs-lookup"><span data-stu-id="78ea9-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="78ea9-117">ضمن **السيناريوهات القابلة للتطبيق**، قم بتعيين **إدارة الميزات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="78ea9-118">(غير قابل للتطبيق إذا لم يتم بعد ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** .)</span><span class="sxs-lookup"><span data-stu-id="78ea9-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="78ea9-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="78ea9-120">ترحيل أكواد السبب يدويًا إلى إدارة العاملين</span><span class="sxs-lookup"><span data-stu-id="78ea9-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="78ea9-121">في يناير 2021، يتم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** بدلا من مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="78ea9-122">سيتم تلقائيًا ترحيل معظم بيانات أكواد السبب في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="78ea9-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="78ea9-123">وقد لا يتم ترحيل بعض بيانات كود السبب.</span><span class="sxs-lookup"><span data-stu-id="78ea9-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="78ea9-124">على سبيل المثال، تحتوي أكواد الأسباب الآن على حد أقصى 15 حرفًا، لذلك لن يتم ترحيل أي أكواد سبب أطول من 15 حرفًا تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="78ea9-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="78ea9-125">ستشاهد شعارًا على صفحة **الارتباطات** بمساحة عمل **إدارة الميزات** لاعلامك بالترحيل وما إذا كانت أي أكواد سبب لم يتم ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="78ea9-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="78ea9-126">حدد **أكواد السبب** للاطلاع على التفاصيل المتعلقة بحالة الترحيل.</span><span class="sxs-lookup"><span data-stu-id="78ea9-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="78ea9-127">[![رموز السبب](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="78ea9-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="78ea9-128">حدد كود سبب الفشل في الترحيل.</span><span class="sxs-lookup"><span data-stu-id="78ea9-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="78ea9-129">[![حالة ترحيل كود السبب](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="78ea9-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="78ea9-130">حدد **كود سبب الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="78ea9-131">[![ترحيل رمز السبب](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="78ea9-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="78ea9-132">في جزء **ترحيل كود سبب الميزة**، يتوفر لديك خياران للتعيين إلى كود سبب إدارة العاملين:</span><span class="sxs-lookup"><span data-stu-id="78ea9-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="78ea9-133">لاستخدام كود سبب موجود في إدارة العاملين، اختر واحدًا من القائمة المنسدلة **استخدام كود السبب الموجود**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="78ea9-134">يمكنك فقط استخدام كود سبب موجود في إدارة العاملين إذا لم يتم ترحيل كود سبب إدارة ميزات آخر إليه.</span><span class="sxs-lookup"><span data-stu-id="78ea9-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="78ea9-135">لإنشاء كود سبب جديد في إدارة العاملين، أدخل اسمًا جديدًا في **كود السبب الجديد**، ثم أدخل وصفا في **الوصف الجديد**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="78ea9-136">[![التعيين إلى كود سبب إدارة العاملين](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="78ea9-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="78ea9-137">بعد ترحيل أكواد السبب إلى إدارة العاملين، يتم تعيين الخيار الخاص باستخدامها في إدارة الميزات تلقائيًا إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="78ea9-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="78ea9-138">[![استخدام أكواد السبب في إدارة الميزات](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="78ea9-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]