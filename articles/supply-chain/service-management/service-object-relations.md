---
title: علاقات كائنات الخدمة
description: يمكنك إنشاء علاقات كائنات الخدمة بين كائن خدمة واتفاقية خدمة أو أمر خدمة.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b1b76dffc2751d51c2a25d831fab512b747c15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421057"
---
# <a name="service-object-relations"></a><span data-ttu-id="d2496-103">علاقات كائنات الخدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2496-104">يمكنك إنشاء علاقات كائنات الخدمة بين كائن خدمة واتفاقية خدمة أو أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="d2496-105">عند قيامك بإنشاء علاقة، ستقوم بإرفاق كائن الخدمة باتفاقية الخدمة أو أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="d2496-106">بعد إنشاء العلاقة، يمكنك إرفاق كائن الخدمة بأية بنود في اتفاقية الخدمة أو أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="d2496-107">شجرة المواد القالب</span><span class="sxs-lookup"><span data-stu-id="d2496-107">Template BOMs</span></span>

<span data-ttu-id="d2496-108">يمكنك أيضًا تحديد شجرة المواد القالب لعلاقة الكائن.</span><span class="sxs-lookup"><span data-stu-id="d2496-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="d2496-109">وشجرة المواد القالب هي عبارة عن كمبيالة مواد للكائن الذي تُجري عليه الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="d2496-110">إذا قمت باستبدال جزء مكون لكائن الخدمة أثناء زيارة خدمة، فيمكنك تسجيل هذا التغيير في قائمة مكونات الصنف الخاصة بالخدمة باستخدام نموذج كائنات الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="d2496-111">مثال</span><span class="sxs-lookup"><span data-stu-id="d2496-111">Example</span></span>

<span data-ttu-id="d2496-112">تقوم بإنشاء اتفاقية خدمة لصيانة مصعدين بموقع أحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="d2496-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="d2496-113">وتشتمل اتفاقية الخدمة على المعرّف ID SAL-001.</span><span class="sxs-lookup"><span data-stu-id="d2496-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="d2496-114">تم إعداد المصعدين في نموذج كائنات الخدمات ككائنات، EL-S/1000 وEL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="d2496-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="d2496-115">وستقوم بإرفاق كائني الخدمة، EL-S/1000 وEL-L/1000، باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="d2496-116">تريد تسجيل التغييرات في شجرة المواد لكائن الخدمة بينما تقوم باستبدال الأجزاء المكونة للكائن، لذا سترفق شجرة مواد الخدمة بعلاقة كائن الخدمة، كما هو موضح بالجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="d2496-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="d2496-117">كائن الخدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-117">Service object</span></span> | <span data-ttu-id="d2496-118">العلاقة – اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-118">Relation – Service agreement</span></span> | <span data-ttu-id="d2496-119">شجرة مواد للخدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="d2496-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-120">EL-S/1000</span></span>      | <span data-ttu-id="d2496-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d2496-121">ID SAL-001</span></span>                   | <span data-ttu-id="d2496-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="d2496-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-123">EL-L/1000</span></span>      | <span data-ttu-id="d2496-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d2496-124">ID SAL-001</span></span>                   | <span data-ttu-id="d2496-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="d2496-126">نظرًا لتوافر علاقات كائن الخدمة للاتفاقية، يمكنك الآن إنشاء بنود اتفاقية خدمة تحتوي على هذه الكائنات، كما هو موضح بالجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="d2496-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="d2496-127">نوع الحركة</span><span class="sxs-lookup"><span data-stu-id="d2496-127">Transaction type</span></span> | <span data-ttu-id="d2496-128">الفئة</span><span class="sxs-lookup"><span data-stu-id="d2496-128">Category</span></span>           | <span data-ttu-id="d2496-129">كائن الخدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="d2496-130">الساعة</span><span class="sxs-lookup"><span data-stu-id="d2496-130">Hour</span></span>             | <span data-ttu-id="d2496-131">فحص</span><span class="sxs-lookup"><span data-stu-id="d2496-131">Inspection</span></span>         | <span data-ttu-id="d2496-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-132">EL-S/1000</span></span>      |
| <span data-ttu-id="d2496-133">الساعة</span><span class="sxs-lookup"><span data-stu-id="d2496-133">Hour</span></span>             | <span data-ttu-id="d2496-134">تنظيف صندوق التروس</span><span class="sxs-lookup"><span data-stu-id="d2496-134">Gear box cleaning</span></span>  | <span data-ttu-id="d2496-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-135">EL-S/1000</span></span>      |
| <span data-ttu-id="d2496-136">الصنف</span><span class="sxs-lookup"><span data-stu-id="d2496-136">Item</span></span>             | <span data-ttu-id="d2496-137">مواد منظفة</span><span class="sxs-lookup"><span data-stu-id="d2496-137">Cleaning materials</span></span> | <span data-ttu-id="d2496-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-138">EL-S/1000</span></span>      |
| <span data-ttu-id="d2496-139">الساعة</span><span class="sxs-lookup"><span data-stu-id="d2496-139">Hour</span></span>             | <span data-ttu-id="d2496-140">فحص</span><span class="sxs-lookup"><span data-stu-id="d2496-140">Inspection</span></span>         | <span data-ttu-id="d2496-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-141">EL-L/1000</span></span>      |
| <span data-ttu-id="d2496-142">الساعة</span><span class="sxs-lookup"><span data-stu-id="d2496-142">Hour</span></span>             | <span data-ttu-id="d2496-143">تنظيف صندوق التروس</span><span class="sxs-lookup"><span data-stu-id="d2496-143">Gearbox cleaning</span></span>   | <span data-ttu-id="d2496-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-144">EL-L/1000</span></span>      |
| <span data-ttu-id="d2496-145">الصنف</span><span class="sxs-lookup"><span data-stu-id="d2496-145">Item</span></span>             | <span data-ttu-id="d2496-146">مواد منظفة</span><span class="sxs-lookup"><span data-stu-id="d2496-146">Cleaning materials</span></span> | <span data-ttu-id="d2496-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d2496-147">EL-L/1000</span></span>      |

