---
title: تدفق عمل العميل
description: يوفر هذا الموضوع معلومات حول تدفق عمل العميل. يمكنك تغيير حقول محددة لأحد العملاء، ثم إرسال هذه التغييرات للموافقة عليها باستخدام تدفق العمل قبل إضافتها إلى العميل.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c769d225ee0f7b35719c37d9b9bc690a20060911
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817259"
---
# <a name="customer-workflow"></a><span data-ttu-id="adf1b-104">تدفق عمل العميل</span><span class="sxs-lookup"><span data-stu-id="adf1b-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adf1b-105">تمت إضافة تدفق عمل العميل إلى الإصدار 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="adf1b-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="adf1b-106">يمكنك تغيير حقول محددة لأحد العملاء، ثم إرسال هذه التغييرات للموافقة عليها باستخدام تدفق العمل قبل إضافتها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="adf1b-107">إعداد تدفق عمل العميل</span><span class="sxs-lookup"><span data-stu-id="adf1b-107">Set up the customer workflow</span></span>

<span data-ttu-id="adf1b-108">قبل أن تتمكن من استخدام ميزة تدفق عمل العميل، يجب عليك تمكينها.</span><span class="sxs-lookup"><span data-stu-id="adf1b-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="adf1b-109">انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="adf1b-110">في علامة التبويب **عام**، في علامة التبويب السريعة **الموافقة على العميل**، قم بتعيين خيار **تمكين الموافقات على العملاء** إلى **نعم** لتمكين الميزة.</span><span class="sxs-lookup"><span data-stu-id="adf1b-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="adf1b-111">في حقل **سلوك كيان البيانات**، حدد السلوك الذي يجب أن تستخدمه كيانات البيانات عند استيراد البيانات:</span><span class="sxs-lookup"><span data-stu-id="adf1b-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="adf1b-112">**السماح بالتغييرات دون موافقة** - يمكن لكيان تحديث سجل العميل دون معالجته من خلال تدفق العمل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="adf1b-113">**رفض التغييرات** - لا يمكن إجراء تغييرات على سجل العميل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="adf1b-114">سوف تفشل عملية الاستيراد للحقول التي تم تمكينها لتدفق العمل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="adf1b-115">**إنشاء مقترحات التغييرات** - سيتم تغيير جميع الحقول فيما عدا الحقول التي تم تمكينها لتدفق العمل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="adf1b-116">ستتم إضافة القيم الجديدة لهذه الحقول إلى العميل كمقترحات تغييرات، وسيبدأ تشغيل تدفق العمل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="adf1b-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="adf1b-117">في قائمة حقول العميل، حدد ثم **تمكين** خانة الاختيار لكل حقل يجب أن تتم الموافقة عليه قبل إجراء التغييرات.</span><span class="sxs-lookup"><span data-stu-id="adf1b-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="adf1b-118">انتقل إلى **الحسابات المدينة \> إعداد \> عمليات تدفق عمل الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="adf1b-119">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-119">Select **New**.</span></span>
7. <span data-ttu-id="adf1b-120">حدد **تدفق عمل تغيير العميل المقترح**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="adf1b-121">قم بإعداد تدفق العمل بحيث يتطابق مع عملية الموافقة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="adf1b-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="adf1b-122">سيطبق عنصر الموافقة على تدفق عمل **الموافقة على تدفق العمل لتغيير العميل المقترح** التغييرات على العميل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="adf1b-123">تغيير معلومات العميل وإرسال التغييرات إلى تدفق العمل</span><span class="sxs-lookup"><span data-stu-id="adf1b-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="adf1b-124">عندما تقوم بتغيير حقل تم تمكينه لتدفق العمل، تظهر صفحة **التغييرات المقترحة**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="adf1b-125">تعرض هذه الصفحة القيمة الأصلية للحقل والقيمة الجديدة التي قمت بإدخالها.</span><span class="sxs-lookup"><span data-stu-id="adf1b-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="adf1b-126">ويتم عكس الحقل الذي قمت بتغييره إلى قيمته الأصلية.</span><span class="sxs-lookup"><span data-stu-id="adf1b-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="adf1b-127">تُعلمك رسالة حالة على الصفحة بأنه لم يتم إرسال التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="adf1b-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="adf1b-128">وفي كل مرة يتم فيها تغيير حقل تم تمكينه لتدفق العمل، تتم إضافة هذا الحقل إلى قائمة التغييرات المقترحة.</span><span class="sxs-lookup"><span data-stu-id="adf1b-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="adf1b-129">لتجاهل القيمة المقترحة لأحد الحقول، استخدم الزر **تجاهل** الموجود بجوار الحقل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="adf1b-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="adf1b-130">لتجاهل جميع التغييرات، استخدم الزر **تجاهل كل التغييرات** الموجود أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="adf1b-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="adf1b-131">حدد **موافق** لإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="adf1b-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="adf1b-132">بعد أن يتوفر لدك تغيير مقترح واحد على الأقل، تظهر قائمتان إضافيتان في "الجزء الإجراء": **التغييرات المقترحة** و **تدفق العمل**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="adf1b-133">حدد **التغييرات المقترحة** لفتح صفحة **التغييرات المقترحة** وقم بمراجعة التغييرات التي أجريتها.</span><span class="sxs-lookup"><span data-stu-id="adf1b-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="adf1b-134">حدد **تدفق العمل \> إرسال** لإرسال التغييرات إلى تدفق العمل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="adf1b-135">تم تغيير الحالة على الصفحة إلى **التغييرات المعلقة للموافقة**.</span><span class="sxs-lookup"><span data-stu-id="adf1b-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="adf1b-136">يتبع تدفق العمل عملية سير العمل القياسية في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="adf1b-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="adf1b-137">يتم توجيه القائم بالموافقة إلى صفحة **العميل** ، حيث يمكنه مراجعة التغييرات في صفحة **التغييرات المقترحة** ثم تحديد **تدفق العمل \> موافقة** للموافقة على تدفق العمل.</span><span class="sxs-lookup"><span data-stu-id="adf1b-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="adf1b-138">بعد إكمال جميع الموافقات، يتم تحديث الحقول بالقيم التي اقترحتها.</span><span class="sxs-lookup"><span data-stu-id="adf1b-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]