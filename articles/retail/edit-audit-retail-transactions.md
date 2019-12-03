---
title: تحرير حركات متجر البيع بالتجزئة والتدقيق فيها
description: يصف هذا الموضوع الوظيفة الخاصة بتحرير حركات متجر البيع بالتجزئة والتدقيق فيها.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: f53573b8afb2003f6796930f5877185e533a4715
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693056"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="91e37-103">تحرير حركات متجر البيع بالتجزئة والتدقيق فيها</span><span class="sxs-lookup"><span data-stu-id="91e37-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="91e37-104">يستخدم عملاء Dynamics 365 Retail تطبيقات نقطة البيع (POS) للطرف الأول والطرف الثالث أيضًا.</span><span class="sxs-lookup"><span data-stu-id="91e37-104">Dynamics 365 Retail customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="91e37-105">مع تطبيق نقطة البيع (POS) للطرف الأول، يتم سحب حركات متجر البيع بالتجزئة إلى Retail Headquarters من القنوات عبر معالجة دُفعة.</span><span class="sxs-lookup"><span data-stu-id="91e37-105">With the first-party POS application, retail store transactions are pulled into Retail Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="91e37-106">ومع تطبيقات الطرف الثالث، يتم سحب الحركات إلى Retail Headquarters من خلال التكامل.</span><span class="sxs-lookup"><span data-stu-id="91e37-106">With third-party applications, transactions are pulled into Retail Headquarters through integration.</span></span> <span data-ttu-id="91e37-107">في الحالتين، بعد سحب الحركات إلى Retail Headquarters، يجب تنفيذ عملية تدقيق التناسق التي تقوم بتشغيل عمليات تحقق من الصحة متعددة على الحركات بحيث يتم سحب فقط الحركات التي نجحت في اجتياز التحقق من الصحة إلى كشف الحساب المراد ترحيله إلى Retail Headquarters.</span><span class="sxs-lookup"><span data-stu-id="91e37-107">In both cases, after transactions are pulled into Retail Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Retail Headquarters.</span></span> 

<span data-ttu-id="91e37-108">تفشل حركات البيع بالتجزئة في اجتياز التحقق من الصحة لأسباب متنوعة.</span><span class="sxs-lookup"><span data-stu-id="91e37-108">Retail transactions fail validation for various reasons.</span></span> <span data-ttu-id="91e37-109">على سبيل المثال، قد يتسبب خطأ في كود التكامل أو خطأ في تطبيق POS في الحصول على بيانات غير متناسقة، كما أن خطأ يقوم به المستخدم، مثل حذف منتج بعد مزامنته مع القناة أو إغلاق فترة مالية بدون ترحيل حركات البيع بالتجزئة لهذه الفترة، قد يتسبب في الحصول على بيانات غير متناسقة.</span><span class="sxs-lookup"><span data-stu-id="91e37-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting retail transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="91e37-110">بينما يتم وضع علامة على هذه الحركات واستبعادها من كشوف الحساب، بإمكان الحركات أن تؤدي إلى تعطيل عملية العميل اليومية المتعلقة بترحيل مبيعات البيع بالتجزئة اليومية إلى الماليات.</span><span class="sxs-lookup"><span data-stu-id="91e37-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily retail sales to the financials.</span></span>

<span data-ttu-id="91e37-111">في Retail، يمكنك تحرير حركات البيع بالتجزئة المحددة التي فشلت في اجتياز التحقق من الصحة مع الاحتفاظ بعمليات التدقيق في جميع التغييرات.</span><span class="sxs-lookup"><span data-stu-id="91e37-111">In Retail, you can edit the specific retail transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="91e37-112">تحرير الحركات والتدقيق فيها</span><span class="sxs-lookup"><span data-stu-id="91e37-112">Edit and audit transactions</span></span>

