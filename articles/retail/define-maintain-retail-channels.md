---
title: "تحديد والاحتفاظ بقنوات البيع بالتجزئة"
description: "توفر هذه المقالة نظرة عامة على عملية إعداد المتاجر التقليدية، والتي يشار إليها كمتاجر البيع بالتجزئة في Microsoft Dynamics 365 for Retail. وهي تتضمن معلومات حول المهام التي يجب إكمالها قبل إعداد متجر البيع بالتجزئة وبعده."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a78df20ce5a9ff0aae7b2b3e93d00c46f747f07
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="dd46c-104">تحديد والاحتفاظ بقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="dd46c-104">Define and maintain retail channels</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="dd46c-105">توفر هذه المقالة نظرة عامة على عملية إعداد المتاجر التقليدية، والتي يشار إليها كمتاجر البيع بالتجزئة في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="dd46c-105">This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="dd46c-106">وهي تتضمن معلومات حول المهام التي يجب إكمالها قبل إعداد متجر البيع بالتجزئة وبعده.</span><span class="sxs-lookup"><span data-stu-id="dd46c-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="dd46c-107">يدعم Dynamics 365 for Retail قنوات بيع بالتجزئة متعددة، مثل المتاجر والأسواق عبر الإنترنت والمتاجر التقليدية ومراكز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="dd46c-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="dd46c-108">يسمى المتجر التقليدي متجر تجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="dd46c-109">ويمكن أن يكون لكل متجر تجزئة طرق الدفع الخاصة به، ومجموعات الأسعار، ونقطة البيع (POS)، وحسابات الإيرادات والمصروفات وفريق العمل.</span><span class="sxs-lookup"><span data-stu-id="dd46c-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="dd46c-110">ويجب إعداد كل هذه العناصر لمتجر بيع بالتجزئة قبل إنشائه.</span><span class="sxs-lookup"><span data-stu-id="dd46c-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="dd46c-111">وبعد قيامك بإنشاء متجر للتجزئة، يمكنك تعيين المنتجات التي ترغب أن يتحملها المتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="dd46c-112">يمكنك أيضًا تعيين الموظفين والسجلات والعملاء للمتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="dd46c-113">وأخيراً، تقوم بإضافة المتجر الجديد إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="dd46c-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="dd46c-114">إعداد متاجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="dd46c-114">Setting up retail stores</span></span>
<span data-ttu-id="dd46c-115">قبل أن تقوم بإعداد متجر بيع بالتجزئة في Dynamics 365 for Retail، يجب إكمال بعض المهام الأساسية.</span><span class="sxs-lookup"><span data-stu-id="dd46c-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="dd46c-116">يمكنك بعد ذلك إنشاء متجر البيع بالتجزئة وإضافة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="dd46c-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="dd46c-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="dd46c-117">Prerequisites</span></span>

<span data-ttu-id="dd46c-118">ويجب عليك المهام التالية قبل أن يمكنك إعداد متجر للبيع بالتجزئة:</span><span class="sxs-lookup"><span data-stu-id="dd46c-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="dd46c-119">تكوين بنية المؤسسة الخاصة بك وإعداد تدرجات هرمية للمؤسسات لعمليات فرز البيع بالتجزئة والتزويد و‏‫إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="dd46c-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="dd46c-120">إعداد ‏‫مستودع‬ ليمثل متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="dd46c-121">إعداد التسلسلات الرقمية لمتاجر البيع بالتجزئة، وكشوف الحسابات، و‏‫إيصالات كشف الحساب‬.</span><span class="sxs-lookup"><span data-stu-id="dd46c-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="dd46c-122">تكوين المحددات للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="dd46c-123">إعداد طرق الدفع التي يقبلها المتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="dd46c-124">لمعالجة حركات بطاقات الائتمان في سجلات نقطة البيع (POS)‬ لمتجر البيع بالتجزئة، يمكن أيضًا إعداد خدمات الدفع.</span><span class="sxs-lookup"><span data-stu-id="dd46c-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="dd46c-125">إعداد مجموعات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="dd46c-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="dd46c-126">إعداد منتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="dd46c-126">Set up retail products.</span></span> <span data-ttu-id="dd46c-127">وكجزء من هذه المهمة، يمكنك أيضًا إعداد التدرجات الهرمية لمنتج البيع بالتجزئة ومتغيرات المنتج وعمليات فرز المنتجات.</span><span class="sxs-lookup"><span data-stu-id="dd46c-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="dd46c-128">إعداد مجموعات سعر المنتج.</span><span class="sxs-lookup"><span data-stu-id="dd46c-128">Set up product price groups.</span></span>
10. <span data-ttu-id="dd46c-129">إعداد تسعير منتج البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-129">Set up retail product pricing.</span></span> <span data-ttu-id="dd46c-130">وكجزء من هذه المهمة، يمكنك أيضًا إعداد تسويات الأسعار والخصومات وفترات الخصم.</span><span class="sxs-lookup"><span data-stu-id="dd46c-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="dd46c-131">إعداد أعضاء الفريق.</span><span class="sxs-lookup"><span data-stu-id="dd46c-131">Set up staff members.</span></span> <span data-ttu-id="dd46c-132">**ملاحظة:** يجب أيضًا تعيين الأذونات المناسبة للعمال، بحيث يمكنهم تسجيل الدخول وتنفيذ المهام باستخدام Dynamics 365 for Retail لنظام نقطة البيع للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="dd46c-133">تكوين ملفات تعريف نقطة البيع بالتجزئة لتعيينها للمتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="dd46c-134">تتضمن هذه المهمة العديد من المهام، مثل إعداد السجلات و‏‫ملفات التعريف غير المتصلة‬ وتنسيقات الإيصالات وملفات التعريف.</span><span class="sxs-lookup"><span data-stu-id="dd46c-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="dd46c-135">مراجعة كافة المهام المضمنة في المتطلب الأساسي، وإكمال المهام التي تنطبق عليك فقط.</span><span class="sxs-lookup"><span data-stu-id="dd46c-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="dd46c-136">إعداد متجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="dd46c-136">Set up a retail store</span></span>

