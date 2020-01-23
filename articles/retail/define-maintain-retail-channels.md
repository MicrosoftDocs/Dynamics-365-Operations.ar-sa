---
title: تحديد والاحتفاظ بقنوات البيع بالتجزئة
description: يوفر هذا الموضوع نظرة عامة على عملية إعداد المتاجر التقليدية، والتي يشار إليها كمتاجر البيع بالتجزئة في Dynamics 365 Retail. وهي تتضمن معلومات حول المهام التي يجب إكمالها قبل إعداد متجر البيع بالتجزئة وبعده.
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
ms.openlocfilehash: 45d0386d215da15103a417502debb245c91f6309
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934598"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="42bd8-104">تحديد والاحتفاظ بقنوات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="42bd8-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42bd8-105">يوفر هذا الموضوع نظرة عامة على عملية إعداد المتاجر التقليدية، والتي يشار إليها كمتاجر البيع بالتجزئة في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="42bd8-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Dynamics 365 Retail.</span></span> <span data-ttu-id="42bd8-106">وهي تتضمن معلومات حول المهام التي يجب إكمالها قبل إعداد متجر البيع بالتجزئة وبعده.</span><span class="sxs-lookup"><span data-stu-id="42bd8-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="42bd8-107">يدعم Retail قنوات بيع بالتجزئة متعددة، مثل المتاجر والأسواق عبر الإنترنت والمتاجر التقليدية ومراكز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="42bd8-107">Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="42bd8-108">يسمى المتجر التقليدي متجر بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="42bd8-109">ويمكن أن يكون لكل متجر تجزئة طرق الدفع الخاصة به، ومجموعات الأسعار، ونقطة البيع (POS)، وحسابات الإيرادات والمصروفات وفريق العمل.</span><span class="sxs-lookup"><span data-stu-id="42bd8-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="42bd8-110">ويجب إعداد كل هذه العناصر لمتجر بيع بالتجزئة قبل إنشائه.</span><span class="sxs-lookup"><span data-stu-id="42bd8-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="42bd8-111">وبعد قيامك بإنشاء متجر للتجزئة، يمكنك تعيين المنتجات التي ترغب أن يتحملها المتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="42bd8-112">يمكنك أيضًا تعيين الموظفين والسجلات والعملاء للمتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="42bd8-113">وأخيراً، تقوم بإضافة المتجر الجديد إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="42bd8-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="42bd8-114">إعداد متاجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="42bd8-114">Setting up retail stores</span></span>

<span data-ttu-id="42bd8-115">قبل أن تقوم بإعداد متجر البيع بالتجزئة في Retail، يجب إكمال بعض المهام الأساسية.</span><span class="sxs-lookup"><span data-stu-id="42bd8-115">Before you can set up a retail store in Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="42bd8-116">يمكنك بعد ذلك إنشاء متجر البيع بالتجزئة وإضافة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="42bd8-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="42bd8-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="42bd8-117">Prerequisites</span></span>

<span data-ttu-id="42bd8-118">ويجب عليك المهام التالية قبل أن يمكنك إعداد متجر للبيع بالتجزئة:</span><span class="sxs-lookup"><span data-stu-id="42bd8-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="42bd8-119">تكوين بنية المؤسسة الخاصة بك وإعداد تدرجات هرمية للمؤسسات لعمليات فرز البيع بالتجزئة والتزويد و‏‫إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="42bd8-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="42bd8-120">إعداد ‏‫مستودع‬ ليمثل متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="42bd8-121">إعداد التسلسلات الرقمية لمتاجر البيع بالتجزئة، وكشوف الحسابات، و‏‫إيصالات كشف الحساب‬.</span><span class="sxs-lookup"><span data-stu-id="42bd8-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="42bd8-122">تكوين المحددات للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="42bd8-123">إعداد طرق الدفع التي يقبلها المتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="42bd8-124">لمعالجة حركات بطاقات الائتمان في سجلات نقطة البيع (POS)‬ لمتجر البيع بالتجزئة، يمكن أيضًا إعداد خدمات الدفع.</span><span class="sxs-lookup"><span data-stu-id="42bd8-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="42bd8-125">إعداد مجموعات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="42bd8-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="42bd8-126">إعداد منتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="42bd8-126">Set up retail products.</span></span> <span data-ttu-id="42bd8-127">وكجزء من هذه المهمة، يمكنك أيضًا إعداد التدرجات الهرمية لمنتج البيع بالتجزئة ومتغيرات المنتج وعمليات فرز المنتجات.</span><span class="sxs-lookup"><span data-stu-id="42bd8-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="42bd8-128">إعداد مجموعات سعر المنتج.</span><span class="sxs-lookup"><span data-stu-id="42bd8-128">Set up product price groups.</span></span>
10. <span data-ttu-id="42bd8-129">إعداد تسعير منتج البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-129">Set up retail product pricing.</span></span> <span data-ttu-id="42bd8-130">وكجزء من هذه المهمة، يمكنك أيضًا إعداد تسويات الأسعار والخصومات وفترات الخصم.</span><span class="sxs-lookup"><span data-stu-id="42bd8-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="42bd8-131">إعداد أعضاء الفريق.</span><span class="sxs-lookup"><span data-stu-id="42bd8-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42bd8-132">يجب أيضًا تعيين الأذونات المناسبة للعاملين، بحيث يمكنهم تسجيل الدخول وتنفيذ المهام باستخدام نظام Retail POS.</span><span class="sxs-lookup"><span data-stu-id="42bd8-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Retail POS system.</span></span>