<span data-ttu-id="91e37-113">في الإصدار 10.0.5 من Retail، تعتبر حركات الدفع نقدًا والاستلام فورًا مثلها مثل المبيعات والمرتجعات الحركات الوحيدة التي يمكن تحريرها.</span><span class="sxs-lookup"><span data-stu-id="91e37-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="91e37-114">أوامر العميل أو الأوامر عبر الإنترنت غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="91e37-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="91e37-115">في الإصدار 10.0.6 من Retail والإصدارات اللاحقة، يعتبر تحرير حركات إدارة النقدية مدعومًا أيضًا.</span><span class="sxs-lookup"><span data-stu-id="91e37-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="91e37-116">قم بتثبيت الوظيفة الإضافية Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="91e37-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="91e37-117">انتقل إلى مساحة العمل **حركات متجر البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="91e37-117">Go to the **Retail store financials** workspace.</span></span> <span data-ttu-id="91e37-118">توفر لوحة **حالات فشل الحركات في اجتياز التحقق من الصحة** طريقة عرض تمت تصفيتها بشكل مسبق لنموذج حركة البيع بالتجزئة التي فشلت في اجتياز قاعدة أو أكثر من قواعد التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="91e37-118">The **Transaction validation failures** tile provides a pre-filtered view of the Retail transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="91e37-119">افتح النموذج.</span><span class="sxs-lookup"><span data-stu-id="91e37-119">Open the form.</span></span> <span data-ttu-id="91e37-120">انقر فوق السجل الذي فشل في اجتياز التحقق من الصحة، وانقر فوق **وظيفة Office الإضافية**، ثم انقر فوق **تحرير الحركة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="91e37-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="91e37-121">يفتح ملف Excel يتضمن تفاصيل الحركة المحددة، مع أوراق العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="91e37-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="91e37-122">البنود: تتضمن ورقة العمل هذه بنود الرأس والمنتج والبيانات المرتبطة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="91e37-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="91e37-123">المدفوعات: تتضمن ورقة العمل هذه تفاصيل بنود الدفع الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="91e37-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="91e37-124">الخصومات: تتضمن ورقة العمل هذه تفاصيل تتعلق بالخصومات الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="91e37-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="91e37-125">الضرائب: تتضمن ورقة العمل هذه تفاصيل تتعلق بالضرائب الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="91e37-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="91e37-126">التكاليف: تتضمن ورقة العمل هذه بيانات تتعلق بالتكاليف الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="91e37-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="91e37-127">في ملف Excel، يمكنك تعديل الحقول المناسبة ثم تحميل البيانات من جديد إلى Retail Headquarters باستخدام وظيفة النشر الإضافية في Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="91e37-127">In the Excel file, you modify the appropriate fields and then upload the data back into Retail Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="91e37-128">وستنعكس التغييرات في النظام عند نشرها.</span><span class="sxs-lookup"><span data-stu-id="91e37-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="91e37-129">أثناء عملية النشر، لا يتم إجراء أي عملية تحقق من الصحة على التغييرات التي يجريها المستخدمون.</span><span class="sxs-lookup"><span data-stu-id="91e37-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="91e37-130">يمكن عرض مسار التدقيق‏‎ الكامل للتغييرات عن طريق النقر فوق **عرض مسار التدقيق** في رأس **حركة البيع بالتجزئة** للتغييرات على مستوى الرأس وفي السجل والمقطع المناسبين في صفحة الحركة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="91e37-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="91e37-131">على سبيل المثال، ستكون جميع التغييرات ذات الصلة ببنود المبيعات مرئية في صفحة **حركات المبيعات‬**، وستكون التغييرات ذات الصلة بالمدفوعات مرئية في صفحة **حركات الدفع** وغير ذلك. تفاصيل التدقيق التي يتم الاحتفاظ بها للتغييرات هي على الشكل التالي.</span><span class="sxs-lookup"><span data-stu-id="91e37-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="91e37-132">تاريخ ووقت التعديل</span><span class="sxs-lookup"><span data-stu-id="91e37-132">Modified date and time</span></span>
   - <span data-ttu-id="91e37-133">الحقل</span><span class="sxs-lookup"><span data-stu-id="91e37-133">Field</span></span> 
   - <span data-ttu-id="91e37-134">قيمة قديمة</span><span class="sxs-lookup"><span data-stu-id="91e37-134">Old value</span></span>
   - <span data-ttu-id="91e37-135">قيمة جديدة</span><span class="sxs-lookup"><span data-stu-id="91e37-135">New value</span></span>
   - <span data-ttu-id="91e37-136">تعديل بواسطة</span><span class="sxs-lookup"><span data-stu-id="91e37-136">Modified by</span></span>

6. <span data-ttu-id="91e37-137">بعد اجراء التغييرات ونشرها، يمكنك تشغيل خيار **التحقق من صحة حركات المتجر‬** مرة أخرى للتأكد من أن التغييرات التي قمت بها متناسقة وصالحة.</span><span class="sxs-lookup"><span data-stu-id="91e37-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="91e37-138">يمكنك تحرير فقط الحركات التي فشلت في اجتياز التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="91e37-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="91e37-139">إذا أردت تحرير الحركات التي اجتازت عملية التحقق من الصحة، يمكنك تغيير حالة التحقق من الصحة للحركة التي تريد تغييرها إلى **خطأ** أو **بلا** وستتمكن عندئذٍ من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="91e37-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="91e37-140">تحرير مجمع‬ للحركات</span><span class="sxs-lookup"><span data-stu-id="91e37-140">Bulk edit transactions</span></span>

