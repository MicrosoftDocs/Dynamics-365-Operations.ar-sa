---
title: محرر المعادلات المتقدم لإعداد التقارير الإلكترونية
description: يوضح هذا الموضوع كيفية استخدام محرر المعادلات المتقدم لتكوين التعبيرات في تعيين نموذج ‏‫إعداد التقارير الإلكترونية (ER) ومكونات التنسيق.
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d9911c858d6832aa70378d37e0fd5cf7d7831b1b
ms.sourcegitcommit: dce8c5d3b2fc4a752d676cf9ba91e0dea2fa80d8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/10/2020
ms.locfileid: "3257051"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="cefd4-103">محرر المعادلات المتقدم ل‏‫إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="cefd4-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cefd4-104">وبالإضافة إلى [محرر صيغ](general-electronic-reporting.md) [إعداد التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)، يمكنك استخدام محرر المعادلات المتقدم لإعداد التقارير الإلكترونية لتحسين تجربة تكوين تعبيرات التقارير الإلكترونية (ER)..</span><span class="sxs-lookup"><span data-stu-id="cefd4-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="cefd4-105">يستند المحرر المتقدم إلى المستعرض ويُشغل بواسطة [محرر موناكو](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="cefd4-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="cefd4-106">يتناول هذا الموضوع توضيح ميزات المحرر المتقدم الاكثر استخدامًا:</span><span class="sxs-lookup"><span data-stu-id="cefd4-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="cefd4-107">إعداد تنسيق الكود تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="cefd4-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="cefd4-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="cefd4-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="cefd4-109">إكمال الكود</span><span class="sxs-lookup"><span data-stu-id="cefd4-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="cefd4-110">تنقل الكود</span><span class="sxs-lookup"><span data-stu-id="cefd4-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="cefd4-111">هيكلة الكود</span><span class="sxs-lookup"><span data-stu-id="cefd4-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="cefd4-112">بحث واستبدال</span><span class="sxs-lookup"><span data-stu-id="cefd4-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="cefd4-113">لصق البيانات</span><span class="sxs-lookup"><span data-stu-id="cefd4-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="cefd4-114">تلوين بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="cefd4-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="cefd4-115"><a name="ActivateAdvEditor">تنشيط محرر المعادلات المتقدم</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="cefd4-116">أكمل الخطوات التالية لبدء استخدام محرر المعادلات المتقدم في مثيل Microsoft Dynamics 365 Finance..</span><span class="sxs-lookup"><span data-stu-id="cefd4-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="cefd4-117">انتقل إلى **إدارة المؤسسة** \> **إعداد التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="cefd4-118">في صفحة  **التكوينات** ، في جزء الإجراءات، في علامة التبويب  **التكوينات** ، في مجموعة  **الإعدادات المتقدمة** ، حدد  **معلمات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="cefd4-119">في مربع الحوار  **معلمات المستخدم** ، في قسم  **تنفيذ التتبع** ، عيِّن المعلمة **تمكين محرر المعادلات المتقدم** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="cefd4-120">[![صفحة تكوينات التقارير الإلكترونية](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="cefd4-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="cefd4-121">لاحظ أن هذه المعلمة خاصة بالمستخدم والشركة.</span><span class="sxs-lookup"><span data-stu-id="cefd4-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="cefd4-122"><a name="Autoformatting">إعداد تنسيق الكود تلقائيًا</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="cefd4-123">عند كتابة تعبير معقد يتكون من عدة صفوف من الاكواد، سيتم إجراء المسافة البادئة للسطر الجديد الذي تم إدخاله تلقائيًا استنادًا إلى المسافة البادئة للصف السابق.</span><span class="sxs-lookup"><span data-stu-id="cefd4-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="cefd4-124">يمكنك تحديد السطور وتغيير المسافات البادئة بكتابة **Tab** أو **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="cefd4-125">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="cefd4-126">يسمح لك إعداد التنسيق تلقائيًا بالاحتفاظ بالتنسيق الجيد للتعبير بالكامل لتسهيل عمليات الصيانة المستقبلية وتبسيط فهم المنطق المكون.</span><span class="sxs-lookup"><span data-stu-id="cefd4-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="cefd4-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="cefd4-128">يوفر المحرر إكمال الكلمة لمساعدتك في كتابة التعبير أسرع وتجنب أخطاء الكتابة.</span><span class="sxs-lookup"><span data-stu-id="cefd4-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="cefd4-129">عند بدء إضافة نص جديد، يقدم المحرر تلقائيًا قائمة بالوظائف المدعومة في وظائف إعداد التقارير الإلكترونية التي تحتوي على الأحرف التي أدخلتها.</span><span class="sxs-lookup"><span data-stu-id="cefd4-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="cefd4-130">ويمكنك أيضًا تشغيل IntelliSense في أي مكان لتعبير مكون بكتابة **Ctrl+Space**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="cefd4-131">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="cefd4-132"><a name="CodeCompletion">إكمال الكود</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="cefd4-133">يوفر المحرر إكمال الكود تلقائيًا بواسطة:</span><span class="sxs-lookup"><span data-stu-id="cefd4-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="cefd4-134">إدراج قوس إغلاق عند إدخال قوس فتح، مع إبقاء المؤشر داخل الأقواس.</span><span class="sxs-lookup"><span data-stu-id="cefd4-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="cefd4-135">إدراج رمز الاقتباس الثاني عند إدخال الأول، مع إبقاء المؤشر داخل علامتي الاقتباس.</span><span class="sxs-lookup"><span data-stu-id="cefd4-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="cefd4-136">إدراج رمز الاقتباس المزدوج الثاني عند إدخال الأول، مع إبقاء المؤشر داخل علامتي الاقتباس.</span><span class="sxs-lookup"><span data-stu-id="cefd4-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="cefd4-137">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="cefd4-138">عند الإشارة إلى القوس المكتوب، يتم تمييز القوس الثاني من هذا الزوج تلقائيًا لإظهار البناء الذي يدعمه.</span><span class="sxs-lookup"><span data-stu-id="cefd4-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="cefd4-139"><a name="CodeNavigation">تنقل الكود</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="cefd4-140">يمكنك تحديد موقع الرموز أو السطور المطلوبة في التعبير بكتابة الأمر **انتقال إلى** باستخدام لوح الأوامر أو قائمة السياق.</span><span class="sxs-lookup"><span data-stu-id="cefd4-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="cefd4-141">على سبيل المثال، للانتقال إلى السطر **8**، اتبع ما يلي:</span><span class="sxs-lookup"><span data-stu-id="cefd4-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="cefd4-142">اضغط على **Ctrl+G**، وأدخل القيمة **8**، ثم اضغط على **Enter**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="cefd4-143">-أو -</span><span class="sxs-lookup"><span data-stu-id="cefd4-143">-or-</span></span>

