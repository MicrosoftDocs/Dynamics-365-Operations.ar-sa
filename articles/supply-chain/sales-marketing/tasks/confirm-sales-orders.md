---
title: تأكيد أوامر المبيعات
description: يوضح هذا الإجراء كيفية تأكيد أوامر المبيعات.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323975"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="b3f9c-103">تأكيد أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="b3f9c-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3f9c-104">يوضح هذا الإجراء كيفية تأكيد أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="b3f9c-105">ستتعرف على كيفية تأكيد أمر واحد وتأكيد أوامر متعددة في مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="b3f9c-106">وعادة ما تُنفذ هذه المهام عن طريق معالج أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="b3f9c-107">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b3f9c-108">قبل البدء، تأكد من وجود العديد من أوامر المبيعات المفتوحة لنفس العميل.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="b3f9c-109">إذا كنت تستخدم USMF، يمكنك استخدام العميل 027-الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="b3f9c-110">قم بتأكيد أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="b3f9c-111">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="b3f9c-112">في القائمة، ابحث عن الأمر الذي تريد تأكيده وحدده.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="b3f9c-113">انقر فوق الارتباط الموجود في رقم أمر المبيعات لفتح الأمر المحدد.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="b3f9c-114">في جزء الإجراءات، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="b3f9c-115">قم بتأكيد أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="b3f9c-116">قم بتوسيع القسم "المعلمات" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="b3f9c-117">تأكد من أن الحقل "ترحيل نعم" نشط.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="b3f9c-118">قم بتعيين خيار تأكيد الطباعة على "نعم".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="b3f9c-119">يحدد الحقل "التحقق من حد الائتمان" الطريقة المُستخدمة لحساب ائتمان العميل المتبقي.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="b3f9c-120">ويُنسخ ائتمان العميل المتبقي افتراضيًا من صفحة معلمات الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="b3f9c-121">إذا كنت ترغب في تخطي التحقق من حد الائتمان عند تأكيد أمر مبيعات معين، فقم بتعيين "التحقق من حد الائتمان" على "بلا".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="b3f9c-122">ومع ذلك، يجب أن تعلم أنه حتى إذا تم تعيين هذا الحقل على "بلا"، سيظل التحقق من حد الائتمان منفذًا إذا تم تحديد الخيار "حد الائتمان الإلزامي" في بيانات العميل الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="b3f9c-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-123">Click OK.</span></span>
9. <span data-ttu-id="b3f9c-124">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-124">Click Yes.</span></span>
10. <span data-ttu-id="b3f9c-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-125">Close the page.</span></span>
11. <span data-ttu-id="b3f9c-126">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="b3f9c-127">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-127">Click Change view.</span></span>
13. <span data-ttu-id="b3f9c-128">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-128">Click Header view.</span></span>
    * <span data-ttu-id="b3f9c-129">عند تأكيد أمر، يتم تعيين حالة المستند على "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="b3f9c-130">في جزء الإجراءات، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="b3f9c-131">انقر فوق "تأكيد أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="b3f9c-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="b3f9c-133">تأكيد أوامر مبيعات متعددة في وقت واحد</span><span class="sxs-lookup"><span data-stu-id="b3f9c-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="b3f9c-134">انتقل إلى المبيعات والتسويق > أوامر المبيعات > تأكيد الأمر > تأكيد أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="b3f9c-135">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-135">Click Select.</span></span>
3. <span data-ttu-id="b3f9c-136">في القائمة بعلامة التبويب "النطاق"، ابحث عن السجل الذي يشير إلى حقل حساب ثم حدده.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="b3f9c-137">في الحقل "المعايير"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b3f9c-138">في القائمة، ابحث عن حساب العميل الذي يحتوي على أوامر متعددة وترغب في إجراء تأكيد جماعي به ثم حدده.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="b3f9c-139">إذا كنت تستخدم USMF، يمكنك تحديد حساب 027-الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="b3f9c-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-140">Click OK.</span></span>
    * <span data-ttu-id="b3f9c-141">تعرض علامة التبويب "نظرة عامة" قائمة بالأوامر التي تطابق معايير الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="b3f9c-142">سيتم تضمين هذه الأوامر في التأكيد.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="b3f9c-143">يحدد الحقل "تحديث الملخص لـ" المعلمة يتم من خلالها تلخيص أوامر متعددة في مستند تأكيد واحد.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="b3f9c-144">بشكل افتراضي، يُنسخ الخيار من القيم الافتراضية لإعداد تحديث الملخص في صفحة معلمات الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="b3f9c-145">في تحديث الملخص للحقل، حدد "أمر".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="b3f9c-146">ويتمثل الحد الأدنى للمعلمات المطلوبة لإنشاء تحديثات ملخص في حساب الفاتورة والعملة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="b3f9c-147">وهذا يعني أن تحديثات الملخص التي لها حسابات فواتير مختلفة وعملات مختلفة غير مسموح بها.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="b3f9c-148">يمكن إعداد معلمات إضافية في صفحة معلمات تحديث الملخص التي يمكن الوصول إليها من صفحة معلومات الحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="b3f9c-149">في الحقل "أمر المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b3f9c-150">في القائمة، حدد العدد الذي تريده أن يمثل أمر الملخص.</span><span class="sxs-lookup"><span data-stu-id="b3f9c-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="b3f9c-151">انقر فوق "ترتيب".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-151">Click Arrange.</span></span>
11. <span data-ttu-id="b3f9c-152">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-152">Click OK.</span></span>
12. <span data-ttu-id="b3f9c-153">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b3f9c-153">Click OK.</span></span>

