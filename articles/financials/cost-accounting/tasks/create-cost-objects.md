---
title: 'إنشاء كائنات تكلفة  '
description: يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة في Dynamics 365 for Finance and Operations, Enterprise edition إلى محاسبة التكاليف عبر موصل بيانات.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "322664"
---
# <a name="create-cost-objects"></a><span data-ttu-id="74f2c-103">إنشاء كائنات تكلفة  </span><span class="sxs-lookup"><span data-stu-id="74f2c-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74f2c-104">يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة في Dynamics 365 for Finance and Operations, Enterprise edition إلى محاسبة التكاليف عبر موصل بيانات.</span><span class="sxs-lookup"><span data-stu-id="74f2c-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="74f2c-105">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="74f2c-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="74f2c-106">يتم استخدام هذا الإجراء لميزة محاسبة التكاليف‬ التي تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="74f2c-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="74f2c-107">إنشاء كائنات تكلفة جديدة</span><span class="sxs-lookup"><span data-stu-id="74f2c-107">Create new cost objects</span></span>
1. <span data-ttu-id="74f2c-108">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="74f2c-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="74f2c-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="74f2c-109">Click New.</span></span>
3. <span data-ttu-id="74f2c-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="74f2c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="74f2c-111">في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="74f2c-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="74f2c-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="74f2c-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="74f2c-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="74f2c-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="74f2c-114">تكوين موصل البيانات</span><span class="sxs-lookup"><span data-stu-id="74f2c-114">Configure the data connector</span></span>
1. <span data-ttu-id="74f2c-115">انقر فوق "تكوين موفر عضو البُعد".</span><span class="sxs-lookup"><span data-stu-id="74f2c-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="74f2c-116">حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="74f2c-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="74f2c-117">حدد "مركز التكلفة" في حقل "اسم البُعد".</span><span class="sxs-lookup"><span data-stu-id="74f2c-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="74f2c-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="74f2c-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="74f2c-119">استيراد مراكز التكلفة</span><span class="sxs-lookup"><span data-stu-id="74f2c-119">Import cost centers</span></span>
1. <span data-ttu-id="74f2c-120">انقر فوق "استيراد أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="74f2c-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="74f2c-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="74f2c-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="74f2c-122">عرض مراكز التكلفة المستوردة</span><span class="sxs-lookup"><span data-stu-id="74f2c-122">View the imported cost centers</span></span>
1. <span data-ttu-id="74f2c-123">انقر فوق "عرض أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="74f2c-123">Click View dimension members.</span></span>

