---
title: وحدة الأكورديون
description: يتناول هذا الموضوع وحدات أكورديون ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a08441f5dffa9c2c65b304d0265dd107a838a685
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206597"
---
# <a name="accordion-module"></a><span data-ttu-id="b22d6-103">وحدة أككورديون</span><span class="sxs-lookup"><span data-stu-id="b22d6-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b22d6-104">يتناول هذا الموضوع وحدات أكورديون ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b22d6-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b22d6-105">وحدات الأكورديون هي وحدات حاوية يتم استخدامها لتنظيم المعلومات أو الوحدات على صفحة عن طريق قدرة مماثلة لدرج قابل للطي.</span><span class="sxs-lookup"><span data-stu-id="b22d6-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="b22d6-106">يمكن استخدام وحدة الأكورديون‬ على أي صفحة.</span><span class="sxs-lookup"><span data-stu-id="b22d6-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="b22d6-107">داخل كل وحدة أكورديون‬، يمكن إضافة وحدة عنصر أكورديون‬ أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="b22d6-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="b22d6-108">تمثل كل وحدة عنصر أكورديون‬ درجًا قابلاً للطي.</span><span class="sxs-lookup"><span data-stu-id="b22d6-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="b22d6-109">داخل كل وحدة عنصر أكورديون‬، يمكن إضافة وحدة‬ أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="b22d6-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="b22d6-110">لا توجد قيود على أنواع الوحدات التي يمكن إضافتها إلى وحدة عنصر أكورديون.</span><span class="sxs-lookup"><span data-stu-id="b22d6-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="b22d6-111">تعرض الصورة التالية مثال عن وحدة أكورديون تستخدم لتنظيم المعلومات في صفحة الأسئلة المتداولة تابعة لمتجر.</span><span class="sxs-lookup"><span data-stu-id="b22d6-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![مثال عن وحدة أكورديون](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="b22d6-113">خصائص وحدة الأكورديون</span><span class="sxs-lookup"><span data-stu-id="b22d6-113">Accordion module properties</span></span>

| <span data-ttu-id="b22d6-114">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="b22d6-114">Property name</span></span> | <span data-ttu-id="b22d6-115">القيم</span><span class="sxs-lookup"><span data-stu-id="b22d6-115">Values</span></span> | <span data-ttu-id="b22d6-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="b22d6-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b22d6-117">العنوان</span><span class="sxs-lookup"><span data-stu-id="b22d6-117">Heading</span></span> | <span data-ttu-id="b22d6-118">النص</span><span class="sxs-lookup"><span data-stu-id="b22d6-118">Text</span></span> | <span data-ttu-id="b22d6-119">تحدد هذه الخاصية عنوان نص اختياري لوحدة الأكورديون.</span><span class="sxs-lookup"><span data-stu-id="b22d6-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="b22d6-120">توسيع الكل</span><span class="sxs-lookup"><span data-stu-id="b22d6-120">Expand All</span></span> | <span data-ttu-id="b22d6-121">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="b22d6-121">**True** or **False**</span></span> | <span data-ttu-id="b22d6-122">إذ تم تعيين القيمة إلى **صواب**، يتم تشغيل وظيفة التوسيع/الطي، بحيث يمكن توسيع كافة العناصر الموجودة في وحدة الأكورديون وطيها.</span><span class="sxs-lookup"><span data-stu-id="b22d6-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="b22d6-123">نمط التفاعل</span><span class="sxs-lookup"><span data-stu-id="b22d6-123">Interaction Style</span></span> | <span data-ttu-id="b22d6-124">**مستقل** أو **توسيع عنصر واحد فقط**</span><span class="sxs-lookup"><span data-stu-id="b22d6-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="b22d6-125">تحدد هذه الخاصية نمط التفاعل لعناصر الأكورديون.</span><span class="sxs-lookup"><span data-stu-id="b22d6-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="b22d6-126">إذا تم تعيين القيمة إلى **مستقل**، فيمكن توسيع كل عنصر أكورديون أو طيه بشكل مستقل.</span><span class="sxs-lookup"><span data-stu-id="b22d6-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="b22d6-127">إذا تم تعيين القيمة إلى **لتوسيع عنصر واحد فقط**، فيمكن توسيع عنصر واحد فقط في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="b22d6-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="b22d6-128">مع توسيع العناصر، يتم طي العناصر التي تم توسيعها في السابق.</span><span class="sxs-lookup"><span data-stu-id="b22d6-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="b22d6-129">خصائص وحدة عنصر الأكورديون</span><span class="sxs-lookup"><span data-stu-id="b22d6-129">Accordion item module properties</span></span>

