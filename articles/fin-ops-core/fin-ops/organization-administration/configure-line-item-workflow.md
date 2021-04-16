---
title: تكوين مهام سير عمل لعنصر بند
description: يشرح هذا الموضوع كيفية تكوين عنصر سير عمل لعنصر بند.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84da7080542b4cc2ecc487b0a1331482fb69b998
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747895"
---
# <a name="configure-line-item-workflows"></a><span data-ttu-id="6a53b-103">تكوين مهام سير عمل لعنصر بند</span><span class="sxs-lookup"><span data-stu-id="6a53b-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a53b-104">يشرح هذا الموضوع كيفية تكوين عنصر سير عمل لعنصر بند.</span><span class="sxs-lookup"><span data-stu-id="6a53b-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="6a53b-105">لتكوين عنصر سير عمل لعنصر بند في محرر سير العمل، انقر بزر الماوس الأيمن فوق العنصر، وثم انقر فوق **خصائص** لفتح الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="6a53b-106">ثم استخدم الإجراءات التالية لتكوين خصائص عنصر سير عمل لعنصر بند.</span><span class="sxs-lookup"><span data-stu-id="6a53b-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="6a53b-107">تسمية عنصر سير عمل لعنصر بند</span><span class="sxs-lookup"><span data-stu-id="6a53b-107">Name the line-item workflow element</span></span>

<span data-ttu-id="6a53b-108">اتبع الخطوات التالية لإدخال اسم لعنصر سير عمل لعنصر بند.</span><span class="sxs-lookup"><span data-stu-id="6a53b-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="6a53b-109">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6a53b-110">في حقل **الاسم**، أدخل اسمًا فريدًا لعنصر سير عمل لعنصر بند.</span><span class="sxs-lookup"><span data-stu-id="6a53b-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="6a53b-111">تحديد ما إذا كان سير العمل نفسه يُستخدم لمعالجة كافة عناصر البنود</span><span class="sxs-lookup"><span data-stu-id="6a53b-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="6a53b-112">اتبع هذه الخطوات لتحديد ما إذا كان يتم استخدام سير العمل نفسه لمعالجة كافة عناصر البنود في مستند.</span><span class="sxs-lookup"><span data-stu-id="6a53b-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="6a53b-113">في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6a53b-114">إذا كان يجب أن يقوم سير العمل نفسه بمعالجة كافة عناصر البنود في مستند، فانقر فوق **استدعاء سير عمل واحد لكل عناصر البنود‬**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="6a53b-115">ثم حدد سير العمل الذي يجب استخدامه لمعالجة عناصر البنود.</span><span class="sxs-lookup"><span data-stu-id="6a53b-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="6a53b-116">إذا كان يجب أن يقوم سير عمل معين بمعالجة عناصر البنود التي تتوافق مع مجموعة محددة من الشروط، فانقر فوق **استدعاء سير عمل لكل عنصر من عناصر البنود‬**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="6a53b-117">ثم اتبع الخطوات لتحديد مجموعة الشروط:</span><span class="sxs-lookup"><span data-stu-id="6a53b-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="6a53b-118">وانقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-118">Click **Add**.</span></span>
    2. <span data-ttu-id="6a53b-119">حدد الشرط من الجدول.</span><span class="sxs-lookup"><span data-stu-id="6a53b-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="6a53b-120">على علامة التبويب **اسم الشرط**، أدخل اسمًا لمجموعة الشروط التي تقوم بتعريفها.</span><span class="sxs-lookup"><span data-stu-id="6a53b-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="6a53b-121">انقر فوق **إضافة شرط** لإدخال شرط.</span><span class="sxs-lookup"><span data-stu-id="6a53b-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="6a53b-122">أدخل أية شروط إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a53b-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="6a53b-123">للتحقق من تكوين مجموعة الشروط التي قمت بإدخالها بشكل صحيح، انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="6a53b-124">في صفحة **اختبار حالة سير العمل**، في الناحية **التحقق من صحة الشرط**، حدد سجلاً، ثم انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="6a53b-125">سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.</span><span class="sxs-lookup"><span data-stu-id="6a53b-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="6a53b-126">انقر فوق **موافق** أو **إلغاء الأمر** للرجوع إلى الصفحة **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="6a53b-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="6a53b-127">على علامة التبويب **سير العمل**، حدد سير العمل الذي يجب استخدامه لمعالجة عناصر البنود التي تفي بالشروط التي قمت بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="6a53b-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]