<span data-ttu-id="91e37-141">في الإصدار 10.0.6 من Retail أو إصدار أحدث، يمكن إجراء تحرير مجمع لحركات البيع بالتجزئة على مستوى كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="91e37-141">In Retail version 10.0.6 and higher, the option to bulk edit retail transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="91e37-142">استخدم وظيفة Excel الإضافية لفتح كشف حساب يتضمن الحركات التي تريد تعديلها باستخدام الخطوات من 1 إلى 3 أعلاه.</span><span class="sxs-lookup"><span data-stu-id="91e37-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="91e37-143">حدد أحد الخيارات أدناه.</span><span class="sxs-lookup"><span data-stu-id="91e37-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="91e37-144">**تحرير حركات الدفع نقدًا والاستلام فورًا‬**.</span><span class="sxs-lookup"><span data-stu-id="91e37-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="91e37-145">يسمح لك هذا الخيار بتحرير كافة حركات الدفع نقدًا والاستلام فورًا المضمنة في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="91e37-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="91e37-146">تتوفر أوراق عمل Excel التالية.</span><span class="sxs-lookup"><span data-stu-id="91e37-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="91e37-147">**الحركة**: تتضمن ورقة العمل هذه جميع المعلومات على مستوى الرأس الخاصة بحركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="91e37-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="91e37-148">**حركة المبيعات**: تتضمن ورقة العمل هذه جميع المعلومات على مستوى البنود الخاصة بحركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="91e37-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="91e37-149">**حركات الدفع‬**: تتضمن ورقة العمل هذه جميع معلومات بنود الدفع‬ لحركات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="91e37-150">**حركات الخصم‬‬**: تتضمن ورقة العمل هذه جميع معلومات بنود الخصم لحركات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="91e37-151">**حركة الضريبة‬**: تتضمن ورقة العمل هذه جميع معلومات بنود الضرائب الخاصة بحركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="91e37-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="91e37-152">**حركات التكلفة‬**: تتضمن ورقة العمل هذه جميع معلومات بنود التكاليف لحركات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="91e37-153">**تحرير حركات إدارة النقد**.</span><span class="sxs-lookup"><span data-stu-id="91e37-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="91e37-154">يسمح لك هذا الخيار بتحرير كافة حركات إدارة النقد المضمنة في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="91e37-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="91e37-155">تتوفر أوراق عمل Excel التالية.</span><span class="sxs-lookup"><span data-stu-id="91e37-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="91e37-156">**الحركة**: تتضمن ورقة العمل هذه جميع المعلومات على مستوى الرأس الخاصة بحركات إدارة النقد.</span><span class="sxs-lookup"><span data-stu-id="91e37-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="91e37-157">**حركات طريقة الدفع البنكية‬**: تتضمن ورقة العمل هذه تفاصيل جميع حركات الإيداع البنكية‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="91e37-158">**حركات طريقة دفع الخزينة‬‬**: تتضمن ورقة العمل هذه تفاصيل جميع حركات الإيداع في الخزينة.</span><span class="sxs-lookup"><span data-stu-id="91e37-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="91e37-159">**إقرار الدفع‬‬**: تتضمن ورقة العمل هذه تفاصيل جميع حركات إقرار الدفع‬‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="91e37-160">**حركات الإيرادات/المصروفات‬**: تتضمن ورقة العمل هذه تفاصيل جميع بنود حركة حركات الإيرادات/المصروفات‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="91e37-161">**حركات الدفع**: تتضمن ورقة العمل هذه جميع المعلومات ذات الصلة بالدفع لعملية **دفع الفاتورة‬** بالإضافة إلى حركة الإيرادات/المصروفات‬.</span><span class="sxs-lookup"><span data-stu-id="91e37-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="91e37-162">لا يتم تنفيذ عمليات التحقق من الصحة عند نشر الحركات التي تم إجراء تحرير مجمع لها.</span><span class="sxs-lookup"><span data-stu-id="91e37-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="91e37-163">يجب أن تتأكد من دقة جميع عمليات التحرير ومن المحافظة على دقة البيانات عبر أوراق العمل.</span><span class="sxs-lookup"><span data-stu-id="91e37-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="91e37-164">على سبيل المثال، إذا أردت تغيير تاريخ الحركة لإدارة السيناريوهات حيث تم إقفال الفترة المالية أو فترة المخزون لحركات البيع بالتجزئة المفتوحة، فعليك تغيير التاريخ على جميع أوراق عمل Excel التي تتضمن عمود **تاريخ العمل**.</span><span class="sxs-lookup"><span data-stu-id="91e37-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open retail transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="91e37-165">للتحقق من صحة الحركات بعد تحريرها، يمكنك استخدام **إعادة التحقق من صحة الحركات** في صفحة **كشوف البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="91e37-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Retail statements** page.</span></span>
