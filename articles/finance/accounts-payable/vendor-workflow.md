---
title: سير عمل المورّد
description: يمكنك تعديل معلومات المورّد واستخدام سير العمل للموافقة عليه.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e5aef18a7f541c6a0d4abf9d4461d1dd9cd27880
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810260"
---
# <a name="vendor-workflow"></a><span data-ttu-id="8c701-103">سير عمل المورّد</span><span class="sxs-lookup"><span data-stu-id="8c701-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c701-104">عند استخدام سير عمل المورّد، يتم إرسال التغييرات التي يتم إدخالها على حقول محددة إلى سير العمل للموافقة عليها قبل إضافتها إلى المورّد.</span><span class="sxs-lookup"><span data-stu-id="8c701-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="8c701-105">إعداد سير عمل المورّد</span><span class="sxs-lookup"><span data-stu-id="8c701-105">Set up the vendor workflow</span></span>

<span data-ttu-id="8c701-106">قبل استخدام ميزة سير العمل، يجب تمكينها.</span><span class="sxs-lookup"><span data-stu-id="8c701-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="8c701-107">انتقل إلى **الحسابات الدائنة \> الإعداد \> محددات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="8c701-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="8c701-108">على علامة التبويب **عام**، على علامة التبويب السريعة **موافقة المورّد‬**، عيّن الخيار **تمكين موافقات المورّدين‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8c701-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="8c701-109">في الحقل **سلوك وحدة البيانات**، حدد السلوك الذي يجب استخدامه عند استيراد البيانات:</span><span class="sxs-lookup"><span data-stu-id="8c701-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="8c701-110">**السماح بالتغييرات دون الموافقة‬** – بإمكان كيان البيانات تحديث سجل المورّد من دون معالجته عبر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c701-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="8c701-111">**رفض التغييرات** – لا يمكن إجراء تغييرات على سجل المورّد.</span><span class="sxs-lookup"><span data-stu-id="8c701-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="8c701-112">سوف تفشل عملية الاستيراد للحقول التي تم تمكينها لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c701-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="8c701-113">**إنشاء مقترحات التغييرات‬** – سيتم تغيير كافة الحقول فيما عدا الحقول التي تم تمكينها لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c701-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="8c701-114">ستتم إضافة القيم الجديدة لهذه الحقول إلى المورّد كتغييرات مقترحة، وسيبدأ سير العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="8c701-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="8c701-115">في قائمة حقول المورّد، حدد خانة الاختيار **تمكين** لكل حقل يجب أن تتم الموافقة عليه قبل إجراء التغييرات.</span><span class="sxs-lookup"><span data-stu-id="8c701-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="8c701-116">انتقل إلى **الحسابات الدائنة \> الإعداد \> عمليات سير عمل الحسابات الدائنة‬**.</span><span class="sxs-lookup"><span data-stu-id="8c701-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="8c701-117">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c701-117">Select **New**.</span></span>
7. <span data-ttu-id="8c701-118">حدد **سير عمل تغييرات الموردين المقترحة‬**.</span><span class="sxs-lookup"><span data-stu-id="8c701-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="8c701-119">قم بإعداد سير العمل بحيث يتوافق مع عملية الموافقة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8c701-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="8c701-120">سيقوم عنصر الموافقة على سير العمل **موافقة سير العمل لتغيير المورد المقترح‬** بتطبيق التغييرات على المورّد.</span><span class="sxs-lookup"><span data-stu-id="8c701-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="8c701-121">تغيير معلومات المورّد وإرسال التغييرات إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="8c701-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="8c701-122">عندما تقوم بتغيير حقل تم تمكينه لسير العمل، تظهر صفحة **التغييرات المقترحة‬**.</span><span class="sxs-lookup"><span data-stu-id="8c701-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="8c701-123">تعرض هذه الصفحة القيمة الأصلية للحقل والقيمة الجديدة التي قمت بإدخالها.</span><span class="sxs-lookup"><span data-stu-id="8c701-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="8c701-124">ويتم عكس الحقل الذي قمت بتغييره إلى قيمته الأصلية.</span><span class="sxs-lookup"><span data-stu-id="8c701-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="8c701-125">تظهر أيضًا رسالة حالة تعلمك بعدم إرسال تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="8c701-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="8c701-126">في كل مرة تقوم فيها بتغيير حقل تم تمكينه لسير العمل، يُضاف هذا الحقل إلى القائمة في صفحة **التغييرات المقترحة‬**.</span><span class="sxs-lookup"><span data-stu-id="8c701-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="8c701-127">لتجاهل القيمة المقترحة لأحد الحقول، استخدم الزر **تجاهل** الموجود إلى جانب الحقل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="8c701-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="8c701-128">لتجاهل كافة التغييرات، استخدم الزر **تجاهل كافة التغييرات** أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c701-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="8c701-129">حدد **موافق** لإغلاق الصحة.</span><span class="sxs-lookup"><span data-stu-id="8c701-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="8c701-130">بعد إجراء تغيير مقترح واحد على الأقل، تظهر علامتا تبويب إضافيتان في جزء الإجراءات: **التغييرات‏‎ المقترحة** و **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="8c701-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="8c701-131">حدد **التغييرات المقترحة** لفتح صفحة **التغييرات المقترحة** ومراجعة التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="8c701-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="8c701-132">حدد **سير العمل \> لإرسال التغييرات إلى سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="8c701-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="8c701-133">تم تغيير الحالة على الصفحة إلى **الموافقة على التغييرات المعلقة**.</span><span class="sxs-lookup"><span data-stu-id="8c701-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="8c701-134">يتبع سير العمل عملية سير العمل القياسية.</span><span class="sxs-lookup"><span data-stu-id="8c701-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="8c701-135">يتم توجيه القائم بالموافقة إلى صفحة **المورد**، حيث يمكنه مراجعة التغييرات في صفحة **التغييرات المقترحة** ثم تحديد **سير العمل \> موافقة** للموافقة على سير العمل.</span><span class="sxs-lookup"><span data-stu-id="8c701-135">The approver is directed to the **Vendor** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="8c701-136">بعد إكمال جميع الموافقات، يتم تحديث الحقول بالقيم التي اقترحتها.</span><span class="sxs-lookup"><span data-stu-id="8c701-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]