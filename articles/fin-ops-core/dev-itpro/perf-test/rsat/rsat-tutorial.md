---
title: البرنامج التعليمي للأداة Regression Suite Automation Tool
description: يوضح هذا الموضوع كيفية استخدام أداة Regression suite automation tool (RSAT). وهو يصف ميزات مختلفة ويوفر أمثلة تستخدم البرمجة النصية المتقدمة.
author: robinarh
manager: AnnBe
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c4c0f9340085341ab60f97b55dacf36624e5f46
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036693"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="b5a09-104">البرنامج التعليمي للأداة Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="b5a09-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b5a09-105">استخدم أدوات مستعرض الإنترنت لتنزيل هذه الصفحة وحفظها بتنسيق pdf.</span><span class="sxs-lookup"><span data-stu-id="b5a09-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="b5a09-106">يعرفك هذا البرنامج التعليمي على بعض الميزات المتقدمة الخاصة بأداة Regression suite automation tool (RSAT)، ويتضمن تعيين عرض توضيحي، ويصف الاستراتيجية ونقاط التعليم الأساسية.</span><span class="sxs-lookup"><span data-stu-id="b5a09-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="b5a09-107">ميزات مهمة في RSAT ومسجل المهام</span><span class="sxs-lookup"><span data-stu-id="b5a09-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="b5a09-108">التحقق من قيمة الحقل</span><span class="sxs-lookup"><span data-stu-id="b5a09-108">Validate a field value</span></span>

