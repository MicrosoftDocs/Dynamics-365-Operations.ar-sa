---
title: التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 4 - تشغيل التقرير)
description: يوضح هذا الموضوع كيفيه تكوين نموذج التقرير الكتروني (ER) لاستخدام الابعاد المالية كمصدر بيانات لتقارير ER. (جزء 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7cc1a60234ef09b80950cbf0c7f18b0d65709d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565204"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="c932b-104">التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 4 - تشغيل التقرير)</span><span class="sxs-lookup"><span data-stu-id="c932b-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c932b-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c932b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c932b-106">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="c932b-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c932b-107">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3: تصميم التقرير)‬".</span><span class="sxs-lookup"><span data-stu-id="c932b-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="c932b-108">يجب أيضًا تكوين أنواع المستندات الافتراضية في صفحة محددات ‏‫إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c932b-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="c932b-109">يتم أيضًا تعيين أنواع المستندات الافتراضية عند تنزيل واستيراد أي تكوين للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c932b-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="c932b-110">تشغيل تقرير</span><span class="sxs-lookup"><span data-stu-id="c932b-110">Run report</span></span>
1. <span data-ttu-id="c932b-111">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="c932b-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c932b-112">في الشجرة، قم بتوسيع "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="c932b-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c932b-113">في الشجرة، حدد "نموذج الأبعاد المالية\تقرير دفتر يومية دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="c932b-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="c932b-114">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="c932b-114">Click Run.</span></span>
<span data-ttu-id="c932b-115">![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="c932b-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="c932b-116">في الحقل "اسم البُعد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c932b-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="c932b-117">لتحديد كافة الأبعاد في الشركة الحالية، أدخل المعلومات التالية: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="c932b-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="c932b-119">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="c932b-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c932b-120">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="c932b-120">Click Filter.</span></span>
8. <span data-ttu-id="c932b-121">حدد الصف في جدول دفتر يومية دفتر الأستاذ وحقل "رقم دُفعة دفتر اليومية‬".</span><span class="sxs-lookup"><span data-stu-id="c932b-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="c932b-122">في الحقل "المعايير، اكتب ''00057".</span><span class="sxs-lookup"><span data-stu-id="c932b-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="c932b-123">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="c932b-123">Click OK.</span></span>
11. <span data-ttu-id="c932b-124">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="c932b-124">Click OK.</span></span>
<span data-ttu-id="c932b-125">![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="c932b-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="c932b-126">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="c932b-126">Review the generated output.</span></span> <span data-ttu-id="c932b-127">بالنسبة إلى كل حركة من الدُفعة المحددة، يتم تقديم الأبعاد المالية من مجموعة الأبعاد المناظرة.</span><span class="sxs-lookup"><span data-stu-id="c932b-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="c932b-128">شغّل هذا التقرير وجدد أبعادً مختلفة لمعرفة ما إذا كان التقرير لا يعتمد على عدد الأبعاد المحددة أو عدد الأبعاد التي تم تكوينها لهذا المثيل.</span><span class="sxs-lookup"><span data-stu-id="c932b-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![صفحة تكوينات التقارير الإلكترونية](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]