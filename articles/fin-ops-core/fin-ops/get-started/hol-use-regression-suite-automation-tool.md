---
title: استخدام برنامج Regression suite automation tool التعليمي
description: يوضح هذا الموضوع كيفية استخدام أداة Regression suite automation tool (RSAT). وهو يصف ميزات مختلفة ويوفر أمثلة تستخدم البرمجة النصية المتقدمة.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070810"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="6f5fc-104">استخدام البرنامج التعليمي للأداة Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="6f5fc-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="6f5fc-105">استخدم أدوات مستعرض الإنترنت لتنزيل هذه الصفحة وحفظها بتنسيق pdf.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="6f5fc-106">يعرفك هذا البرنامج التعليمي على بعض الميزات المتقدمة الخاصة بأداة Regression suite automation tool (RSAT)، ويتضمن تعيين عرض توضيحي، ويصف الاستراتيجية ونقاط التعليم الأساسية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="6f5fc-107">ميزات RSAT/مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="6f5fc-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="6f5fc-108">التحقق من قيمة الحقل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-108">Validate a field value</span></span>

<span data-ttu-id="6f5fc-109">للحصول على معلومات حول هذه الميزة، راجع [إنشاء تسجيل مهمة جديدة يحتوي وظيفة التحقق من الصحة](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="6f5fc-110">المتغير المحفوظ</span><span class="sxs-lookup"><span data-stu-id="6f5fc-110">Saved variable</span></span>

<span data-ttu-id="6f5fc-111">للحصول على معلومات حول هذه الميزة، راجع [تعديل تسجيل مهمة موجودة لإنشاء متغير محفوظ](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="6f5fc-112">حالة الاختبار المشتقة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-112">Derived test case</span></span>

1. <span data-ttu-id="6f5fc-113">افتح أداة Regression suite automation tool (RSAT)، وحدد كلا من حالتي الاختبار التي أنشأتها في [إعداد وتثبيت أداة Regression suite automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="6f5fc-114">حدد **جديد \> إنشاء حالة اختبار مشتقة**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-114">Select **New \> Create derived test case**.</span></span>

    ![أمر إنشاء أمر حالة اختبار مشتق في القائمة جديد](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="6f5fc-116">ستستلم رسالة توضح أنه سيتم إنشاء حالة اختبار مشتقة لكل حالة اختبار محددة في مجموعة الاختبار الحالية، وأن كل حالة اختبار مشتقة سيكون لها نسختها الخاصة من ملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-117">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f5fc-118">عند تشغيل حالة اختبار مشتقة، فإنها تستخدم تسجيل المهمة لحالة الاختبار الرئيسية الخاصة بها ونسخة خاصة بها من ملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-119">وبهذه الطريقة، يمكنك تشغيل نفس الاختبار مع معلمات مختلفة، دون الحاجة إلى الاحتفاظ بأكثر من تسجيل مهمة واحد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="6f5fc-120">لا يجب أن تكون حالة الاختبار المشتقة جزءا من مجموعة الاختبار نفسها المتخذة كحالة اختبار الأصل لها.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![مربع الرسالة](./media/use_rsa_tool_02.png)

    <span data-ttu-id="6f5fc-122">يتم إنشاء حالتي اختبار مشتقين إضافيتين، مع تحديد خانة الاختيار **مشتق؟** لهما.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![حالات الاختبار المشتقة التي تم إنشاؤها](./media/use_rsa_tool_03.png)

    <span data-ttu-id="6f5fc-124">يتم إنشاء حالة اختبار مشتقة بشكل تلقائي Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="6f5fc-125">وهي عنصر فرعي لحالة الاختبار **إنشاء منتج جديد** ويتم تعليمه بكلمة أساسية خاصة: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="6f5fc-126">يتم أيضا إضافة حالات الاختبار هذه تلقائيا إلى خطة الاختبار في Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT:الكلمة الأساسية DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="6f5fc-128">إذا كانت حالات الاختبار المشتقة التي تم إنشائها بترتيب غير صحيح لأي سبب، فاذهب إلى Azure DevOps، وأعد ترتيب حالات الاختبار في مجموعة الاختبار، بحيث يمكن لأداة RSAT تشغيلها بالترتيب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="6f5fc-129">حدد حالات الاختبار المشتقة، ثم حدد **تحرير** لفتح ملفات معلمات Excel المطابقة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="6f5fc-130">حرر ملفات معلمات Excel هذه بنفس الطريقة التي تم بها تحرير الملفات الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="6f5fc-131">بمعنى آخر، تأكد من تعيين معرف المنتج بحيث يتم إنشاؤه تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="6f5fc-132">وتأكد أيضا من نسخ المتغير المحفوظ إلى الحقول ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="6f5fc-133">في علامة التبويب **عام** لكل من ملفات معلمات Excel، قم بتحديث قائمة حقل **الشركة** إلى **USSI**، بحيث يتم تشغيل حالات الاختبار المشتقة مقابل كيان قانوني مختلف عن حالة الاختبار الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="6f5fc-134">لتشغيل حالات الاختبار لمستخدم محدد (أو الدور المرتبط بمستخدم معين)، يمكنك تحديث قيمه حقل **اختبار المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="6f5fc-135">حدد **تشغيل**، وتحقق من إنشاء المنتج في كل من الكيان القانوني USMF والكيان القانوني USSI.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="6f5fc-136">إخطارات التحقق</span><span class="sxs-lookup"><span data-stu-id="6f5fc-136">Validate notifications</span></span>

<span data-ttu-id="6f5fc-137">يمكن استخدام هذه الميزة للتحقق مما إذا كان الإجراء قد حدث أم لا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="6f5fc-138">علي سبيل المثال، عند إنشاء أمر إنتاج وتقديره ثم بدء تشغيله، يعرض التطبيق الرسالة "الإنتاج – بدء" لإعلامك بأنه قد تم بدء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![إخطار الإنتاج - بدء](./media/use_rsa_tool_05.png)

<span data-ttu-id="6f5fc-140">يمكنك التحقق من صحة هذه الرسالة عن طريق RSAT وذلك بإدخال نص الرسالة في علامة التبويب **MessageValidation** في ملف معلمة Excel للتسجيل المناسب.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![علامة تبويب التحقق من الرسالة](./media/use_rsa_tool_06.png)

<span data-ttu-id="6f5fc-142">بعد تشغيل حالة الاختبار، تتم مقارنة الرسالة الموجودة في ملف معلمة Excel بالرسالة المعروضة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="6f5fc-143">في حالة عدم تطابق الرسائل، ستفشل حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="6f5fc-144">يمكنك إدخال أكثر من رسالة واحدة في علامة تبويب **MessageValidation** في ملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-145">يمكن أن تكون الرسائل أيضا رسائل خطا أو تحذيرات بدلا من الرسائل الإخبارية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="6f5fc-146">التحقق من صحة القيم باستخدام عوامل التشغيل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-146">Validate values by using operators</span></span>

<span data-ttu-id="6f5fc-147">في الإصدارات السابقة من RSAT، يمكنك التحقق من صحة القيم فقط إذا كانت قيمة العنصر التحكم مساوية لقيمة متوقعة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="6f5fc-148">تتيح لك الميزة الجديدة التحقق من أن أحد المتغيرات لا يساوي أو أقل من أو أكبر من القيمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="6f5fc-149">لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة في العنصر التالي من **false** إلى **true**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="6f5fc-150">في ملف معلمة Excel، يظهر حقل **عامل تشغيل** جديد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f5fc-151">إذا كنت تستخدم إصدارا قديما من RSAT، يجب إنشاء ملفات معلمات جديدة لـ Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![حقل عامل التشغيل](./media/use_rsa_tool_07.png)

<span data-ttu-id="6f5fc-153">يوضح المثال التالي كيفية استخدام هذه الميزة للتحقق مما إذا كان المخزون الفعلي أكبر من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="6f5fc-154">في البيانات التوضيحية في شركة **USMF**، قم بإنشاء تسجيل مهام بالخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="6f5fc-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="6f5fc-155">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="6f5fc-156">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6f5fc-157">على سبيل المثال، قم بإجراء التصفية على قيمة **1000** للحقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="6f5fc-158">حدد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="6f5fc-159">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6f5fc-160">على سبيل المثال، قم بإجراء التصفية على القيمة **1** لحقل **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="6f5fc-161">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="6f5fc-162">تحقق من أن قيمة حقل **الإجمالي المتاح** هي **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="6f5fc-163">احفظ تسجيل المهام في مكتبة BPM في LCS، وقم بمزامنته مع Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="6f5fc-164">قم بإضافة حالة الاختبار إلى خطة الاختبار، وقم بتحميل حالة الاختبار إلى RSAT.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="6f5fc-165">افتح ملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-165">Open the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-166">في علامة تبويب **InventOnhandItem**، سوف تشاهد قسم **التحقق من InventOnhandItem** الذي يتضمن حقل **عامل التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![حقل عامل التشغيل](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="6f5fc-168">للتحقق مما إذا كان المخزون الفعلي سيكون دائمًا أكبر من 0، قم بتغيير القيمة في حقل **القيمة** من **411** إلى **0** وقيمة حقل **عامل التشغيل** من علامة يساوي (**=**) إلى أكبر من (**\>**).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![تم تغيير القيم لحقول القيمة وعامل التشغيل](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="6f5fc-170">احفظ ملف معلمات Excel وأغلقه.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="6f5fc-171">حدد **تحميل** لحفظ التغييرات التي أجريتها على ملف معلمات Excel إلى Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="6f5fc-172">والآن، إذا كانت قيمة حقل **الإجمالي المتوفر** للصنف المحدد في المخزون أكبر من 0 (صفر)، سيتم اجتياز الاختبارات، بغض النظر عن قيمة المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="6f5fc-173">سجلات المنشئ</span><span class="sxs-lookup"><span data-stu-id="6f5fc-173">Generator logs</span></span>

<span data-ttu-id="6f5fc-174">تقوم هذه الميزة بإنشاء مجلد يحتوي على سجلات حالات الاختبار التي تم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="6f5fc-175">لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة في العنصر التالي من **false** إلى **true**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="6f5fc-176">بعد تشغيل حالات الاختبار، يمكنك العثور على ملفات السجل تحت **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![المجلد GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="6f5fc-178">إذا كانت هناك حالات اختبار موجودة قبل تغيير القيمة في ملف .config، لن يتم إنشاء السجلات لحالات الاختبار هذه حتى تقوم بإنشاء ملفات تنفيذ اختبار جديدة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![إنشاء أمر ملفات تنفيذ النص فقط في القائمة جديد](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="6f5fc-180">لقطة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-180">Snapshot</span></span>

<span data-ttu-id="6f5fc-181">تقوم هذه الميزة بأخذ لقطات شاشة الخطوات التي تم إجراؤها أثناء تسجيل المهام.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="6f5fc-182">لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة للعنصر التالي من **false** إلى **true**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="6f5fc-183">تحت **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**، يتم إنشاء مجلد منفصل لكل حالة اختبار يتم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![مجلد اللقطات لحالة اختبار](./media/use_rsa_tool_12.png)

<span data-ttu-id="6f5fc-185">في كل من هذه المجلدات، يمكنك العثور على لقطات للخطوات التي تم تنفيذها أثناء تشغيل حالات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![ملفات اللقطات](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="6f5fc-187">التعيين</span><span class="sxs-lookup"><span data-stu-id="6f5fc-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="6f5fc-188">سيناريو</span><span class="sxs-lookup"><span data-stu-id="6f5fc-188">Scenario</span></span>

1. <span data-ttu-id="6f5fc-189">يقوم مصمم المنتج بإنشاء منتج جديد تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="6f5fc-190">تقوم إدارة الإنتاج بتهيئة أمر إنتاج لجعل مستوى المخزون من جزئين.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="6f5fc-191">ويبدأ التصنيع أمر الإنتاج وينهيه، ويتحقق من أن الكمية الفعلية من جزئين.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="6f5fc-192">يتلقى فريق المبيعات طلبا بأربعة أجزاء من المنتج الجديد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="6f5fc-193">بالتالي، يقوم فريق المبيعات بتحديث صافي المتطلبات عبر الخطة الديناميكية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="6f5fc-194">وبسبب عدم توفر سعة إضافية، يتم تعيين سياسة الترتيب الافتراضي إلى "الشراء بدلا من الصنع".</span><span class="sxs-lookup"><span data-stu-id="6f5fc-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="6f5fc-195">بالتالي، يتم إنشاء أمر شراء مخطط</span><span class="sxs-lookup"><span data-stu-id="6f5fc-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="6f5fc-196">يقوم المشتري بإضافة مورد، ويؤكد أمر الشراء المخطط، ثم يقوم بتأكيد أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="6f5fc-197">عند وصول البضائع التي تم شراؤها إلى المتجر، يقوم مشغل المتجر بالبحث في أمر الشراء المرتبط ويستلم البضائع.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="6f5fc-198">نظرا لأن الأمر مكتمل الآن، فيمكن انتقاء البضائع وتعبئتها مقابل أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="6f5fc-199">ينشر تطبيق المالية فاتورة الشراء وفاتورة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="6f5fc-200">يعرض الرسم التوضيحي التالي سير العمل لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-200">The following illustration shows the flow for this scenario.</span></span>

![سير عمل السيناريو التوضيحي](./media/use_rsa_tool_14.png)

<span data-ttu-id="6f5fc-202">يعرض الرسم التوضيحي التالي العمليات التجارية لهذا السيناريو في RSAT.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![العمليات التجارية للسيناريو التوضيحي](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="6f5fc-204">الاستراتيجية – التعليم الأساسي</span><span class="sxs-lookup"><span data-stu-id="6f5fc-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="6f5fc-205">البيانات</span><span class="sxs-lookup"><span data-stu-id="6f5fc-205">Data</span></span>

- <span data-ttu-id="6f5fc-206">تأكد أن لديك وحدات تخزين بيانات تمثيلية (نسخة من بيانات الإنتاج/التكوين الذهبي بالإضافة إلى بيانات تم ترحيلها).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="6f5fc-207">عند إنشاء البيانات الجديدة عبر مسجل المهام، قم بإنشاء أسماء الاختبارات التي لا تتعارض مع الأسماء الموجودة (علي سبيل المثال، استخدم بادئة مثل **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="6f5fc-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="6f5fc-208">استخدم استعادة النقطة الزمنية في Azure لإعادة تشغيل الاختبارات في بيئات ليست من المستوي 1.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="6f5fc-209">على الرغم من أنه يمكنك استخدام دالتي Excel **RANDOM** و**NOW** لإنشاء مجموعة فريدة، فإن الجهد يكون مرتفعا بشكل كبير.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="6f5fc-210">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="6f5fc-211">مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="6f5fc-211">Task recorder</span></span>

- <span data-ttu-id="6f5fc-212">حدد السيناريوهات قبل بدء التسجيل.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="6f5fc-213">يحتوي المشروع جيد الإدارة على سيناريوهات اختبار معرفة مسبقا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="6f5fc-214">لبناء حالة اختبار، ضع في الاعتبار مدي توقع نتيجة سيناريوهات الاختبار هذه.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="6f5fc-215">قسم التسجيلات في حالة تنفيذها بواسطة أدوار مختلفة، أو إذا كان هناك وقت انتظار أو حدث خارجي قبل الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="6f5fc-216">تجنب تحديد القيم في القوائم.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="6f5fc-217">بدلا من ذلك، استخدم تنسيقات نصية، مثل **FIFO** و **AudioRM** و **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="6f5fc-218">عندم تحدد في القائمة، يتم تسجيل موضع القيمة في القائمة، وليس القيمة نفسها.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="6f5fc-219">إذا تمت إضافة عناصر إلى هذه القائمة، يمكن تغيير وضع القيمة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="6f5fc-220">لذلك، سيقوم التسجيل الخاص بك باستخدام معلمة مختلفة، وقد يتأثر باقي السيناريو.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="6f5fc-221">فكر في سلوك المستخدمين المتعددين.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-221">Think about multi-user behavior.</span></span> <span data-ttu-id="6f5fc-222">علي سبيل المثال، لا تفترض أن أمر التوريد الذي تم إنشاؤه حديثا سيتم دوما تحديده تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="6f5fc-223">بدلا من ذلك، استخدم عامل التصفية دائما للعثور على الطلب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="6f5fc-224">استخدم وظيفة النسخ في مسجل المهام لحفظ اسم منتج تم إنشاؤه حديثا بحيث يمكن استخدامه في حالات الاختبار المتسلسلة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="6f5fc-225">استخدم وظيفة التحقق من الصحة في مسجل المهام لتعيين نقاط التحقق التي تتحقق من أن الخطوات تم تشغيلها بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="6f5fc-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="6f5fc-226">RSAT</span></span>

- <span data-ttu-id="6f5fc-227">لتشغيل الاختبار في شركة أخرى، يمكنك تغيير الشركة في علامة التبويب **عام** بملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-228">تأكد من توفر الإعدادات والبيانات في الشركة المحددة حديثا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="6f5fc-229">يمكنك تغيير مستخدم الاختبار في علامة التبويب **عام** بملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-230">حدد معرف البريد الإلكتروني الخاص بالمستخدم الذي سيقوم بتشغيل حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="6f5fc-231">بهذه الطريقة، يمكن تشغيل حالة الاختبار باستخدام أذونات الأمان الخاصة بالمستخدم المحدد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="6f5fc-232">للانتظار قبل بدء الاختبار، يمكنك تعريف توقف مؤقت في علامة التبويب **عام** بملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="6f5fc-233">يمكن استخدام الإيقاف المؤقت هذا في وظيفة دفعية (علي سبيل المثال، إذا كان من الضروري تشغيل سير عمل قبل إجراء الخطوة التالية.)</span><span class="sxs-lookup"><span data-stu-id="6f5fc-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="6f5fc-234">البرمجة المتقدمة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="6f5fc-235">CLI</span><span class="sxs-lookup"><span data-stu-id="6f5fc-235">CLI</span></span>

<span data-ttu-id="6f5fc-236">يمكن استدعاء RSAT من نافذة **موجه الأوامر** أو **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="6f5fc-237">تحقق من تعيين متغير البيئة **TestRoot** على مسار تثبيت RSAT.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="6f5fc-238">(في Microsoft Windows، افتح **لوحة التحكم**، وحدد **النظام والأمان \> النظام \> إعدادات الأمان المتقدمة**، ثم حدد **متغيرات البيئة**.)</span><span class="sxs-lookup"><span data-stu-id="6f5fc-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="6f5fc-239">افتح نافذة **موجه الأوامر** أو **PowerShell** كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="6f5fc-240">انتقل إلى دليل التثبيت RSAT.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="6f5fc-241">اسرد كافة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="6f5fc-242">؟</span><span class="sxs-lookup"><span data-stu-id="6f5fc-242">?</span></span> 
<span data-ttu-id="6f5fc-243">يظهر تعليمات حول كافة الأوامر المتوفرة والمعلمات الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="6f5fc-244">معلمات اختيارية</span><span class="sxs-lookup"><span data-stu-id="6f5fc-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="6f5fc-245">حيث ``[command]`` يكون أحد الأوامر المحددة أدناه.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="6f5fc-246">حول</span><span class="sxs-lookup"><span data-stu-id="6f5fc-246">about</span></span>
<span data-ttu-id="6f5fc-247">يعرض الإصدار الحالي.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="6f5fc-248">cls</span><span class="sxs-lookup"><span data-stu-id="6f5fc-248">cls</span></span>
<span data-ttu-id="6f5fc-249">يمسح الشاشة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="6f5fc-250">تنزيل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-250">download</span></span>
<span data-ttu-id="6f5fc-251">يقوم بتنزيل مرفقات لحالة الاختبار المحددة إلى دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="6f5fc-252">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6f5fc-253">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-254">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-254">Required parameters</span></span>
<span data-ttu-id="6f5fc-255">**``test_case_id``** تمثل معرف حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="6f5fc-256">**``output_dir``** تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6f5fc-257">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-258">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="6f5fc-259">تحرير</span><span class="sxs-lookup"><span data-stu-id="6f5fc-259">edit</span></span>
<span data-ttu-id="6f5fc-260">يسمح لك بفتح ملف المعلمات في برنامج Excel وتحريره.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-261">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-261">Required parameters</span></span>
<span data-ttu-id="6f5fc-262">**``excel_file``** يجب أن يحتوي على مسار كامل لملف Excel موجود.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-263">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="6f5fc-264">إنشاء</span><span class="sxs-lookup"><span data-stu-id="6f5fc-264">generate</span></span>
<span data-ttu-id="6f5fc-265">يقوم بإنشاء ملفات تنفيذ تجريبي ومعلمات لحالة الاختبار المحددة في دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="6f5fc-266">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6f5fc-267">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-268">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-268">Required parameters</span></span>
<span data-ttu-id="6f5fc-269">**``test_case_id``** تمثل معرف حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="6f5fc-270">**``output_dir``** تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6f5fc-271">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-272">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="6f5fc-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="6f5fc-273">generatederived</span></span>
<span data-ttu-id="6f5fc-274">يقوم بإنشاء حالة اختبار جديدة، مشتقة من حالة الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="6f5fc-275">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6f5fc-276">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-277">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-277">Required parameters</span></span>
<span data-ttu-id="6f5fc-278">**``parent_test_case_id``** تمثل معرف حالة الاختبار الأصلية.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="6f5fc-279">**``test_plan_id``** تمثل معرف خطة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="6f5fc-280">**``test_suite_id``** تمثل معرف مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-281">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="6f5fc-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="6f5fc-282">generatetestonly</span></span>
<span data-ttu-id="6f5fc-283">يقوم بإنشاء ملف تنفيذ تجريبي فقط لحالة الاختبار المحددة في دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="6f5fc-284">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6f5fc-285">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-286">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-286">Required parameters</span></span>
<span data-ttu-id="6f5fc-287">**``test_case_id``** تمثل معرف حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="6f5fc-288">**``output_dir``** تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6f5fc-289">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-290">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="6f5fc-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="6f5fc-291">generatetestsuite</span></span>
<span data-ttu-id="6f5fc-292">يقوم بإنشاء كافة حالات الاختبار للمجموعة المحددة في دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="6f5fc-293">يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="6f5fc-294">استخدم أي قيمة من العمود كمعلمة **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-295">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-295">Required parameters</span></span>
<span data-ttu-id="6f5fc-296">**``test_suite_name``** تمثل اسم مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="6f5fc-297">**``output_dir``** تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="6f5fc-298">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-299">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="6f5fc-300">تعليمات</span><span class="sxs-lookup"><span data-stu-id="6f5fc-300">help</span></span>
<span data-ttu-id="6f5fc-301">مماثل لـ [?](####?)</span><span class="sxs-lookup"><span data-stu-id="6f5fc-301">Identical to the [?](####?)</span></span> <span data-ttu-id="6f5fc-302">الأمر</span><span class="sxs-lookup"><span data-stu-id="6f5fc-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="6f5fc-303">القائمة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-303">list</span></span>
<span data-ttu-id="6f5fc-304">يسرد كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="6f5fc-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="6f5fc-305">listtestplans</span></span>
<span data-ttu-id="6f5fc-306">يسرد كافة خطط الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="6f5fc-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="6f5fc-307">listtestsuite</span></span>
<span data-ttu-id="6f5fc-308">يسرد حالات الاختبار لمجموعة الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="6f5fc-309">يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="6f5fc-310">استخدم أي قيمة من العمود الأول كمعلمة **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-311">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-311">Required parameters</span></span>
<span data-ttu-id="6f5fc-312">**``suite_name``** اسم المجموعة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-313">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="6f5fc-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="6f5fc-314">listtestsuitenames</span></span>
<span data-ttu-id="6f5fc-315">يسرد كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="6f5fc-316">تشغيل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-316">playback</span></span>
<span data-ttu-id="6f5fc-317">يقوم بتشغيل حالة اختبار باستخدام ملف Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-318">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-318">Required parameters</span></span>
<span data-ttu-id="6f5fc-319">**``excel_file``** مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="6f5fc-320">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="6f5fc-321">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="6f5fc-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="6f5fc-322">playbackbyid</span></span>
<span data-ttu-id="6f5fc-323">يقوم بتشغيل عدة حالات اختبار في الحال.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="6f5fc-324">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="6f5fc-325">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-326">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-326">Required parameters</span></span>
<span data-ttu-id="6f5fc-327">**``test_case_id1``** معرف حالة اختبار موجودة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="6f5fc-328">**``test_case_id2``** معرف حالة اختبار موجودة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="6f5fc-329">**``test_case_idN``** معرف حالة اختبار موجودة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="6f5fc-330">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="6f5fc-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="6f5fc-331">playbackmany</span></span>
<span data-ttu-id="6f5fc-332">يقوم بتشغيل العديد من حالات الاختبار في الحال، باستخدام ملفات Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-333">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-333">Required parameters</span></span>
<span data-ttu-id="6f5fc-334">**``excel_file1``** مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="6f5fc-335">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-335">File must exist.</span></span>  
<span data-ttu-id="6f5fc-336">**``excel_file2``** مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="6f5fc-337">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-337">File must exist.</span></span>  
<span data-ttu-id="6f5fc-338">**``excel_fileN``** مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="6f5fc-339">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="6f5fc-340">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="6f5fc-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="6f5fc-341">playbacksuite</span></span>
<span data-ttu-id="6f5fc-342">يقوم بتشغيل كافة حالات الاختبار من مجموعة الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="6f5fc-343">يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="6f5fc-344">استخدم أي قيمة من العمود الأول كمعلمة **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-345">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-345">Required parameters</span></span>
<span data-ttu-id="6f5fc-346">**``suite_name``** اسم المجموعة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-347">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="6f5fc-348">إنهاء</span><span class="sxs-lookup"><span data-stu-id="6f5fc-348">quit</span></span>
<span data-ttu-id="6f5fc-349">يغلق التطبيق.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="6f5fc-350">تحميل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-350">upload</span></span>
<span data-ttu-id="6f5fc-351">يقوم بتحميل كل الملفات التي تنتمي لمجموعة الاختبار المحددة أو حالات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="6f5fc-352">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-352">Required parameters</span></span>
<span data-ttu-id="6f5fc-353">**``suite_name``** سيتم تحميل كل الملفات التي تنتمي لمجموعة الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="6f5fc-354">**``testcase_id``** سيتم تحميل كل الملفات التي تنتمي لحالة (حالات) الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-355">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="6f5fc-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="6f5fc-356">uploadrecording</span></span>
<span data-ttu-id="6f5fc-357">يقوم بتحميل ملف تسجيل واحد ينتمي لحالات الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="6f5fc-358">المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-358">Required parameters</span></span>
<span data-ttu-id="6f5fc-359">**``testcase_id``** سيتم تحميل ملف تسجيل واحد ينتمي لحالات الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="6f5fc-360">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="6f5fc-361">استخدام</span><span class="sxs-lookup"><span data-stu-id="6f5fc-361">usage</span></span>
<span data-ttu-id="6f5fc-362">يظهر طريقتين لاستدعاء هذا التطبيق: واحد باستخدام ملف إعداد افتراضي، آخر يوفر ملف إعداد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="6f5fc-363">أمثلة Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f5fc-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="6f5fc-364">تشغيل حالة اختبار في حلقة</span><span class="sxs-lookup"><span data-stu-id="6f5fc-364">Run a test case in a loop</span></span>

<span data-ttu-id="6f5fc-365">لديك برنامج اختبار نصي يقوم بإنشاء عميل جديد.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="6f5fc-366">بواسطة البرمجة النصية، يمكن تشغيل حالة الاختبار هذه في حلقة عن طريق الترتيب العشوائي للبيانات التالية قبل تشغيل كل تكرار:</span><span class="sxs-lookup"><span data-stu-id="6f5fc-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="6f5fc-367">معرف العميل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-367">Customer ID</span></span>
- <span data-ttu-id="6f5fc-368">اسم العميل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-368">Customer name</span></span>
- <span data-ttu-id="6f5fc-369">عنوان العميل</span><span class="sxs-lookup"><span data-stu-id="6f5fc-369">Customer address</span></span>

<span data-ttu-id="6f5fc-370">سيكون معرف العميل بالتنسيق *ATCUS\<رقم\>*، حيث يكون \<الرقم\> قيمة بين **000000001** و **999999999**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="6f5fc-371">يستخدم المثال التالي معلمة واحدة **البدء**، لتعريف الرقم الأول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="6f5fc-372">يستخدم معلمة ثانية، **nr**، لتحديد عدد العملاء الذين يجب إنشاؤهم.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="6f5fc-373">بالنسبة لكل تكرار، يتم تغيير المعلمات الموجودة في ملف معلمة Excel باستخدام دالة UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="6f5fc-374">بعد ذلك يتم استدعاء سطر أوامر RSAT في دالة RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="6f5fc-375">افتح بيئة البرمجة المتكاملة (ISE) في Microsoft Windows PowerShell في وضع المسؤول، والصق الكود التالي في الإطار الذي يسمى **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="6f5fc-376">تشغيل برنامج نصي يعتمد على البيانات في Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6f5fc-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="6f5fc-377">يستخدم المثال التالي استدعاء بروتوكول البيانات المفتوحة (OData) للعثور على حالة الأمر لأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="6f5fc-378">إذا لم تتم **فوترة** الحالة، يمكنك، على سبيل المثال، استدعاء حالة اختبار RSAT التي ترحّل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