- <span data-ttu-id="cefd4-144">اضغط على **F1**، واكتب **G**، وحدد **انتقال إلى السطر**، وأدخل القيمة **8**، واضغط على **Enter**.</span><span class="sxs-lookup"><span data-stu-id="cefd4-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="cefd4-145">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="cefd4-146"><a name="CodeStructuring">هيكلة الكود</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="cefd4-147">يتم بناء الكود لبعض الوظائف، مثل [IF](er-functions-logical-if.md) أو [CASE](er-functions-logical-case.md) تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="cefd4-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="cefd4-148">يمكنك توسيع وطي أيًا من مناطق الطي لهذا الكود او كلها لتقليل الجزء القابل للتحرير من التعبير للتركيز فقط على جزء الكود الذي يتطلب انتباهك.</span><span class="sxs-lookup"><span data-stu-id="cefd4-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="cefd4-149">يمكن استخدام أوامر تبديل الطي/التوسيع لذلك.</span><span class="sxs-lookup"><span data-stu-id="cefd4-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="cefd4-150">على سبيل المثال، لطي كل المناطق، اتبع ما يلي:</span><span class="sxs-lookup"><span data-stu-id="cefd4-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="cefd4-151">اضغط على **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="cefd4-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="cefd4-152">-أو -</span><span class="sxs-lookup"><span data-stu-id="cefd4-152">-or-</span></span>

- <span data-ttu-id="cefd4-153">اضغط على **F1**، واضغط على **FO**، وحدد **Fold all**، ثم اضغط على **Enter**</span><span class="sxs-lookup"><span data-stu-id="cefd4-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="cefd4-154">لتوسيع كل المناطق، اتبع ما يلي:</span><span class="sxs-lookup"><span data-stu-id="cefd4-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="cefd4-155">اضغط على **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="cefd4-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="cefd4-156">-أو -</span><span class="sxs-lookup"><span data-stu-id="cefd4-156">-or-</span></span>
  
- <span data-ttu-id="cefd4-157">اضغط على **F1**، واكتب **UN**، وحدد **Unfold all**، ثم اضغط على **Enter**</span><span class="sxs-lookup"><span data-stu-id="cefd4-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="cefd4-158">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="cefd4-159"><a name="FindAndReplace">بحث واستبدال</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="cefd4-160">للبحث عن تكرارات نص معين، حدد النص في التعبير، ونفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="cefd4-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="cefd4-161">اضغط على **Ctrl+F** ثم اضغط **F3** للبحث عن التواجد التالي للنص المحدد، أو اضغط **Shift+F3** للبحث عن التواجد السابق.</span><span class="sxs-lookup"><span data-stu-id="cefd4-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="cefd4-162">-أو -</span><span class="sxs-lookup"><span data-stu-id="cefd4-162">-or-</span></span>
  
- <span data-ttu-id="cefd4-163">اضغط **F1**، واكتب **F**، ثم حدد الخيار المطلوب للبحث عن النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="cefd4-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="cefd4-164">لاستبدال تكرارات نص معين، حدد النص في التعبير، ونفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="cefd4-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="cefd4-165">اضغط على **Ctrl+H**</span><span class="sxs-lookup"><span data-stu-id="cefd4-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="cefd4-166">ادخل النص البديل وحدد الخيار استبدال لاستبدال النص المحدد أو كافة تكرارات هذا النص في التعبير الحالي.</span><span class="sxs-lookup"><span data-stu-id="cefd4-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="cefd4-167">-أو -</span><span class="sxs-lookup"><span data-stu-id="cefd4-167">-or-</span></span>
  
