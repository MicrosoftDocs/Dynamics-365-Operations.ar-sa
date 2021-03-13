---
title: طلبات الصيانة
description: يوفر هذا الموضوع نظرة عامة حول إدارة طلبات الصيانة في إدارة الأصول
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019619"
---
# <a name="maintenance-requests"></a><span data-ttu-id="9c384-103">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="9c384-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9c384-104">طلبات الصيانة هي ملاحظات أو إقرارات تم إنشاؤها لإعلام المدير أو المخطط بأن أحد الأصول قد يحتاج إلى مهمة صيانة أو إصلاح، ولكن من دون إنشاء أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="9c384-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="9c384-105">إذا تم اعتبار محتويات طلب الصيانة صالحة، يمكن بعد ذلك إنشاء أمر عمل استنادًا إلى طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9c384-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="9c384-106">يمكن إنشاء طلبات الصيانة لأي أصل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="9c384-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="9c384-107">يمكن إنشاء أنواع مختلفة من طلبات الصيانة، استنادًا إلى كيفية استخدام شركتك لطلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9c384-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="9c384-108">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="9c384-108">Here are some examples:</span></span>

- <span data-ttu-id="9c384-109">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="9c384-109">Maintenance requests</span></span>
- <span data-ttu-id="9c384-110">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="9c384-110">Notes</span></span>
- <span data-ttu-id="9c384-111">التصحيحات أو التحسينات</span><span class="sxs-lookup"><span data-stu-id="9c384-111">Corrections or enhancements</span></span>
- <span data-ttu-id="9c384-112">استثمارات</span><span class="sxs-lookup"><span data-stu-id="9c384-112">Investments</span></span>
- <span data-ttu-id="9c384-113">إصلاح المستودع (يتم استخدام هذا النوع عند تلقي الأصول من موقع آخر بحيث يمكنك القيام بمهمة صيانة أو إصلاح، ثم تقوم بإرجاع الأصل بعد اكتمال المهمة.)</span><span class="sxs-lookup"><span data-stu-id="9c384-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="9c384-114">عرض طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="9c384-114">View maintenance requests</span></span>

<span data-ttu-id="9c384-115">لعرض طلبات الصيانة، حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة** أو **طلبات الصيانة الخاصة بموقع العمل لدي**.</span><span class="sxs-lookup"><span data-stu-id="9c384-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="9c384-116">تعرض كل صفحة قائمة بعض المعلومات المتعلقة بطلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="9c384-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![عرض طلبات الصيانة](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="9c384-118">استخدم صفحة قائمة **طلبات الصيانة الخاصة بموقع العمل لدي** لعرض قائمة بطلبات الصيانة التي تحتوي على مواقع العمل التي ترتبط بها كعامل أو أصول يتم تثبيتها في مواقع عمل ترتبط بها كعامل.</span><span class="sxs-lookup"><span data-stu-id="9c384-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="9c384-119">(لمزيد من المعلومات حول كيفيه إعداد مواقع عمل على عاملي الصيانة، راجع [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="9c384-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="9c384-120">علي الرغم من توفر معلومات حساب العميل في إدارة خدمة الأصول (صيانة خارجية)، إلا أنها لا تتوفر في إدارة الأصول (صيانة داخلية).</span><span class="sxs-lookup"><span data-stu-id="9c384-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="9c384-121">لفتح طريقه عرض تفاصيل أحد السجلات، في صفحة قائمة **جميع طلبات الصيانة**، في طريقة عرض الشبكة، حدد ارتباطًا في عمود **طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="9c384-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![عرض تفاصيل طلب الصيانة.](media/02-manage-maintenance-requests.png)

<span data-ttu-id="9c384-123">تم تنظيم الأزرار الموجودة في جزء الإجراءات على علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="9c384-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="9c384-124">يصف الجدول التالي بإيجاز الأزرار المتعلقة بإدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="9c384-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="9c384-125">اسم الزر</span><span class="sxs-lookup"><span data-stu-id="9c384-125">Button name</span></span>                      | <span data-ttu-id="9c384-126">الوصف</span><span class="sxs-lookup"><span data-stu-id="9c384-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="9c384-127">تحرير</span><span class="sxs-lookup"><span data-stu-id="9c384-127">Edit</span></span>                             | <span data-ttu-id="9c384-128">تحرير طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-129">القيمة الجديدة</span><span class="sxs-lookup"><span data-stu-id="9c384-129">New</span></span>                              | <span data-ttu-id="9c384-130">إنشاء طلب صيانة جديد.</span><span class="sxs-lookup"><span data-stu-id="9c384-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="9c384-131">حذف</span><span class="sxs-lookup"><span data-stu-id="9c384-131">Delete</span></span>                           | <span data-ttu-id="9c384-132">حذف طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-133">مجموعة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="9c384-133">Work order pool</span></span>                  | <span data-ttu-id="9c384-134">ربط طلب الصيانة المحدد بمجموعة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="9c384-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="9c384-135">أمر العمل</span><span class="sxs-lookup"><span data-stu-id="9c384-135">Work order</span></span>                       | <span data-ttu-id="9c384-136">إنشاء أمر عمل استنادًا إلى طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-137">خطأ الأصل‬</span><span class="sxs-lookup"><span data-stu-id="9c384-137">Asset fault</span></span>                      | <span data-ttu-id="9c384-138">انقر **فوق أخطاء الأصل‬**، حيث يمكنك إنشاء تسجيل خاطئ في طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-139">أوامر العمل</span><span class="sxs-lookup"><span data-stu-id="9c384-139">Work orders</span></span>                      | <span data-ttu-id="9c384-140">عرض قائمة بجميع أوامر العمل المرتبطة بطلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-141">تحديث حالة طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="9c384-141">Update maintenance request state</span></span> | <span data-ttu-id="9c384-142">تحديث حالة طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="9c384-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="9c384-143">سجل حالة دورة الحياة</span><span class="sxs-lookup"><span data-stu-id="9c384-143">Lifecycle state log</span></span>              | <span data-ttu-id="9c384-144">عرض سجل يُظهر حالات دورة حياة طلب الصيانة المحدد,</span><span class="sxs-lookup"><span data-stu-id="9c384-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-145">تفاصيل طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="9c384-145">Maintenance request details</span></span>      | <span data-ttu-id="9c384-146">طباعه تقرير يوضح تفاصيل طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-147">إرسال الأصل المقترض</span><span class="sxs-lookup"><span data-stu-id="9c384-147">Send loan asset</span></span>                  | <span data-ttu-id="9c384-148">حدد أصلاً مقترضًا يجب أن يكون بديلاً مؤقتًا للأصل المحدد في طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="9c384-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="9c384-149">الأصل المقترض المرتجع</span><span class="sxs-lookup"><span data-stu-id="9c384-149">Return loan asset</span></span>                | <span data-ttu-id="9c384-150">تسجيل الأصل المقترض كمرتجع.</span><span class="sxs-lookup"><span data-stu-id="9c384-150">Register the loan asset as returned.</span></span> |

