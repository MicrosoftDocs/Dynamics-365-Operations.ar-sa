---
title: التعاقد من الباطن
description: سيساعدك هذا الموضوع على بناء نظرة عامة على التعاقد من الباطن في التصنيع في Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3e282e0676e53200b0993dd9cb2b52e08fe97dca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981446"
---
# <a name="subcontracting"></a><span data-ttu-id="3a152-103">التعاقد من الباطن</span><span class="sxs-lookup"><span data-stu-id="3a152-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a152-104">سيساعدك هذا الموضوع على بناء نظرة عامة على التعاقد من الباطن في التصنيع في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3a152-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3a152-105">يوضح الجزء الأول من الموضع كيفية إعداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="3a152-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="3a152-106">يستعرض الجزء الثاني من الموضع الخطوات في الإرشادات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="3a152-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="3a152-107">الجمهور المستهدف</span><span class="sxs-lookup"><span data-stu-id="3a152-107">Target audience</span></span>

<span data-ttu-id="3a152-108">في هذا الموضوع، سوف تتعلم كيفية إعداد التعاقد من الباطن في التصنيع.</span><span class="sxs-lookup"><span data-stu-id="3a152-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="3a152-109">سوف تستخدم البيانات الموجودة في الكيان القانوني HQUS للقيام بالإعداد الأساسي لتدفق نشاط التعاقد من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="3a152-110">تشمل بيانات العرض التوضيحي في الكيان القانوني HQUS مُحددات الإعداد المُعدة مسبقًا لدعم الخطوات الواردة في هذه الإرشادات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="3a152-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="3a152-111">على الرغم من أن الإرشادات التفصيلية تتناول نقاط المشكلات الرئيسية والتحديات لمختلف الأدوار، إلا أنه يمكن لمسؤول النظام إكمالها.</span><span class="sxs-lookup"><span data-stu-id="3a152-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="3a152-112">سيناريو العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="3a152-112">Demo scenario</span></span>

<span data-ttu-id="3a152-113">في الكيان القانوني HQUS، يتم تصنيع مكبرات الصوت الحديثة عالية الجودة.</span><span class="sxs-lookup"><span data-stu-id="3a152-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="3a152-114">خلال عملية التصنيع، تمر مكبرات الصوت بالعمليات الثلاثة التالية.</span><span class="sxs-lookup"><span data-stu-id="3a152-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="3a152-115">**ما قبل التجميع** -يتم تجميع خزانة مكبر الصوت.</span><span class="sxs-lookup"><span data-stu-id="3a152-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="3a152-116">يتم انتقاء المواد الخاصة بالخزانة في مستودع المواد قبل بدء العملية.</span><span class="sxs-lookup"><span data-stu-id="3a152-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="3a152-117">**التغطية** -بعد أن يتم تجميع خزانة مكبر الصوت، يجب تغطيتها.</span><span class="sxs-lookup"><span data-stu-id="3a152-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="3a152-118">يقوم بإكمال هذه العملية مورد (مقاول من الباطن).</span><span class="sxs-lookup"><span data-stu-id="3a152-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="3a152-119">يتم شحن خزانة مكبر الصوت المُجمعة مسبقًا للمقاول من الباطن الذي سوف يقوم البتغطية بالإضافة إلى المادتين.</span><span class="sxs-lookup"><span data-stu-id="3a152-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="3a152-120">**إنهاء** -بعد قيام المقاول من الباطن بتغطية خزانة مكبر الصوت المُجمع مسبقًا، تُعاد إلى الكيان القانوني HQUS، بحيث يتم الانتهاء من التجميع النهائي لمكبر الصوت.</span><span class="sxs-lookup"><span data-stu-id="3a152-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="3a152-121">يوضح الشرح التالي العمليات الثلاث والمواد المستهلكة.</span><span class="sxs-lookup"><span data-stu-id="3a152-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![ما قبل التجميع، التغطية، وعمليات الإنهاء، والمواد المستهلكة](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="3a152-123">إعداد</span><span class="sxs-lookup"><span data-stu-id="3a152-123">Setup</span></span>

