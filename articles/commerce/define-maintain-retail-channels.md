---
title: تحديد والاحتفاظ بقنوات البيع بالتجزئة
description: يوفر هذا الموضوع نظرة عامة على عملية إعداد المتاجر التقليدية، والتي يشار إليها كمتاجر في Dynamics 365 Commerce. وهي تتضمن معلومات حول المهام التي يجب إتمامها قبل إعداد متجر وبعده.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057904"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="19a5d-104">تحديد قنوات البيع بالتجزئة والاحتفاظ بها</span><span class="sxs-lookup"><span data-stu-id="19a5d-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="19a5d-105">يوفر هذا الموضوع نظرة عامة على عملية إعداد المتاجر التقليدية، والتي يشار إليها كمتاجر في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="19a5d-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="19a5d-106">وهي تتضمن معلومات حول المهام التي يجب إتمامها قبل إعداد متجر وبعده.</span><span class="sxs-lookup"><span data-stu-id="19a5d-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="19a5d-107">تدعم التجارة قنوات متعددة، مثل المتاجر عبر الإنترنت ومراكز الاتصال والمتاجر التقليدية.</span><span class="sxs-lookup"><span data-stu-id="19a5d-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="19a5d-108">يُعرف المتجر التقليدي باسم متجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="19a5d-109">وقد يكون لكل متجر طرق الدفع الخاصة ومجموعات الأسعار وسجلات نقاط البيع (POS) وحسابات الإيرادات والمصروفات وفريق العمل.</span><span class="sxs-lookup"><span data-stu-id="19a5d-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="19a5d-110">ويجب إعداد كل هذه العناصر للمتجر قبل إنشائه.</span><span class="sxs-lookup"><span data-stu-id="19a5d-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="19a5d-111">وبعد إنشاء المتجر، يمكنك تعيين المنتجات التي ترغب في احتواء المتجر عليها.</span><span class="sxs-lookup"><span data-stu-id="19a5d-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="19a5d-112">يمكنك أيضًا تعيين الموظفين والسجلات والعملاء للمتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="19a5d-113">وأخيراً، تقوم بإضافة المتجر الجديد إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="19a5d-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="19a5d-114">إعداد المتاجر</span><span class="sxs-lookup"><span data-stu-id="19a5d-114">Setting up stores</span></span>

<span data-ttu-id="19a5d-115">قبل إعداد متجر في التجارة، يجب إتمام بعض مهام المتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="19a5d-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="19a5d-116">يمكنك بعد ذلك إنشاء المتجر وإضافة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="19a5d-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="19a5d-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="19a5d-117">Prerequisites</span></span>

<span data-ttu-id="19a5d-118">يجب إتمام المهام التالية قبل أن تتمكن من إعداد متجر:</span><span class="sxs-lookup"><span data-stu-id="19a5d-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="19a5d-119">تكوين بنية المؤسسة الخاصة بك وإعداد تدرجات هرمية للمؤسسات لعمليات فرز البيع بالتجزئة والتزويد و‏‫إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="19a5d-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="19a5d-120">إعداد ‏‫مستودع‬ لتمثيل المتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="19a5d-121">إعداد التسلسلات الرقمية للمتاجر وكشوف حساباتالمتجر و‏‫إيصالات كشف الحساب‬.</span><span class="sxs-lookup"><span data-stu-id="19a5d-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="19a5d-122">تكوين معلمات التجارة.</span><span class="sxs-lookup"><span data-stu-id="19a5d-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="19a5d-123">إعداد طرق الدفع التي يقبلها المتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="19a5d-124">لمعالجة حركات بطاقات الائتمان في سجلات نقطة البيع، يمكن أيضًا إعداد خدمات الدفع.</span><span class="sxs-lookup"><span data-stu-id="19a5d-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="19a5d-125">إعداد مجموعات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="19a5d-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="19a5d-126">إعداد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="19a5d-126">Set up products.</span></span> <span data-ttu-id="19a5d-127">وكجزء من هذه المهمة، ستكون مسؤولاً أيضًا عن إعداد التدرجات الهرمية للمنتج ومتغيرات المنتج وعمليات فرز المنتجات.</span><span class="sxs-lookup"><span data-stu-id="19a5d-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="19a5d-128">إعداد مجموعات سعر المنتج.</span><span class="sxs-lookup"><span data-stu-id="19a5d-128">Set up product price groups.</span></span>
10. <span data-ttu-id="19a5d-129">إعداد تسعير المنتج.</span><span class="sxs-lookup"><span data-stu-id="19a5d-129">Set up product pricing.</span></span> <span data-ttu-id="19a5d-130">وكجزء من هذه المهمة، يمكنك أيضًا إعداد تسويات الأسعار والخصومات وفترات الخصم.</span><span class="sxs-lookup"><span data-stu-id="19a5d-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="19a5d-131">إعداد أعضاء الفريق.</span><span class="sxs-lookup"><span data-stu-id="19a5d-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="19a5d-132">يجب أيضًا تعيين الأذونات المناسبة للعاملين، حتى يمكنهم تسجيل الدخول وتنفيذ المهام باستخدام نظام نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="19a5d-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="19a5d-133">تكوين ملفات تعريف نقطة البيع لتعيينها للمتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="19a5d-134">تتضمن هذه المهمة العديد من المهام، مثل إعداد السجلات و‏‫ملفات التعريف غير المتصلة‬ وتنسيقات الإيصالات وملفات التعريف.</span><span class="sxs-lookup"><span data-stu-id="19a5d-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="19a5d-135">مراجعة كافة المهام المضمنة في المتطلبات الأساسية، وإتمام المهام التي تنطبق عليك فقط.</span><span class="sxs-lookup"><span data-stu-id="19a5d-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="19a5d-136">إعداد متجر</span><span class="sxs-lookup"><span data-stu-id="19a5d-136">Set up a store</span></span>

