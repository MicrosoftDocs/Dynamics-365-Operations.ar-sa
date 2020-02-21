---
title: تحرير حركات متجر البيع بالتجزئة والتدقيق فيها
description: يصف هذا الموضوع الوظيفة الخاصة بتحرير حركات المتجر والتدقيق فيها.
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
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004379"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="abff3-103">تحرير حركات متجر البيع بالتجزئة والتدقيق فيها</span><span class="sxs-lookup"><span data-stu-id="abff3-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="abff3-104">يستخدم عملاء Dynamics 365 Commerce تطبيقات نقطة البيع (POS) للطرف الأول والطرف الثالث أيضًا.</span><span class="sxs-lookup"><span data-stu-id="abff3-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="abff3-105">مع تطبيق نقطة البيع (POS) للطرف الأول، يتم سحب حركات المتجر إلى Headquarters من القنوات عبر معالجة دُفعة.</span><span class="sxs-lookup"><span data-stu-id="abff3-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="abff3-106">ومع تطبيقات الطرف الثالث، يتم سحب الحركات إلى Headquarters من خلال التكامل.</span><span class="sxs-lookup"><span data-stu-id="abff3-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="abff3-107">في الحالتين، بعد سحب الحركات إلى Headquarters، يجب تنفيذ عملية تدقيق التناسق التي تقوم بتشغيل عمليات تحقق من الصحة متعددة على الحركات بحيث يتم سحب فقط الحركات التي نجحت في اجتياز التحقق من الصحة إلى كشف الحساب المراد ترحيله إلى Headquarters.</span><span class="sxs-lookup"><span data-stu-id="abff3-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="abff3-108">تفشل حركات Commerce في اجتياز التحقق من الصحة لأسباب متنوعة.</span><span class="sxs-lookup"><span data-stu-id="abff3-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="abff3-109">على سبيل المثال، قد يتسبب خطأ في كود التكامل أو خطأ في تطبيق POS في الحصول على بيانات غير متناسقة، كما أن خطأ يقوم به المستخدم، مثل حذف منتج بعد مزامنته مع القناة أو إغلاق فترة مالية بدون ترحيل الحركات لهذه الفترة، قد يتسبب في الحصول على بيانات غير متناسقة.</span><span class="sxs-lookup"><span data-stu-id="abff3-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="abff3-110">بينما يتم وضع علامة على هذه الحركات واستبعادها من كشوف الحساب، بإمكان الحركات أن تؤدي إلى تعطيل عملية العميل اليومية المتعلقة بترحيل المبيعات اليومية إلى الماليات.</span><span class="sxs-lookup"><span data-stu-id="abff3-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="abff3-111">في Commerce، يمكنك تحرير حركات محددة والتي فشلت في اجتياز التحقق من الصحة مع الاحتفاظ بعمليات التدقيق في جميع التغييرات.</span><span class="sxs-lookup"><span data-stu-id="abff3-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="abff3-112">تحرير الحركات والتدقيق فيها</span><span class="sxs-lookup"><span data-stu-id="abff3-112">Edit and audit transactions</span></span>

