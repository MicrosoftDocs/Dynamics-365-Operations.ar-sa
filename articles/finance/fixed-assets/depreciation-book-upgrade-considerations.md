---
title: نظرة عامة حول ترقية دفتر الإهلاك
description: 'في الإصدارات السابقة، كان هناك مفهومان لتقييم الأصول الثابتة: نماذج القيم ودفاتر الإهلاك.'
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efa1b492fec085cc8bac5a786af4aaba854899e5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249645"
---
# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="ee44d-103">نظرة عامة على ترقية دفاتر الإهلاك</span><span class="sxs-lookup"><span data-stu-id="ee44d-103">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee44d-104">في الإصدارات السابقة، كان هناك مفهومان لتقييم الأصول الثابتة- نماذج القيم ودفاتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ee44d-104">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="ee44d-105">في Microsoft Dynamics 365 for Operations (1611)، تم دمج وظيفة نموذج القيم ووظيفة دفتر الإهلاك في مفهوم واحد يعرف باسم الدفتر.</span><span class="sxs-lookup"><span data-stu-id="ee44d-105">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="ee44d-106">يوفر هذا الموضوع بعض الأشياء الواجب مراعاتها عند إجراء الترقية.</span><span class="sxs-lookup"><span data-stu-id="ee44d-106">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="ee44d-107">ستقوم عملية الترقية بنقل إعدادك الموجود وكافة الحركات الموجودة إلى بنية الدفتر الجديد.</span><span class="sxs-lookup"><span data-stu-id="ee44d-107">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="ee44d-108">سوف تبقى نماذج القيم على حالها، كدفتر يتم ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="ee44d-108">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="ee44d-109">سيتم نقل دفاتر الإهلاك إلى دفتر حيث تم تعيين الخيار **الترحيل إلى دفتر الأستاذ العام** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="ee44d-109">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="ee44d-110">سيتم نقل أسماء دفاتر اليومية لدفتر الإهلاك إلى اسم دفتر يومية دفتر أستاذ عام تم فيه تعيين طبقة الترحيل إلى **بلا**.</span><span class="sxs-lookup"><span data-stu-id="ee44d-110">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="ee44d-111">سوف يتم نقل حركات دفتر الإهلاك إلى حركات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="ee44d-111">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="ee44d-112">قبل تشغيل عملية ترقية البيانات، يجب عليك فهم اثنين من الخيارات المتاحة لتحديث بنود دفتر يومية دفتر الإهلاك إلى إيصالات الحركة والتسلسل الرقمي الذي سيتم استخدامه لمسلسل الإيصال.</span><span class="sxs-lookup"><span data-stu-id="ee44d-112">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="ee44d-113">الخيار 1:  **التسلسل الرقمي المعرّف من قِبل النظام** - هذا هو الخيار الافتراضي لتحسين أداء الترقية.</span><span class="sxs-lookup"><span data-stu-id="ee44d-113">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="ee44d-114">لن تستخدم عملية الترقية إطار عمل التسلسلات الرقمية، ولكن بدلاً من ذلك ستقوم بتخصيص الإيصالات من خلال نهج يستند إلى المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ee44d-114">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="ee44d-115">بعد الترقية، سوف يتم إنشاء التسلسل الرقمي الجديد باستخدام **تعيين الرقم التالي** والتي تستند بشكل مناسب على الحركات التي تمت ترقيتها.</span><span class="sxs-lookup"><span data-stu-id="ee44d-115">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="ee44d-116">بشكل افتراضي، سوف يكون استخدام التسلسل الرقمي في تنسيق\#\#\#\#\#\#\#\#\# .</span><span class="sxs-lookup"><span data-stu-id="ee44d-116">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="ee44d-117">يوجد عدد قليل من المعلمات المتاحة لك لضبط التنسيق عند استخدام هذه الطريقة:</span><span class="sxs-lookup"><span data-stu-id="ee44d-117">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="ee44d-118">**كود التسلسل الرقمي** - وهو الكود المستخدم لتحديد التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-118">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="ee44d-119">لا يُمكن إيجاد كود التسلسل الرقمي هذا حيث سيتم إنشاؤه من خلال الترقية.</span><span class="sxs-lookup"><span data-stu-id="ee44d-119">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="ee44d-120">اسم الثابت: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="ee44d-120">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="ee44d-121">القيمة الافتراضية: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="ee44d-121">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="ee44d-122">**البادئة** – قيمة السلسلة الثابتة التي سيتم استخدامها كبادئة لأرقام الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="ee44d-122">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="ee44d-123">اسم الثابت: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="ee44d-123">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="ee44d-124">القيمة الافتراضية: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="ee44d-124">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="ee44d-125">**الطول الأبجدي الرقمي‬** – طول الجزء الأبجدي الرقمي‬ في التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-125">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="ee44d-126">اسم الثابت: **NumberSequenceDefaultParameterAlpanumericLength**</span><span class="sxs-lookup"><span data-stu-id="ee44d-126">Constant name: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span></span>
    -   <span data-ttu-id="ee44d-127">القيمة الافتراضية: 9</span><span class="sxs-lookup"><span data-stu-id="ee44d-127">Default value: 9</span></span>
