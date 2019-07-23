---
title: استخدام مسار نسبي في روابط البيانات لتنسيقات ونماذج ER
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726542"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="39131-103">استخدام مسار نسبي في روابط البيانات لتنسيقات ونماذج ER</span><span class="sxs-lookup"><span data-stu-id="39131-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39131-104">تتيح أداة إعداد التقارير الإلكترونية‬ (ER) للمستخدمين تحديد بنيات التنسيق الإلكتروني ثم توضيح كيفية تعبئة تلك البنيات باستخدام البيانات والخوارزميات الموجودة في Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="39131-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="39131-105">للحصول على مزيد من التفاصيل، راجع [إنشاء تكوينات إعداد التقارير الإلكترونية (ER)](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="39131-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="39131-106">لتحديد تدفق البيانات لاسترداد بيانات Finance and Operations واستخدامها لإنشاء مستند إلكتروني، يجب إجراء ما يلي:</span><span class="sxs-lookup"><span data-stu-id="39131-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="39131-107">ربط مصادر البيانات المكونة بعناصر نموذج البيانات الخاص بالمجال المصمم.</span><span class="sxs-lookup"><span data-stu-id="39131-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="39131-108">قد يكون هيكل النموذج ومصادر البيانات المحددة جزءًا من بنية هرمية معقدة.</span><span class="sxs-lookup"><span data-stu-id="39131-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="39131-109">ولهذا السبب، يمكن أن تكون الروابط النهائية كبيرة جدًا وتحتوي علي العديد من العناصر من أنواع مختلفة (علي سبيل المثال، العلاقات والجداول والأساليب).</span><span class="sxs-lookup"><span data-stu-id="39131-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="39131-110">يمكن أن تصبح الروابط أقل قابلية للقراءة ومعقدة لإجراء المراجعة والفهم، وتحديدًا لغير المالكين.</span><span class="sxs-lookup"><span data-stu-id="39131-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="39131-111">ربط عناصر نموذج البيانات بمكونات التنسيق لتحديد البيانات التي سيتم ملؤها من نموذج البيانات إلى إخراج التنسيق الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="39131-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="39131-112">لتحسين قابلية استخدام مصممي تعيين التقارير الإلكترونية، تم إصدار ميزة المسار النسبي.</span><span class="sxs-lookup"><span data-stu-id="39131-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="39131-113">يتم تشغيل خيار تمثيل المسار النسبي لأي مثيل جديد لـ Finance and Operations افتراضيًا حيث يتم تمكين تجربة تصميم التقارير الإلكترونية (Microsoft Dynamics 365 for Finance and operations و Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="39131-113">By default, the relative path representation option is turned on for any new instance of Finance and Operations where ER design experience is enabled (Microsoft Dynamics 365 for Finance and operations, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="39131-114">تم تطبيق معلمة المسار النسبي بحيث يمكن للمستخدمين الاستمرار في استخدام المسار الكامل عند العمل مع هذا العرض التقديمي لروابط التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="39131-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="39131-115">[![معلمات المستخدم](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="39131-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="39131-116">عند تشغيل معلمة استخدام المسار النسبي، يقوم حرف @ مفرد باستبدال المسار بالعنصر الأصل في ربط عنصر النموذج الحالي.</span><span class="sxs-lookup"><span data-stu-id="39131-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="39131-117">ويصبح مسار الربط بأكمله أقصر، مما يجعل التعيين بأكمله أكثر وضوحًا ويسهل فهمه.</span><span class="sxs-lookup"><span data-stu-id="39131-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="39131-118">وفي أغلب الحالات، لا تكون هناك حاجة إلى تمرير إضافي في مصمم التقارير الإلكترونية لعرض كل ارتباطات نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="39131-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="39131-119">[![‬‏‫مصمم تعيين النموذج‬‏‫](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="39131-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="39131-120">عند بدء تصميم تعبير جديد للتقرير الإلكتروني، يجب إدخال حرف واحد فقط لتعريف الربط بحقل من العنصر الأصل.</span><span class="sxs-lookup"><span data-stu-id="39131-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="39131-121">[![مصمم التركيبة](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="39131-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="39131-122">عندما تقرر تغيير مصدر البيانات لصنف النموذج الرئيسي، يجب إعادة ربط عنصر النموذج هذا يدويًا باستخدام المسار المطلق، بالإضافة إلى كل العناصر المتداخلة، بمصدر بيانات جديد.</span><span class="sxs-lookup"><span data-stu-id="39131-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="39131-123">عند تشغيل استخدام المسار النسبي، وتحديد مصدر بيانات جديد لربطه بعنصر أصلي، سيُعرض عليك خيار لإعادة ربط كل العناصر المتداخلة لهذا العنصر الرئيسي بنقرة واحدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="39131-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="39131-124">[![استبدال رسالة المسار الموجودة](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="39131-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="39131-125">في حالة تأكيد إعادة ربط العناصر المتداخلة، سيتم وضع العنصر الأصل الجديد بمسار كل عنصر متداخل يحتوي علي العنصر الأصلي الموجود.</span><span class="sxs-lookup"><span data-stu-id="39131-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="39131-126">لا تقوم هذه الميزة بفصل التوافق مع الإصدارات السابقة لإطار عمل التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="39131-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="39131-127">ستعمل كل تكوينات التقارير الإلكترونية التي تم تصميمها مسبقًا مع هذه الميزة الجديدة، ولا يتطلب الأمر أي ترقيات أو تحويلات.</span><span class="sxs-lookup"><span data-stu-id="39131-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="39131-128">يتم حفظ كل التغييرات التي يتم تقديمها بواسطة التعديل الشامل لروابط العناصر المتداخلة في تعيينات النموذج بشكل صحيح في دلتا التكوين (تتبع التغييرات).</span><span class="sxs-lookup"><span data-stu-id="39131-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="39131-129">ويسمح هذا للعملاء بتغيير العنوان الأساسي للإصدار المشتق من تعيينات النموذج إلى أي إصدار أساسي جديد منه تم تعديله باستخدام هذه الميزة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="39131-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>