- <span data-ttu-id="cefd4-168">اضغط **F1**، واكتب **R**، ثم حدد الخيار المطلوب لاستبدال النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="cefd4-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="cefd4-169">ادخل النص البديل وحدد الخيار استبدال لاستبدال النص المحدد أو كافة تكرارات هذا النص في التعبير الحالي.</span><span class="sxs-lookup"><span data-stu-id="cefd4-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="cefd4-170">لتغيير تكرارات نص معين، حدد النص في التعبير، ونفذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="cefd4-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="cefd4-171">اضغط على **Ctrl+F2**، ثم أدخل النص البديل.</span><span class="sxs-lookup"><span data-stu-id="cefd4-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="cefd4-172">-أو -</span><span class="sxs-lookup"><span data-stu-id="cefd4-172">-or-</span></span>
  
- <span data-ttu-id="cefd4-173">اضغط **F1**، واكتب **C**، ثم حدد الخيار المطلوب لتغيير النص المحدد.</span><span class="sxs-lookup"><span data-stu-id="cefd4-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="cefd4-174">أدخل النص البديل.</span><span class="sxs-lookup"><span data-stu-id="cefd4-174">Enter the alternative text.</span></span>

<span data-ttu-id="cefd4-175">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="cefd4-176"><a name="DataPasting">مصادر البيانات ولصق الوظائف</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="cefd4-177">يمكنك تحديد **إضافة مصدر بيانات**، الذي يلصق بالتعبير الحالي مصدر البيانات المحدد حاليًا على لوحة **مصدر البيانات** اليمنى.</span><span class="sxs-lookup"><span data-stu-id="cefd4-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="cefd4-178">وبالمثل، يمكنك تحديد **إضافة وظيفة**، الذي يلصق بالتعبير الحالي مصدر البيانات المحدد حاليًا على لوحة **الوظائف** اليسرى.</span><span class="sxs-lookup"><span data-stu-id="cefd4-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="cefd4-179">عند استخدام محرر معادلات إعداد التقارير الإلكترونية، دائمًا ما يتم لصق الوظيفة المحددة أو مصدر البيانات المحدد إلى نهاية التعبير المكون.</span><span class="sxs-lookup"><span data-stu-id="cefd4-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="cefd4-180">عند استخدام ‏‫محرر المعادلات المتقدم ل‏‫إعداد التقارير الإلكترونية، يمكن لصق الوظيفة المحددة أو مصدر البيانات المحدد في أي جزء بالتعبير المكون.</span><span class="sxs-lookup"><span data-stu-id="cefd4-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="cefd4-181">ستحتاج إلى استخدام المؤشر لتحديد المكان الذي تريد لصق البيانات فيه.</span><span class="sxs-lookup"><span data-stu-id="cefd4-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="cefd4-182">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="cefd4-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="cefd4-183"><a name="SyntaxColorization">تلوين بناء الجملة</a></span><span class="sxs-lookup"><span data-stu-id="cefd4-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="cefd4-184">يتم حاليًا استخدام ألوان مختلفة لتمييز الأجزاء التالية من التعبيرات:</span><span class="sxs-lookup"><span data-stu-id="cefd4-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="cefd4-185">النص الموجود داخل الأقواس المزدوجة والذي يمكن أن يمثل معرف تسمية ثابت نصي.</span><span class="sxs-lookup"><span data-stu-id="cefd4-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="cefd4-186">[![محرر معادلات إعداد التقارير الإلكترونية](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="cefd4-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="cefd4-187">قيود</span><span class="sxs-lookup"><span data-stu-id="cefd4-187">Limitations</span></span>

<span data-ttu-id="cefd4-188">المحرر معتمد حاليًا في مستعرضات الويب التالية:</span><span class="sxs-lookup"><span data-stu-id="cefd4-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="cefd4-189">Chrome</span><span class="sxs-lookup"><span data-stu-id="cefd4-189">Chrome</span></span>
- <span data-ttu-id="cefd4-190">Edge</span><span class="sxs-lookup"><span data-stu-id="cefd4-190">Edge</span></span>
- <span data-ttu-id="cefd4-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="cefd4-191">Firefox</span></span>
- <span data-ttu-id="cefd4-192">Opera</span><span class="sxs-lookup"><span data-stu-id="cefd4-192">Opera</span></span>
- <span data-ttu-id="cefd4-193">Safari</span><span class="sxs-lookup"><span data-stu-id="cefd4-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cefd4-194">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cefd4-194">Additional resources</span></span>

- [<span data-ttu-id="cefd4-195">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="cefd4-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cefd4-196">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="cefd4-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="cefd4-197">محرر موناكو</span><span class="sxs-lookup"><span data-stu-id="cefd4-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
