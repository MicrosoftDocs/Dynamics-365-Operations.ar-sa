---
title: إنشاء التكوينات المستندة إلى أبعاد
description: يوضح هذا الإجراء كيفية تعريف تكوين لمنتج يستند إلى البعد.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920671"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="32944-103">إنشاء التكوينات المستندة إلى أبعاد</span><span class="sxs-lookup"><span data-stu-id="32944-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32944-104">يوضح هذا الإجراء كيفية تعريف تكوين لمنتج يستند إلى البعد.</span><span class="sxs-lookup"><span data-stu-id="32944-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="32944-105">وهذا هو الإجراء الأخير في السلسلة التي توضح كيفية إنشاء مجموعات للتكوين المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="32944-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="32944-106">ويعتمد تنفيذ هذا الإجراء على البيانات التي تم إنشاؤها في التسجيلات السبعة السابقة.</span><span class="sxs-lookup"><span data-stu-id="32944-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="32944-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="32944-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="32944-108">إيجاد أصل منتج يستند إلى البعد</span><span class="sxs-lookup"><span data-stu-id="32944-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="32944-109">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="32944-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="32944-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32944-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="32944-111">حدد أصل المنتج المستند إلى البعد الذي قمت بإنشائه في التسجيل الأول في هذه السلسلة من التسجيلات الثمانية.</span><span class="sxs-lookup"><span data-stu-id="32944-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="32944-112">إنشاء التكوينات</span><span class="sxs-lookup"><span data-stu-id="32944-112">Create configurations</span></span>

1. <span data-ttu-id="32944-113">في جزء الإجراءات **الهندسية**، حدد **الحفاظ على التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="32944-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="32944-114">حدد **تكوين**.</span><span class="sxs-lookup"><span data-stu-id="32944-114">Select **Configure**.</span></span>
1. <span data-ttu-id="32944-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32944-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="32944-116">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32944-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="32944-117">حدد أي من الأصناف في مجموعة التكوين الأولى.</span><span class="sxs-lookup"><span data-stu-id="32944-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="32944-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="32944-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="32944-119">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="32944-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="32944-120">حدد أي صنف من مجموعة التكوين الثاني.</span><span class="sxs-lookup"><span data-stu-id="32944-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="32944-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="32944-121">Select **OK**.</span></span>
1. <span data-ttu-id="32944-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="32944-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="32944-123">في حقل **التكوين**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="32944-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="32944-124">أدخل اسم تكوين الذي سيجعل تحديد التكوين أمرًا سهلاً.</span><span class="sxs-lookup"><span data-stu-id="32944-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="32944-125">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="32944-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="32944-126">أدخل وصف التكوين لشرح محتواه.</span><span class="sxs-lookup"><span data-stu-id="32944-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="32944-127">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="32944-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]