<span data-ttu-id="3a152-124">قبل بدء المعاينة، يجب عليك إعداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="3a152-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="3a152-125">إعداد المنتج النهائي</span><span class="sxs-lookup"><span data-stu-id="3a152-125">Set up the finished product</span></span>

<span data-ttu-id="3a152-126">يقوم هذا الإجراء بتعريفك بالإعداد الخاص بالمنتج المصدر D8100، "الخزانة المُغطاة."</span><span class="sxs-lookup"><span data-stu-id="3a152-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="3a152-127">حدد **إدارة معلومات المنتج \>المنتجات \>المنتجات المُصدرة** لفتح صفحة **تفاصيل المنتج المُصدر**.</span><span class="sxs-lookup"><span data-stu-id="3a152-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="3a152-128">في حقل عامل التصفية السريع، أدخل **D8100** للبحث عن المنتج المُصدر الحالي.</span><span class="sxs-lookup"><span data-stu-id="3a152-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![تصفية المنتج المُصدر D8100 في صفحة تفاصيل المنتجات المُصدرة](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="3a152-130">في جزء الإجراءات، في علامة تبويب **هندسة** ، حدد **المسار** لفتح صفحة **المسار**.</span><span class="sxs-lookup"><span data-stu-id="3a152-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="3a152-131">توضح صفحة **المسار** إصدارات المسارات الثمانية للمنتج المُصدر D8100.</span><span class="sxs-lookup"><span data-stu-id="3a152-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="3a152-132">يتم تقسيم إصدارات المسارات الثمانية بين أربعة مسارات في الموقع 1 والموقع 5.</span><span class="sxs-lookup"><span data-stu-id="3a152-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="3a152-133">يتم استخدام المسار 000400 لحساب التكلفة، والمسار 00041 عندما تكون عملية التغطية عملية داخلية، ويستخدم المسار 00042 عندما تكون عملية التغطية عملية خارجية.</span><span class="sxs-lookup"><span data-stu-id="3a152-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![إصدارات المسارات الثمانية في صفحة المسار](./media/subcontract03_route-page.png)

