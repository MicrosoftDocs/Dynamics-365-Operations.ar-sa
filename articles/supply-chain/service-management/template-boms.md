---
title: قوائم مكونات الصنف القالب
description: توفر قوائم مكونات الصنف القالب (BOM) قائمة معيارية من مكوِّنات كائنات الخدمة التي يتم تقديمها بصورة منتظمة.
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e732f64b389acafee23427594225dfacda71cc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421321"
---
# <a name="template-boms"></a><span data-ttu-id="1093b-103">قوائم مكونات الصنف القالب</span><span class="sxs-lookup"><span data-stu-id="1093b-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1093b-104">توفر لك قوائم مكونات الصنف القالب (BOM) قائمة معيارية من مكوِّنات كائنات الخدمة التي يتم تقديمها بصورة منتظمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="1093b-105">وتمثل المكوِّنات المدرجة في قائمة مكونات الصنف القالب المكونات الفرعية الفردية لكائن الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="1093b-106">من خلال تطبيق قائمة مكونات الصنف القالب على أمر خدمة، يمكنك الاحتفاظ بسجل يتضمن المكونات الفرعية التي تم استبدالها في كائن الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="1093b-107">لتطبيق شجرة مواد قالب على اتفاقية خدمة أو أمر خدمة، فإنه يمكن إرفاقها بعلاقة كائن الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1093b-108">يمكن تطبيق قائمة مكونات صنف قالب واحدة فقط على كائن خدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="1093b-109">إنشاء شجرة مواد قالب</span><span class="sxs-lookup"><span data-stu-id="1093b-109">Create a template BOM</span></span>

<span data-ttu-id="1093b-110">يحتوي الجدول التالي على معلومات حول العديد من الطرق التي يمكنك استخدامها لإنشاء قائمة مكونات صنف قالب.</span><span class="sxs-lookup"><span data-stu-id="1093b-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1093b-111">الأسلوب</span><span class="sxs-lookup"><span data-stu-id="1093b-111">Method</span></span></p></th>
<th><p><span data-ttu-id="1093b-112">الوصف</span><span class="sxs-lookup"><span data-stu-id="1093b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1093b-113">الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1093b-113">Production</span></span></p></td>
<td><p><span data-ttu-id="1093b-114">تكون قائمة مكونات الصنف القالب مستندة إلى أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="1093b-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="1093b-115">ويمكن تطبيق هذا الخيار فقط في حالة العمل داخل بيئة إنتاج.</span><span class="sxs-lookup"><span data-stu-id="1093b-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="1093b-116">ويتميز ذلك بتوفر قائمة مفصلة حالية من المكوِّنات التي تشكل الصنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1093b-117">قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="1093b-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="1093b-118">تكون قائمة مكونات الصنف القالب مستندة إلى قائمة مكونات صنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="1093b-119">بخلاف قائمة مكونات صنف الإنتاج، تكون قائمة مكونات الصنف عبارة عن قائمة إحصائية للمكونات التي تشكل الصنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1093b-120">قالب موجود</span><span class="sxs-lookup"><span data-stu-id="1093b-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="1093b-121">تكون قائمة مكونات الصنف القالب مستندة إلى قائمة مكونات صنف قالب موجود.</span><span class="sxs-lookup"><span data-stu-id="1093b-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1093b-122">يدوي</span><span class="sxs-lookup"><span data-stu-id="1093b-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="1093b-123">إذا كنت تعرف ما هي قطع الغيار التي يتم استبدالها في العادة في كائن الخدمة، فيمكنك إنشاء قائمة مكونات صنف قالب يدويًا.</span><span class="sxs-lookup"><span data-stu-id="1093b-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="1093b-124">تساعد هذه الطريقة في تأكد من أن المكوِّنات المضمنة في القالب تعكس المتطلبات الفعلية لمساحة العمل لديك.</span><span class="sxs-lookup"><span data-stu-id="1093b-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="1093b-125">تطبيق قائمة مكونات الصنف القالب على اتفاقية خدمة أو أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="1093b-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="1093b-126">يمكنك تطبيق قائمة مكونات الصنف القالب على اتفاقية وأمر خدمة أو كليهما.</span><span class="sxs-lookup"><span data-stu-id="1093b-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="1093b-127">عادة ما تغطي اتفاقية الخدمة علاقة طويلة الأمد مع عميل.</span><span class="sxs-lookup"><span data-stu-id="1093b-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="1093b-128">يعد سجل عمليات الاستبدال التي تم تسجيلها في قائمة مكونات صنف الخدمة بيانات مفيدة لتسجيلها في اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="1093b-129">يمكنك أيضا تطبيق قائمة مكونات الصنف القالب على أمر خدمة لتسجيل سجل الخدمة التي تم تنفيذها على كائن خدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="1093b-130">نسخ سجل قائمة مكونات صنف خدمة</span><span class="sxs-lookup"><span data-stu-id="1093b-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="1093b-131">يمكن نسخ سجل بند قائمة مكونات صنف خدمة من اتفاقية خدمة إلى اتفاقية خدمة أخرى.</span><span class="sxs-lookup"><span data-stu-id="1093b-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="1093b-132">عن طريق نسخ سجل الخدمة بين اتفاقيات الخدمة، يمكن الاحتفاظ بسجل عمليات الاستبدال الخاصة بأحد الأصناف.</span><span class="sxs-lookup"><span data-stu-id="1093b-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="1093b-133">**مثال**</span><span class="sxs-lookup"><span data-stu-id="1093b-133">**Example**</span></span>

