---
title: مهام صيانة أوامر العمل المجدولة
description: يوضح هذا الموضوع مهام صيانة أوامر العمل المجدولة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a36a32193d9a4f009c1c56b054a45b7dab0ca50d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215230"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="dfa13-103">مهام الصيانة المجدولة الخاصة بأمر العمل</span><span class="sxs-lookup"><span data-stu-id="dfa13-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="dfa13-104">تعرض صفحة **مهام صيانة أوامر العمل المجدولة‬** نظرة عامة حول أوامر العمل المخصصة لأحد الموارد.</span><span class="sxs-lookup"><span data-stu-id="dfa13-104">The **Scheduled work order maintenance jobs** page shows an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="dfa13-105">يتم إظهار أوامر العمل التي تستخدم أنواع الموارد "الموارد البشرية" و "الأداة" و "الجهاز".</span><span class="sxs-lookup"><span data-stu-id="dfa13-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown.</span></span> <span data-ttu-id="dfa13-106">على سبيل المثال إذا اتصل صباحًا عامل صيانة للإبلاغ بأنه مريض، يمكنك استخدام هذه الصفحة للبحث بسرعة عن أوامر العمل التي تم تخصيصها للعامل، ثم تخصيص عامل صيانة آخر بسرعة للمهمة.</span><span class="sxs-lookup"><span data-stu-id="dfa13-106">For example, if a maintenance worker calls in sick, you can use this page to quickly find work orders allocated to the worker, and then allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="dfa13-107">عرض مهام صيانة أوامر العمل المجدولة</span><span class="sxs-lookup"><span data-stu-id="dfa13-107">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="dfa13-108">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **مهام صيانة أوامر العمل المجدولة‬**.</span><span class="sxs-lookup"><span data-stu-id="dfa13-108">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="dfa13-109">ستري قائمة بكافة أوامر العمل التي تم تعيينها لحالة دورة حياة أمر العمل "مجدول" أو "قيد التقدم".</span><span class="sxs-lookup"><span data-stu-id="dfa13-109">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="dfa13-110">يمكنك فرز القائمة، على سبيل المثال، حسب عامل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="dfa13-110">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="dfa13-111">يمكنك أيضًا استخدام عامل التصفية لتحديد القائمة لعرض أوامر العمل المخصصة لمورد معين أو عامل صيانة معين.</span><span class="sxs-lookup"><span data-stu-id="dfa13-111">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="dfa13-112">يمكنك الاطلاع على ملاحظات حول أمر العمل، وإضافة ملاحظات جديدة، إذا لزم الأمر، عن طريق تحديد مهمة أمر العمل، والنقر فوق **ملاحظات**.</span><span class="sxs-lookup"><span data-stu-id="dfa13-112">You can see notes on the work order and, if required, add new notes by selecting the work order job, and then click **Notes**.</span></span>

4. <span data-ttu-id="dfa13-113">إذا كنت ترغب في تخصيص عامل صيانة واحد إلى أمر عمل، فحدد أمر العمل، وانقر فوق **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="dfa13-113">If you want to allocate one maintenance worker to a work order, select the work order, and then click **Work order**.</span></span>

5. <span data-ttu-id="dfa13-114">عندئذ يتم فتح صفحة **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="dfa13-114">The **Work order** page opens.</span></span> <span data-ttu-id="dfa13-115">انقر فوق **إرسال** لجدولة أمر العمل إلى عامل صيانة معين.</span><span class="sxs-lookup"><span data-stu-id="dfa13-115">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="dfa13-116">اقرأ المزيد حول جدولة عدة أوامر عمل أو أمر عمل واحد في [جدولة أوامر العمل](../work-order-scheduling/schedule-work-orders.md) و[إرسال أمر عمل](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="dfa13-116">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="dfa13-117">تظهر لقطة الشاشة التالية مثال لصفحة **مهام صيانة أوامر العمل المجدولة‬**.</span><span class="sxs-lookup"><span data-stu-id="dfa13-117">The following screenshot shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![الشكل 1](media/07-work-order-scheduling.png)