4. <span data-ttu-id="3a152-135">في الجزء العلوي، في شبكة **الإصدارات**، حدد إصدار المسار **00042** لموقع **5**.</span><span class="sxs-lookup"><span data-stu-id="3a152-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="3a152-136">في الجزء السفلي، في علامة تبويب **نظرة عامة**، حدد العملية **20** (**Cbnt CtSc**) في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3a152-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![العملية 20 لإصدار المسار 00042 لموقع 5 المُحدد](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="3a152-138">حدد علامة التبويب **عام**.</span><span class="sxs-lookup"><span data-stu-id="3a152-138">Select the **General** tab.</span></span>

    <span data-ttu-id="3a152-139">لاحظ أن الحقل **نوع المسار** تم تعيينه إلى **المورد**.</span><span class="sxs-lookup"><span data-stu-id="3a152-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="3a152-140">تشير هذه القيمة إلى أن العملية 20 (Cbnt CtSc) عملية متعاقد عليها من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![تعيين حقل نوع المسار إلى المورد في علامة التبويب عام](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="3a152-142">حدد علامة التبويب **متطلبات المصدر**.</span><span class="sxs-lookup"><span data-stu-id="3a152-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="3a152-143">سوف يتم استخدام القدرات للبحث عن مورد قابل للتطبيق في أثناء جدولة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3a152-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="3a152-144">بالنسبة للعملية 20 (Cbnt CtSc)، لاحظ أن المورد الذي يحتوي على قدرتين، **التغطية** و **الخزانات المُغطاة**، مطلوب.</span><span class="sxs-lookup"><span data-stu-id="3a152-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![التغطية وقدرات الخزانات المغطاة في علامة تبويب متطلبات الموارد.](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="3a152-146">حدد **الموارد القابلة للتطبيق** لفتح مربع حوار **الموارد القابلة للتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="3a152-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="3a152-147">تم العثور على ثلاثة موارد التي تطابق متطلبات الموارد للعملية.</span><span class="sxs-lookup"><span data-stu-id="3a152-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="3a152-148">لاحظ أن الموارد 8851 و 8852 من نوع **المورد**.</span><span class="sxs-lookup"><span data-stu-id="3a152-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![ثلاثة موارد مناسبة في مربع حوار الموارد القابلة للتطبيق.](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="3a152-150">حدد **موافق** لإغلاق مربع حوار **الموارد القابلة للتطبيق** والعودة إلى صفحة **المسار**.</span><span class="sxs-lookup"><span data-stu-id="3a152-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="3a152-151">قم بإغلاق صفحة **المسار** للرجوع إلى صفحة **تفاصيل المنتج المُصدر**.</span><span class="sxs-lookup"><span data-stu-id="3a152-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![صفحة تفاصيل المنتج المُصدر](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="3a152-153">في جزء الإجراءات، في علامة تبويب **هندسة** ، حدد **إصدارات BOM** لفتح صفحة **إصدارات BOM**.</span><span class="sxs-lookup"><span data-stu-id="3a152-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="3a152-154">توضح صفحة **إصدارات BOM** أربعة إصدارات لشجرة المواد (BOM) للمنتج المُصدر D8100.</span><span class="sxs-lookup"><span data-stu-id="3a152-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="3a152-155">يتم استخدام BOM 000040 للتكلفة والتخطيط، تستخدم قائمة مكونات الصنف 000041 إذا كانت عملية التغطية تتم داخليًا وتستخدم قوائم مكونات الصنف 000042 وقوائم مكونات الصنف 000043 إذا تم التعاقد على عملية التغطية من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="3a152-156">لاحظ أن الصنف S8050 هو منتج من نوع الصنف **الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="3a152-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="3a152-157">يمثل هذا البند العمل المتعاقد عليه من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-157">This item represents the subcontracted work.</span></span>

    ![أربعة إصدارات لقائمة مكونات الصنف في صفحة إصدارات قائمة مكونات الصنف](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="3a152-159">في علامة التبويب السريعة **بنود قائمة مكونات الصنف**، حدد **تحرير** لفتح مربع حوار **تحرير بند قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="3a152-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="3a152-160">عندما يتم إنشاء أمر إنتاج وتقديره لمنتج D8100 المُصدر، سوف يتم إنشاء أمر شراء تلقائيًا للصنف S8050.</span><span class="sxs-lookup"><span data-stu-id="3a152-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="3a152-161">سوف يتم ربط أمر الشراء هذا بأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3a152-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="3a152-162">لأوامر الشراء التي تم إنشائها تلقائيًا، يجب تعيين حقل **نوع السطر** إلى **المورد**، ويجب تحديد حساب المورد للمقاول من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="3a152-163">في هذه الحالة، حساب المورد هو US-801.</span><span class="sxs-lookup"><span data-stu-id="3a152-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="3a152-164">لاحظ أن بند قائمة مكونات الصنف متصل بعملية التغطية من خلال رقم العملية (في هذه الحالة، رقم العملية 20).</span><span class="sxs-lookup"><span data-stu-id="3a152-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![تحرير مربع حوار سطر قائمة مكونات الصنف](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="3a152-166">إنشاء كلمة مرور للعاملين في المستودع</span><span class="sxs-lookup"><span data-stu-id="3a152-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="3a152-167">يجب عليك تحديد كلمة مرور لعمال المستودع الذين يستخدمون جهاز محمول باليد.</span><span class="sxs-lookup"><span data-stu-id="3a152-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="3a152-168">حدد **إدارة المستودعات \>الإعداد \> العامل** لفتح صفحة **مستخدمو العمل**.</span><span class="sxs-lookup"><span data-stu-id="3a152-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="3a152-169">في علامة التبويب السريعة **المستخدمون**، حدد الصف الخاص بالمستخدم **51**.</span><span class="sxs-lookup"><span data-stu-id="3a152-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![صفحة مستخدمي العمل](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="3a152-171">حدد **إعادة تعيين كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="3a152-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="3a152-172">في حقول **كلمة المرور** و **تأكيد كلمة المرور** ، أدخل **1**.</span><span class="sxs-lookup"><span data-stu-id="3a152-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="3a152-173">حدد **تعيين كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="3a152-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="3a152-174">الإرشادات التفصيلية خطوة بخطوة</span><span class="sxs-lookup"><span data-stu-id="3a152-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="3a152-175">**السيناريو والخلفية**</span><span class="sxs-lookup"><span data-stu-id="3a152-175">**Scenario and background**</span></span>

<span data-ttu-id="3a152-176">يتم إنشاء أمر إنتاج من عشر قطع للمنتج D8100، "الخزانة المُغطاة."</span><span class="sxs-lookup"><span data-stu-id="3a152-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="3a152-177">تمثل تغطية الخزانات عملية متعاقد عليها من الباطن يتم إجراؤها عند المورد US-801، حلول التغطية المثالية.</span><span class="sxs-lookup"><span data-stu-id="3a152-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="3a152-178">يتكون أمر الإنتاج من ثلاث عمليات.</span><span class="sxs-lookup"><span data-stu-id="3a152-178">The production order consists of three operations.</span></span> <span data-ttu-id="3a152-179">في العملية الأولى، يتم تجميع الخزانة مسبقة كعملية داخلية.</span><span class="sxs-lookup"><span data-stu-id="3a152-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="3a152-180">يتم إصدار المواد الخاصة بالتجميع المسبق للانتقاء في مستودع المادة الخام.</span><span class="sxs-lookup"><span data-stu-id="3a152-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="3a152-181">بعد الإنتهاء من عملية التجميع المسبق، تٌرسل الخزانة المُجمعة مسبقًا حلول التغطية المثالية بالإضافة إلى المادتين المطلوبتين لعملية التغطية.</span><span class="sxs-lookup"><span data-stu-id="3a152-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="3a152-182">عند استلام الخزانة المُغطاة مرة أخرى من المورد، تمر بعملية تجميع داخلية نهائية قبل أن يتم الإبلاغ عنها كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="3a152-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="3a152-183">حدد **التحكم بالإنتاج \>أوامر الإنتاج \>كافة أوامر الإنتاج** لفتح صفحة **كافة أوامر الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="3a152-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="3a152-184">في جزء الإجراءات، حدد **أمر إنتاج جديد** لفتح مربع حوار **إنشاء أمر إنتاج**.</span><span class="sxs-lookup"><span data-stu-id="3a152-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![إنشاء مربع حوار أمر إنتاج](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="3a152-186">في حقل **رقم الصنف**، حدد **D8100**.</span><span class="sxs-lookup"><span data-stu-id="3a152-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="3a152-187">بعد تحديد رقم الصنف، تظهر حقول أبعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="3a152-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="3a152-188">في حقل **اللونن** ، حدد **Chrome**.</span><span class="sxs-lookup"><span data-stu-id="3a152-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="3a152-189">يظهر مربع رسالة يسألك ما إذا كان يجب إدراج الإصدارات النشطة لقائمة مكونات الصنف والمسار.</span><span class="sxs-lookup"><span data-stu-id="3a152-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![مربع الرسالة](./media/subcontract13_message-box.png)

5. <span data-ttu-id="3a152-191">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3a152-191">Select **Yes**.</span></span> 

    <span data-ttu-id="3a152-192">في مربع حوار **إنشاء أمر إنتاج**، يتم تحديد الإصدارات النشطة لقائمة مكونات الصنف والمسار لمنتج D8100 تلقائيًا في الحقول **رقم قائمة مكونات الصنف** و **رقم المسار**، على التوالي.</span><span class="sxs-lookup"><span data-stu-id="3a152-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="3a152-193">في هذه الحالة، يتم تحديد قائمة مكونات الصنف **000040** والمسار **000040** .</span><span class="sxs-lookup"><span data-stu-id="3a152-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="3a152-194">بالنسبة لكل من قائمة مكونات الصنف والمسار، يستخدم الإصدار 000040 للتكاليف والتخطيط.</span><span class="sxs-lookup"><span data-stu-id="3a152-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="3a152-195">في حقل **الموقع** ، حدد **5**.</span><span class="sxs-lookup"><span data-stu-id="3a152-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="3a152-196">في حقل **المستودع**، حدد **51**.</span><span class="sxs-lookup"><span data-stu-id="3a152-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="3a152-197">في حقول **رقم قائمة مكونات الصنف** و **رقم المسار** ، قم بتغيير القيمة التي تم تحديدها تلقائياً لـ **000042**.</span><span class="sxs-lookup"><span data-stu-id="3a152-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a152-198">بالنسبة لكل من قائمة مكونات الصنف والمسار، يستخدم الإصدار 000042 للتعاقد على تغطية الخزانة من الباطن للمورد US-801.</span><span class="sxs-lookup"><span data-stu-id="3a152-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![مجموعة القيم في مربع حوار إنشاء أمر إنتاج](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="3a152-200">حدد **إنشاء** لإنشاء أمر الإنتاج والرجوع إلى صفحة **كافة أوامر الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="3a152-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![أمر الإنتاج الجديد في صفحة كافة أوامر الإنتاج](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="3a152-202">في جزء الإجراءات، في علامة التبويب **أمر الإنتاج**، حدد **التقدير** لفتح مربع الحوار **التقدير**.</span><span class="sxs-lookup"><span data-stu-id="3a152-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![مربع حوار التقدير](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="3a152-204">حدد **موافق** لتأكيد التقدير والعودة إلى صفحة **كافة أوامر الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="3a152-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a152-205">عندما يتم تقدير أمر الإنتاج، يتم إنشاء أمر الشراء لصنف الخدمة S8050 للمورد US-801.</span><span class="sxs-lookup"><span data-stu-id="3a152-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="3a152-206">في جزء الإجراءات، في علامة التبويب **أمر الإنتاج** ، حدد **قائمة مكونات الصنف** لفتح صفحة **قائمة مكونات الصنف**، حيث يمكنك عرض بنود قائمة مكونات الصنف لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3a152-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="3a152-207">بالنسبة لصنف الخدمة S8050، لاحظ أنه يوجد مرجع لأمر الإنتاج الذي تم إنشائه عند تقدير أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3a152-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![بنود قائمة مكونات الصنف في أمر الإنتاج في صفحة قائمة مكونات الصنف](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="3a152-209">قم بإغلاق صفحة **قائمة مكونات الصنف** للرجوع إلى صفحة **كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="3a152-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="3a152-210">في جزء الإجراءات، في علامة التبويب **الجدول**، حدد **جدولة الوظائف** لفتح مربع الحوار **جدولة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="3a152-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="3a152-211">حدد القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3a152-211">Specify the following values:</span></span>

    - <span data-ttu-id="3a152-212">في حقل **اتجاه الجدولة**، حدد **تقديم من الغد**.</span><span class="sxs-lookup"><span data-stu-id="3a152-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="3a152-213">قم بتعيين خيار **قدرة محدودة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3a152-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![مربع حوار جدولة الوظائف](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="3a152-215">حدد **موافق** لإغلاق مربع حوار **جدولة الوظائف** والعودة إلى صفحة **كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="3a152-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="3a152-216">في جزء "الإجراءات"، في علامة التبويب **الجدول** ، حدد **"جانت"** لفتح صفحة **مخطط جانت - عرض المورد**.</span><span class="sxs-lookup"><span data-stu-id="3a152-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="3a152-217">يوفر مخطط جانت نظرة عامة مرئية لكيفية جدولة وظائف الإنتاج في الموارد.</span><span class="sxs-lookup"><span data-stu-id="3a152-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="3a152-218">لاحظ أن عملية التغطية الخارجية تتكون من ثلاث وظائف: وظيفة المعالجة، وظيفة النقل ووظيفة وقت انتظار.</span><span class="sxs-lookup"><span data-stu-id="3a152-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![مخطط جانت في صفحة مخطط جانت - عرض الموارد](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="3a152-220">قم بإغلاق صفحة **مخطط جانت- عرض الموارد** للرجوع إلى صفحة **كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="3a152-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="3a152-221">في جزء الإجراءات، في علامة التبويب **أمر الإنتاج**، حدد **الإصدار** لفتح مربع الحوار **الإصدار**.</span><span class="sxs-lookup"><span data-stu-id="3a152-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![مربع حوار الإصدار](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="3a152-223">حدد **موافق** لإغلاق مربع الحوار **الإصدار**.</span><span class="sxs-lookup"><span data-stu-id="3a152-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="3a152-224">حدد **التحكم بالإنتاج \>المهام الدورية \>إصدار إلى المستودع \>الإصدار التلقائي لقائمة مكونات الصنف وبنود المعادلة** لفتح مربع حوار **الإصدار التلقائي لقائمة مكونات الصنف وبنود المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="3a152-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![الإصدار التلقائي لمربع حوار قائمة مكونات الصنف وبنود المعادلة](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="3a152-226">حدد **موافق** لتشغيل الإصدار التلقائي لوظيفة قائمة مكونات الصنف وبنود المعادلة.</span><span class="sxs-lookup"><span data-stu-id="3a152-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="3a152-227">تنتقي إصدارات الوظيفة هذه العمل للمواد الخام للمستودع.</span><span class="sxs-lookup"><span data-stu-id="3a152-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="3a152-228">حدد **التحكم بالإنتاج \>أوامر الإنتاج \>كافة أوامر الإنتاج** لفتح صفحة **كافة أوامر الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="3a152-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="3a152-229">استخدم حقل عامل التصفية السريع لتحديد أمر الإنتاج الذي كنت تعمل عليه.</span><span class="sxs-lookup"><span data-stu-id="3a152-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="3a152-230">في جزء الإجراءات، في علامة تبويب **المستودع** ، حدد **تفاصيل العمل** لفتح صفحة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="3a152-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="3a152-231">لاحظ أن الصفحة تعرض مجموعتي عمل لانتقاء المادة الخام.</span><span class="sxs-lookup"><span data-stu-id="3a152-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="3a152-232">يكون العمل الأول للمواد M8100 و M8101.</span><span class="sxs-lookup"><span data-stu-id="3a152-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="3a152-233">تستهلك هذه المواد من خلال العملية 10.</span><span class="sxs-lookup"><span data-stu-id="3a152-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="3a152-234">يكون العمل الثاني للمواد M8202 و M8250.</span><span class="sxs-lookup"><span data-stu-id="3a152-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="3a152-235">تم استهلاك هذه المواد بواسطة العملية 20، والتي تُعد عملية متعاقد عليها من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![مجموعتي عمل لانتقاء المادة الخام في صفحة العمل](./media/subcontract22_work-page.png)

26. <span data-ttu-id="3a152-237">بدء تشغيل تطبيق المستودع لمعالجة عمل المستودع للعملية 10.</span><span class="sxs-lookup"><span data-stu-id="3a152-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="3a152-238">حدد **التحكم بالإنتاج \>أوامر الإنتاج \>كافة أوامر الإنتاج** لفتح صفحة **كافة أوامر الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="3a152-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="3a152-239">استخدم حقل عامل التصفية السريع لتحديد أمر الإنتاج الذي كنت تعمل عليه.</span><span class="sxs-lookup"><span data-stu-id="3a152-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="3a152-240">في جزء الإجراءات، في علامة التبويب **أمر الإنتاج**، حدد **بداية** لفتح مربع الحوار **بداية**.</span><span class="sxs-lookup"><span data-stu-id="3a152-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="3a152-241">في علامة التبويب **عام** ، حدد القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3a152-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="3a152-242">في حقل **من العملية رقم.**</span><span class="sxs-lookup"><span data-stu-id="3a152-242">In the **From Oper. No.**</span></span> <span data-ttu-id="3a152-243">حدد **10**.</span><span class="sxs-lookup"><span data-stu-id="3a152-243">field, select **10**.</span></span>
    - <span data-ttu-id="3a152-244">في حقل **إلى العملية رقم.**</span><span class="sxs-lookup"><span data-stu-id="3a152-244">In the **To Oper. No.**</span></span> <span data-ttu-id="3a152-245">، حدد **10**.</span><span class="sxs-lookup"><span data-stu-id="3a152-245">field, select **10**.</span></span>

    ![مجموعة القيم في علامة التبويب عام](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="3a152-247">حدد **موافق** لإغلاق مربع حوار **بداية** والعودة إلى صفحة **كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="3a152-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="3a152-248">لاحظ أن حالة أمر الإنتاج الآن هي **تم البدء**.</span><span class="sxs-lookup"><span data-stu-id="3a152-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="3a152-249">تم استهلاك المواد للعملية 10 من خلال الترحيل التلقائي لدفتر يومية قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="3a152-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="3a152-250">يتم حساب استهلاك الوقت للعملية 10 من خلال الترحيل التلقائي لدفتر يومية بطاقة المسار.</span><span class="sxs-lookup"><span data-stu-id="3a152-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="3a152-251">بدء تشغيل تطبيق المستودع لمعالجة عمل المستودع للعملية 20.</span><span class="sxs-lookup"><span data-stu-id="3a152-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="3a152-252">في جزء الإجراءات، في علامة التبويب **أمر الإنتاج**، حدد **بداية** لفتح مربع الحوار **بداية**.</span><span class="sxs-lookup"><span data-stu-id="3a152-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="3a152-253">في علامة التبويب **عام** ، حدد القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="3a152-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="3a152-254">في حقل **من العملية رقم.**</span><span class="sxs-lookup"><span data-stu-id="3a152-254">In the **From Oper. No.**</span></span> <span data-ttu-id="3a152-255">، حدد **20**.</span><span class="sxs-lookup"><span data-stu-id="3a152-255">field, select **20**.</span></span>
    - <span data-ttu-id="3a152-256">في حقل **إلى العملية رقم.**</span><span class="sxs-lookup"><span data-stu-id="3a152-256">In the **To Oper. No.**</span></span> <span data-ttu-id="3a152-257">، حدد **20**.</span><span class="sxs-lookup"><span data-stu-id="3a152-257">field, select **20**.</span></span>
    - <span data-ttu-id="3a152-258">في حقل **كمية** ، أدخل **10**.</span><span class="sxs-lookup"><span data-stu-id="3a152-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="3a152-259">حدد خيار **ترحيل قائمة الانتقاء الآن** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="3a152-259">Set the **Post picking list now** option to **No**.</span></span>

    ![مجموعة القيم في علامة التبويب عام](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="3a152-261">حدد **موافق** لإغلاق مربع حوار **بداية** والعودة إلى صفحة **كافة أوامر الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="3a152-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="3a152-262">يتم إنشاء قائمة انتقاء للمواد المستخدمة لعملية التغطية ولصنف الخدمة.</span><span class="sxs-lookup"><span data-stu-id="3a152-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="3a152-263">يمثل صنف الخدمة تكلفة العملية المتعاقد عليها من الباطن.</span><span class="sxs-lookup"><span data-stu-id="3a152-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="3a152-264">في جزء الإجراءات، في علامة التبويب **عرض** ، حدد **قائمة الانتقاء** لفتح صفحة **قائمة الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="3a152-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="3a152-265">حدد قائمة الانتقاء التي لم يتم ترحيلها، ثم حدد رقم دفتر اليومية لعرض بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="3a152-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![بنود دفتر اليومية في صفحة قائمة الانتقاء](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="3a152-267">في جزء الإجراءات، حدد **طباعة**\>**تقرير قائمة الانتقاء** لفتح مربع حوار **تقرير قائمة الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="3a152-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="3a152-268">تعيين خيار **استخدام مخطط مذكرة التسليم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3a152-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![مربع حوار تقرير قائمة الانتقاء](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="3a152-270">حدد **موافق** لإنشاء تقرير **قائمة الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="3a152-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="3a152-271">في هذه الحالة، تتم طباعة مذكرة تسليم مورد من دفتر يومية قائمة انتقاء الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="3a152-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="3a152-272">تُحدد مذكرة التسليم المواد المشحونة إلى المورد الذي سوف يقوم بتنفيذ عملية التغطية.</span><span class="sxs-lookup"><span data-stu-id="3a152-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![تقرير قائمة الانتقاء](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="3a152-274">قم بإغلاق تقرير **قائمة الانتقاء** للرجوع إلى صفحة **قائمة الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="3a152-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="3a152-275">في جزء الإجراءات، حدد **ترحيل** لفتح مربع حوار **ترحيل دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="3a152-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![مربع حوار ترحيل دفتر اليومية](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="3a152-277">حدد **موافق** لإغلاق مربع الحوار **ترحيل دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="3a152-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="3a152-278">فتح أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3a152-278">Open the purchase order.</span></span>

    ![صفحة أمر الشراء](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="3a152-280">في جزء الإجراءات،  في علامة التبويب **شراء** ، حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="3a152-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="3a152-281">حدد **ترحيل** لفتح مربع الحوار **ترحيل دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="3a152-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="3a152-282">حدد **موافق** لإغلاق مربع حوار **ترحيل دفتر اليومية** والعودة إلى صفحة **أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="3a152-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="3a152-283">قم بتغيير سعر الوحدة من **33** إلى **40**.</span><span class="sxs-lookup"><span data-stu-id="3a152-283">Change the unit price from **33** to **40**.</span></span>

    ![سعر الوحدة الذي تم تغييره على صفحة أمر الشراء](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="3a152-285">تأكيد أمر الشراء مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="3a152-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="3a152-286">إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="3a152-286">Product receipt.</span></span>

    ![مربع حوار ترحيل إيصال استلام المنتجات](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="3a152-288">فاتورة الشراء.</span><span class="sxs-lookup"><span data-stu-id="3a152-288">Purchase invoice.</span></span>
52. <span data-ttu-id="3a152-289">تحديث حالة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="3a152-289">Update the match status.</span></span>

    ![صفحة فواتير الموردين](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="3a152-291">الإبلاغ كمنته.</span><span class="sxs-lookup"><span data-stu-id="3a152-291">Report as finished.</span></span>

    ![مربع حوار الإبلاغ كمنتهِ](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="3a152-293">إنهاء.</span><span class="sxs-lookup"><span data-stu-id="3a152-293">End.</span></span>

    ![مربع حوار إنهاء](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="3a152-295">مقارنة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3a152-295">Cost comparison.</span></span>

    ![مخططات مقارنة التكلفة](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="3a152-297">إعداد مفقود في البيانات.</span><span class="sxs-lookup"><span data-stu-id="3a152-297">Missing setup in data.</span></span>
