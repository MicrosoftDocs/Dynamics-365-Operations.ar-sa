---
title: أنواع أمر العمل
description: يشرح هذا الموضوع أنواع أوامر العمل في إدارة الأصول.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6bdc9d226d8e1aa6960cac38b95b0245e46ee1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825580"
---
# <a name="work-order-types"></a><span data-ttu-id="090e7-103">أنواع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="090e7-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="090e7-104">يتم استخدام أنواع أوامر العمل لتصنيف أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="090e7-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="090e7-105">على سبيل المثال، قد يكون لديك أنواع أوامر عمل تتعلق بالصيانة الوقائية أو الصيانة التصحيحية.</span><span class="sxs-lookup"><span data-stu-id="090e7-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="090e7-106">يحدد نوع أمر العمل تبعية مع نموذج دورو حياة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="090e7-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="090e7-107">يحدد نموذج دورة حياة أمر العمل حالات دورة حياة أمر العمل التي يمكن تعيينها على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="090e7-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="090e7-108">(تتضمن أمثلة حالات دورة حياة أمر العمل **تم الإنشاء** و **قيد التنفيذ‬** و **منتهي**.)</span><span class="sxs-lookup"><span data-stu-id="090e7-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="090e7-109">لمزيد من المعلومات حول حالات دورة حياة أمر العمل ومراحل المشروع، راجع [حالات دورة حياة أمر العمل](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="090e7-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="090e7-110">حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **أنواع أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="090e7-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="090e7-111">حدد **جديد** لإنشاء أمر عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="090e7-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="090e7-112">في الحقل **نوع أمر العمل**، أدخل معرفًا لنوع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="090e7-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="090e7-113">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="090e7-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="090e7-114">في الحقل **نموذج دورة حياة أمر العمل‬**، حدد نموذج دورة حياة.</span><span class="sxs-lookup"><span data-stu-id="090e7-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="090e7-115">عيّن الخيار **عامل صيانة واحد‬‏‫** إلى to **نعم** إذا كان يجب تعيين جميع وظائف أمر العمل التي ترتبط بأمر عمل من هذا النوع إلى عامل الصيانة نفسه.</span><span class="sxs-lookup"><span data-stu-id="090e7-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="090e7-116">في الحقل **نوع التكلفة**، حدد **تصحيحي** أو **وقائي** أو **استثمار**، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="090e7-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="090e7-117">يجب أن يكون نوع التكلفة هو نفسه لجميع وظائف أمر العمل على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="090e7-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="090e7-118">في القسم **إلزامي**، عيّن الخيارات ذات الصلة إلى **نعم** لتحديد المعلومات المتعلقة بالأخطاء أو المتعلقة بوقت تعطل الصيانة التي تُضاف إلى أمر عمل من هذا النوع</span><span class="sxs-lookup"><span data-stu-id="090e7-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="090e7-119">ترتبط الخيارات في القسم **إلزامي** بالخيارات على علامة التبويب السريعة **التحقق من الصحة** في صفحة **حالات دورة حياة أمر العمل** (**إدارة الأصول** \> **الإعداد‏‎** \> **أوامر العمل** \> **حالات دورة الحياة**).</span><span class="sxs-lookup"><span data-stu-id="090e7-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="090e7-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="090e7-120">Select **Save**.</span></span>

![أنواع أمر العمل](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]