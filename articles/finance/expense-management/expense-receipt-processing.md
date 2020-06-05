---
title: معالجة إيصال المصروفات
description: يوفر هذا الموضوع معلومات حول معالجة التعرف البصري على الحرىف (OCR) للإيصالات. تم تصميم هذه الميزة لتحسين تجربة المستخدم عند إنشاء تقارير المصروفات في Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378221"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="4070f-104">معالجة استلام المصروفات</span><span class="sxs-lookup"><span data-stu-id="4070f-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4070f-105">تم تحسين إدخال المصروفات من خلال مقدمة معالجة التعرف البصري على الحروف (OCR) للإيصالات.</span><span class="sxs-lookup"><span data-stu-id="4070f-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="4070f-106">تم تصميم هذه الميزة لتحسين تجربة المستخدم عند إنشاء تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4070f-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="4070f-107">الميزات الرئيسية</span><span class="sxs-lookup"><span data-stu-id="4070f-107">Key features</span></span>

- <span data-ttu-id="4070f-108">يتم استخراج اسم التاجر والتاريخ والمبلغ الإجمالي من الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="4070f-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="4070f-109">تحاول هذه الميزة مطابقة الإيصالات غير المرفقة بحركات المصروفات غير المرفقة.</span><span class="sxs-lookup"><span data-stu-id="4070f-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="4070f-110">يمكن للمستخدمين إنشاء حركات مصروفات يتم إدخالها يدويًا من الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="4070f-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="4070f-111">أمثلة الاستخدام</span><span class="sxs-lookup"><span data-stu-id="4070f-111">Usage examples</span></span>

<span data-ttu-id="4070f-112">لإرفاق الإيصالات تلقائيًا التي تشتمل على حركات بطاقة الائتمان عند إنشاء تقرير مصروفات، افعل مع يلي:</span><span class="sxs-lookup"><span data-stu-id="4070f-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="4070f-113">افتح مساحة عمل **إدارة المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="4070f-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="4070f-114">في علامة التبويب **الإيصالات**، تحقق من وجود الإيصالات غير المرفقة.</span><span class="sxs-lookup"><span data-stu-id="4070f-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="4070f-115">يمكنك أيضًا تحميل الإيصالات في علامة التبويب **الإيصالات**.</span><span class="sxs-lookup"><span data-stu-id="4070f-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="4070f-116">في علامة التبويب **المصروفات**، تحقق من وجود المصروفات غير المرفقة.</span><span class="sxs-lookup"><span data-stu-id="4070f-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="4070f-117">عادة ما يستورد مسؤول المصروفات هذه المصروفات من موفر بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="4070f-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="4070f-118">حدد  **تقرير مصروفات جديد**.</span><span class="sxs-lookup"><span data-stu-id="4070f-118">Select **New expense report**.</span></span> <span data-ttu-id="4070f-119">لاحظ أنه يمكنك أيضًا حاليًا تضمين المصروفات والإيصالات عند إنشاء تقرير مصروفات.</span><span class="sxs-lookup"><span data-stu-id="4070f-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="4070f-120">عند إضافة كل من المصروفات والإيصالات، سيتم تشغيل المطابقة التلقائية للإيصالات مقابل المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4070f-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="4070f-121">لإنشاء مصروفات، أو مطابقة مصروفات من إيصال، افعل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="4070f-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="4070f-122">في تقرير مصروفات، من علامة التبويب **الإيصالات**، ارفق إيصالاً بتحديد **إضافة إيصالات**.</span><span class="sxs-lookup"><span data-stu-id="4070f-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="4070f-123">ضمن الصورة التي تم تحميلها من الإيصال، لاحظ الخيارين **إنشاء** و**مطابقة**.</span><span class="sxs-lookup"><span data-stu-id="4070f-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="4070f-124">حدد **إنشاء** لإنشاء حركة مصروفات يتم إدخالها يدويًا وملء القيم المستخرجة من الإيصال.</span><span class="sxs-lookup"><span data-stu-id="4070f-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="4070f-125">في حالة تحديد **مطابقة**، يحاول النظام مطابقة المصروفات الموجودة بالإيصال.</span><span class="sxs-lookup"><span data-stu-id="4070f-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="4070f-126">التثبيت</span><span class="sxs-lookup"><span data-stu-id="4070f-126">Installation</span></span>

