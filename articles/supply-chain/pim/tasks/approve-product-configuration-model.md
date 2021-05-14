---
title: الموافقة على نموذج تكوين المنتج
description: يتطلب تشغيل هذا الإجراء توفر نموذج تكوين منتج واحد على الأقل.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920497"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="0f15d-103">الموافقة على نموذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="0f15d-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f15d-104">يتطلب تشغيل هذا الإجراء توفر نموذج تكوين منتج واحد على الأقل.</span><span class="sxs-lookup"><span data-stu-id="0f15d-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="0f15d-105">يستخدم هذا الإجراء نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="0f15d-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="0f15d-106">لاحظ أن هذا النموذج قد تم اعتماده بالفعل، ولكن الإجراء يوضح لك العملية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="0f15d-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="0f15d-107">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="0f15d-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="0f15d-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0f15d-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0f15d-109">حدد نموذج مكبر الصوت المتطور لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0f15d-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="0f15d-110">حدد **الإصدارات**.</span><span class="sxs-lookup"><span data-stu-id="0f15d-110">Select **Versions**.</span></span>
1. <span data-ttu-id="0f15d-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0f15d-111">Select **New**.</span></span>
1. <span data-ttu-id="0f15d-112">في حقل **رقم المنتج**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0f15d-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0f15d-113">تمثل الإشارة إلى منتج إصدار نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="0f15d-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="0f15d-114">ولن تُعرض في هذه القائمة إلا أصول المنتجات ذات تقنية التكوين المستنِد إلى قاعدة.</span><span class="sxs-lookup"><span data-stu-id="0f15d-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="0f15d-115">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0f15d-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="0f15d-116">حدد الوقت الذي سيتوفر به إصدار نموذج المنتج.</span><span class="sxs-lookup"><span data-stu-id="0f15d-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="0f15d-117">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0f15d-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="0f15d-118">حدد تاريخ انتهاء تنتهي عنده صلاحية نموذج المنتج هذا، أو حدد "أبدا".</span><span class="sxs-lookup"><span data-stu-id="0f15d-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="0f15d-119">حدد **موافقة** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="0f15d-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="0f15d-120">في حقل **تمت الموافقة بواسطة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0f15d-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="0f15d-121">حدد الشخص المسؤول عن اعتماد نماذج المنتج للاستخدام في العمليات.</span><span class="sxs-lookup"><span data-stu-id="0f15d-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="0f15d-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0f15d-122">Select **OK**.</span></span>
1. <span data-ttu-id="0f15d-123">في حقل **أسلوب تحديد السعر‬**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="0f15d-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="0f15d-124">قم بتنشيط إصدار نموذج المنتج.</span><span class="sxs-lookup"><span data-stu-id="0f15d-124">Activate the product model version.</span></span> <span data-ttu-id="0f15d-125">يمكن وجود منتج نشط واحد فقط لنموذج منتج واحد في المرة.</span><span class="sxs-lookup"><span data-stu-id="0f15d-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="0f15d-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0f15d-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]