| <span data-ttu-id="b22d6-130">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="b22d6-130">Property name</span></span> | <span data-ttu-id="b22d6-131">القيم</span><span class="sxs-lookup"><span data-stu-id="b22d6-131">Values</span></span> | <span data-ttu-id="b22d6-132">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="b22d6-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b22d6-133">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="b22d6-133">Title</span></span> | <span data-ttu-id="b22d6-134">النص</span><span class="sxs-lookup"><span data-stu-id="b22d6-134">Text</span></span> | <span data-ttu-id="b22d6-135">تحدد هذه الخاصية عنوانًا نصيًا لوحدة عنصر الأكورديون.</span><span class="sxs-lookup"><span data-stu-id="b22d6-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="b22d6-136">عند تحديد منطقة العنوان، سيتمكن المستخدمون من توسيع القسم أو طيه.</span><span class="sxs-lookup"><span data-stu-id="b22d6-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="b22d6-137">موسّع بشكل افتراضي</span><span class="sxs-lookup"><span data-stu-id="b22d6-137">Expand by default</span></span> | <span data-ttu-id="b22d6-138">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="b22d6-138">**True** or **False**</span></span> | <span data-ttu-id="b22d6-139">إذا تم تعيين القيمة إلى **صواب**، يتم توسيع عنصر الأكورديون بشكل افتراضي عند تحميل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b22d6-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="b22d6-140">إضافة وحدة أكورديون‬ إلى صفحة الأسئلة المتداولة</span><span class="sxs-lookup"><span data-stu-id="b22d6-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="b22d6-141">إضافة وحدة أكورديون‬ إلى صفحة الأسئلة المتداولة وتعيين خصائصها في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b22d6-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b22d6-142">انتقل إلى **الصفحات**، واستخدم قالب التسويق Fabrikam (أو أي قالب لا توجد في قيود) لإنشاء صفحة جديدة تسمى **الأسئلة المتداولة حول المتجر**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="b22d6-143">في الفتحة **الرئيسية‏‎** في **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b22d6-144">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b22d6-145">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b22d6-146">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الأكورديون‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b22d6-147">في جزء الخصائص لوحدة الأكورديون، حدد **العنوان** بجوار رمز القلم الرصاص.</span><span class="sxs-lookup"><span data-stu-id="b22d6-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="b22d6-148">في مربع الحوار **العنوان**، ضمن **نص العنوان**، أدخل **الأسئلة المتداولة**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="b22d6-149">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-149">Then select **OK**.</span></span>
1. <span data-ttu-id="b22d6-150">في جزء الخصائص لوحدة الأكورديون، حدد خانة الاختيار **إظهار توسيع الكل**، ثم في **نمط التفاعل**، حدد **مستقل**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="b22d6-151">في فتحة **الأكورديون‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b22d6-152">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**عنصر الأكورديون‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b22d6-153">في جزء الخصائص لوحدة عنصر الأكورديون، ضمن **العنوان**، أدخل نص العنوان (على سبيل المثال، **كيف تعمل المرتجعات؟**).</span><span class="sxs-lookup"><span data-stu-id="b22d6-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="b22d6-154">في فتحة **عنصر الأكورديون‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b22d6-155">في مربع الحوار **إضافة وحدة**، حدد وحدة **كتلة النص‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b22d6-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b22d6-156">في جزء الخصائص لوحدة كتلة النص، أدخل فقرة نص (على سبيل المثال، **يجب معالجة المرتجعات من خلال مركز الاتصال. اتصل على 1-800-FABRIKAM فيما يتعلق بالمرتجعات. تخضع المنتجات لسياسة الإرجاع لمدة 30 يومًا. يجب بدء الإرجاع ضمن هذا الإطار الزمني.**).</span><span class="sxs-lookup"><span data-stu-id="b22d6-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="b22d6-157">في فتحة **الأكورديون**، أضع بعض وحدات عنصر الأكورديون.</span><span class="sxs-lookup"><span data-stu-id="b22d6-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="b22d6-158">في كل وحدة عنصر أكورديون، أضف وحدة كتلة نص تتضمن هذا المحتوى.</span><span class="sxs-lookup"><span data-stu-id="b22d6-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="b22d6-159">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b22d6-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="b22d6-160">ستعرض الصفحة وحدة أكورديون تتضمن المحتوى الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="b22d6-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="b22d6-161">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="b22d6-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b22d6-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b22d6-162">Additional resources</span></span>

[<span data-ttu-id="b22d6-163">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="b22d6-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b22d6-164">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="b22d6-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b22d6-165">وحدة علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="b22d6-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="b22d6-166">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="b22d6-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]