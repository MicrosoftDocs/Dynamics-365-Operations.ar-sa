---
title: "الأبعاد المالية"
description: "يصف هذا الموضوع مختلف أنواع الأبعاد المالية وكيفية إعدادها."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3950dc3fcd1e293802c88bf2616a27e139b48399
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions"></a><span data-ttu-id="5c798-103">الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="5c798-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5c798-104">يصف هذا الموضوع مختلف أنواع الأبعاد المالية وكيفية إعدادها.</span><span class="sxs-lookup"><span data-stu-id="5c798-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="5c798-105">استخدم صفحة **الأبعاد المالية** لإنشاء الأبعاد المالية التي تستطيع استخدامها كشرائح حساب لمخططات الحسابات.</span><span class="sxs-lookup"><span data-stu-id="5c798-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="5c798-106">هناك نوعان من الأبعاد المالية: والأبعاد المخصصة والأبعاد المدعومة من الكيان.</span><span class="sxs-lookup"><span data-stu-id="5c798-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="5c798-107">تتم مشاركة الأبعاد المخصصة عبر الكيانات القانونية، ويتم إدخال القيم والاحتفاظ بها من قِبل المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="5c798-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="5c798-108">بالنسبة إلى الأبعاد المدعومة من الكيان، يتم تحديد القيم في مكان آخر في النظام، مثل العملاء أو كيانات المتاجر.</span><span class="sxs-lookup"><span data-stu-id="5c798-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="5c798-109">وتتم مشاركة بعض الأبعاد المدعومة من الكيان عبر الكيانات القانونية، في حين تكون لأبعاد الأخرى المدعومة من الكيان خاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="5c798-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="5c798-110">بعد إنشاء الأبعاد المالية، استخدم صفحة **قيم الأبعاد المالية** لتعيين خصائص إضافية لكل بُعد مالي.</span><span class="sxs-lookup"><span data-stu-id="5c798-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="5c798-111">يمكنك استخدام الأبعاد المالية لتمثيل الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="5c798-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="5c798-112">لست بحاجة إلى إنشاء الكيانات القانونية في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="5c798-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="5c798-113">ومع ذلك، لم يتم تصميم الأبعاد المالية لمعالجة المتطلبات التشغيلية أو متطلبات الأعمال الخاصة بالكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="5c798-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="5c798-114">تم تصميم وظيفة المحاسبة بين الوحدات في تطبيق Finance and Operations فقط لمعالجة الإدخالات المحاسبية التي تم إنشاؤها بواسطة كل حركة.</span><span class="sxs-lookup"><span data-stu-id="5c798-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="5c798-115">قبل إعداد الأبعاد المالية ككيانات قانونية، قم بتقييم العمليات التجارية في المجالات التالية لتحديد إذا كان هذا الإعداد سيصلح لمؤسستك:</span><span class="sxs-lookup"><span data-stu-id="5c798-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="5c798-116">المخزون</span><span class="sxs-lookup"><span data-stu-id="5c798-116">Inventory</span></span>
- <span data-ttu-id="5c798-117">المبيعات والمشتريات بين الأبعاد المالية والكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="5c798-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="5c798-118">حساب ضريبة المبيعات وإعداد التقارير</span><span class="sxs-lookup"><span data-stu-id="5c798-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="5c798-119">التقارير التشغيلية</span><span class="sxs-lookup"><span data-stu-id="5c798-119">Operational reporting</span></span>

<span data-ttu-id="5c798-120">فيما يلي بعض القيود:</span><span class="sxs-lookup"><span data-stu-id="5c798-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="5c798-121">يمكنك استخدام وظيفة ضريبة المبيعات مع الكيانات القانونية فقط وليس مع الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="5c798-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="5c798-122">لا تتضمن بعض التقارير أبعادًا مالية.</span><span class="sxs-lookup"><span data-stu-id="5c798-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="5c798-123">وبالتالي، لإعداد تقرير حسب البعد المالي، قد تحتاج إلى تعديل التقارير.</span><span class="sxs-lookup"><span data-stu-id="5c798-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="5c798-124">الأبعاد المخصصة</span><span class="sxs-lookup"><span data-stu-id="5c798-124">Custom dimensions</span></span>

