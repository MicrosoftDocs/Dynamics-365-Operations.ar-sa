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
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c911f1a0cd895899f85ae8f5ec4c3fcc847c0cf0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205151"
---
# <a name="maintenance-requests"></a><span data-ttu-id="f28f8-103">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="f28f8-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f28f8-104">طلبات الصيانة هي ملاحظات أو إقرارات تم إنشاؤها لإعلام المدير أو المخطط بأن أحد الأصول قد يحتاج إلى مهمة صيانة أو إصلاح، ولكن من دون إنشاء أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="f28f8-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="f28f8-105">إذا تم اعتبار محتويات طلب الصيانة صالحة، يمكن بعد ذلك إنشاء أمر عمل استنادًا إلى طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="f28f8-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="f28f8-106">يمكن إنشاء طلبات الصيانة لأي أصل في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="f28f8-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="f28f8-107">يمكن إنشاء أنواع مختلفة من طلبات الصيانة، استنادًا إلى كيفية استخدام شركتك لطلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="f28f8-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="f28f8-108">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="f28f8-108">Here are some examples:</span></span>

- <span data-ttu-id="f28f8-109">طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="f28f8-109">Maintenance requests</span></span>
- <span data-ttu-id="f28f8-110">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="f28f8-110">Notes</span></span>
- <span data-ttu-id="f28f8-111">التصحيحات أو التحسينات</span><span class="sxs-lookup"><span data-stu-id="f28f8-111">Corrections or enhancements</span></span>
- <span data-ttu-id="f28f8-112">استثمارات</span><span class="sxs-lookup"><span data-stu-id="f28f8-112">Investments</span></span>
- <span data-ttu-id="f28f8-113">إصلاح المستودع (يتم استخدام هذا النوع عند تلقي الأصول من موقع آخر بحيث يمكنك القيام بمهمة صيانة أو إصلاح، ثم تقوم بإرجاع الأصل بعد اكتمال المهمة.)</span><span class="sxs-lookup"><span data-stu-id="f28f8-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="f28f8-114">عرض طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="f28f8-114">View maintenance requests</span></span>

<span data-ttu-id="f28f8-115">لعرض طلبات الصيانة، حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة** أو **طلبات الصيانة الخاصة بموقع العمل لدي**.</span><span class="sxs-lookup"><span data-stu-id="f28f8-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="f28f8-116">تعرض كل صفحة قائمة بعض المعلومات المتعلقة بطلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="f28f8-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![عرض طلبات الصيانة](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="f28f8-118">استخدم صفحة قائمة **طلبات الصيانة الخاصة بموقع العمل لدي** لعرض قائمة بطلبات الصيانة التي تحتوي على مواقع العمل التي ترتبط بها كعامل أو أصول يتم تثبيتها في مواقع عمل ترتبط بها كعامل.</span><span class="sxs-lookup"><span data-stu-id="f28f8-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="f28f8-119">(لمزيد من المعلومات حول كيفيه إعداد مواقع عمل على عاملي الصيانة، راجع [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="f28f8-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="f28f8-120">علي الرغم من توفر معلومات حساب العميل في إدارة خدمة الأصول (صيانة خارجية)، إلا أنها لا تتوفر في إدارة الأصول (صيانة داخلية).</span><span class="sxs-lookup"><span data-stu-id="f28f8-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="f28f8-121">لفتح طريقه عرض تفاصيل أحد السجلات، في صفحة قائمة **جميع طلبات الصيانة**، في طريقة عرض الشبكة، حدد ارتباطًا في عمود **طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="f28f8-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![عرض تفاصيل طلب الصيانة.](media/02-manage-maintenance-requests.png)

<span data-ttu-id="f28f8-123">تم تنظيم الأزرار الموجودة في جزء الإجراءات على علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="f28f8-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="f28f8-124">يصف الجدول التالي بإيجاز الأزرار المتعلقة بإدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="f28f8-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="f28f8-125">اسم الزر</span><span class="sxs-lookup"><span data-stu-id="f28f8-125">Button name</span></span>                      | <span data-ttu-id="f28f8-126">الوصف</span><span class="sxs-lookup"><span data-stu-id="f28f8-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="f28f8-127">تحرير</span><span class="sxs-lookup"><span data-stu-id="f28f8-127">Edit</span></span>                             | <span data-ttu-id="f28f8-128">تحرير طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-129">القيمة الجديدة</span><span class="sxs-lookup"><span data-stu-id="f28f8-129">New</span></span>                              | <span data-ttu-id="f28f8-130">إنشاء طلب صيانة جديد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="f28f8-131">حذف</span><span class="sxs-lookup"><span data-stu-id="f28f8-131">Delete</span></span>                           | <span data-ttu-id="f28f8-132">حذف طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-133">مجموعة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="f28f8-133">Work order pool</span></span>                  | <span data-ttu-id="f28f8-134">ربط طلب الصيانة المحدد بمجموعة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="f28f8-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="f28f8-135">أمر العمل</span><span class="sxs-lookup"><span data-stu-id="f28f8-135">Work order</span></span>                       | <span data-ttu-id="f28f8-136">إنشاء أمر عمل استنادًا إلى طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-137">خطأ الأصل‬</span><span class="sxs-lookup"><span data-stu-id="f28f8-137">Asset fault</span></span>                      | <span data-ttu-id="f28f8-138">انقر **فوق أخطاء الأصل‬**، حيث يمكنك إنشاء تسجيل خاطئ في طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-139">أوامر العمل</span><span class="sxs-lookup"><span data-stu-id="f28f8-139">Work orders</span></span>                      | <span data-ttu-id="f28f8-140">عرض قائمة بجميع أوامر العمل المرتبطة بطلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-141">تحديث حالة طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="f28f8-141">Update maintenance request state</span></span> | <span data-ttu-id="f28f8-142">تحديث حالة طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="f28f8-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="f28f8-143">سجل حالة دورة الحياة</span><span class="sxs-lookup"><span data-stu-id="f28f8-143">Lifecycle state log</span></span>              | <span data-ttu-id="f28f8-144">عرض سجل يُظهر حالات دورة حياة طلب الصيانة المحدد,</span><span class="sxs-lookup"><span data-stu-id="f28f8-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-145">تفاصيل طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="f28f8-145">Maintenance request details</span></span>      | <span data-ttu-id="f28f8-146">طباعه تقرير يوضح تفاصيل طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-147">إرسال الأصل المقترض</span><span class="sxs-lookup"><span data-stu-id="f28f8-147">Send loan asset</span></span>                  | <span data-ttu-id="f28f8-148">حدد أصلاً مقترضًا يجب أن يكون بديلاً مؤقتًا للأصل المحدد في طلب الصيانة المحدد.</span><span class="sxs-lookup"><span data-stu-id="f28f8-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="f28f8-149">الأصل المقترض المرتجع</span><span class="sxs-lookup"><span data-stu-id="f28f8-149">Return loan asset</span></span>                | <span data-ttu-id="f28f8-150">تسجيل الأصل المقترض كمرتجع.</span><span class="sxs-lookup"><span data-stu-id="f28f8-150">Register the loan asset as returned.</span></span> |