<span data-ttu-id="abff3-113">في الإصدار 10.0.5 من Retail، تعتبر حركات الدفع نقدًا والاستلام فورًا مثلها مثل المبيعات والمرتجعات الحركات الوحيدة التي يمكن تحريرها.</span><span class="sxs-lookup"><span data-stu-id="abff3-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="abff3-114">أوامر العميل أو الأوامر عبر الإنترنت غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="abff3-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="abff3-115">في الإصدار 10.0.6 من Retail والإصدارات اللاحقة، يعتبر تحرير حركات إدارة النقدية مدعومًا أيضًا.</span><span class="sxs-lookup"><span data-stu-id="abff3-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="abff3-116">قم بتثبيت الوظيفة الإضافية Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="abff3-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="abff3-117">انتقل إلى مساحة العمل **ماليات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="abff3-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="abff3-118">توفر لوحة **حالات فشل الحركات في اجتياز التحقق من الصحة** طريقة عرض تمت تصفيتها بشكل مسبق لنموذج الحركة التي فشلت في اجتياز قاعدة أو أكثر من قواعد التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="abff3-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="abff3-119">افتح النموذج.</span><span class="sxs-lookup"><span data-stu-id="abff3-119">Open the form.</span></span> <span data-ttu-id="abff3-120">انقر فوق السجل الذي فشل في اجتياز التحقق من الصحة، وانقر فوق **وظيفة Office الإضافية**، ثم انقر فوق **تحرير الحركة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="abff3-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="abff3-121">يفتح ملف Excel يتضمن تفاصيل الحركة المحددة، مع أوراق العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="abff3-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="abff3-122">البنود: تتضمن ورقة العمل هذه بنود الرأس والمنتج والبيانات المرتبطة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="abff3-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="abff3-123">المدفوعات: تتضمن ورقة العمل هذه تفاصيل بنود الدفع الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="abff3-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="abff3-124">الخصومات: تتضمن ورقة العمل هذه تفاصيل تتعلق بالخصومات الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="abff3-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="abff3-125">الضرائب: تتضمن ورقة العمل هذه تفاصيل تتعلق بالضرائب الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="abff3-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="abff3-126">التكاليف: تتضمن ورقة العمل هذه بيانات تتعلق بالتكاليف الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="abff3-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="abff3-127">في ملف Excel، يمكنك تعديل الحقول المناسبة ثم تحميل البيانات من جديد إلى Headquarters باستخدام وظيفة النشر الإضافية في Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="abff3-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="abff3-128">وستنعكس التغييرات في النظام عند نشرها.</span><span class="sxs-lookup"><span data-stu-id="abff3-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="abff3-129">أثناء عملية النشر، لا يتم إجراء أي عملية تحقق من الصحة على التغييرات التي يجريها المستخدمون.</span><span class="sxs-lookup"><span data-stu-id="abff3-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="abff3-130">يمكن عرض مسار التدقيق‏‎ الكامل للتغييرات عن طريق النقر فوق **عرض مسار التدقيق** في رأس **حركة البيع بالتجزئة** للتغييرات على مستوى الرأس وفي السجل والمقطع المناسبين في صفحة الحركة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="abff3-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="abff3-131">على سبيل المثال، ستكون جميع التغييرات ذات الصلة ببنود المبيعات مرئية في صفحة **حركات المبيعات‬**، وستكون التغييرات ذات الصلة بالمدفوعات مرئية في صفحة **حركات الدفع** وغير ذلك. تفاصيل التدقيق التي يتم الاحتفاظ بها للتغييرات هي على الشكل التالي.</span><span class="sxs-lookup"><span data-stu-id="abff3-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="abff3-132">تاريخ ووقت التعديل</span><span class="sxs-lookup"><span data-stu-id="abff3-132">Modified date and time</span></span>
   - <span data-ttu-id="abff3-133">الحقل</span><span class="sxs-lookup"><span data-stu-id="abff3-133">Field</span></span> 
   - <span data-ttu-id="abff3-134">قيمة قديمة</span><span class="sxs-lookup"><span data-stu-id="abff3-134">Old value</span></span>
   - <span data-ttu-id="abff3-135">قيمة جديدة</span><span class="sxs-lookup"><span data-stu-id="abff3-135">New value</span></span>
   - <span data-ttu-id="abff3-136">تعديل بواسطة</span><span class="sxs-lookup"><span data-stu-id="abff3-136">Modified by</span></span>

6. <span data-ttu-id="abff3-137">بعد اجراء التغييرات ونشرها، يمكنك تشغيل خيار **التحقق من صحة حركات المتجر‬** مرة أخرى للتأكد من أن التغييرات التي قمت بها متناسقة وصالحة.</span><span class="sxs-lookup"><span data-stu-id="abff3-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="abff3-138">يمكنك تحرير فقط الحركات التي فشلت في اجتياز التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="abff3-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="abff3-139">إذا أردت تحرير الحركات التي اجتازت عملية التحقق من الصحة، يمكنك تغيير حالة التحقق من الصحة للحركة التي تريد تغييرها إلى **خطأ** أو **بلا** وستتمكن عندئذٍ من تحريرها.</span><span class="sxs-lookup"><span data-stu-id="abff3-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="abff3-140">تحرير مجمع‬ للحركات</span><span class="sxs-lookup"><span data-stu-id="abff3-140">Bulk edit transactions</span></span>