<span data-ttu-id="dd46c-137">بعد إكمال المهام اللازمة، عليك إكمال هذه المهام لإعداد تفاصيل متجر البيع بالتجزئة:</span><span class="sxs-lookup"><span data-stu-id="dd46c-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="dd46c-138">إنشاء متجر بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-138">Create a retail store.</span></span>
2.  <span data-ttu-id="dd46c-139">تعيين مجموعات ضرائب مبيعات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="dd46c-140">تعيين طرق الدفع المقبولة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="dd46c-141">إضافة تفاصيل وصف المنتج للمنتجات التي تقدمها في متاجر التجزئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="dd46c-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="dd46c-142">على سبيل المثال، يمكنك إضافة نص منسق وصور.</span><span class="sxs-lookup"><span data-stu-id="dd46c-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="dd46c-143">تظهر تفاصيل المنتج هذه في سياقات مختلفة، مثل سجل نقطة البيع أو التسميات المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="dd46c-144">قم بإضافة المتجر إلى تدرج الهرمي الافتراضي للمؤسسات الذي تم تعيينه لغرض **فرز البيع بالتجزئة** أو **تزويد البيع بالتجزئة** أو **تقارير البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="dd46c-144">Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="dd46c-145">بعد إعداد متجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="dd46c-145">After you set up a retail store</span></span>

<span data-ttu-id="dd46c-146">بعد إدخال تفاصيل متجر البيع بالتجزئة، عليك إكمال هذه المهام لإرسال البيانات الجديدة لمتجر البيع بالتجزئة إلى نقطة البيع الخاصة بالبيع بالتجزئة:</span><span class="sxs-lookup"><span data-stu-id="dd46c-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="dd46c-147">تكوين سجلات نقاط البيع (POS)‬ للمتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="dd46c-148">تعيين عمليات فرز المنتجات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="dd46c-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="dd46c-149">معالجة عمليات الفرز لإنشاء قائمة المنتجات المضمنة في عملية الفرز وتوفير المنتجات في متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="dd46c-150">إرسال بيانات مثل التسلسلات رقمية، وملفات تعريف الأجهزة‬، وتخطيطات شاشة نقطة البيع إلى سجلات نقاط البيع الخاصة بالبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="dd46c-151">نشر متجر البيع بالتجزئة لإرسال بيانات المتجر إلى نقطة البيع الخاصة بالبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="dd46c-152">تشغيل الوظائف لإرسال بيانات المتجر إلى نقطة البيع الخاصة بالبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="dd46c-153">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="dd46c-153">Organization hierarchies</span></span>
<span data-ttu-id="dd46c-154">يستخدم Retail التدرجات الهرمية للمؤسسات في هيكلة قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="dd46c-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="dd46c-155">تمثل التدرجات الهرمية للمؤسسات العلاقات بين المؤسسات التي تتألف منها أعمالك.</span><span class="sxs-lookup"><span data-stu-id="dd46c-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="dd46c-156">عند إعداد المتاجر، يمكنك إضافتها إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="dd46c-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="dd46c-157">وقتئذٍ تتشارك المتاجر البيانات المستخدمة لعمليات الفرز، والتزويد، وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="dd46c-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




