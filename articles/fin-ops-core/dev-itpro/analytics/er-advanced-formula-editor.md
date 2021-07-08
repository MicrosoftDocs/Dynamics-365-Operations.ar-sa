---
title: محرر المعادلات المتقدم لإعداد التقارير الإلكترونية
description: يوضح هذا الموضوع كيفية استخدام محرر المعادلات المتقدم لتكوين التعبيرات في تعيين نموذج ‏‫إعداد التقارير الإلكترونية (ER) ومكونات التنسيق.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270697"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="b178b-103">محرر المعادلات المتقدم ل‏‫إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b178b-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b178b-104">وبالإضافة إلى [محرر صيغ](general-electronic-reporting.md) [إعداد التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)، يمكنك استخدام محرر المعادلات المتقدم لإعداد التقارير الإلكترونية لتحسين تجربة تكوين تعبيرات التقارير الإلكترونية (ER)..</span><span class="sxs-lookup"><span data-stu-id="b178b-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="b178b-105">يستند المحرر المتقدم إلى المستعرض ويُشغل بواسطة [محرر موناكو](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="b178b-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="b178b-106">يتناول هذا الموضوع توضيح ميزات المحرر المتقدم الاكثر استخدامًا:</span><span class="sxs-lookup"><span data-stu-id="b178b-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="b178b-107">إعداد تنسيق الكود تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="b178b-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="b178b-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="b178b-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="b178b-109">إكمال الكود</span><span class="sxs-lookup"><span data-stu-id="b178b-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="b178b-110">تنقل الكود</span><span class="sxs-lookup"><span data-stu-id="b178b-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="b178b-111">هيكلة الكود</span><span class="sxs-lookup"><span data-stu-id="b178b-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="b178b-112">بحث واستبدال</span><span class="sxs-lookup"><span data-stu-id="b178b-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="b178b-113">لصق البيانات</span><span class="sxs-lookup"><span data-stu-id="b178b-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="b178b-114">تلوين بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="b178b-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="b178b-115"><a name="ActivateAdvEditor">تنشيط محرر المعادلات المتقدم</a></span><span class="sxs-lookup"><span data-stu-id="b178b-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="b178b-116">أكمل الخطوات التالية لبدء استخدام محرر المعادلات المتقدم في مثيل Microsoft Dynamics 365 Finance..</span><span class="sxs-lookup"><span data-stu-id="b178b-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="b178b-117">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="b178b-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="b178b-118">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="b178b-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="b178b-119">في مربع الحوار **معلمات المستخدم**، في قسم **تتبع التنفيذ**، قم بتعيين **تمكين محرر المعادلات المتقدم** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b178b-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="b178b-120">[![مربع حوار معلمات المستخدم، تمكين معلمة محرر الصيغ المتقدمة المميزة](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="b178b-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b178b-121">لاحظ أن هذه المعلمة خاصة بالمستخدم والشركة.</span><span class="sxs-lookup"><span data-stu-id="b178b-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="b178b-122">البدء في Microsoft Dynamics 365 Finance الإصدار 10.0.19، يمكنك التحكم فيما يتم تقديمه محرر صيغة التقارير الإلكترونية بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="b178b-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="b178b-123">أكمل الخطوات التالية لتمكين محرر الصيغ المتقدمة لكافة المستخدمين والشركات الخاصة بمثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="b178b-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="b178b-124">افتح مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="b178b-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="b178b-125">ابحث وحدد الميزة وتحديدها **تعيين محرر الصيغة المتقدمة للتقارير الإلكترونية كالمحرر الافتراضي لكافة المستخدمين** في القائمة، ثم حدد **التمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="b178b-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="b178b-126">انتقل إلى **إدارة المؤسسة** > **إعداد التقارير الإلكترونية** > **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="b178b-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="b178b-127">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="b178b-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="b178b-128">في مربع الحوار **معلمات المستخدم**، قم بالبحث عن المعلمة **تعطيل محرر الصيغة المتقدمة** والتحقق من تعيينها إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="b178b-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="b178b-129">[![مربع حوار معلمات المستخدم، تعطيل معلمة محرر الصيغ المتقدمة المميزة](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="b178b-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b178b-130">تظل قيم المعلمات **تمكين محرر الصيغ المتقدمة** و **تعطيل محرر الصيغ المتقدمة** الصيغ المتقدمة منفصلة لكل مستخدم ويتم تقديمها في مربع حوار **معلمات المستخدم** استنادًا إلى حالة الميزة **تعيين محرر الصيغ المتقدمة للتقارير الإلكترونية كالمحرر الافتراضي لكل المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="b178b-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="b178b-131"><a name="Autoformatting">إعداد تنسيق الكود تلقائيًا</a></span><span class="sxs-lookup"><span data-stu-id="b178b-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="b178b-132">عند كتابة تعبير معقد يتكون من عدة صفوف من الاكواد، سيتم إجراء المسافة البادئة للسطر الجديد الذي تم إدخاله تلقائيًا استنادًا إلى المسافة البادئة للصف السابق.</span><span class="sxs-lookup"><span data-stu-id="b178b-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="b178b-133">يمكنك تحديد السطور وتغيير المسافات البادئة بكتابة **Tab** أو **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="b178b-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="b178b-134">[![محرر صيغة التقارير الإلكترونية بتنسيق gif يظهر تحديد البنود وتغيير المسافة البادئة](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="b178b-135">يسمح لك إعداد التنسيق تلقائيًا بالاحتفاظ بالتنسيق الجيد للتعبير بالكامل لتسهيل عمليات الصيانة المستقبلية وتبسيط فهم المنطق المكون.</span><span class="sxs-lookup"><span data-stu-id="b178b-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="b178b-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="b178b-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="b178b-137">يوفر المحرر إكمال الكلمة لمساعدتك في كتابة التعبير أسرع وتجنب أخطاء الكتابة.</span><span class="sxs-lookup"><span data-stu-id="b178b-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="b178b-138">عند بدء إضافة نص جديد، يقدم المحرر تلقائيًا قائمة بالوظائف المدعومة في وظائف إعداد التقارير الإلكترونية التي تحتوي على الأحرف التي أدخلتها.</span><span class="sxs-lookup"><span data-stu-id="b178b-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="b178b-139">ويمكنك أيضًا تشغيل IntelliSense في أي مكان لتعبير مكون بكتابة **Ctrl+Space**.</span><span class="sxs-lookup"><span data-stu-id="b178b-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="b178b-140">[![محرر صيغة التقارير الإلكترونية بتنسيق gif يظهر تشغيل IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="b178b-141"><a name="CodeCompletion">إكمال الكود</a></span><span class="sxs-lookup"><span data-stu-id="b178b-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="b178b-142">يوفر المحرر إكمال الكود تلقائيًا بواسطة:</span><span class="sxs-lookup"><span data-stu-id="b178b-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="b178b-143">إدراج قوس إغلاق عند إدخال قوس فتح، مع إبقاء المؤشر داخل الأقواس.</span><span class="sxs-lookup"><span data-stu-id="b178b-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="b178b-144">إدراج رمز الاقتباس الثاني عند إدخال الأول، مع إبقاء المؤشر داخل علامتي الاقتباس.</span><span class="sxs-lookup"><span data-stu-id="b178b-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="b178b-145">إدراج رمز الاقتباس المزدوج الثاني عند إدخال الأول، مع إبقاء المؤشر داخل علامتي الاقتباس.</span><span class="sxs-lookup"><span data-stu-id="b178b-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="b178b-146">[![محرر صيغة التقارير الإلكترونية بصيغة gif يعرض المحرر الذي يوفر إكمال التعليمات البرمجية تلقائيًا](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="b178b-147">عند الإشارة إلى القوس المكتوب، يتم تمييز القوس الثاني من هذا الزوج تلقائيًا لإظهار البناء الذي يدعمه.</span><span class="sxs-lookup"><span data-stu-id="b178b-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="b178b-148"><a name="CodeNavigation">تنقل الكود</a></span><span class="sxs-lookup"><span data-stu-id="b178b-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="b178b-149">يمكنك تحديد موقع الرموز أو السطور المطلوبة في التعبير بكتابة الأمر **انتقال إلى** باستخدام لوح الأوامر أو قائمة السياق.</span><span class="sxs-lookup"><span data-stu-id="b178b-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="b178b-150">على سبيل المثال، للانتقال إلى السطر **8**، اتبع ما يلي:</span><span class="sxs-lookup"><span data-stu-id="b178b-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="b178b-151">اضغط على **Ctrl+G**، وأدخل القيمة **8**، ثم اضغط على **Enter**.</span><span class="sxs-lookup"><span data-stu-id="b178b-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="b178b-152">-أو -</span><span class="sxs-lookup"><span data-stu-id="b178b-152">-or-</span></span>

- <span data-ttu-id="b178b-153">اضغط على **F1**، واكتب **G**، وحدد **انتقال إلى السطر**، وأدخل القيمة **8**، واضغط على **Enter**.</span><span class="sxs-lookup"><span data-stu-id="b178b-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="b178b-154">[![محرر صيغة التقارير الإلكترونية بتنسيق gif يظهر كيفية تحديد الأجزاء من التعبير باستخدام لوح الألوان](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="b178b-155"><a name="CodeStructuring">هيكلة الكود</a></span><span class="sxs-lookup"><span data-stu-id="b178b-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="b178b-156">يتم بناء الكود لبعض الوظائف، مثل [IF](er-functions-logical-if.md) أو [CASE](er-functions-logical-case.md) تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b178b-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="b178b-157">يمكنك توسيع وطي أيًا من مناطق الطي لهذا الكود او كلها لتقليل الجزء القابل للتحرير من التعبير للتركيز فقط على جزء الكود الذي يتطلب انتباهك.</span><span class="sxs-lookup"><span data-stu-id="b178b-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="b178b-158">يمكن استخدام أوامر تبديل الطي/التوسيع لذلك.</span><span class="sxs-lookup"><span data-stu-id="b178b-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="b178b-159">على سبيل المثال، لطي كل المناطق، اتبع ما يلي:</span><span class="sxs-lookup"><span data-stu-id="b178b-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="b178b-160">اضغط على **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="b178b-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="b178b-161">-أو -</span><span class="sxs-lookup"><span data-stu-id="b178b-161">-or-</span></span>

- <span data-ttu-id="b178b-162">اضغط على **F1**، واضغط على **FO**، وحدد **Fold all**، ثم اضغط على **Enter**</span><span class="sxs-lookup"><span data-stu-id="b178b-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="b178b-163">لتوسيع كل المناطق، اتبع ما يلي:</span><span class="sxs-lookup"><span data-stu-id="b178b-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="b178b-164">اضغط على **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="b178b-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="b178b-165">-أو -</span><span class="sxs-lookup"><span data-stu-id="b178b-165">-or-</span></span>
  
- <span data-ttu-id="b178b-166">اضغط على **F1**، واكتب **UN**، وحدد **Unfold all**، ثم اضغط على **Enter**</span><span class="sxs-lookup"><span data-stu-id="b178b-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="b178b-167">[![محرر صيغة التقارير الإلكترونية بتنسيق gif يظهر كود موسع](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="b178b-168"><a name="FindAndReplace">بحث واستبدال</a></span><span class="sxs-lookup"><span data-stu-id="b178b-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="b178b-169">للبحث عن تكرارات نص معين، حدد النص في التعبير، ونفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="b178b-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="b178b-170">اضغط على **Ctrl+F** ثم اضغط **F3** للبحث عن التواجد التالي للنص المحدد، أو اضغط **Shift+F3** للبحث عن التواجد السابق.</span><span class="sxs-lookup"><span data-stu-id="b178b-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="b178b-171">-أو -</span><span class="sxs-lookup"><span data-stu-id="b178b-171">-or-</span></span>
  
- <span data-ttu-id="b178b-172">اضغط **F1**، واكتب **F**، ثم حدد الخيار المطلوب للبحث عن النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="b178b-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="b178b-173">لاستبدال تكرارات نص معين، حدد النص في التعبير، ونفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="b178b-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="b178b-174">اضغط على **Ctrl+H**</span><span class="sxs-lookup"><span data-stu-id="b178b-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="b178b-175">ادخل النص البديل وحدد الخيار استبدال لاستبدال النص المحدد أو كافة تكرارات هذا النص في التعبير الحالي.</span><span class="sxs-lookup"><span data-stu-id="b178b-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="b178b-176">-أو -</span><span class="sxs-lookup"><span data-stu-id="b178b-176">-or-</span></span>
  
- <span data-ttu-id="b178b-177">اضغط **F1**، واكتب **R**، ثم حدد الخيار المطلوب لاستبدال النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="b178b-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="b178b-178">ادخل النص البديل وحدد الخيار استبدال لاستبدال النص المحدد أو كافة تكرارات هذا النص في التعبير الحالي.</span><span class="sxs-lookup"><span data-stu-id="b178b-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="b178b-179">لتغيير تكرارات نص معين، حدد النص في التعبير، ونفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="b178b-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="b178b-180">اضغط على **Ctrl+F2**، ثم أدخل النص البديل.</span><span class="sxs-lookup"><span data-stu-id="b178b-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="b178b-181">-أو -</span><span class="sxs-lookup"><span data-stu-id="b178b-181">-or-</span></span>
  
- <span data-ttu-id="b178b-182">اضغط **F1**، واكتب **C**، ثم حدد الخيار المطلوب لتغيير النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="b178b-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="b178b-183">أدخل النص البديل.</span><span class="sxs-lookup"><span data-stu-id="b178b-183">Enter the alternative text.</span></span>

<span data-ttu-id="b178b-184">[![محرر صيغة التقارير الإلكترونية بتنسيق gif يظهر البحث والاستبدال](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="b178b-185"><a name="DataPasting">مصادر البيانات ولصق الوظائف</a></span><span class="sxs-lookup"><span data-stu-id="b178b-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="b178b-186">يمكنك تحديد **إضافة مصدر بيانات**، الذي يلصق بالتعبير الحالي مصدر البيانات المحدد حاليًا على لوحة **مصدر البيانات** اليمنى.</span><span class="sxs-lookup"><span data-stu-id="b178b-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="b178b-187">وبالمثل، يمكنك تحديد **إضافة وظيفة**، الذي يلصق بالتعبير الحالي مصدر البيانات المحدد حاليًا على لوحة **الوظائف** اليسرى.</span><span class="sxs-lookup"><span data-stu-id="b178b-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="b178b-188">عند استخدام محرر معادلات إعداد التقارير الإلكترونية، دائمًا ما يتم لصق الوظيفة المحددة أو مصدر البيانات المحدد إلى نهاية التعبير المكون.</span><span class="sxs-lookup"><span data-stu-id="b178b-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="b178b-189">عند استخدام ‏‫محرر المعادلات المتقدم ل‏‫إعداد التقارير الإلكترونية، يمكن لصق الوظيفة المحددة أو مصدر البيانات المحدد في أي جزء بالتعبير المكون.</span><span class="sxs-lookup"><span data-stu-id="b178b-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="b178b-190">ستحتاج إلى استخدام المؤشر لتحديد المكان الذي تريد لصق البيانات فيه.</span><span class="sxs-lookup"><span data-stu-id="b178b-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="b178b-191">[![محرر صيغة التقارير الإلكترونية بتنسيق gif تظهر إضافة مصدر بيانات وظيفة](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="b178b-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="b178b-192"><a name="SyntaxColorization">تلوين بناء الجملة</a></span><span class="sxs-lookup"><span data-stu-id="b178b-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="b178b-193">يتم حاليًا استخدام ألوان مختلفة لتمييز الأجزاء التالية من التعبيرات:</span><span class="sxs-lookup"><span data-stu-id="b178b-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="b178b-194">النص الموجود داخل الأقواس المزدوجة والذي يمكن أن يمثل معرف تسمية ثابت نصي.</span><span class="sxs-lookup"><span data-stu-id="b178b-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="b178b-195">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="b178b-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="b178b-196">قيود</span><span class="sxs-lookup"><span data-stu-id="b178b-196">Limitations</span></span>

<span data-ttu-id="b178b-197">المحرر معتمد حاليًا في مستعرضات الويب التالية:</span><span class="sxs-lookup"><span data-stu-id="b178b-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="b178b-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="b178b-198">Chrome</span></span>
- <span data-ttu-id="b178b-199">Edge</span><span class="sxs-lookup"><span data-stu-id="b178b-199">Edge</span></span>
- <span data-ttu-id="b178b-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="b178b-200">Firefox</span></span>
- <span data-ttu-id="b178b-201">Opera</span><span class="sxs-lookup"><span data-stu-id="b178b-201">Opera</span></span>
- <span data-ttu-id="b178b-202">Safari</span><span class="sxs-lookup"><span data-stu-id="b178b-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b178b-203">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b178b-203">Additional resources</span></span>

- [<span data-ttu-id="b178b-204">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="b178b-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b178b-205">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b178b-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="b178b-206">محرر موناكو</span><span class="sxs-lookup"><span data-stu-id="b178b-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