<span data-ttu-id="4070f-127">تعمل هذه الميزة بالاشتراك مع ميزة **‏‫إعادة تصور تقارير المصروفات** للمساعدة في تبسيط تجربة المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4070f-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="4070f-128">تتوفر هذه الميزة فقط لبيئات الطبقة 2+، وهي بيئة الاختبار المعزولة وبيئة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="4070f-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="4070f-129">لاستخدام قدرات المصروفات المتقدمة هذه، ثبت الوظيفة الإضافية خدمة إدارة المصروفات لـ Microsoft Dynamics 365 Finance، ثم شغَّل الميزات الموجودة في المثيل لديك.</span><span class="sxs-lookup"><span data-stu-id="4070f-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="4070f-130">يمكنك الوصول إلى الوظيفة الإضافية من المشروع في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4070f-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="4070f-131">قم بتسجيل الدخول إلى LCS، وافتح البيئة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="4070f-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="4070f-132">انتقل إلى **التفاصيل الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="4070f-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="4070f-133">حدد **الاحتفاظ**، أو قم بالتمرير لأسفل إلى علامة التبويب السريع **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="4070f-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="4070f-134">حدد **تثبيت وظيفة إضاية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="4070f-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="4070f-135">حدد **خدمة إدارة المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="4070f-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="4070f-136">اتبع دليل التثبيت، ووافق على البنود والشروط.</span><span class="sxs-lookup"><span data-stu-id="4070f-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="4070f-137">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="4070f-137">Select **Install**.</span></span>

<span data-ttu-id="4070f-138">في مساحة عمل **إدارة الميزات**، شغَّل الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="4070f-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="4070f-139">إعادة تصور تقارير المصروفات</span><span class="sxs-lookup"><span data-stu-id="4070f-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="4070f-140">المطابقة التلقائية وإنشاء المصروفات من الإيصال</span><span class="sxs-lookup"><span data-stu-id="4070f-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="4070f-141">عند تشغيل هذه الميزات تحدث الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="4070f-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="4070f-142">تحل مساحة العمل الجديدة محل مساحة عمل **إدارة المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="4070f-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="4070f-143">يُضاف عنصر قائمة جديد لرؤية حقل المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4070f-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="4070f-144">لا يزال بإمكانك فتح صفحة **تقارير المصروفات** السابقة بالانتقال إلى **إدارة المصروفات > مصروفاتي > تقارير المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="4070f-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="4070f-145">ما زالت عمليات سير العمل والموافقات تنقلك إلى صفحة تقارير المصروفات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="4070f-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="4070f-146">ستتم معالجة الإيصالات من خلال Microsoft Azure Cognitive Services، وسيتم استخراج بيانات التعريف وإضافتها.</span><span class="sxs-lookup"><span data-stu-id="4070f-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="4070f-147">تتم إضافة خيار يتيح لك إنشاء تقرير مصروفات يتضمن الإيصالات غير المرفقة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="4070f-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="4070f-148">يتيح لك خيار تتم إضافته إلى تقارير المصروفات إنشاء سطر مصروفات من أحد الإيصالات، أو محاولة مطابقة إيصال موجود بسطر مصروفات موجود.</span><span class="sxs-lookup"><span data-stu-id="4070f-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="4070f-149">لمزيد من المعلومات حول ميزة ‏‫إعادة تصور تقارير المصروفات‬، راجع [‏‫إعادة تصور تقارير المصروفات‬](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="4070f-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="4070f-150">الأسئلة المتداولة</span><span class="sxs-lookup"><span data-stu-id="4070f-150">Frequently asked questions</span></span>

<span data-ttu-id="4070f-151">**هل تستخدم Microsoft بياناتي لنماذجها؟**</span><span class="sxs-lookup"><span data-stu-id="4070f-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="4070f-152">لا، لقد أنشأت Microsoft نموذج تعلم آلي عام لخدمة معالجة الإيصالات الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="4070f-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="4070f-153">ولا يستند هذا النموذج إلى الإيصالات التي تحمِّلها.</span><span class="sxs-lookup"><span data-stu-id="4070f-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="4070f-154">**أين تتوفر هذه الميزة وتتم معالجتها؟**</span><span class="sxs-lookup"><span data-stu-id="4070f-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="4070f-155">في الوقت الحالي، تحظى الولايات المتحدة بالدعم.</span><span class="sxs-lookup"><span data-stu-id="4070f-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="4070f-156">**أين تذهب إيصالاتي؟**</span><span class="sxs-lookup"><span data-stu-id="4070f-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="4070f-157">ستتصل Finance بالخدمات المعرفية لاستخراج بيانات الحقل.</span><span class="sxs-lookup"><span data-stu-id="4070f-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="4070f-158">ستحتفظ الخدمات المعرفية بنسخة من إيصالك لمدة تصل إلى 24 ساعة أثناء حدوث المعالجة.</span><span class="sxs-lookup"><span data-stu-id="4070f-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="4070f-159">بعد اكتمال المعالجة، تقوم الخدمات المعرفية بإزالة الإيصال.</span><span class="sxs-lookup"><span data-stu-id="4070f-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="4070f-160">لا يزال يتم تخزين الإيصالات في Finance.</span><span class="sxs-lookup"><span data-stu-id="4070f-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="4070f-161">لمزيد من المعلومات، راجع [تمكين فهم الإيصال باستخدام قدرة منظم النموذج الجديدة](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="4070f-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