<span data-ttu-id="1093b-134">تم إعداد اتفاقية خدمة مدتها ثلاث سنوات لسيارة أحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="1093b-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="1093b-135">أثناء هذه الفترة، يصبح العميل معتاداً على الخدمة الجيدة التي توفرها الشركة.</span><span class="sxs-lookup"><span data-stu-id="1093b-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="1093b-136">لذلك، بعد انتهاء صلاحية الاتفاقية، يرغب العميل في إعداد اتفاقية جديدة.</span><span class="sxs-lookup"><span data-stu-id="1093b-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="1093b-137">أصبح الآن بمقدورك المفاوضة على عقد اتفاقية لصالح الشركة بصورة أكبر.</span><span class="sxs-lookup"><span data-stu-id="1093b-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="1093b-138">ونظرًا لأن سجل المكوِّنات المستبدلة قد يكون مفيدًا في المستقبل، فيمكن نسخ سجل قائمة مكونات صنف الخدمة إلى الاتفاقية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1093b-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="1093b-139">تعديل قائمة مكونات الصنف القالب</span><span class="sxs-lookup"><span data-stu-id="1093b-139">Modify the template BOM</span></span>

<span data-ttu-id="1093b-140">إن لم يتم إرفاق قائمة مكونات الصنف القالب بكائن خدمة، عندئذ يمكنك تعديل البنود بها أو حذفها.</span><span class="sxs-lookup"><span data-stu-id="1093b-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="1093b-141">بعد إرفاق قائمة مكونات الصنف القالب بكائن خدمة، فلن يمكن تعديل سوى الإصدار المحلي من قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="1093b-142">وإذا كنت ترغب في تكرار إعداد الإصدار المحلي من شجرة مواد القالب، فيمكنك إنشاء شجرة مواد قالب جديدة استنادًا إلى الإصدار المحلي.</span><span class="sxs-lookup"><span data-stu-id="1093b-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="1093b-143">لمزيد من المعلومات، راجع [تعديل قائمة مكونات صنف خدمة](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="1093b-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="1093b-144">إذا استبدلت صنفًا داخل قائمة مكونات الصنف، فمن الممكن تسجيل هذا الاستبدال في بند قائمة مكونات الصنف في مصمم قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="1093b-145">اختياريًا، يمكنك إنشاء بند أمر خدمة لكائن الاستبدال.</span><span class="sxs-lookup"><span data-stu-id="1093b-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="1093b-146">إذا قمت بإنشاء بند أمر خدمة، عندئذ يمكنك فوترة صنف الاستبدال.</span><span class="sxs-lookup"><span data-stu-id="1093b-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="1093b-147">وإن لم تقم بإنشاء بند أمر خدمة للاستبدال، يتم الاحتفاظ بتسجيل الاستبدال لتعقب سجل كائن الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="1093b-148">تغيير كيفية عرض معلومات في بند قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="1093b-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="1093b-149">يمكن تغيير طريقة عرض المعلومات في بند قائمة مكونات الصنف لجميع قوائم مكونات الصنف للقالب والخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="1093b-150">يتم تطبيق التغييرات على كل قوائم مكونات صنف القالب وقوائم مكونات صنف الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="1093b-151">وهذا يشمل تلك التي تم إرفاقها بكائنات الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="1093b-152">إعداد تسلسلات رقمية لقوائم مكونات الصنف القالب</span><span class="sxs-lookup"><span data-stu-id="1093b-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="1093b-153">لاستخدام قوائم مكونات الصنف القالب، يجب إعداد تسلسلين رقميين.</span><span class="sxs-lookup"><span data-stu-id="1093b-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="1093b-154">قم بإعداد تسلسل رقمي واحد لقائمة مكونات الصنف القالب والآخر لرقم بند سجل قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1093b-155">يتم استخدام التسلسلات الرقمية لتخصيص المعرفات للسجلات التي تحتاج إليها.</span><span class="sxs-lookup"><span data-stu-id="1093b-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="1093b-156">قبل تعيين تسلسل أرقام لقائمة مكونات الصنف القالب أو رقم بند سجل قائمة مكونات الصنف، يجب إعداد أكواد التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="1093b-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="1093b-157">إعداد التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="1093b-157">Set up number sequences</span></span>

1.  <span data-ttu-id="1093b-158">في صفحة قائمة **التسلسلات الرقمية**، قم بإنشاء تسلسلات رقمية لقائمة مكونات الصنف القالب ورقم بند سجل قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="1093b-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="1093b-159">انقر فوق **إدارة الخدمة‬** \> **الإعداد** \> **محددات إدارة الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="1093b-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="1093b-160">انقر فوق **التسلسلات الرقمية**، ثم حدد كود تسلسل رقمي لمراجع التسلسل الرقمي التي قمت بإنشائها في نموذج **التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="1093b-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="1093b-161">أغلق النموذج لحفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="1093b-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1093b-162">يتم استخدام رقم بند سجل قائمة مكونات الصنف بواسطة النظام لربط الحركات في سجل قائمة مكونات الصنف باتفاقية خدمة أو أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1093b-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="1093b-163">لا يتم عرض الرقم في واجهة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="1093b-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="1093b-164">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="1093b-164">See also</span></span>

[<span data-ttu-id="1093b-165">إنشاء شجرة مواد قالب</span><span class="sxs-lookup"><span data-stu-id="1093b-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="1093b-166">إدارة شجرة مواد القالب على علاقات الكائن</span><span class="sxs-lookup"><span data-stu-id="1093b-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="1093b-167">تعديل شجرة مواد الخدمة</span><span class="sxs-lookup"><span data-stu-id="1093b-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 


