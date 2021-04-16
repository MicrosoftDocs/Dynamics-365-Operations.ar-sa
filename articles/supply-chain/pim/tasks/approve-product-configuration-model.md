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
ms.openlocfilehash: 4767d5dc3944d2595a5b2a74a6d5c7c0ea0c849a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809436"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="2f2c1-103">الموافقة على نموذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="2f2c1-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f2c1-104">يتطلب تشغيل هذا الإجراء توفر نموذج تكوين منتج واحد على الأقل.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="2f2c1-105">يستخدم هذا الإجراء نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="2f2c1-106">لاحظ أن هذا النموذج قد تم اعتماده بالفعل، ولكن الإجراء يوضح لك العملية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="2f2c1-107">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="2f2c1-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="2f2c1-108">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="2f2c1-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="2f2c1-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2f2c1-110">حدد نموذج مكبر الصوت المتطور لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="2f2c1-111">انقر فوق "الإصدارات".</span><span class="sxs-lookup"><span data-stu-id="2f2c1-111">Click Versions.</span></span>
5. <span data-ttu-id="2f2c1-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2f2c1-112">Click New.</span></span>
6. <span data-ttu-id="2f2c1-113">في الحقل "رقم المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="2f2c1-114">تمثل الإشارة إلى منتج إصدار نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="2f2c1-115">ولن تُعرض في هذه القائمة إلا أصول المنتجات ذات تقنية التكوين المستنِد إلى قاعدة.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="2f2c1-116">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="2f2c1-117">حدد الوقت الذي سيتوفر به إصدار نموذج المنتج.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="2f2c1-118">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="2f2c1-119">حدد تاريخ انتهاء تنتهي عنده صلاحية نموذج المنتج هذا، أو حدد "أبدا".</span><span class="sxs-lookup"><span data-stu-id="2f2c1-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="2f2c1-120">انقر فوق "اعتماد" لفتح نموذج مربع حوار الإسقاط.‬</span><span class="sxs-lookup"><span data-stu-id="2f2c1-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="2f2c1-121">في الحقل "تم اعتماده بوساطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="2f2c1-122">حدد الشخص المسؤول عن اعتماد نماذج المنتج للاستخدام في العمليات.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="2f2c1-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2f2c1-123">Click OK.</span></span>
12. <span data-ttu-id="2f2c1-124">في الحقل "أسلوب تحديد السعر‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="2f2c1-125">قم بتنشيط إصدار نموذج المنتج.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-125">Activate the product model version.</span></span> <span data-ttu-id="2f2c1-126">يمكن وجود منتج نشط واحد فقط لنموذج منتج واحد في المرة.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="2f2c1-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]