-   <span data-ttu-id="ee44d-128">**رقم البدء** - الرقم الأول لاستخدامه في التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-128">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="ee44d-129">اسم الثابت: **NumberSequenceDefaultParameterStartNumber**</span><span class="sxs-lookup"><span data-stu-id="ee44d-129">Constant name: \*\*NumberSequenceDefaultParameterStartNumber  \*\*</span></span>
    -   <span data-ttu-id="ee44d-130">القيمة الافتراضية: 1</span><span class="sxs-lookup"><span data-stu-id="ee44d-130">Default value: 1</span></span>

<span data-ttu-id="ee44d-131">الخيار 2: **التسلسل الرقمي المعرّف من قبل مستخدم موجود** - يتيح هذا الخيار إمكانية تحديد التسلسل الرقمي لاستخدامه للترقية.</span><span class="sxs-lookup"><span data-stu-id="ee44d-131">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="ee44d-132">يمكنك استخدام هذا الخيار إذا احتجت إلى تكوين متقدم للتسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-132">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="ee44d-133">لاستخدام تسلسل رقمي، يجب عليك تعديل فئة ترقية ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans بالمعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="ee44d-133">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="ee44d-134">**كود التسلسل الرقمي** - كود التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-134">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="ee44d-135">اسم الثابت: \*\*NumberSequenceExistingCode \*\*</span><span class="sxs-lookup"><span data-stu-id="ee44d-135">Constant name: \*\*NumberSequenceExistingCode \*\*</span></span>
    -   <span data-ttu-id="ee44d-136">القيمة الافتراضية: لا قيمة افتراضية، يجب تحديثها إلى كود التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-136">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="ee44d-137">**التسلسل الرقمي المشترك** – قيمة منطقية لتحديد نطاق التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-137">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="ee44d-138">استخدم "true" للتسلسلات الرقمية المشتركة عبر كافة الشركات و "false" لنطاق خاص بالشركة.</span><span class="sxs-lookup"><span data-stu-id="ee44d-138">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="ee44d-139">عند استخدام "false"، يجب أن يكون التسلسل الرقمي بالاسم المحدد موجودًا في كل شركة تحتوي على حركات دفتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ee44d-139">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="ee44d-140">توجد التسلسلات الرقمية المشتركة في كل قسم يحتوي على حركات دفتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ee44d-140">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="ee44d-141">اسم الثابت: \*\*NumberSequenceExistingIsShared \*\*</span><span class="sxs-lookup"><span data-stu-id="ee44d-141">Constant name: \*\*NumberSequenceExistingIsShared \*\*</span></span>
    -   <span data-ttu-id="ee44d-142">القيمة الافتراضية: true</span><span class="sxs-lookup"><span data-stu-id="ee44d-142">Default value: true</span></span>