<span data-ttu-id="19a5d-137">بعد إتمام مهام المتطلبات الأساسية، عليك إتمام هذه المهام لإعداد تفاصيل المتجر:</span><span class="sxs-lookup"><span data-stu-id="19a5d-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="19a5d-138">قم بإنشاء متجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-138">Create a store.</span></span>
2. <span data-ttu-id="19a5d-139">تعيين مجموعات ضرائب مبيعات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="19a5d-140">تعيين طرق الدفع المقبولة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="19a5d-141">إضافة تفاصيل وصف المنتج للمنتجات التي تقدمها في المتاجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="19a5d-142">على سبيل المثال، يمكنك إضافة نص منسق وصور.</span><span class="sxs-lookup"><span data-stu-id="19a5d-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="19a5d-143">تظهر تفاصيل المنتج هذه في سياقات مختلفة، مثل سجل نقطة البيع أو التسميات المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="19a5d-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="19a5d-144">قم بإضافة المتجر إلى التدرج الهرمي الافتراضي للمؤسسات الذي تم تعيينه لغرض **فرز البيع بالتجزئة** أو **تزويد البيع بالتجزئة** أو **تقارير البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="19a5d-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="19a5d-145">بعد الانتهاء من إعداد متجر</span><span class="sxs-lookup"><span data-stu-id="19a5d-145">After you set up a store</span></span>

<span data-ttu-id="19a5d-146">بعد إدخال تفاصيل المتجر، عليك إتمام هذه المهام لإرسال بيانات المتجر الجديد إلى نقطة البيع:</span><span class="sxs-lookup"><span data-stu-id="19a5d-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="19a5d-147">تكوين سجلات نقاط البيع (POS)‬ للمتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="19a5d-148">تعيين عمليات فرز المنتجات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="19a5d-149">معالجة عمليات الفرز لإنشاء قائمة المنتجات المضمنة في عملية الفرز وتوفير المنتجات في المتجر.</span><span class="sxs-lookup"><span data-stu-id="19a5d-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="19a5d-150">إرسال البيانات كالتسلسلات الرقمية وملفات تعريف الأجهزة وتخطيطات شاشة نقطة البيع إلى سجلات نقاط البيع.</span><span class="sxs-lookup"><span data-stu-id="19a5d-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="19a5d-151">نشر المتجر لإرسال بيانات المتجر إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="19a5d-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="19a5d-152">تشغيل الوظائف لإرسال بيانات المتجر إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="19a5d-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="19a5d-153">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="19a5d-153">Organization hierarchies</span></span>

<span data-ttu-id="19a5d-154">تستخدم التجارة التدرجات الهرمية للمؤسسات لهيكلة القنوات.</span><span class="sxs-lookup"><span data-stu-id="19a5d-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="19a5d-155">تمثل التدرجات الهرمية للمؤسسات العلاقات بين المؤسسات التي تتألف منها أعمالك.</span><span class="sxs-lookup"><span data-stu-id="19a5d-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="19a5d-156">عند إعداد المتاجر، يمكنك إضافتها إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="19a5d-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="19a5d-157">وقتئذٍ تتشارك المتاجر البيانات المستخدمة لعمليات الفرز، والتزويد، وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="19a5d-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="19a5d-158">لاستخدام وظيفة مبيعات Commerce، يجب تمكين مفتاح التكوين الخاص بـ **‏‫شحن إلى متعدد‬** .</span><span class="sxs-lookup"><span data-stu-id="19a5d-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="19a5d-159">يمكن العثور علي مفتاح التكوين هذا في مفاتيح **تكوين التجارة** ضمن **‏‫إدارة النظام‬**\> **إعداد** \> **تكوين الرخصة**.</span><span class="sxs-lookup"><span data-stu-id="19a5d-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="19a5d-160">يُطلب ذلك نظرًا لعمليات تحقق متعددة بناءً على عنوان التسليم الذي تم تكوينه على مستوى سطر أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="19a5d-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

