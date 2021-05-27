---
title: طلبات الصيانة
description: يوفر هذا الموضوع نظرة عامة حول إدارة طلبات الصيانة في إدارة الأصول
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c72a16b8f3865129ad737c511e50eb34c9f2e91
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015867"
---
# <a name="maintenance-requests"></a><span data-ttu-id="79337-103">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="79337-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79337-104">طلبات الصيانة هي ملاحظات أو إقرارات تم إنشاؤها لإعلام المدير أو المخطط بأن أحد الأصول قد يحتاج إلى مهمة صيانة أو إصلاح، ولكن من دون إنشاء أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="79337-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="79337-105">إذا تم اعتبار محتويات طلب الصيانة صالحة، يمكن بعد ذلك إنشاء أمر عمل استنادًا إلى طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="79337-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="79337-106">يمكن إنشاء طلبات الصيانة لأي أصل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="79337-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="79337-107">يمكن إنشاء أنواع مختلفة من طلبات الصيانة، استنادًا إلى كيفية استخدام شركتك لطلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="79337-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="79337-108">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="79337-108">Here are some examples:</span></span>

- <span data-ttu-id="79337-109">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="79337-109">Maintenance requests</span></span>
- <span data-ttu-id="79337-110">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="79337-110">Notes</span></span>
- <span data-ttu-id="79337-111">التصحيحات أو التحسينات</span><span class="sxs-lookup"><span data-stu-id="79337-111">Corrections or enhancements</span></span>
- <span data-ttu-id="79337-112">استثمارات</span><span class="sxs-lookup"><span data-stu-id="79337-112">Investments</span></span>
- <span data-ttu-id="79337-113">إصلاح المستودع (يتم استخدام هذا النوع عند تلقي الأصول من موقع آخر بحيث يمكنك القيام بمهمة صيانة أو إصلاح، ثم تقوم بإرجاع الأصل بعد اكتمال المهمة.)</span><span class="sxs-lookup"><span data-stu-id="79337-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="79337-114">عرض طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="79337-114">View maintenance requests</span></span>

<span data-ttu-id="79337-115">لعرض طلبات الصيانة، حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة** أو **طلبات الصيانة الخاصة بموقع العمل لدي**.</span><span class="sxs-lookup"><span data-stu-id="79337-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="79337-116">تعرض كل صفحة قائمة بعض المعلومات المتعلقة بطلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="79337-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![عرض طلبات الصيانة](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="79337-118">استخدم صفحة قائمة **طلبات الصيانة الخاصة بموقع العمل لدي** لعرض قائمة بطلبات الصيانة التي تحتوي على مواقع العمل التي ترتبط بها كعامل أو أصول يتم تثبيتها في مواقع عمل ترتبط بها كعامل.</span><span class="sxs-lookup"><span data-stu-id="79337-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="79337-119">(لمزيد من المعلومات حول كيفيه إعداد مواقع عمل على عاملي الصيانة، راجع [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="79337-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="79337-120">علي الرغم من توفر معلومات حساب العميل في إدارة خدمة الأصول (صيانة خارجية)، إلا أنها لا تتوفر في إدارة الأصول (صيانة داخلية).</span><span class="sxs-lookup"><span data-stu-id="79337-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="79337-121">لفتح طريقه عرض تفاصيل أحد السجلات، في صفحة قائمة **جميع طلبات الصيانة**، في طريقة عرض الشبكة، حدد ارتباطًا في عمود **طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="79337-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![عرض تفاصيل طلب الصيانة.](media/02-manage-maintenance-requests.png)

<span data-ttu-id="79337-123">تم تنظيم الأزرار الموجودة في جزء الإجراءات على علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="79337-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="79337-124">يصف الجدول التالي بإيجاز الأزرار المتعلقة بإدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="79337-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="79337-125">اسم الزر</span><span class="sxs-lookup"><span data-stu-id="79337-125">Button name</span></span>                      | <span data-ttu-id="79337-126">الوصف</span><span class="sxs-lookup"><span data-stu-id="79337-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="79337-127">تحرير</span><span class="sxs-lookup"><span data-stu-id="79337-127">Edit</span></span>                             | <span data-ttu-id="79337-128">تحرير طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-129">القيمة الجديدة</span><span class="sxs-lookup"><span data-stu-id="79337-129">New</span></span>                              | <span data-ttu-id="79337-130">إنشاء طلب صيانة جديد.</span><span class="sxs-lookup"><span data-stu-id="79337-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="79337-131">حذف</span><span class="sxs-lookup"><span data-stu-id="79337-131">Delete</span></span>                           | <span data-ttu-id="79337-132">حذف طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-133">مجموعة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="79337-133">Work order pool</span></span>                  | <span data-ttu-id="79337-134">ربط طلب الصيانة المحدد بمجموعة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="79337-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="79337-135">أمر العمل</span><span class="sxs-lookup"><span data-stu-id="79337-135">Work order</span></span>                       | <span data-ttu-id="79337-136">إنشاء أمر عمل استنادًا إلى طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-137">خطأ الأصل‬</span><span class="sxs-lookup"><span data-stu-id="79337-137">Asset fault</span></span>                      | <span data-ttu-id="79337-138">انقر **فوق أخطاء الأصل‬**، حيث يمكنك إنشاء تسجيل خاطئ في طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-139">أوامر العمل</span><span class="sxs-lookup"><span data-stu-id="79337-139">Work orders</span></span>                      | <span data-ttu-id="79337-140">عرض قائمة بجميع أوامر العمل المرتبطة بطلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-141">تحديث حالة طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="79337-141">Update maintenance request state</span></span> | <span data-ttu-id="79337-142">تحديث حالة طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="79337-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="79337-143">سجل حالة دورة الحياة</span><span class="sxs-lookup"><span data-stu-id="79337-143">Lifecycle state log</span></span>              | <span data-ttu-id="79337-144">عرض سجل يُظهر حالات دورة حياة طلب الصيانة المحدد,</span><span class="sxs-lookup"><span data-stu-id="79337-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-145">تفاصيل طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="79337-145">Maintenance request details</span></span>      | <span data-ttu-id="79337-146">طباعه تقرير يوضح تفاصيل طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-147">إرسال الأصل المقترض</span><span class="sxs-lookup"><span data-stu-id="79337-147">Send loan asset</span></span>                  | <span data-ttu-id="79337-148">حدد أصلاً مقترضًا يجب أن يكون بديلاً مؤقتًا للأصل المحدد في طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="79337-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="79337-149">الأصل المقترض المرتجع</span><span class="sxs-lookup"><span data-stu-id="79337-149">Return loan asset</span></span>                | <span data-ttu-id="79337-150">تسجيل الأصل المقترض كمرتجع.</span><span class="sxs-lookup"><span data-stu-id="79337-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]