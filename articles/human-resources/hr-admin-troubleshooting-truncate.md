---
title: تجنب اقتطاع نص في التدرج الهرمي للمناصب والتصدير إلى Visio
description: يوضح هذا المقال كيفية حل مشكلة تم فيها اقتطاع أسماء الأفراد ومناصبهم عندما قام العملاء بعرض التدرج الهرمي للمنصب في Microsoft Dynamics 365 Human Resources. يُصعب اقتطاع النص أخذ لقطة شاشة أو طباعة التدرج الهرمي.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc723728801909c67cb823a043a2ae3e7eaf9f05
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892193"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="e196c-104">تجنب اقتطاع نص في التدرج الهرمي للمنصب والتصدير إلى Visio</span><span class="sxs-lookup"><span data-stu-id="e196c-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e196c-105">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="e196c-105">**Issue**</span></span>

<span data-ttu-id="e196c-106">عندما يستعرض العميل التدرج الهرمي للمنصب في Microsoft Dynamics 365 Human Resources، يتم اقتطاع أسماء الأفراد ومناصبهم.</span><span class="sxs-lookup"><span data-stu-id="e196c-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="e196c-107">لذلك، فقد يكون من الصعب أخذ لقطة شاشة أو طباعة وتوزيع التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="e196c-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![التدرج الهرمي للمناصب الوظيفية](media/position-h.png)

<span data-ttu-id="e196c-109">**السبب**</span><span class="sxs-lookup"><span data-stu-id="e196c-109">**Cause**</span></span>

<span data-ttu-id="e196c-110">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="e196c-110">This behavior is by design.</span></span>

<span data-ttu-id="e196c-111">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="e196c-111">**Resolution**</span></span>

<span data-ttu-id="e196c-112">لسوء الحظ، لا يمكن للمستخدمين تغيير حجم النص بسهولة.</span><span class="sxs-lookup"><span data-stu-id="e196c-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="e196c-113">ومع ذلك، يمكنك تصدير التدرج الهرمي للمنصب خارج Human Resources ثم استيراده إلى Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="e196c-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="e196c-114">على الرغم من كتابة المقالة التالية لبرنامج Microsoft Dynamics AX 2012، فإن العملية تنطبق مع ذلك على Human Resources: [تصدير التدرج الهرمي للمنصب إلى Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="e196c-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="e196c-115">اتبع هذه الخطوات للتصدير إلى Visio.</span><span class="sxs-lookup"><span data-stu-id="e196c-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="e196c-116">في Human Resources، افتح صفحة قائمة **المناصب** .</span><span class="sxs-lookup"><span data-stu-id="e196c-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="e196c-117">لتضمين المزيد من المعلومات في مخطط بنية المؤسسة، أضف الحقول إلى قائمة **المناصب**، بحيث تكون متاحة عندما تقوم باستخدام المعالج لاحقًا في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e196c-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="e196c-118">في جزء الإجراءات، حدد الزر **فتح في Microsoft Office**، ثم ضمن **تصدير إلى Excel**، حدد **المناصب‏‎**.</span><span class="sxs-lookup"><span data-stu-id="e196c-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="e196c-119">بدلاً من ذلك، اضغط على Ctrl + T.</span><span class="sxs-lookup"><span data-stu-id="e196c-119">Alternatively, press Ctrl+T.</span></span>

    ![تصدير صفحة قائمة المناصب إلى Excel](media/org-admin.png)

3. <span data-ttu-id="e196c-121">حفظ ملف Excel الذي تم تصديره.</span><span class="sxs-lookup"><span data-stu-id="e196c-121">Save the Excel file that is exported.</span></span>

    ![تصدير إلى مربع حوار Excel](media/export-excel.png)

4. <span data-ttu-id="e196c-123">في Visio، حدد **Visio-إنشاء جديد**، ثم حدد فئة قالب **العمل**.</span><span class="sxs-lookup"><span data-stu-id="e196c-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![مخطط جديد](media/new.png)

5. <span data-ttu-id="e196c-125">حدد **مُعالج مخطط مؤسسة**، ثم قم بتحديد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="e196c-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![مربع حوار مُعالج مخطط مؤسسة](media/orgchart-wizard.png)

6. <span data-ttu-id="e196c-127">حدد **المعلومات التي تم تخزينها مسبقًا في ملف أو قاعدة بيانات**، ثم قم بتحديد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![معالج مخطط المؤسسة 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="e196c-129">اختر **نص، Org Plus (\*.txt) أو ملف Excel**، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![معالج مخطط المؤسسة 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="e196c-131">استعرض لتحديد ملف Excel الذي تم تصديره الذي يحتوي على التدرج الهرمي للمناصب ثم قم بتحديد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![معالج مخطط المؤسسة 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="e196c-133">حدد حقل **الاسم** إلى **المنصب**، ثم قم بتعيين حقل **تقارير إلى** إلى  **تقارير إلى المنصب**، ثم قم بتحديد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![معالج مخطط المؤسسة 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="e196c-135">حدد الحقول التي ينبغي إظهارها في كل عقدة، ثم قم بتحديد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![معالج مخطط المؤسسة 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="e196c-137">إضافة عمود **المنصب** إلى قائمة **حقول بيانات الشكل**، ثم قم بتحديد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![معالج مخطط المؤسسة 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="e196c-139">الصور غير متوفرة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="e196c-139">Pictures aren't currently available.</span></span> <span data-ttu-id="e196c-140">لذلك، في الصفحة التالية، حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="e196c-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="e196c-141">حدد **أريد أن يقوم المعالج بتقسيم مخطط المؤسسة الخاص بي تلقائيًا عبر الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="e196c-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![معالج مخطط المؤسسة 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="e196c-143">حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="e196c-143">Select **Finish**.</span></span>

    <span data-ttu-id="e196c-144">إذا كانت هناك أي مناصب غير موجودة في البنية، سوف يُطلب منك تضمينها في المخطط.</span><span class="sxs-lookup"><span data-stu-id="e196c-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="e196c-145">يُظهر المخطط الذي تم إنشاؤه في Visio كل مدير في ورقة عمل منفصلة.</span><span class="sxs-lookup"><span data-stu-id="e196c-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="e196c-146">استنادًا إلى الحقول التي حددتها لتضمينها في المخطط، تُظهر كل عقدة المعلومات المناسبة عندما يتم إنشاء ملف Visio.</span><span class="sxs-lookup"><span data-stu-id="e196c-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![مخطط التدرج الهرمي](media/hierarchy.png)

<span data-ttu-id="e196c-148">**خيار إضافي**</span><span class="sxs-lookup"><span data-stu-id="e196c-148">**Additional option**</span></span>

<span data-ttu-id="e196c-149">في Human Resources، قد تتمكن أيضا من استخدام مساحة عمل **الأشخاص** لعرض بعض المعلومات المتعلقة بالتدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="e196c-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]