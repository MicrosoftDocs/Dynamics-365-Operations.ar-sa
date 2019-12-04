---
title: إعداد معلمات تنسيق التقارير الإلكترونية لكل كيان قانوني
description: يشرح هذا الموضوع كيف يمكنك إعداد معلمات تنسيق التقارير الإلكترونية (ER) لكل كيان قانوني.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9c5884bba494d2dd44f9204667144402a88ddec8
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694328"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="85a1d-103">إعداد معلمات تنسيق التقارير الإلكترونية لكل كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="85a1d-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="85a1d-104">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="85a1d-104">Prerequisites</span></span>

<span data-ttu-id="85a1d-105">لإكمال هذه الخطوات، يجب أولا إكمال الخطوات في موضوع [تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة للكيان القانوني](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="85a1d-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="85a1d-106">لإكمال الامثله الموجودة في هذا الموضوع ، يجب ان يكون لديك حق الوصول إلى Microsoft Dynamics 365 Finance (Finance) لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="85a1d-107">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="85a1d-107">Electronic reporting developer</span></span>
- <span data-ttu-id="85a1d-108">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="85a1d-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="85a1d-109">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="85a1d-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="85a1d-110">استيراد تكوينات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="85a1d-110">Import ER configurations</span></span>

1.  <span data-ttu-id="85a1d-111">تسجيل الدخول إلى البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="85a1d-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="85a1d-112">في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="85a1d-113">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="85a1d-114">قم باستيراد، إلى المثيل الحالي لـ Finance، التكوينات التي قمت بتصديرها من خدمات التكوين التنظيمية (RCS) اثناء قيامك بإكمال الخطوات الموجودة في موضوع [تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة لكل كيان قانوني](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="85a1d-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="85a1d-115">اتبع الخطوات التالية لكل تكوين خاص بالتقرير الكتروني (ER) ، بالترتيب التالي: نموذج البيانات وتعيين الطراز والتنسيقات.</span><span class="sxs-lookup"><span data-stu-id="85a1d-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="85a1d-116">حدد **Exchange \> تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="85a1d-117">حدد **استعراض** لتحديد الملف اللازم لتكوين التقارير الإلكترونية المطلوب بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="85a1d-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="85a1d-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-118">Select **OK**.</span></span>
    
    <span data-ttu-id="85a1d-119">يبين الرسم التوضيحي التالي التكوينات التي يجب ان تكون لديك عند الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="85a1d-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![صفحة تكوينات التقارير الإلكترونية](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="85a1d-121">إعداد المعلمات الخاصة بشركة DEMF</span><span class="sxs-lookup"><span data-stu-id="85a1d-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="85a1d-122">يمكنك استخدام إطار عمل التقارير الإلكترونية لاعداد المعلمات الخاصة بالتطبيق لتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="85a1d-123">حدد الكيان القانوني **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="85a1d-124">في شجره التكوينات، حدد تنسيق **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="85a1d-125">في جزء الإجراءات، على علامة تبويب **التكوينات**، في المجموعة **المعلمات الخاصة بالتطبيق**، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![صفحة المعلمات الخاصة بتطبيق التقارير الإلكترونية](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="85a1d-127">في صفحة **المعلمات الخاصة بالتطبيق**، يمكنك تكوين قواعد مصدر بيانات **المحدد** لتنسيق **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="85a1d-128">إذا كان التنسيق الأساسي للتقارير الإلكترونية يحتوي علي العديد من مصادر البيانات من نوع **البحث**، يجب عليك تحديد مصدر البيانات المطلوب في علامة التبويب السريعة **عمليات البحث** قبل ن يمكنك بدء تكوين مجموعة القواعد لمصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="85a1d-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="85a1d-129">بالنسبة لكل مصدر بيانات ، يمكنك تكوين قواعد منفصلة لكل إصدار من إصدارات التنسيق المحددة للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="85a1d-130">تقوم المجموعة الكاملة من القواعد لكافة مصادر بيانات البحث المتوفرة في الإصدار المحدد من التنسيق الأساسي لللتقارير الإلكترونية بإنشاء المعلمات الخاصة بالتطبيق لتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="85a1d-131">حدد الإصدار **1.1.1** الخاص بتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="85a1d-132">على علامة التبويب السريعة **الشروط** ، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="85a1d-133">في حقل **الكود** الخاص بالسجل الجدسد، حدد سهم القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="85a1d-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="85a1d-134">يقدم البحث قائمه بأكواد الضريبة للتحديد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="85a1d-135">يتم إرجاع هذه القائمة بواسطة مصدر بيانات **Model.Data.Tax** الذي تم تكوينه باستخدام التنسيق الأساسي للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="85a1d-136">نظرا لان مصدر البيانات هذا يحتوي علي حقل **الاسم**، يظهر اسم كل كود ضريبة في البحث.</span><span class="sxs-lookup"><span data-stu-id="85a1d-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![صفحة المعلمات الخاصة بتطبيق التقارير الإلكترونية](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="85a1d-138">حدد كود الضريبة **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="85a1d-139">في حقل **نتيجة البحث** الخاص بالسجل الجديد، حدد سهم القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="85a1d-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="85a1d-140">يقدم البحث قائمه بالقيم الخاصة بتعداد تنسيق TaxationLevel للتحديد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="85a1d-141">لاحظ انه إذا تم تحديد اللغة المانيه كلغة المستخدم المفضلة التي قمت بتسجيل الدخول بها ، ستكون تسميات القيم في البحث باللغة المانيه ، شرط ان تتم ترجمتها في التنسيق الأساسي للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="85a1d-142">بالاضافه إلى ذلك ، إذا تمت ترجمه تسميه مصدر بيانات البحث، ستظهر هذه التسمية في اللغة المفضلة للمستخدم في علامة التبويب **عمليات البحث**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![صفحة المعلمات الخاصة بتطبيق التقارير الإلكترونية](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="85a1d-144">حدد قيمه **الضرائب العادية**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="85a1d-145">باضافه هذا السجل ، قم بتحديد القاعدة التالية: كلما تم طلب مصدر بيانات البحث عن **المحدد** وتم تمرير كود ضريبة **VAT19** كوسيطة، فسيتم إرجاع **الضرائب العادية** كمستوي الضرائب المطلوب.</span><span class="sxs-lookup"><span data-stu-id="85a1d-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="85a1d-146">حدد **إضافة**، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="85a1d-147">في حقل **الكود**، حدد كود الضريبة **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="85a1d-148">في حقل **نتيجة البحث**، حدد قيمة **الضرائب العادية**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="85a1d-149">حدد **إضافة** مرة أخرى، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="85a1d-150">في حقل **الكود**، حدد كود الضريبة **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="85a1d-151">في حقل **نتيجة البحث**، حدد قيمة **الضرائب المخفضة**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="85a1d-152">حدد **إضافة** مرة أخرى، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="85a1d-153">في حقل **الكود**، حدد كود الضريبة **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="85a1d-154">في حقل **نتيجة البحث**، حدد قيمة **الضرائب المخفضة**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="85a1d-155">حدد **إضافة** مرة أخرى، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="85a1d-156">في حقل **الكود**، حدد كود الضريبة **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="85a1d-157">في حقل **نتيجة البحث**، حدد قيمة **لا ضرائب**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="85a1d-158">حدد **إضافة** مرة أخرى، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="85a1d-159">في حقل **الكود**، حدد كود الضريبة **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="85a1d-160">في حقل **نتيجة البحث**، حدد قيمة **لا ضرائب**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="85a1d-161">حدد **إضافة** مرة أخرى، ثم اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="85a1d-162">في حقل **الكود**، حدد خيار **\*غير فارغ\***.</span><span class="sxs-lookup"><span data-stu-id="85a1d-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="85a1d-163">في حقل **نتيجة البحث**، حدد قيمة **آخر**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="85a1d-164">بإضافة هذا السجل الأخير ، فإنك تحدد القاعدة التالية: عندما لا يفي رمز الضريبة الذي يتم تمريره كوسيطة بأي من القواعد السابقة ، سيرجع مصدر بيانات البحث **آخر** باعتباره مستوى الضرائب المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="85a1d-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![صفحة المعلمات الخاصة بتطبيق التقارير الإلكترونية](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="85a1d-166">في حقل **الحالة**، حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="85a1d-167">عند تشغيل إصدار تنسيق التقارير الإلكترونية بحالة **مكتمل** أو **مشترك**، يجب ان تكون هذه المجموعة بحالة **مكتملة**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="85a1d-168">والا، ستتم مقاطعه عمليه تنفيذ تنسيق التقارير الإلكترونية الأساسي عند محاولة التنسيق تحميل البيانات من مجموعة القواعد هذه أثناء تشغيل مصدر بيانات البحث عن **المحدد**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="85a1d-169">عند تشغيل إصدار تنسيق تقارير إلكترونية بحالة **مسودة**، يمكن ان يصل التنسيق الأساسي للتقارير الإلكترونية إلى مجموعة القواعد هذه، بغض النظر عن حالتها.</span><span class="sxs-lookup"><span data-stu-id="85a1d-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="85a1d-170">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-170">Select **Save**.</span></span>
18. <span data-ttu-id="85a1d-171">أغلق صفحة **المعلمات الخاصة بالتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="85a1d-172">تشغيل تنسيق التقارير الإلكترونية في شركة DEMF</span><span class="sxs-lookup"><span data-stu-id="85a1d-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="85a1d-173">في شجره التكوينات، حدد تنسيق **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="85a1d-174">في جزء الإجراءات، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="85a1d-175">في مربع الحوار الذي يظهر، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="85a1d-176">تنزيل كشف الحساب الذي تم إنشاؤه وتخزينه محليا.</span><span class="sxs-lookup"><span data-stu-id="85a1d-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="85a1d-177">في العبارة التي تم إنشاؤها، لاحظ أنه تم وضع كود الضريبة **InVAT7** في المستوى **المخفض**، وتم وضع ملخصات أكواد الضرائب **VAT19** و**InVA19** في المستوى **العادي**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="85a1d-178">يتم تحديد هذا السلوك بواسطة التكوين في مجموعه القواعد التابعة للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="85a1d-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="85a1d-179">انتقل إلى **الضريبة \> الضرائب غير المباشرة \> ضريبة المبيعات \> أكواد ضرائب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="85a1d-180">حدد كود الضريبة **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="85a1d-181">في جزء الإجراءات، ضمن علامة التبويب **كود ضريبة المبيعات**، في مجموعة **الاستعلامات**، حدد **ضريبة المبيعات المنشورة** لعرض معلومات حول قيمه الضريبة وسعر الضريبة المطبق لكل كود ضريبة.</span><span class="sxs-lookup"><span data-stu-id="85a1d-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![صفحة ضريبة المبيعات المرحّلة](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="85a1d-183">قم بإغلاق صفحة ضريبة المبيعات المرحلة.</span><span class="sxs-lookup"><span data-stu-id="85a1d-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="85a1d-184">إعداد المعلمات الخاصة بشركة USMF</span><span class="sxs-lookup"><span data-stu-id="85a1d-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="85a1d-185">حدد الكيان القانوني **USMF**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="85a1d-186">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="85a1d-187">في شجره التكوينات، قم بتوسيع عنصر **النموذج للتعرف على الاستدعاءات ذات المعلمات**، وقم بتوسيع عنصر **التنسيق للتعرف على الاستدعاءات ذات المعلمات**، وحدد تنسيق **التنسيق للتعرف على كيفيه البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="85a1d-188">في جزء الإجراءات، على علامة تبويب **التكوينات**، في المجموعة **المعلمات الخاصة بالتطبيق**، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="85a1d-189">حدد الإصدار **1.1.1** الخاص بتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="85a1d-190">على علامة التبويب السريعة **الشروط** ، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="85a1d-191">في حقل **الكود** الخاص بالسجل الجدسد، حدد سهم القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="85a1d-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="85a1d-192">يقدم البحث الآن قائمه بأكواد الضريبة لضريبة شركة **USMF** للتحديد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![صفحة المعلمات الخاصة بتطبيق التقارير الإلكترونية](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="85a1d-194">حدد كود الضريبة **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="85a1d-195">في حقل **نتيجة البحث** في السجل الجديد، حدد قيمة **لا ضرائب**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="85a1d-196">حدد **إضافة** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="85a1d-196">Select **Add** again.</span></span>
11. <span data-ttu-id="85a1d-197">في حقل **الكود** في السجل الجديد، حدد خيار **\*غير فارغ\***.</span><span class="sxs-lookup"><span data-stu-id="85a1d-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="85a1d-198">في حقل **نتيجة البحث** في السجل الجديد، حدد قيمة **الضرائب العادية**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="85a1d-199">في حقل **الحالة**، حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="85a1d-200">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-200">Select **Save**.</span></span>

    ![صفحة المعلمات الخاصة بتطبيق التقارير الإلكترونية](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="85a1d-202">أغلق صفحة **المعلمات الخاصة بالتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="85a1d-203">تشغيل تنسيق التقارير الإلكترونية في شركة USMF</span><span class="sxs-lookup"><span data-stu-id="85a1d-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="85a1d-204">في شجره التكوينات، حدد تنسيق **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="85a1d-205">في جزء الإجراءات، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="85a1d-206">في مربع الحوار الذي يظهر، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="85a1d-207">تنزيل كشف الحساب الذي تم إنشاؤه وتخزينه محليا.</span><span class="sxs-lookup"><span data-stu-id="85a1d-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="85a1d-208">في العبارة التي تم إنشاؤها، لاحظ انك قمت الآن باعاده استخدام نفس تنسيق التقارير الإلكترونية لكيان قانوني مختلف، ولكن دون اجراء إيه تعديلات علي تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="85a1d-209">إعادة استخدام المعلمات التابعة للكيان القانوني</span><span class="sxs-lookup"><span data-stu-id="85a1d-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="85a1d-210">تصدير المعلمات</span><span class="sxs-lookup"><span data-stu-id="85a1d-210">Export parameters</span></span>

1.  <span data-ttu-id="85a1d-211">انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="85a1d-212">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="85a1d-213">في شجره التكوينات، حدد تنسيق **تنسيق للتعرف على كيفية البحث عن بيانات الكيان القانوني**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="85a1d-214">في جزء الإجراءات، على علامة تبويب **التكوينات**، في المجموعة **المعلمات الخاصة بالتطبيق**، حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="85a1d-215">حدد الإصدار **1.1.1** الخاص بتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="85a1d-216">في جزء الإجراءات، حدد **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="85a1d-217">قم بتنزيل كشف الحساب الذي تم إنشاؤه وتخزينه محليا.</span><span class="sxs-lookup"><span data-stu-id="85a1d-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="85a1d-218">لقد تم الآن تصدير المجموعة المكونة من المعلمات الخاصة بالتطبيق كملف XML.</span><span class="sxs-lookup"><span data-stu-id="85a1d-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="85a1d-219">استيراد المعلمات</span><span class="sxs-lookup"><span data-stu-id="85a1d-219">Import parameters</span></span>

1.  <span data-ttu-id="85a1d-220">حدد الإصدار **1.1.2** الخاص بتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="85a1d-221">في جزء الإجراءات، حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="85a1d-222">حدد **نعم** لتأكيد انك تريد تجاوز المعلمات الخاصة بالتطبيق الموجود لإصدار التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="85a1d-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="85a1d-223">حدد **استعراض** للبحث عن الملف الذي يحتوي علي المعلمات الخاصة بالتطبيق المصدر للإصدار **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="85a1d-224">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-224">Select **OK**.</span></span>

    <span data-ttu-id="85a1d-225">يحتوي الإصدار **1.1.2** لتنسيق التقارير الإلكترونية على نفس معلمات التطبيق التي قمت بتكوينها في الأصل لإصدار **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="85a1d-226">لاحظ ان المعلمات الخاصة بالتطبيق الخاص بتنسيق التقارير الإلكترونية تعتمد علي الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="85a1d-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="85a1d-227">لأعاده استخدام المعلمات الخاصة بالتطبيق والتي تم تكوينها لأحد الكيانات القانونية في كيان قانوني مختلف ، يجب تصديرها اثناء تسجيل الدخول إلى الكيان القانوني الأول ثم استيرادها بعد تسجيل الدخول إلى الكيان القانوني الآخر.</span><span class="sxs-lookup"><span data-stu-id="85a1d-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="85a1d-228">يمكنك أيضا استخدام هذا الأسلوب لتحويل المعلمات الخاصة بالتطبيق المرتبط بالتطبيق المرتبط التي تم تكوينها أصلا في مثيل واحد من Finance لمثيل آخر من Finance.</span><span class="sxs-lookup"><span data-stu-id="85a1d-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="85a1d-229">يجب مراعاه انك إذا قمت بتكوين المعلمات الخاصة بالتطبيق لإصدار واحد من التنسيق الخاص بالتطبيق واستيراد إصدار أحدث من نفس التنسيق إلى المثيل المالي الحالي ، فلن يتم تطبيق المعلمات الخاصة بالتطبيق الموجود علي الإصدار المستورد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="85a1d-230">عليك أيضا ان تدرك انه عند تحديد ملف للاستيراد ، تتم مقارنه بنيه المعلمات الخاصة بالتطبيق في ذلك الملف ببنيه مصدر البيانات لنوع **البحث** الذي تم تحديده للاستيراد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="85a1d-231">يتم اجراء عمليه الاستيراد عندما تطابق بنيه كل معلمه خاصه بتطبيق ما بنيه مصدر البيانات المقابل في تنسيق التقارير الإلكترونية المحدد للاستيراد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="85a1d-232">في حاله عدم تطابق البنيات ، ستظهر لك رسالة تحذير توضح انه لا يمكن اجراء الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="85a1d-233">إذا قمت بفرض اجراء الاستيراد ، سيتم تنظيف المعلمات الخاصة بالتطبيق الموجود لتنسيق التقارير الإلكترونية المحدد ، ويجب اعدادها من البداية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="85a1d-234">العلاقة بين المعلمات الخاصة بالتطبيق وتنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="85a1d-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="85a1d-235">يتم إنشاء العلاقة بين تنسيق التقارير الإلكترونية والمعلمات الخاصة بالتطبيق الخاص به بواسطة كود التعريف الفريد المستقل الخاص بتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="85a1d-236">ولذلك ، عند أزاله تنسيق التقارير الإلكترونية من Finance، يتم الاحتفاظ بالمعلمات الخاصة بالتطبيق والتي تم تكوينها لتنسيق التقارير الإلكترونية في المثيل الحالي لـ Finance.</span><span class="sxs-lookup"><span data-stu-id="85a1d-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="85a1d-237">ويمكن الوصول اليها في اي وقت يتم فيه إعادة استيراد التنسيق الأساسي للتقارير الإلكترونية في هذا المثيل الخاص بـ Finance.</span><span class="sxs-lookup"><span data-stu-id="85a1d-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="85a1d-238">الوصول إلى المعلمات الخاصة بالتطبيق باستخدام إطار عمل التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="85a1d-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="85a1d-239">في المثال السابق ، لقد قمت بالوصول إلى معلمات خاصه بالتطبيق لتنسيق التقارير الإلكترونية باستخدام إطار عمل التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="85a1d-240">وهذا الأسلوب لا يسمح لك بتقييد الوصول إلى المعلمات الخاصة بالتطبيق لتنسيق تقارير إلكترونية محدد.</span><span class="sxs-lookup"><span data-stu-id="85a1d-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="85a1d-241">إذا كان من الضروري تطبيق مثل هذه القيود، فاتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="85a1d-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="85a1d-242">قم إما باعاده استخدام عنصر قائمة **ERSolutionAppSpecificParametersDesigner** أو نفذ عنصر قائمة **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![صفحة Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="85a1d-244">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="85a1d-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="85a1d-245">قم بإنشاء زر عنصر قائمه جديد، وقم بربطه بالسجل المقابل من جدول **ERSolutionTable** عن طريق تعيين خاصية **مصدر البيانات** الخاص به إلى **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="85a1d-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![صفحة Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="85a1d-247">قم بإنشاء زر بسيط، وتجاوز طريقة **النقر** كما هو موضح في المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="85a1d-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="85a1d-248">وباستخدام هذا الأسلوب، يمكنك تحديد معرف حل فريد (معرف من خلال قيمة **GUID**) للسماح بالوصول إلى المعلمات الخاصة بالتطبيق فقط بالتنسيق المحدد للتقارير الإلكترونية والنسخ التابعة التي تم اشتقاقها منها.</span><span class="sxs-lookup"><span data-stu-id="85a1d-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="85a1d-249">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="85a1d-249">Additional resources</span></span>

[<span data-ttu-id="85a1d-250">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="85a1d-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="85a1d-251">تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة لكل كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="85a1d-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
