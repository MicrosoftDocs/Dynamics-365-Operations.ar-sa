---
title: إنشاء التكوينات المستندة إلى أبعاد
description: يوضح هذا الإجراء كيفية تعريف تكوين لمنتج يستند إلى البعد.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9190d6dfd4b3f6cf0634e86845e7de028631bdd4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "328575"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="c861f-103">إنشاء التكوينات المستندة إلى أبعاد</span><span class="sxs-lookup"><span data-stu-id="c861f-103">Create dimension-based configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c861f-104">يوضح هذا الإجراء كيفية تعريف تكوين لمنتج يستند إلى البعد.</span><span class="sxs-lookup"><span data-stu-id="c861f-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="c861f-105">وهذا هو الإجراء الأخير في السلسلة التي توضح كيفية إنشاء مجموعات للتكوين المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="c861f-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="c861f-106">ويعتمد تنفيذ هذا الإجراء على البيانات التي تم إنشاؤها في التسجيلات السبعة السابقة.</span><span class="sxs-lookup"><span data-stu-id="c861f-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="c861f-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="c861f-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="c861f-108">إيجاد أصل منتج يستند إلى البعد</span><span class="sxs-lookup"><span data-stu-id="c861f-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="c861f-109">انقر فوق "صيانة المنتج الذي تم إصداره".</span><span class="sxs-lookup"><span data-stu-id="c861f-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="c861f-110">انقر فوق "المنتجات التي تم إصدارها".</span><span class="sxs-lookup"><span data-stu-id="c861f-110">Click Released products.</span></span>
3. <span data-ttu-id="c861f-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c861f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c861f-112">حدد أصل المنتج المستند إلى البعد الذي قمت بإنشائه في التسجيل الأول في هذه السلسلة من التسجيلات الثمانية.</span><span class="sxs-lookup"><span data-stu-id="c861f-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="c861f-113">إنشاء التكوينات</span><span class="sxs-lookup"><span data-stu-id="c861f-113">Create configurations</span></span>
1. <span data-ttu-id="c861f-114">في جزء "الإجراءات الهندسية"، انقر فوق "الحفاظ على التكوينات".</span><span class="sxs-lookup"><span data-stu-id="c861f-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="c861f-115">انقر فوق "تكوين".</span><span class="sxs-lookup"><span data-stu-id="c861f-115">Click Configure.</span></span>
3. <span data-ttu-id="c861f-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c861f-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c861f-117">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c861f-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c861f-118">حدد أي من الأصناف في مجموعة التكوين الأولى.</span><span class="sxs-lookup"><span data-stu-id="c861f-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="c861f-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c861f-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c861f-120">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c861f-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c861f-121">حدد أي صنف من مجموعة التكوين الثاني.</span><span class="sxs-lookup"><span data-stu-id="c861f-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="c861f-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c861f-122">Click OK.</span></span>
8. <span data-ttu-id="c861f-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c861f-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c861f-124">في حقل "التكوين"، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="c861f-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="c861f-125">أدخل اسم تكوين الذي سيجعل تحديد التكوين أمرًا سهلاً.</span><span class="sxs-lookup"><span data-stu-id="c861f-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="c861f-126">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c861f-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c861f-127">أدخل وصف التكوين لشرح محتواه.</span><span class="sxs-lookup"><span data-stu-id="c861f-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="c861f-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c861f-128">Click OK.</span></span>

