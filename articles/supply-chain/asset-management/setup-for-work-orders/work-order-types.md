---
title: أنواع أمر العمل
description: يشرح هذا الموضوع أنواع أوامر العمل في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 375b18a4bd37ddadecee03a01b3b2125f5cc8d0a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215414"
---
# <a name="work-order-types"></a><span data-ttu-id="d2dfe-103">أنواع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="d2dfe-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d2dfe-104">يتم استخدام أنواع أوامر العمل لتصنيف أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="d2dfe-105">على سبيل المثال، قد يكون لديك أنواع أوامر عمل تتعلق بالصيانة الوقائية أو الصيانة التصحيحية.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="d2dfe-106">يحدد نوع أمر العمل تبعية مع نموذج دورو حياة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="d2dfe-107">يحدد نموذج دورة حياة أمر العمل حالات دورة حياة أمر العمل التي يمكن تعيينها على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="d2dfe-108">(تتضمن أمثلة حالات دورة حياة أمر العمل **تم الإنشاء** و**قيد التنفيذ‬** و**منتهي**.)</span><span class="sxs-lookup"><span data-stu-id="d2dfe-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="d2dfe-109">لمزيد من المعلومات حول حالات دورة حياة أمر العمل ومراحل المشروع، راجع [حالات دورة حياة أمر العمل](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="d2dfe-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="d2dfe-110">حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **أنواع أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="d2dfe-111">حدد **جديد** لإنشاء أمر عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="d2dfe-112">في الحقل **نوع أمر العمل**، أدخل معرفًا لنوع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="d2dfe-113">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="d2dfe-114">في الحقل **نموذج دورة حياة أمر العمل‬**، حدد نموذج دورة حياة.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="d2dfe-115">عيّن الخيار **عامل صيانة واحد‬‏‫** إلى to **نعم** إذا كان يجب تعيين جميع وظائف أمر العمل التي ترتبط بأمر عمل من هذا النوع إلى عامل الصيانة نفسه.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="d2dfe-116">في الحقل **نوع التكلفة**، حدد **تصحيحي** أو **وقائي** أو **استثمار**، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="d2dfe-117">يجب أن يكون نوع التكلفة هو نفسه لجميع وظائف أمر العمل على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="d2dfe-118">في القسم **إلزامي**، عيّن الخيارات ذات الصلة إلى **نعم** لتحديد المعلومات المتعلقة بالأخطاء أو المتعلقة بوقت تعطل الصيانة التي تُضاف إلى أمر عمل من هذا النوع</span><span class="sxs-lookup"><span data-stu-id="d2dfe-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2dfe-119">ترتبط الخيارات في القسم **إلزامي** بالخيارات على علامة التبويب السريعة **التحقق من الصحة** في صفحة **حالات دورة حياة أمر العمل** (**إدارة الأصول** \> **الإعداد‏‎** \> **أوامر العمل** \> **حالات دورة الحياة**).</span><span class="sxs-lookup"><span data-stu-id="d2dfe-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="d2dfe-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d2dfe-120">Select **Save**.</span></span>

![أنواع أمر العمل](media/16-setup-for-work-orders.png)
