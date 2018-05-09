--- 
title: "إنشاء كائنات تكلفة  "
description: "يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة في Dynamics 365 for Finance and Operations إلى محاسبة التكاليف عبر موصل بيانات."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2c76a26ea63d1fd44c20fbee271d2767b8ea68b1
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="10cbc-103">إنشاء كائنات تكلفة  </span><span class="sxs-lookup"><span data-stu-id="10cbc-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10cbc-104">يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة في Dynamics 365 for Finance and Operations إلى محاسبة التكاليف عبر موصل بيانات.</span><span class="sxs-lookup"><span data-stu-id="10cbc-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="10cbc-105">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="10cbc-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="10cbc-106">يتم استخدام هذا الإجراء لميزة محاسبة التكاليف التي تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="10cbc-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="10cbc-107">إنشاء كائنات تكلفة جديدة</span><span class="sxs-lookup"><span data-stu-id="10cbc-107">Create new cost objects</span></span>
1. <span data-ttu-id="10cbc-108">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="10cbc-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="10cbc-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="10cbc-109">Click New.</span></span>
3. <span data-ttu-id="10cbc-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="10cbc-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="10cbc-111">في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="10cbc-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="10cbc-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="10cbc-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="10cbc-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="10cbc-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="10cbc-114">تكوين موصل البيانات</span><span class="sxs-lookup"><span data-stu-id="10cbc-114">Configure the data connector</span></span>
1. <span data-ttu-id="10cbc-115">انقر فوق "تكوين موفر عضو البُعد".</span><span class="sxs-lookup"><span data-stu-id="10cbc-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="10cbc-116">حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="10cbc-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="10cbc-117">حدد "مركز التكلفة" في حقل "اسم البُعد".</span><span class="sxs-lookup"><span data-stu-id="10cbc-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="10cbc-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10cbc-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="10cbc-119">استيراد مراكز التكلفة</span><span class="sxs-lookup"><span data-stu-id="10cbc-119">Import cost centers</span></span>
1. <span data-ttu-id="10cbc-120">انقر فوق "استيراد أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="10cbc-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="10cbc-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10cbc-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="10cbc-122">عرض مراكز التكلفة المستوردة</span><span class="sxs-lookup"><span data-stu-id="10cbc-122">View the imported cost centers</span></span>
1. <span data-ttu-id="10cbc-123">انقر فوق "عرض أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="10cbc-123">Click View dimension members.</span></span>