<span data-ttu-id="d2496-148">أثناء إجراء زيارة خدمة، ينبغي استبدال صندوق تروس مصعد EL-S/1000.</span><span class="sxs-lookup"><span data-stu-id="d2496-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="d2496-149">لاستبدال جزء مكون من الكائن، يمكنك الوصول إلى مصمم شجرة المواد باستخدام علاقة كائن الخدمة التي قمت بإعدادها لاتفاقية الخدمة الحالية.</span><span class="sxs-lookup"><span data-stu-id="d2496-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="d2496-150">الوصول إلى مصمم شجرة المواد باستخدام علاقة كائن خدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="d2496-151">اتفاقيات الخدمة</span><span class="sxs-lookup"><span data-stu-id="d2496-151">Service agreements</span></span>
2. <span data-ttu-id="d2496-152">انقر نقرًا مزدوجًا فوق اتفاقية خدمة، أو انقر فوق "اتفاقية الخدمة" لإنشاء اتفاقية خدمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="d2496-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="d2496-153">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="d2496-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="d2496-154">انقر فوق "كائنات الخدمة" لإرفاق قائمة مكونات الصنف للقالب باتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="d2496-155">في نموذج "كائنات الخدمة"، انقر فوق "المصمم" لفتح نموذج المصمم لتعديل قائمة مكونات الصنف للقالب.</span><span class="sxs-lookup"><span data-stu-id="d2496-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="d2496-156">أوامر خدمة تم إنشاؤها تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="d2496-156">Automatically created service orders</span></span>

<span data-ttu-id="d2496-157">إذا قمت بإنشاء أوامر الخدمة لاتفاقية الخدمة بشكل تلقائي، فإن علاقات كائن الخدمة في الاتفاقية ستنشأ أيضًا في أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d2496-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>