<span data-ttu-id="ee44d-143">توجد المحددات في بداية الفئة ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span><span class="sxs-lookup"><span data-stu-id="ee44d-143">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="ee44d-144">*// تحديد نهج مفضل لتوزيع الإيصالات* 
 *// صحيح,إذا أردت استخدام كود تسلسل رقمي موجود* 
 *// خطأ,إذا كنت تخطط لاستخدام التسلسل الرقمي المُعرّف من قبل النظام (افتراضي)* const boolean NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="ee44d-144">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="ee44d-145">*//إذا كنت تستخدم نهج التسلسل الرقمي المُعرف من قبل النظام، فعيّن محددات للتسلسل الرقمي..*
 *// سيتم إنشاء تسلسل رقمي جديد مع هذه المحددات.*</span><span class="sxs-lookup"><span data-stu-id="ee44d-145">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="ee44d-146">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="ee44d-146">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="ee44d-147">*//إذا كنت تستخدم نهج التسلسل الرقمي الموجود، فحدد كود التسلسل الرقمي الموجود.* 
 *//سينتقل توزيع الإيصالات من صف إلى آخر للتسلسلات الرقمية الموجودة.*</span><span class="sxs-lookup"><span data-stu-id="ee44d-147">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="ee44d-148">const str NumberSequenceExistingCode = ''; *// حدد نطاق رمز التسلسل الرقمي الموجود* 
 *// صحيح, إذا كان التسلسل الرقمي المحدد مشتركًأ* 
 *// خطأ, إذا كان التسلسل الرقمي المحدد حسب الشركة* 
 *// سيتم استخدام التسلسل الرقمي الافتراضي المُعرّف من قبل النظام إذا لم يتم العثور على كود تسلسل رقمي مع النطاق المحدد.*</span><span class="sxs-lookup"><span data-stu-id="ee44d-148">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="ee44d-149">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="ee44d-149">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="ee44d-150">إعادة بناء المشروع الذي يحتوي على الفئة بعد تعديل الثوابت.</span><span class="sxs-lookup"><span data-stu-id="ee44d-150">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="ee44d-151">عند استخدام نهج التسلسل الرقمي المُنشأ بواسطة النظام (الخيار 1)، سوف تستخدم عملية الترقية المعالجة المستندة إلى مجموعة لتوزيع أرقام الإيصالات كما هو محدد في محددات البرنامج النصي للترقية.</span><span class="sxs-lookup"><span data-stu-id="ee44d-151">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="ee44d-152">وستقوم أيضًا بإنشاء تسلسل رقمي جديد باستخدام المحددات المعينة بعد التوزيع.</span><span class="sxs-lookup"><span data-stu-id="ee44d-152">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="ee44d-153">عند استخدام نهج التسلسل الرقمي المعرّف من قِبل المستخدم (الخيار 2)، سوف تقوم عملية الترقية بالتحقق مما إذا كان التسلسل الرقمي مع النطاق المحدد موجودًا في قاعدة البيانات لكل قسم وشركة مع حركات كتب الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="ee44d-153">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="ee44d-154">إذا كان موجودًا، فإن عملية الترقية ستستخدم معالجة كل صف بعد الآخر لتوزيع أرقام الإيصالات كما هو محدد بواسطة التسلسل الرقمي باستخدام إطار عمل التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="ee44d-154">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="ee44d-155">إذا لم يكن التسلسل الرقمي موجودًا مع النطاق المُحدد، فإن عملية الترقية سوف تستخدم نهج التسلسل الرقمي الافتراضي المُعرّف من قبل النظام لتوزيع أرقام الإيصالات، وسوف تنشأ تسلسل رقمي جديد مع المحددات الافتراضية المحددة بعد التوزيع.</span><span class="sxs-lookup"><span data-stu-id="ee44d-155">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="ee44d-156">باستخدام أي من النهجين، سيستخدم أيضًا البرنامج النصي للترقية بيانات التسلسل الرقمي لحقل **مسلسل الإيصال** على أسماء دفاتر يومية دفتر الأستاذ العام الجديد التي تم إنشاؤها لأسماء دفاتر يومية دفتر الإهلاك السابق.</span><span class="sxs-lookup"><span data-stu-id="ee44d-156">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>