<span data-ttu-id="b5a09-109">يسمح لك RSAT بتضمين خطوات التحقق من الصحة داخل حالة اختبار بك للتحقق من صحة القيم المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="b5a09-110">للحصول على معلومات حول هذه الميزة، راجع المقال [التحقق من صحة القيم المتوقعة](rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="b5a09-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="b5a09-111">يوضح المثال التالي كيفية استخدام هذه الميزة للتحقق مما إذا كان المخزون الفعلي أكبر من 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="b5a09-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="b5a09-112">في البيانات التوضيحية في شركة **USMF**، قم بإنشاء تسجيل مهام بالخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b5a09-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="b5a09-113">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="b5a09-114">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="b5a09-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b5a09-115">على سبيل المثال، قم بإجراء التصفية على قيمة **1000** للحقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="b5a09-116">حدد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="b5a09-117">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="b5a09-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b5a09-118">على سبيل المثال، قم بإجراء التصفية على القيمة **1** لحقل **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="b5a09-119">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5a09-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="b5a09-120">تحقق من أن قيمة حقل **الإجمالي المتاح** هي **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="b5a09-121">حفظ تسجيل المهام **كتسجيل مطور** وأرفقه بحالة اختبارك في Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="b5a09-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="b5a09-122">قم بإضافة حالة الاختبار إلى خطة الاختبار، وقم بتحميل حالة الاختبار إلى RSAT.</span><span class="sxs-lookup"><span data-stu-id="b5a09-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="b5a09-123">قم بفتح ملف معلمه Excel وانتقل إلى علامة التبويب **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="b5a09-124">للتحقق مما إذا كان المخزون الفعلي سيكون دائما أكبر من **0**، انتقل إلى **الخطوة الاجماليه للتحقق من الصحة** المتوفرة وقم بتغيير قيمتها من **411** إلى **0**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="b5a09-125">قم بتغيير قيمه حقل **عامل التشغيل** من علامة يساوي (**=**) إلى علامة أكبر من ( **\>**).</span><span class="sxs-lookup"><span data-stu-id="b5a09-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="b5a09-126">احفظ ملف معلمات Excel وأغلقه.</span><span class="sxs-lookup"><span data-stu-id="b5a09-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="b5a09-127">حدد **تحميل** لحفظ التغييرات التي أجريتها على ملف معلمات Excel إلى Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b5a09-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="b5a09-128">والآن، إذا كانت قيمة حقل **الإجمالي المتوفر** للصنف المحدد في المخزون أكبر من 0 (صفر)، سيتم اجتياز الاختبارات، بغض النظر عن قيمة المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="b5a09-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="b5a09-129">المتغيرات المحفوظة وتسلسل حالات الاختبار</span><span class="sxs-lookup"><span data-stu-id="b5a09-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="b5a09-130">إحدى الميزات الرئيسية لـ RSAT هي تسلسل حالات الاختبار، أي، قدرة الاختبار على تمرير المتغيرات إلى اختبارات أخرى.</span><span class="sxs-lookup"><span data-stu-id="b5a09-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="b5a09-131">لمزيد من المعلومات، راجع المقال [نسخ المتغيرات إلى تسلسل حالات الاختبار](rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="b5a09-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="b5a09-132">حالة الاختبار المشتقة</span><span class="sxs-lookup"><span data-stu-id="b5a09-132">Derived test case</span></span>

<span data-ttu-id="b5a09-133">يتيح لك RSAT استخدام تسجيل المهام نفسه مع حالات اختبار متعددة، مما يمكّن تشغيل مهمة باستخدام تكوينات مختلفة للبيانات.</span><span class="sxs-lookup"><span data-stu-id="b5a09-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="b5a09-134">راجع المقال [حالات الاختبار المشتقة](rsat-derived-test-cases.md) لمزيد من المعلومات.</span><span class="sxs-lookup"><span data-stu-id="b5a09-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="b5a09-135">التحقق من صحة الإعلامات والرسائل</span><span class="sxs-lookup"><span data-stu-id="b5a09-135">Validate notifications and messages</span></span>

<span data-ttu-id="b5a09-136">يمكن استخدام هذه الميزة للتحقق مما إذا كان الإجراء قد حدث أم لا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="b5a09-137">على سبيل المثال، عند إنشاء أمر إنتاج وتقديره ثم بدء تشغيله، يعرض التطبيق الرسالة "الإنتاج – بدء" لإعلامك بأنه قد تم بدء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![إخطار الإنتاج - بدء](./media/use_rsa_tool_05.png)

<span data-ttu-id="b5a09-139">يمكنك التحقق من صحة هذه الرسالة عن طريق RSAT وذلك بإدخال نص الرسالة في علامة التبويب **MessageValidation** في ملف معلمة Excel للتسجيل المناسب.</span><span class="sxs-lookup"><span data-stu-id="b5a09-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![علامة تبويب التحقق من الرسالة](./media/use_rsa_tool_06.png)

<span data-ttu-id="b5a09-141">بعد تشغيل حالة الاختبار، تتم مقارنة الرسالة الموجودة في ملف معلمة Excel بالرسالة المعروضة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="b5a09-142">في حالة عدم تطابق الرسائل، ستفشل حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="b5a09-143">يمكنك إدخال أكثر من رسالة واحدة في علامة تبويب **MessageValidation** في ملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="b5a09-144">يمكن أن تكون الرسائل أيضا رسائل خطا أو تحذيرات بدلا من الرسائل الإخبارية.</span><span class="sxs-lookup"><span data-stu-id="b5a09-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="b5a09-145">اللقطة</span><span class="sxs-lookup"><span data-stu-id="b5a09-145">Snapshot</span></span>

<span data-ttu-id="b5a09-146">تقوم هذه الميزة بأخذ لقطات شاشة الخطوات التي تم إجراؤها أثناء تسجيل المهام.</span><span class="sxs-lookup"><span data-stu-id="b5a09-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="b5a09-147">وهي مفيدة لأغراض للتدقيق أو التصحيح.</span><span class="sxs-lookup"><span data-stu-id="b5a09-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="b5a09-148">لاستخدام هذه الميزة، افتح ملف **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**، تحت مجلد تثبيت RSAT (على سبيل المثال، **C:\\Program Files (x86)\\Regression Suite Automation Tool**)، وقم بتغيير القيمة للعنصر التالي من **false** إلى **true**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="b5a09-149">عند تشغيل حالة الاختبار، ينشئ RSAT لقطات (صور) للخطوات في مجلد التشغيل لحالات الاختبار في الدليل الفعال.</span><span class="sxs-lookup"><span data-stu-id="b5a09-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="b5a09-150">إذا كنت تستخدم إصدارًا أقدم من RSAT، فسيتم حفظ الصور في **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**، ويتم إنشاء مجلد منفصل لكل حالة اختبار قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="b5a09-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="b5a09-151">تعيين</span><span class="sxs-lookup"><span data-stu-id="b5a09-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="b5a09-152">سيناريو</span><span class="sxs-lookup"><span data-stu-id="b5a09-152">Scenario</span></span>

1. <span data-ttu-id="b5a09-153">يقوم مصمم المنتج بإنشاء منتج جديد تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="b5a09-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="b5a09-154">تقوم إدارة الإنتاج بتهيئة أمر إنتاج لجعل مستوى المخزون من جزئين.</span><span class="sxs-lookup"><span data-stu-id="b5a09-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="b5a09-155">ويبدأ التصنيع أمر الإنتاج وينهيه، ويتحقق من أن الكمية الفعلية من جزئين.</span><span class="sxs-lookup"><span data-stu-id="b5a09-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="b5a09-156">يتلقى فريق المبيعات طلبا بأربعة أجزاء من المنتج الجديد.</span><span class="sxs-lookup"><span data-stu-id="b5a09-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="b5a09-157">بالتالي، يقوم فريق المبيعات بتحديث صافي المتطلبات عبر الخطة الديناميكية.</span><span class="sxs-lookup"><span data-stu-id="b5a09-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="b5a09-158">وبسبب عدم توفر سعة إضافية، يتم تعيين سياسة الترتيب الافتراضي إلى "الشراء بدلا من الصنع".</span><span class="sxs-lookup"><span data-stu-id="b5a09-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="b5a09-159">بالتالي، يتم إنشاء أمر شراء مخطط</span><span class="sxs-lookup"><span data-stu-id="b5a09-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="b5a09-160">يقوم المشتري بإضافة مورد، ويؤكد أمر الشراء المخطط، ثم يقوم بتأكيد أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b5a09-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="b5a09-161">عند وصول البضائع التي تم شراؤها إلى المتجر، يقوم مشغل المتجر بالبحث في أمر الشراء المرتبط ويستلم البضائع.</span><span class="sxs-lookup"><span data-stu-id="b5a09-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="b5a09-162">نظرا لأن الأمر مكتمل الآن، فيمكن انتقاء البضائع وتعبئتها مقابل أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="b5a09-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="b5a09-163">ينشر تطبيق المالية فاتورة الشراء وفاتورة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b5a09-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="b5a09-164">يعرض الرسم التوضيحي التالي سير العمل لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="b5a09-164">The following illustration shows the flow for this scenario.</span></span>

![سير عمل السيناريو التوضيحي](./media/use_rsa_tool_14.png)

<span data-ttu-id="b5a09-166">يبين الرسم التوضيحي التالي التسلسل الهرمي للعمليات التجارية لهذا السيناريو في أداة تكوين عمليات الأعمال في LCS.</span><span class="sxs-lookup"><span data-stu-id="b5a09-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![العمليات التجارية للسيناريو التوضيحي](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="b5a09-168">الاستراتيجية – التعليم الأساسي</span><span class="sxs-lookup"><span data-stu-id="b5a09-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="b5a09-169">البيانات</span><span class="sxs-lookup"><span data-stu-id="b5a09-169">Data</span></span>

- <span data-ttu-id="b5a09-170">تأكد أن لديك وحدات تخزين بيانات تمثيلية (نسخة من بيانات الإنتاج/التكوين الذهبي بالإضافة إلى بيانات تم ترحيلها).</span><span class="sxs-lookup"><span data-stu-id="b5a09-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="b5a09-171">عند إنشاء البيانات الجديدة عبر مسجل المهام، قم بإنشاء أسماء الاختبارات التي لا تتعارض مع الأسماء الموجودة (على سبيل المثال، استخدم بادئة مثل **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="b5a09-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="b5a09-172">استخدم استعادة النقطة الزمنية في Azure لإعادة تشغيل الاختبارات في بيئات ليست من المستوي 1.</span><span class="sxs-lookup"><span data-stu-id="b5a09-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="b5a09-173">على الرغم من أنه يمكنك استخدام دالتي Excel **RANDOM** و **NOW** لإنشاء مجموعة فريدة، فإن الجهد يكون مرتفعا بشكل كبير.</span><span class="sxs-lookup"><span data-stu-id="b5a09-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="b5a09-174">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="b5a09-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="b5a09-175">مسجل المهام</span><span class="sxs-lookup"><span data-stu-id="b5a09-175">Task recorder</span></span>

- <span data-ttu-id="b5a09-176">حدد السيناريوهات قبل بدء التسجيل.</span><span class="sxs-lookup"><span data-stu-id="b5a09-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="b5a09-177">يحتوي المشروع جيد الإدارة على سيناريوهات اختبار معرفة مسبقا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="b5a09-178">لبناء حالة اختبار، ضع في الاعتبار مدي توقع نتيجة سيناريوهات الاختبار هذه.</span><span class="sxs-lookup"><span data-stu-id="b5a09-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="b5a09-179">قسم التسجيلات في حالة تنفيذها بواسطة أدوار مختلفة، أو إذا كان هناك وقت انتظار أو حدث خارجي قبل الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="b5a09-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="b5a09-180">تجنب تحديد القيم في القوائم.</span><span class="sxs-lookup"><span data-stu-id="b5a09-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="b5a09-181">بدلا من ذلك، استخدم تنسيقات نصية، مثل **FIFO** و **AudioRM** و **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="b5a09-182">عندم تحدد في القائمة، يتم تسجيل موضع القيمة في القائمة، وليس القيمة نفسها.</span><span class="sxs-lookup"><span data-stu-id="b5a09-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="b5a09-183">إذا تمت إضافة عناصر إلى هذه القائمة، يمكن تغيير وضع القيمة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="b5a09-184">لذلك، سيقوم التسجيل الخاص بك باستخدام معلمة مختلفة، وقد يتأثر باقي السيناريو.</span><span class="sxs-lookup"><span data-stu-id="b5a09-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="b5a09-185">فكر في سلوك المستخدمين المتعددين.</span><span class="sxs-lookup"><span data-stu-id="b5a09-185">Think about multi-user behavior.</span></span> <span data-ttu-id="b5a09-186">على سبيل المثال، لا تفترض أن أمر التوريد الذي تم إنشاؤه حديثا سيتم دوما تحديده تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="b5a09-187">بدلا من ذلك، استخدم عامل التصفية دائما للعثور على الطلب الصحيح.</span><span class="sxs-lookup"><span data-stu-id="b5a09-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="b5a09-188">استخدم وظيفة النسخ في مسجل المهام لحفظ اسم منتج تم إنشاؤه حديثا بحيث يمكن استخدامه في حالات الاختبار المتسلسلة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="b5a09-189">استخدم وظيفة التحقق من الصحة في مسجل المهام لتعيين نقاط التحقق التي تتحقق من أن الخطوات تم تشغيلها بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="b5a09-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="b5a09-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="b5a09-190">RSAT</span></span>

- <span data-ttu-id="b5a09-191">لتشغيل الاختبار في شركة أخرى، يمكنك تغيير الشركة في علامة التبويب **عام** بملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b5a09-192">تأكد من توفر الإعدادات والبيانات في الشركة المحددة حديثا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="b5a09-193">يمكنك تغيير مستخدم الاختبار في علامة التبويب **عام** بملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b5a09-194">حدد معرف البريد الإلكتروني الخاص بالمستخدم الذي سيقوم بتشغيل حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="b5a09-195">بهذه الطريقة، يمكن تشغيل حالة الاختبار باستخدام أذونات الأمان الخاصة بالمستخدم المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5a09-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="b5a09-196">للانتظار قبل بدء الاختبار، يمكنك تعريف توقف مؤقت في علامة التبويب **عام** بملف معلمة Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b5a09-197">يمكن استخدام الإيقاف المؤقت هذا في وظيفة دفعية (على سبيل المثال، إذا كان من الضروري تشغيل سير عمل قبل إجراء الخطوة التالية.)</span><span class="sxs-lookup"><span data-stu-id="b5a09-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="b5a09-198">البرمجة المتقدمة</span><span class="sxs-lookup"><span data-stu-id="b5a09-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="b5a09-199">CLI</span><span class="sxs-lookup"><span data-stu-id="b5a09-199">CLI</span></span>

<span data-ttu-id="b5a09-200">يمكن استدعاء RSAT من نافذة **موجه الأوامر** أو **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="b5a09-201">تحقق من تعيين متغير البيئة **TestRoot** على مسار تثبيت RSAT.</span><span class="sxs-lookup"><span data-stu-id="b5a09-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="b5a09-202">(في Microsoft Windows، افتح **لوحة التحكم**، وحدد **النظام والأمان \> النظام \> إعدادات الأمان المتقدمة**، ثم حدد **متغيرات البيئة**.)</span><span class="sxs-lookup"><span data-stu-id="b5a09-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="b5a09-203">افتح نافذة **موجه الأوامر** أو **PowerShell** كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="b5a09-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="b5a09-204">انتقل إلى دليل التثبيت RSAT.</span><span class="sxs-lookup"><span data-stu-id="b5a09-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="b5a09-205">اسرد كافة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="b5a09-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="b5a09-206">؟</span><span class="sxs-lookup"><span data-stu-id="b5a09-206">?</span></span>

<span data-ttu-id="b5a09-207">يظهر تعليمات حول كافة الأوامر المتوفرة والمعلمات الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="b5a09-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="b5a09-208">?: معلمات اختيارية</span><span class="sxs-lookup"><span data-stu-id="b5a09-208">?: Optional parameters</span></span>

<span data-ttu-id="b5a09-209">`command`: حيث ``[command]`` يكون أحد الأوامر المحددة أدناه.</span><span class="sxs-lookup"><span data-stu-id="b5a09-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="b5a09-210">حول</span><span class="sxs-lookup"><span data-stu-id="b5a09-210">about</span></span>

<span data-ttu-id="b5a09-211">يعرض الإصدار الحالي.</span><span class="sxs-lookup"><span data-stu-id="b5a09-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="b5a09-212">cls</span><span class="sxs-lookup"><span data-stu-id="b5a09-212">cls</span></span>

<span data-ttu-id="b5a09-213">يمسح الشاشة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="b5a09-214">تنزيل</span><span class="sxs-lookup"><span data-stu-id="b5a09-214">download</span></span>

<span data-ttu-id="b5a09-215">يقوم بتنزيل مرفقات لحالة الاختبار المحددة إلى دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="b5a09-216">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b5a09-217">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="b5a09-218">تنزيل: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-218">download: required parameters</span></span>

+ <span data-ttu-id="b5a09-219">`test_case_id`: تمثل معرف حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="b5a09-220">`output_dir`: تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b5a09-221">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="b5a09-222">تنزيل: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="b5a09-223">تحرير</span><span class="sxs-lookup"><span data-stu-id="b5a09-223">edit</span></span>

<span data-ttu-id="b5a09-224">يسمح لك بفتح ملف المعلمات في برنامج Excel وتحريره.</span><span class="sxs-lookup"><span data-stu-id="b5a09-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="b5a09-225">edit: المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-225">edit: required parameters</span></span>

+ <span data-ttu-id="b5a09-226">`excel_file`: يجب أن يحتوي على مسار كامل لملف Excel موجود.</span><span class="sxs-lookup"><span data-stu-id="b5a09-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="b5a09-227">edit: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="b5a09-228">إنشاء</span><span class="sxs-lookup"><span data-stu-id="b5a09-228">generate</span></span>

<span data-ttu-id="b5a09-229">يقوم بإنشاء ملفات تنفيذ تجريبي ومعلمات لحالة الاختبار المحددة في دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="b5a09-230">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b5a09-231">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="b5a09-232">generate: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-232">generate: required parameters</span></span>

+ <span data-ttu-id="b5a09-233">`test_case_id`: تمثل معرف حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="b5a09-234">`output_dir`: تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b5a09-235">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="b5a09-236">generate: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="b5a09-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="b5a09-237">generatederived</span></span>

<span data-ttu-id="b5a09-238">يقوم بإنشاء حالة اختبار جديدة، مشتقة من حالة الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="b5a09-239">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b5a09-240">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="b5a09-241">generatederived: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="b5a09-242">`parent_test_case_id`: تمثل معرف حالة الاختبار الأصلية.</span><span class="sxs-lookup"><span data-stu-id="b5a09-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="b5a09-243">`test_plan_id`: تمثل معرف خطة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="b5a09-244">`test_suite_id`: تمثل معرف مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="b5a09-245">generatederived: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="b5a09-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="b5a09-246">generatetestonly</span></span>

<span data-ttu-id="b5a09-247">يقوم بإنشاء ملف تنفيذ تجريبي فقط لحالة الاختبار المحددة في دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="b5a09-248">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b5a09-249">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="b5a09-250">generatetestonly: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="b5a09-251">`test_case_id`: تمثل معرف حالة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="b5a09-252">`output_dir`: تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b5a09-253">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="b5a09-254">generatetestonly: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="b5a09-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="b5a09-255">generatetestsuite</span></span>

<span data-ttu-id="b5a09-256">يقوم بإنشاء كافة حالات الاختبار للمجموعة المحددة في دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="b5a09-257">يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="b5a09-258">استخدم أي قيمة من العمود كمعلمة **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="b5a09-259">generatetestsuite: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="b5a09-260">`test_suite_name`: تمثل اسم مجموعة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="b5a09-261">`output_dir`: تمثل دليل الإخراج.</span><span class="sxs-lookup"><span data-stu-id="b5a09-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="b5a09-262">الدليل يجب أن يكون موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="b5a09-263">generatetestsuite: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="b5a09-264">تعليمات</span><span class="sxs-lookup"><span data-stu-id="b5a09-264">help</span></span>

<span data-ttu-id="b5a09-265">مماثل لـ [?](#section)</span><span class="sxs-lookup"><span data-stu-id="b5a09-265">Identical to the [?](#section)</span></span> <span data-ttu-id="b5a09-266">أمر.</span><span class="sxs-lookup"><span data-stu-id="b5a09-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="b5a09-267">القائمة</span><span class="sxs-lookup"><span data-stu-id="b5a09-267">list</span></span>

<span data-ttu-id="b5a09-268">يسرد كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="b5a09-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="b5a09-269">listtestplans</span></span>

<span data-ttu-id="b5a09-270">يسرد كافة خطط الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="b5a09-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="b5a09-271">listtestsuite</span></span>

<span data-ttu-id="b5a09-272">يسرد حالات الاختبار لمجموعة الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="b5a09-273">يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="b5a09-274">استخدم أي قيمة من العمود الأول كمعلمة **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="b5a09-275">listtestsuite: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="b5a09-276">`suite_name`: اسم المجموعة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="b5a09-277">listtestsuite: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="b5a09-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="b5a09-278">listtestsuitenames</span></span>

<span data-ttu-id="b5a09-279">يسرد كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="b5a09-280">تشغيل</span><span class="sxs-lookup"><span data-stu-id="b5a09-280">playback</span></span>

<span data-ttu-id="b5a09-281">يقوم بتشغيل حالة اختبار باستخدام ملف Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="b5a09-282">playback: المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-282">playback: required parameters</span></span>

+ <span data-ttu-id="b5a09-283">`excel_file`: مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="b5a09-284">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="b5a09-285">playback: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="b5a09-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="b5a09-286">playbackbyid</span></span>

<span data-ttu-id="b5a09-287">يقوم بتشغيل عدة حالات اختبار في الحال.</span><span class="sxs-lookup"><span data-stu-id="b5a09-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="b5a09-288">يمكنك استخدام الأمر ``list`` للحصول على كافة حالات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="b5a09-289">استخدم أي قيمة من العمود الأول كمعلمة **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="b5a09-290">playbackbyid: المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="b5a09-291">`test_case_id1`: معرف حالة اختبار موجودة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="b5a09-292">`test_case_id2`: معرف حالة اختبار موجودة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="b5a09-293">`test_case_idN`: معرف حالة اختبار موجودة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="b5a09-294">playbackbyid: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="b5a09-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="b5a09-295">playbackmany</span></span>

<span data-ttu-id="b5a09-296">يقوم بتشغيل العديد من حالات الاختبار في الحال، باستخدام ملفات Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="b5a09-297">playbackmany: المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="b5a09-298">`excel_file1`: مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="b5a09-299">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-299">File must exist.</span></span>
+ <span data-ttu-id="b5a09-300">`excel_file2`: مسار كامل لملف Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="b5a09-301">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-301">File must exist.</span></span>
+ <span data-ttu-id="b5a09-302">`excel_fileN`: المسار الكامل إلى ملف Excel.</span><span class="sxs-lookup"><span data-stu-id="b5a09-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="b5a09-303">يجب أن يكون الملف موجودًا.</span><span class="sxs-lookup"><span data-stu-id="b5a09-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="b5a09-304">playbackmany: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="b5a09-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="b5a09-305">playbacksuite</span></span>

<span data-ttu-id="b5a09-306">يقوم بتشغيل كافة حالات الاختبار من مجموعة الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="b5a09-307">يمكنك استخدام الأمر ``listtestsuitenames`` للحصول على كافة مجموعات الاختبار المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="b5a09-308">استخدم أي قيمة من العمود الأول كمعلمة **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="b5a09-309">playbacksuite: المعلمات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="b5a09-310">`suite_name`: اسم المجموعة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="b5a09-311">playbacksuite: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="b5a09-312">إنهاء</span><span class="sxs-lookup"><span data-stu-id="b5a09-312">quit</span></span>

<span data-ttu-id="b5a09-313">يغلق التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b5a09-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="b5a09-314">تحميل</span><span class="sxs-lookup"><span data-stu-id="b5a09-314">upload</span></span>

<span data-ttu-id="b5a09-315">يقوم بتحميل كل الملفات التي تنتمي لمجموعة الاختبار المحددة أو حالات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b5a09-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="b5a09-316">upload: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-316">upload: required parameters</span></span>

+ <span data-ttu-id="b5a09-317">`suite_name`: سيتم تحميل كل الملفات التي تنتمي لمجموعة الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="b5a09-318">`testcase_id`: سيتم تحميل كل الملفات التي تنتمي لحالة (حالات) الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="b5a09-319">upload: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="b5a09-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="b5a09-320">uploadrecording</span></span>

<span data-ttu-id="b5a09-321">يقوم بتحميل ملف تسجيل واحد ينتمي لحالات الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="b5a09-322">uploadrecording: المحددات المطلوبة</span><span class="sxs-lookup"><span data-stu-id="b5a09-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="b5a09-323">`testcase_id`: سيتم تحميل ملف تسجيل واحد ينتمي لحالات الاختبار المحددة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="b5a09-324">uploadrecording: أمثله</span><span class="sxs-lookup"><span data-stu-id="b5a09-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="b5a09-325">استخدام</span><span class="sxs-lookup"><span data-stu-id="b5a09-325">usage</span></span>

<span data-ttu-id="b5a09-326">يظهر طريقتين لاستدعاء هذا التطبيق: واحد باستخدام ملف إعداد افتراضي، آخر يوفر ملف إعداد.</span><span class="sxs-lookup"><span data-stu-id="b5a09-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="b5a09-327">أمثلة Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b5a09-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="b5a09-328">تشغيل حالة اختبار في حلقة</span><span class="sxs-lookup"><span data-stu-id="b5a09-328">Run a test case in a loop</span></span>

<span data-ttu-id="b5a09-329">لديك برنامج اختبار نصي يقوم بإنشاء عميل جديد.</span><span class="sxs-lookup"><span data-stu-id="b5a09-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="b5a09-330">بواسطة البرمجة النصية، يمكن تشغيل حالة الاختبار هذه في حلقة عن طريق الترتيب العشوائي للبيانات التالية قبل تشغيل كل تكرار:</span><span class="sxs-lookup"><span data-stu-id="b5a09-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="b5a09-331">معرف العميل</span><span class="sxs-lookup"><span data-stu-id="b5a09-331">Customer ID</span></span>
- <span data-ttu-id="b5a09-332">اسم العميل</span><span class="sxs-lookup"><span data-stu-id="b5a09-332">Customer name</span></span>
- <span data-ttu-id="b5a09-333">عنوان العميل</span><span class="sxs-lookup"><span data-stu-id="b5a09-333">Customer address</span></span>

<span data-ttu-id="b5a09-334">سيكون معرف العميل بالتنسيق *ATCUS\<number\>*، حيث \<number\> عبارة عن قيمة بين **000000001** و **999999999**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="b5a09-335">يستخدم المثال التالي معلمة واحدة **البدء**، لتعريف الرقم الأول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b5a09-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="b5a09-336">يستخدم معلمة ثانية، **nr**، لتحديد عدد العملاء الذين يجب إنشاؤهم.</span><span class="sxs-lookup"><span data-stu-id="b5a09-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="b5a09-337">بالنسبة لكل تكرار، يتم تغيير المعلمات الموجودة في ملف معلمة Excel باستخدام دالة UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="b5a09-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="b5a09-338">بعد ذلك يتم استدعاء سطر أوامر RSAT في دالة RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="b5a09-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="b5a09-339">افتح بيئة البرمجة المتكاملة (ISE) في Microsoft Windows PowerShell في وضع المسؤول، والصق الكود التالي في الإطار الذي يسمى **Untitled1.ps1**.</span><span class="sxs-lookup"><span data-stu-id="b5a09-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="b5a09-340">تشغيل برنامج نصي يعتمد على البيانات في Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b5a09-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="b5a09-341">يستخدم المثال التالي استدعاء بروتوكول البيانات المفتوحة (OData) للعثور على حالة الأمر لأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="b5a09-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="b5a09-342">إذا لم تتم **فوترة** الحالة، يمكنك، على سبيل المثال، استدعاء حالة اختبار RSAT التي ترحّل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="b5a09-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
