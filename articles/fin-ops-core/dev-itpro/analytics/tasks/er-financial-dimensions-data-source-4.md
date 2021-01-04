---
title: التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 4 - تشغيل التقرير)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684729"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="83df5-103">التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 4 - تشغيل التقرير)</span><span class="sxs-lookup"><span data-stu-id="83df5-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83df5-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="83df5-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="83df5-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="83df5-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="83df5-106">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3: تصميم التقرير)‬".</span><span class="sxs-lookup"><span data-stu-id="83df5-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="83df5-107">يجب أيضًا تكوين أنواع المستندات الافتراضية في صفحة محددات ‏‫إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="83df5-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="83df5-108">يتم أيضًا تعيين أنواع المستندات الافتراضية عند تنزيل واستيراد أي تكوين للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="83df5-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="83df5-109">تشغيل تقرير</span><span class="sxs-lookup"><span data-stu-id="83df5-109">Run report</span></span>
1. <span data-ttu-id="83df5-110">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="83df5-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="83df5-111">في الشجرة، قم بتوسيع "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="83df5-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="83df5-112">في الشجرة، حدد "نموذج الأبعاد المالية\تقرير دفتر يومية دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="83df5-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="83df5-113">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="83df5-113">Click Run.</span></span>
<span data-ttu-id="83df5-114">![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="83df5-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="83df5-115">في الحقل "اسم البُعد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="83df5-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="83df5-116">لتحديد كافة الأبعاد في الشركة الحالية، أدخل المعلومات التالية: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="83df5-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="83df5-118">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="83df5-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="83df5-119">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="83df5-119">Click Filter.</span></span>
8. <span data-ttu-id="83df5-120">حدد الصف في جدول دفتر يومية دفتر الأستاذ وحقل "رقم دُفعة دفتر اليومية‬".</span><span class="sxs-lookup"><span data-stu-id="83df5-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="83df5-121">في الحقل "المعايير، اكتب ''00057".</span><span class="sxs-lookup"><span data-stu-id="83df5-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="83df5-122">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="83df5-122">Click OK.</span></span>
11. <span data-ttu-id="83df5-123">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="83df5-123">Click OK.</span></span>
<span data-ttu-id="83df5-124">![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="83df5-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="83df5-125">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="83df5-125">Review the generated output.</span></span> <span data-ttu-id="83df5-126">بالنسبة إلى كل حركة من الدُفعة المحددة، يتم تقديم الأبعاد المالية من مجموعة الأبعاد المناظرة.</span><span class="sxs-lookup"><span data-stu-id="83df5-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="83df5-127">شغّل هذا التقرير وجدد أبعادً مختلفة لمعرفة ما إذا كان التقرير لا يعتمد على عدد الأبعاد المحددة أو عدد الأبعاد التي تم تكوينها لهذا المثيل.</span><span class="sxs-lookup"><span data-stu-id="83df5-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run4.png)
