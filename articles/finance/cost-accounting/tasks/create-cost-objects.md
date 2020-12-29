---
title: 'إنشاء كائنات تكلفة  '
description: يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440083"
---
# <a name="create-cost-objects"></a><span data-ttu-id="bff3d-103">إنشاء كائنات تكلفة  </span><span class="sxs-lookup"><span data-stu-id="bff3d-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bff3d-104">يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات.</span><span class="sxs-lookup"><span data-stu-id="bff3d-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="bff3d-105">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="bff3d-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="bff3d-106">إنشاء كائنات تكلفة جديدة</span><span class="sxs-lookup"><span data-stu-id="bff3d-106">Create new cost objects</span></span>
1. <span data-ttu-id="bff3d-107">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="bff3d-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="bff3d-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bff3d-108">Click New.</span></span>
3. <span data-ttu-id="bff3d-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bff3d-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bff3d-110">في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="bff3d-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="bff3d-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bff3d-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="bff3d-112">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bff3d-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="bff3d-113">تكوين موصل البيانات</span><span class="sxs-lookup"><span data-stu-id="bff3d-113">Configure the data connector</span></span>
1. <span data-ttu-id="bff3d-114">انقر فوق "تكوين موفر عضو البُعد".</span><span class="sxs-lookup"><span data-stu-id="bff3d-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="bff3d-115">حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="bff3d-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="bff3d-116">حدد "مركز التكلفة" في حقل "اسم البُعد".</span><span class="sxs-lookup"><span data-stu-id="bff3d-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="bff3d-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bff3d-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="bff3d-118">استيراد مراكز التكلفة</span><span class="sxs-lookup"><span data-stu-id="bff3d-118">Import cost centers</span></span>
1. <span data-ttu-id="bff3d-119">انقر فوق "استيراد أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="bff3d-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="bff3d-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bff3d-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="bff3d-121">عرض مراكز التكلفة المستوردة</span><span class="sxs-lookup"><span data-stu-id="bff3d-121">View the imported cost centers</span></span>
1. <span data-ttu-id="bff3d-122">انقر فوق "عرض أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="bff3d-122">Click View dimension members.</span></span>