12. <span data-ttu-id="42bd8-133">تكوين ملفات تعريف نقطة البيع بالتجزئة لتعيينها للمتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="42bd8-134">تتضمن هذه المهمة العديد من المهام، مثل إعداد السجلات و‏‫ملفات التعريف غير المتصلة‬ وتنسيقات الإيصالات وملفات التعريف.</span><span class="sxs-lookup"><span data-stu-id="42bd8-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="42bd8-135">مراجعة كافة المهام المضمنة في المتطلب الأساسي، وإكمال المهام التي تنطبق عليك فقط.</span><span class="sxs-lookup"><span data-stu-id="42bd8-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="42bd8-136">إعداد متجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="42bd8-136">Set up a retail store</span></span>

<span data-ttu-id="42bd8-137">بعد إكمال المهام اللازمة، عليك إكمال هذه المهام لإعداد تفاصيل متجر البيع بالتجزئة:</span><span class="sxs-lookup"><span data-stu-id="42bd8-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="42bd8-138">إنشاء متجر بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-138">Create a retail store.</span></span>
2. <span data-ttu-id="42bd8-139">تعيين مجموعات ضرائب مبيعات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="42bd8-140">تعيين طرق الدفع المقبولة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="42bd8-141">إضافة تفاصيل وصف المنتج للمنتجات التي تقدمها في متاجر التجزئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="42bd8-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="42bd8-142">على سبيل المثال، يمكنك إضافة نص منسق وصور.</span><span class="sxs-lookup"><span data-stu-id="42bd8-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="42bd8-143">تظهر تفاصيل المنتج هذه في سياقات مختلفة، مثل سجل نقطة البيع أو التسميات المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="42bd8-144">قم بإضافة المتجر إلى التدرج الهرمي الافتراضي للمؤسسات الذي تم تعيينه لغرض **فرز البيع بالتجزئة** أو **تزويد البيع بالتجزئة** أو **تقارير البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="42bd8-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="42bd8-145">بعد إعداد متجر البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="42bd8-145">After you set up a retail store</span></span>

<span data-ttu-id="42bd8-146">بعد إدخال تفاصيل متجر البيع بالتجزئة، عليك إكمال هذه المهام لإرسال البيانات الجديدة لمتجر البيع بالتجزئة إلى نقطة البيع الخاصة بالبيع بالتجزئة:</span><span class="sxs-lookup"><span data-stu-id="42bd8-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="42bd8-147">تكوين سجلات نقاط البيع (POS)‬ للمتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="42bd8-148">تعيين عمليات فرز المنتجات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="42bd8-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="42bd8-149">معالجة عمليات الفرز لإنشاء قائمة المنتجات المضمنة في عملية الفرز وتوفير المنتجات في متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="42bd8-150">إرسال بيانات مثل التسلسلات رقمية، وملفات تعريف الأجهزة‬، وتخطيطات شاشة نقطة البيع إلى سجلات نقاط البيع الخاصة بالبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="42bd8-151">نشر متجر البيع بالتجزئة لإرسال بيانات المتجر إلى نقطة البيع الخاصة بالبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="42bd8-152">تشغيل الوظائف لإرسال بيانات المتجر إلى نقطة البيع الخاصة بالبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="42bd8-153">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="42bd8-153">Organization hierarchies</span></span>

<span data-ttu-id="42bd8-154">يستخدم Retail التدرجات الهرمية للمؤسسات في هيكلة قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="42bd8-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="42bd8-155">تمثل التدرجات الهرمية للمؤسسات العلاقات بين المؤسسات التي تتألف منها أعمالك.</span><span class="sxs-lookup"><span data-stu-id="42bd8-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="42bd8-156">عند إعداد المتاجر، يمكنك إضافتها إلى تدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="42bd8-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="42bd8-157">وقتئذٍ تتشارك المتاجر البيانات المستخدمة لعمليات الفرز، والتزويد، وإعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="42bd8-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="42bd8-158">لاستخدام وظيفة مبيعات البيع بالتجزئة، يجب تمكين مفتاح التكوين الخاص بـ **‏‫شحن إلى متعدد‬** .</span><span class="sxs-lookup"><span data-stu-id="42bd8-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="42bd8-159">يمكن العثور علي مفتاح التكوين هذا في مفاتيح **تكوين التجارة** ضمن **‏‫إدارة النظام‬**\> **إعداد** \> **تكوين الرخصة**.</span><span class="sxs-lookup"><span data-stu-id="42bd8-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="42bd8-160">يُطلب ذلك نظرًا لوظائف البيع بالتجزئة التي تنفذ عمليات تحقق متعددة بناءً على عنوان التسليم الذي تم تكوينه على مستوى سطر أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="42bd8-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>