<span data-ttu-id="5c798-125">لإنشاء بُعد مالي محدد من قِبل المستخدم، في حقل **استخدام القيم من**، حدد **&lt; بُعد مخصص &gt;**.</span><span class="sxs-lookup"><span data-stu-id="5c798-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="5c798-126">يمكنك أيضًا تعيين قناع تنسيق لتقييد كمية ونوع المعلومات التي تستطيع إدخالها لقيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="5c798-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="5c798-127">تستطيع إدخال الحروف التي تظل كما هي لكل قيمة بُعد مثل الأحرف أو واصلة (-).</span><span class="sxs-lookup"><span data-stu-id="5c798-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="5c798-128">كما يمكنك إدخال علامات الأرقام (\#) وعلامات العطف (&) كعناصر نائبة للحروف والأرقام التي ستتغير كلما يتم إنشاء قيمة بُعد.</span><span class="sxs-lookup"><span data-stu-id="5c798-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="5c798-129">استخدم علامة الأرقام (\#) كعنصر نائب لرقم وعلامة العطف (&) كعنصر نائب لحرف.</span><span class="sxs-lookup"><span data-stu-id="5c798-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="5c798-130">يتوفر حقل قناع التنسيق فقط عندما تحدد **&lt; بُعد مخصص &gt;** في الحقل **استخدام القيم من**.</span><span class="sxs-lookup"><span data-stu-id="5c798-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="5c798-131">**مثال**</span><span class="sxs-lookup"><span data-stu-id="5c798-131">**Example**</span></span>

<span data-ttu-id="5c798-132">لتقييد قيمة البُعد بالأحرف "CC" وثلاثة أرقام، أدخل **CC-\#\#\#** كقناع التنسيق.</span><span class="sxs-lookup"><span data-stu-id="5c798-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="5c798-133">الأبعاد المدعومة من الكيان</span><span class="sxs-lookup"><span data-stu-id="5c798-133">Entity-backed dimensions</span></span>

<span data-ttu-id="5c798-134">لإنشاء بُعد مالي مدعوم من كيان، في حقل **استخدام القيم من** حدد كيانًا محددًا من قِبل نظام لتأسيس البُعد المالي عليه.</span><span class="sxs-lookup"><span data-stu-id="5c798-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="5c798-135">يتم عندئذٍ إنشاء قيم الأبعاد المالية من هذا الكيان.</span><span class="sxs-lookup"><span data-stu-id="5c798-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="5c798-136">على سبيل المثال، لإنشاء قيم أبعاد للمشاريع، حدد **مشاريع**.</span><span class="sxs-lookup"><span data-stu-id="5c798-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="5c798-137">يتم عندئذٍ إنشاء قيمة بُعد لكل اسم مشروع.</span><span class="sxs-lookup"><span data-stu-id="5c798-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="5c798-138">تظهر صفحة **قيم الأبعاد المالية** القيم الخاصة بالكيان.</span><span class="sxs-lookup"><span data-stu-id="5c798-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="5c798-139">إذا كانت هذه القيم خاصة بالشركة، فستظهر الصفحة الشركة أيضًا.</span><span class="sxs-lookup"><span data-stu-id="5c798-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="5c798-140">تنشيط الأبعاد‬‏‫</span><span class="sxs-lookup"><span data-stu-id="5c798-140">Activating dimensions</span></span>

<span data-ttu-id="5c798-141">عند تنشيط البُعد المالي، يتم تحديث الجدول لكي يتضمن اسم البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="5c798-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="5c798-142">يتم إزالة الأبعاد المحذوفة.</span><span class="sxs-lookup"><span data-stu-id="5c798-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="5c798-143">يمكنك إدخال قيم البُعد قبل أن تقوم بتنشيط بُعد مالي.</span><span class="sxs-lookup"><span data-stu-id="5c798-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="5c798-144">ومع ذلك، لا يمكن استهلاك البُعد المالي في أي مكان حتى يتم تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="5c798-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="5c798-145">على سبيل المثال، لا يمكنك إضافة بُعد مالي إلى بنية حساب حتى يتم تنشيط البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="5c798-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="5c798-146">عند النقر فوق **تنشيط**، يتم تحديث كافة الأبعاد وإظهار تغييرات الحالة.</span><span class="sxs-lookup"><span data-stu-id="5c798-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="5c798-147">الترجمات</span><span class="sxs-lookup"><span data-stu-id="5c798-147">Translations</span></span>

<span data-ttu-id="5c798-148">في صفحة **ترجمة النص**، يمكنك إدخال نص للبُعد المالي المحدد بلغات متعددة.</span><span class="sxs-lookup"><span data-stu-id="5c798-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="5c798-149">في صفحة **ترجمة الحساب الرئيسي**، يمكنك إدخال نص للحساب الرئيسي بلغات متعددة.</span><span class="sxs-lookup"><span data-stu-id="5c798-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="5c798-150">تجاوزات الكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="5c798-150">Legal entity overrides</span></span>

<span data-ttu-id="5c798-151">لا تصلح كافة الأبعاد لكافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="5c798-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="5c798-152">بالإضافة إلى ذلك، بعض الأبعاد قد تكون ذات صلة فقط بفترة محددة.</span><span class="sxs-lookup"><span data-stu-id="5c798-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="5c798-153">في هذه الحالات، يمكن استخدام المقطع **تجاوزات الكيان القانوني** لتحديد الشركات التي يجب تعليق البُعد لها، وهو المالك والفترة الزمنية التي يكون البُعد نشطاً خلالها.</span><span class="sxs-lookup"><span data-stu-id="5c798-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="5c798-154">حذف الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="5c798-154">Deleting financial dimensions</span></span>

<span data-ttu-id="5c798-155">للمساعدة في الحفاظ على التكامل المرجعي للبيانات، نادرًا ما يمكن حذف الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="5c798-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="5c798-156">إذا حاولت حذف بُعد مالي، يتم تقييم المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="5c798-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="5c798-157">هل تم استخدام البُعد المالي في أي من الحركات المرحلة أو غير المرحلة أو أي نوع من مجموعة قيم أبعاد؟</span><span class="sxs-lookup"><span data-stu-id="5c798-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="5c798-158">هل البُعد المالي مستخدم في أي بنية حساب نشطة، أو بنية قاعدة متقدمة، أو مجموعة أبعاد مالية؟</span><span class="sxs-lookup"><span data-stu-id="5c798-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="5c798-159">هل البُعد المالي عبارة عن جزء من تنسيق تكامل الأبعاد المالية الافتراضية؟</span><span class="sxs-lookup"><span data-stu-id="5c798-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="5c798-160">هل تم إعداد البُعد كبُعد افتراضي؟</span><span class="sxs-lookup"><span data-stu-id="5c798-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="5c798-161">إذا تمت تلبية أي واحد من المعايير، فلا يمكنك حذف البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="5c798-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="5c798-162">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="5c798-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="5c798-163">تحديد الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="5c798-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="5c798-164">الاحتفاظ بالقوالب الافتراضية للأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="5c798-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

