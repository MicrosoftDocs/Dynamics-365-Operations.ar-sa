---
title: 'إنشاء كائنات تكلفة  '
description: يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810044"
---
# <a name="create-cost-objects"></a><span data-ttu-id="b457b-103">إنشاء كائنات تكلفة  </span><span class="sxs-lookup"><span data-stu-id="b457b-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b457b-104">يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات.</span><span class="sxs-lookup"><span data-stu-id="b457b-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="b457b-105">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="b457b-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="b457b-106">إنشاء كائنات تكلفة جديدة</span><span class="sxs-lookup"><span data-stu-id="b457b-106">Create new cost objects</span></span>
1. <span data-ttu-id="b457b-107">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b457b-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="b457b-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b457b-108">Click New.</span></span>
3. <span data-ttu-id="b457b-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b457b-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b457b-110">في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b457b-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b457b-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b457b-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b457b-112">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b457b-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b457b-113">تكوين موصل البيانات</span><span class="sxs-lookup"><span data-stu-id="b457b-113">Configure the data connector</span></span>
1. <span data-ttu-id="b457b-114">انقر فوق "تكوين موفر عضو البُعد".</span><span class="sxs-lookup"><span data-stu-id="b457b-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="b457b-115">حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b457b-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="b457b-116">حدد "مركز التكلفة" في حقل "اسم البُعد".</span><span class="sxs-lookup"><span data-stu-id="b457b-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="b457b-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b457b-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="b457b-118">استيراد مراكز التكلفة</span><span class="sxs-lookup"><span data-stu-id="b457b-118">Import cost centers</span></span>
1. <span data-ttu-id="b457b-119">انقر فوق "استيراد أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="b457b-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="b457b-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b457b-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="b457b-121">عرض مراكز التكلفة المستوردة</span><span class="sxs-lookup"><span data-stu-id="b457b-121">View the imported cost centers</span></span>
1. <span data-ttu-id="b457b-122">انقر فوق "عرض أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="b457b-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]