<span data-ttu-id="abff3-141">في الإصدار 10.0.6 من Retail أو إصدار أحدث، يمكن إجراء تحرير مجمع للحركات على مستوى كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="abff3-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="abff3-142">استخدم وظيفة Excel الإضافية لفتح كشف حساب يتضمن الحركات التي تريد تعديلها باستخدام الخطوات من 1 إلى 3 أعلاه.</span><span class="sxs-lookup"><span data-stu-id="abff3-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="abff3-143">حدد أحد الخيارات أدناه.</span><span class="sxs-lookup"><span data-stu-id="abff3-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="abff3-144">**تحرير حركات الدفع نقدًا والاستلام فورًا‬**.</span><span class="sxs-lookup"><span data-stu-id="abff3-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="abff3-145">يسمح لك هذا الخيار بتحرير كافة حركات الدفع نقدًا والاستلام فورًا المضمنة في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="abff3-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="abff3-146">تتوفر أوراق عمل Excel التالية.</span><span class="sxs-lookup"><span data-stu-id="abff3-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="abff3-147">**الحركة**: تتضمن ورقة العمل هذه جميع المعلومات على مستوى الرأس الخاصة بحركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="abff3-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="abff3-148">**حركة المبيعات**: تتضمن ورقة العمل هذه جميع المعلومات على مستوى البنود الخاصة بحركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="abff3-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="abff3-149">**حركات الدفع‬**: تتضمن ورقة العمل هذه جميع معلومات بنود الدفع‬ لحركات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="abff3-150">**حركات الخصم‬‬**: تتضمن ورقة العمل هذه جميع معلومات بنود الخصم لحركات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="abff3-151">**حركة الضريبة‬**: تتضمن ورقة العمل هذه جميع معلومات بنود الضرائب الخاصة بحركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="abff3-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="abff3-152">**حركات التكلفة‬**: تتضمن ورقة العمل هذه جميع معلومات بنود التكاليف لحركات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="abff3-153">**تحرير حركات إدارة النقد**.</span><span class="sxs-lookup"><span data-stu-id="abff3-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="abff3-154">يسمح لك هذا الخيار بتحرير كافة حركات إدارة النقد المضمنة في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="abff3-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="abff3-155">تتوفر أوراق عمل Excel التالية.</span><span class="sxs-lookup"><span data-stu-id="abff3-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="abff3-156">**الحركة**: تتضمن ورقة العمل هذه جميع المعلومات على مستوى الرأس الخاصة بحركات إدارة النقد.</span><span class="sxs-lookup"><span data-stu-id="abff3-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="abff3-157">**حركات طريقة الدفع البنكية‬**: تتضمن ورقة العمل هذه تفاصيل جميع حركات الإيداع البنكية‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="abff3-158">**حركات طريقة دفع الخزينة‬‬**: تتضمن ورقة العمل هذه تفاصيل جميع حركات الإيداع في الخزينة.</span><span class="sxs-lookup"><span data-stu-id="abff3-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="abff3-159">**إقرار الدفع‬‬**: تتضمن ورقة العمل هذه تفاصيل جميع حركات إقرار الدفع‬‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="abff3-160">**حركات الإيرادات/المصروفات‬**: تتضمن ورقة العمل هذه تفاصيل جميع بنود حركة حركات الإيرادات/المصروفات‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="abff3-161">**حركات الدفع**: تتضمن ورقة العمل هذه جميع المعلومات ذات الصلة بالدفع لعملية **دفع الفاتورة‬** بالإضافة إلى حركة الإيرادات/المصروفات‬.</span><span class="sxs-lookup"><span data-stu-id="abff3-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="abff3-162">لا يتم تنفيذ عمليات التحقق من الصحة عند نشر الحركات التي تم إجراء تحرير مجمع لها.</span><span class="sxs-lookup"><span data-stu-id="abff3-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="abff3-163">يجب أن تتأكد من دقة جميع عمليات التحرير ومن المحافظة على دقة البيانات عبر أوراق العمل.</span><span class="sxs-lookup"><span data-stu-id="abff3-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="abff3-164">على سبيل المثال، إذا أردت تغيير تاريخ الحركة لإدارة السيناريوهات حيث تم إقفال الفترة المالية أو فترة المخزون للحركات المفتوحة، فعليك تغيير التاريخ على جميع أوراق عمل Excel التي تتضمن عمود **تاريخ العمل**.</span><span class="sxs-lookup"><span data-stu-id="abff3-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="abff3-165">للتحقق من صحة الحركات بعد تحريرها، يمكنك استخدام **إعادة التحقق من صحة الحركات** في صفحة **كشوف الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="abff3-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
