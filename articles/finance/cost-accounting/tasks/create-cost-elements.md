---
title: 'إنشاء عناصر تكلفة  '
description: هناك عدة طرق لإنشاء عناصر تكلفة في محاسبة التكاليف.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c4c1e2aee7ba98c1cca378286afb643eaca1600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810068"
---
# <a name="create-cost-elements"></a><span data-ttu-id="17527-103">إنشاء عناصر تكلفة  </span><span class="sxs-lookup"><span data-stu-id="17527-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17527-104">هناك عدة طرق لإنشاء عناصر تكلفة في محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="17527-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="17527-105">يوضح هذا الإجراء كيفية إنشاء عناصر التكلفة عن طريق استيراد الحسابات الرئيسية عبر موصل بيانات.</span><span class="sxs-lookup"><span data-stu-id="17527-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="17527-106">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="17527-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="17527-107">يتم استخدام هذا الإجراء لميزة محاسبة التكاليف‬ التي تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="17527-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="17527-108">إنشاء عناصر تكلفة جديدة</span><span class="sxs-lookup"><span data-stu-id="17527-108">Create new cost elements</span></span>
1. <span data-ttu-id="17527-109">انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد عنصر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="17527-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="17527-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="17527-110">Click New.</span></span>
3. <span data-ttu-id="17527-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="17527-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="17527-112">في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17527-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="17527-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="17527-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="17527-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="17527-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="17527-115">تكوين موصل البيانات</span><span class="sxs-lookup"><span data-stu-id="17527-115">Configure the data connector</span></span>
1. <span data-ttu-id="17527-116">انقر فوق "تكوين موفر عضو البُعد".</span><span class="sxs-lookup"><span data-stu-id="17527-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="17527-117">في الحقل "دليل الحسابات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17527-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="17527-118">حدد "مشترك" لاستخدام دليل الحسابات المشترك.</span><span class="sxs-lookup"><span data-stu-id="17527-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="17527-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="17527-119">Click New.</span></span>
4. <span data-ttu-id="17527-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="17527-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="17527-121">يمكنك تطبيق عوامل التصفية على الحسابات للوفاء بالمعايير.</span><span class="sxs-lookup"><span data-stu-id="17527-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="17527-122">في الحقل "من الحساب الرئيسي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17527-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="17527-123">في الحقل "إلى الحساب الرئيسي‬‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17527-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="17527-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="17527-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="17527-125">استيراد الحسابات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="17527-125">Import main accounts</span></span>
1. <span data-ttu-id="17527-126">انقر فوق "استيراد أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="17527-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="17527-127">سيتم استيراد الحسابات الرئيسية إلى محاسبة التكاليف وسيتم استخدامها كعناصر تكلفة.</span><span class="sxs-lookup"><span data-stu-id="17527-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="17527-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="17527-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="17527-129">عرض الحسابات المستوردة كعناصر تكلفة</span><span class="sxs-lookup"><span data-stu-id="17527-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="17527-130">انقر فوق "عرض أعضاء الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="17527-130">Click View dimension members.</span></span>
    * <span data-ttu-id="17527-131">اعرض حسابات دفتر الأستاذ التي تم استيرادها كعناصر تكلفة في شركتك والتي يمكن للتكاليف أن تتدفق إليها.</span><span class="sxs-lookup"><span data-stu-id="17527-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]