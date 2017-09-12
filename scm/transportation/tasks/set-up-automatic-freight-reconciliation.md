--- 
title: "إعداد تسوية الشحن التلقائية"
description: "يوضح هذا الإجراء كيفية إعداد البيانات لتسوية الشحن التلقائية."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="30dec-103">إعداد تسوية الشحن التلقائية</span><span class="sxs-lookup"><span data-stu-id="30dec-103">Set up automatic freight reconciliation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30dec-104">يوضح هذا الإجراء كيفية إعداد البيانات لتسوية الشحن التلقائية.</span><span class="sxs-lookup"><span data-stu-id="30dec-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="30dec-105">عادة ما يتم تنفيذ هذه العملية عن طريق مدير المستودع.</span><span class="sxs-lookup"><span data-stu-id="30dec-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="30dec-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="30dec-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="30dec-107">إعداد نوع فاتورة الشحن</span><span class="sxs-lookup"><span data-stu-id="30dec-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="30dec-108">انتقل إلى إدارة النقل > الإعداد > تسوية الشحن > نوع فاتورة الشحن.</span><span class="sxs-lookup"><span data-stu-id="30dec-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="30dec-109">يعرف نوع فاتورة الشحن كيف يجب أن تتطابق فواتير الشحن وفواتير شركة النقل.</span><span class="sxs-lookup"><span data-stu-id="30dec-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="30dec-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="30dec-110">Click New.</span></span>
3. <span data-ttu-id="30dec-111">في الحقل "نوع فاتورة الشحن"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30dec-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="30dec-112">في حقل "تجميع المحرك"، اكتب 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span><span class="sxs-lookup"><span data-stu-id="30dec-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="30dec-113">هذه هي إدارة النقل القياسية المطابقة لمكتبة أكواد المحرك.</span><span class="sxs-lookup"><span data-stu-id="30dec-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="30dec-114">في حقل "فئة المحرك"، اكتب 'Microsoft.Dynamics.Ax.Tms.dll'.</span><span class="sxs-lookup"><span data-stu-id="30dec-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="30dec-115">هذه هي إدارة النقل القياسية المطابقة لفئة المحرك.</span><span class="sxs-lookup"><span data-stu-id="30dec-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="30dec-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="30dec-116">Click New.</span></span>
7. <span data-ttu-id="30dec-117">في حقل "الوصف"، اختر القيمة التي يجب أن تتطابق على فاتورة الشحن وفاتورة شركة النقل.</span><span class="sxs-lookup"><span data-stu-id="30dec-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="30dec-118">في الحقل "المطابقة مطلوبة"، حدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="30dec-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="30dec-119">إذا قمت بتعيين هذا الحقل إلى "نعم"، فهذا يعني أن القيمة المحددة في حقل "الوصف" يجب أن تكون مطابقة على كل من فاتورة الشحن وفاتورة شركة النقل.</span><span class="sxs-lookup"><span data-stu-id="30dec-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="30dec-120">إما إذا قمت بتعيينه إلى "لا"، فبإمكان الحقل أن يكون فارغًا في إحدى القيمتين.</span><span class="sxs-lookup"><span data-stu-id="30dec-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="30dec-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="30dec-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="30dec-122">إعداد تعيين نوع فاتورة الشحن</span><span class="sxs-lookup"><span data-stu-id="30dec-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="30dec-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30dec-123">Close the page.</span></span>
2. <span data-ttu-id="30dec-124">انتقل إلى إدارة النقل > الإعداد > تسوية الشحن > تعيينات نوع كمبيالة الشحن.</span><span class="sxs-lookup"><span data-stu-id="30dec-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="30dec-125">يُستخدم تعيين نوع فاتورة الشحن لتحديد نوع فاتورة الشحن المستخدم لشركة معينة.</span><span class="sxs-lookup"><span data-stu-id="30dec-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="30dec-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="30dec-126">Click New.</span></span>
4. <span data-ttu-id="30dec-127">في الحقل "الوضع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="30dec-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="30dec-128">في الحقل "شركة الشحن"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="30dec-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="30dec-129">في الحقل "نوع فاتورة الشحن"، حدد نوع فاتورة الشحن التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="30dec-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="30dec-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30dec-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="30dec-131">إعداد أصل التدقيق</span><span class="sxs-lookup"><span data-stu-id="30dec-131">Set up the audit master</span></span>
1. <span data-ttu-id="30dec-132">انتقل إلى إدارة النقل > الإعداد > تسوية الشحن > أصل التدقيق.</span><span class="sxs-lookup"><span data-stu-id="30dec-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="30dec-133">يحدد السجل الرئيسي للتدقيق حدود السماح لتسوية الشحن التلقائية.</span><span class="sxs-lookup"><span data-stu-id="30dec-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="30dec-134">فهو يحدد مقدار الاختلاف الممكن بين المبالغ النقدية على فاتورة الشحن والمبالغ النقدية على فاتورة شركة النقل ومع ذلك يسمح بحدوث التسوية.</span><span class="sxs-lookup"><span data-stu-id="30dec-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="30dec-135">وهو يحدد أيضًا كيفية التعامل مع الاختلافات.</span><span class="sxs-lookup"><span data-stu-id="30dec-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="30dec-136">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="30dec-136">Click New.</span></span>
3. <span data-ttu-id="30dec-137">في الحقل "معرف أصل التدقيق‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="30dec-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="30dec-138">في حقل "شركة الشحن"، حدد شركة الشحن نفسها كما فعلت سابقًا.</span><span class="sxs-lookup"><span data-stu-id="30dec-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="30dec-139">في الحقل "نوع فاتورة الشحن"، حدد نوع فاتورة الشحن التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="30dec-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="30dec-140">قم بتوسيع مقطع "السماح".</span><span class="sxs-lookup"><span data-stu-id="30dec-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="30dec-141">في حقل "‏‫الحد الأدنى لمستوى السماح"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="30dec-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="30dec-142">في حقل "‏‫الحد الأقصى لمستوى السماح"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="30dec-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="30dec-143">قم بتوسيع مقطع "النتيجة".</span><span class="sxs-lookup"><span data-stu-id="30dec-143">Expand the Result section.</span></span>
10. <span data-ttu-id="30dec-144">في حقل "‏‫كود سبب الدفع بالزيادة‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="30dec-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="30dec-145">إذا كانت المبالغ النقدية على فاتورة الشحن مختلفة عما هي عليه على فاتورة شركة النقل، فإن أكواد أسباب الدفع بالزيادة والدفع بالنقصان تحدد الحسابات التي يجب تسجيل الفرق عليها، طالما وقع الفرق ضمن مستويات السماح.</span><span class="sxs-lookup"><span data-stu-id="30dec-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="30dec-146">في حقل "‏‫كود سبب الدفع بالنقصان"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="30dec-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="30dec-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="30dec-147">Close the page.</span></span>


