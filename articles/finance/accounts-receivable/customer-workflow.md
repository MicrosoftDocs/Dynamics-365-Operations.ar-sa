---
title: سير عمل العميل
description: يوفر هذا الموضوع معلومات حول سير عمل العميل. يمكنك تغيير حقول محددة لأحد العملاء، ثم إرسال هذه التغييرات للموافقة عليها باستخدام سير العمل قبل إضافتها إلى العميل.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175819"
---
# <a name="customer-workflow"></a><span data-ttu-id="6a5be-104">سير عمل العميل</span><span class="sxs-lookup"><span data-stu-id="6a5be-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a5be-105">تمت إضافة سير عمل العميل إلى الإصدار 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="6a5be-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="6a5be-106">يمكنك تغيير حقول محددة لأحد العملاء، ثم إرسال هذه التغييرات للموافقة عليها باستخدام سير العمل قبل إضافتها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="6a5be-107">إعداد سير عمل العميل</span><span class="sxs-lookup"><span data-stu-id="6a5be-107">Set up the customer workflow</span></span>

<span data-ttu-id="6a5be-108">قبل أن تتمكن من استخدام ميزة سير عمل العميل، يجب عليك تمكينها.</span><span class="sxs-lookup"><span data-stu-id="6a5be-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="6a5be-109">انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="6a5be-110">في علامة التبويب **عام**، في علامة التبويب السريعة **الموافقة على العميل**، قم بتعيين خيار **تمكين الموافقات على العملاء** إلى **نعم** لتمكين الميزة.</span><span class="sxs-lookup"><span data-stu-id="6a5be-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="6a5be-111">في حقل **سلوك كيان البيانات**، حدد السلوك الذي يجب أن تستخدمه كيانات البيانات عند استيراد البيانات:</span><span class="sxs-lookup"><span data-stu-id="6a5be-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="6a5be-112">**السماح بالتغييرات دون موافقة** - يمكن لكيان تحديث سجل العميل دون معالجته من خلال سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="6a5be-113">**رفض التغييرات** - لا يمكن إجراء تغييرات على سجل العميل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="6a5be-114">سوف تفشل عملية الاستيراد للحقول التي تم تمكينها لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="6a5be-115">**إنشاء مقترحات التغييرات** - سيتم تغيير جميع الحقول فيما عدا الحقول التي تم تمكينها لسير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="6a5be-116">ستتم إضافة القيم الجديدة لهذه الحقول إلى العميل كمقترحات تغييرات، وسيبدأ تشغيل سير العمل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6a5be-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="6a5be-117">في قائمة حقول العميل، حدد ثم **تمكين** خانة الاختيار لكل حقل يجب أن تتم الموافقة عليه قبل إجراء التغييرات.</span><span class="sxs-lookup"><span data-stu-id="6a5be-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="6a5be-118">انتقل إلى **الحسابات المدينة \> إعداد \> عمليات سير عمل الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="6a5be-119">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-119">Select **New**.</span></span>
7. <span data-ttu-id="6a5be-120">حدد **سير عمل تغيير العميل المقترح**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="6a5be-121">قم بإعداد سير العمل بحيث يتطابق مع عملية الموافقة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="6a5be-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="6a5be-122">سيطبق عنصر الموافقة على سير عمل **الموافقة على سير العمل لتغيير العميل المقترح** التغييرات على العميل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="6a5be-123">تغيير معلومات العميل وإرسال التغييرات إلى سير العمل</span><span class="sxs-lookup"><span data-stu-id="6a5be-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="6a5be-124">عندما تقوم بتغيير حقل تم تمكينه لسير العمل، تظهر صفحة **التغييرات المقترحة**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="6a5be-125">تعرض هذه الصفحة القيمة الأصلية للحقل والقيمة الجديدة التي قمت بإدخالها.</span><span class="sxs-lookup"><span data-stu-id="6a5be-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="6a5be-126">ويتم عكس الحقل الذي قمت بتغييره إلى قيمته الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6a5be-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="6a5be-127">تُعلمك رسالة حالة على الصفحة بأنه لم يتم إرسال التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="6a5be-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="6a5be-128">وفي كل مرة يتم فيها تغيير حقل تم تمكينه لسير العمل، تتم إضافة هذا الحقل إلى قائمة التغييرات المقترحة.</span><span class="sxs-lookup"><span data-stu-id="6a5be-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="6a5be-129">لتجاهل القيمة المقترحة لأحد الحقول، استخدم الزر **تجاهل** الموجود بجوار الحقل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="6a5be-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="6a5be-130">لتجاهل جميع التغييرات، استخدم الزر **تجاهل كل التغييرات** الموجود أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a5be-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="6a5be-131">حدد **موافق** لإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6a5be-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="6a5be-132">بعد أن يتوفر لدك تغيير مقترح واحد على الأقل، تظهر قائمتان إضافيتان في "الجزء الإجراء": **التغييرات المقترحة** و**سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="6a5be-133">حدد **التغييرات المقترحة** لفتح صفحة **التغييرات المقترحة** وقم بمراجعة التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="6a5be-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="6a5be-134">حدد **سير العمل \> إرسال** لإرسال التغييرات إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="6a5be-135">تم تغيير الحالة على الصفحة إلى **التغييرات المعلقة للموافقة**.</span><span class="sxs-lookup"><span data-stu-id="6a5be-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="6a5be-136">يتبع سير العمل عملية سير العمل القياسية في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="6a5be-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="6a5be-137">يتم توجيه القائم بالموافقة إلى صفحة **العميل**، حيث يمكنه مراجعة التغييرات في صفحة **التغييرات المقترحة** ثم تحديد **سير العمل \> موافقة** للموافقة على سير العمل.</span><span class="sxs-lookup"><span data-stu-id="6a5be-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="6a5be-138">بعد إكمال جميع الموافقات، يتم تحديث الحقول بالقيم التي اقترحتها.</span><span class="sxs-lookup"><span data-stu-id="6a5be-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
