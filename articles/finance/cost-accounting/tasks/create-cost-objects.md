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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c25c52a2c6dc7f096a494577b361ff30406e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236784"
---
# <a name="create-cost-objects"></a><span data-ttu-id="a86ab-103">إنشاء كائنات تكلفة  </span><span class="sxs-lookup"><span data-stu-id="a86ab-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a86ab-104">يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات.</span><span class="sxs-lookup"><span data-stu-id="a86ab-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="a86ab-105">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="a86ab-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="a86ab-106">إنشاء كائنات تكلفة جديدة</span><span class="sxs-lookup"><span data-stu-id="a86ab-106">Create new cost objects</span></span>
1. <span data-ttu-id="a86ab-107">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a86ab-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="a86ab-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a86ab-108">Click New.</span></span>
3. <span data-ttu-id="a86ab-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a86ab-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a86ab-110">في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a86ab-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="a86ab-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a86ab-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a86ab-112">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a86ab-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="a86ab-113">تكوين موصل البيانات</span><span class="sxs-lookup"><span data-stu-id="a86ab-113">Configure the data connector</span></span>
1. <span data-ttu-id="a86ab-114">انقر فوق "تكوين موفر عضو البُعد".</span><span class="sxs-lookup"><span data-stu-id="a86ab-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="a86ab-115">حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a86ab-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="a86ab-116">حدد "مركز التكلفة" في حقل "اسم البُعد".</span><span class="sxs-lookup"><span data-stu-id="a86ab-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="a86ab-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a86ab-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="a86ab-118">استيراد مراكز التكلفة</span><span class="sxs-lookup"><span data-stu-id="a86ab-118">Import cost centers</span></span>
1. <span data-ttu-id="a86ab-119">انقر فوق "استيراد أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="a86ab-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="a86ab-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a86ab-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="a86ab-121">عرض مراكز التكلفة المستوردة</span><span class="sxs-lookup"><span data-stu-id="a86ab-121">View the imported cost centers</span></span>
1. <span data-ttu-id="a86ab-122">انقر فوق "عرض أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="a86ab-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]