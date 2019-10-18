---
title: حساب ضريبة المبيعات على بنود دفتر اليومية العامة
description: يوضح هذا الموضوع كيفية حساب ضرائب المبيعات لأنواع مختلفة من الحسابات (المورد والعميل ودفتر الأستاذ والمشروع) في بنود دفتر اليومية العام.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 354076dbc14f34b83d1cd24f591874b9af856af1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186292"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="4ce1a-103">حساب ضريبة المبيعات على بنود دفتر اليومية العامة</span><span class="sxs-lookup"><span data-stu-id="4ce1a-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4ce1a-104">يوضح هذا الموضوع كيفية حساب ضرائب المبيعات لأنواع مختلفة من الحسابات (المورد والعميل ودفتر الأستاذ والمشروع) في بنود دفتر اليومية العام.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="4ce1a-105">يمكن تقسيم العملية إلى ثلاث خطوات:</span><span class="sxs-lookup"><span data-stu-id="4ce1a-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="4ce1a-106">حدد اتجاه ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="4ce1a-107">حدد مبلغ ضريبة المبيعات الذي سيتم تخزين جدول ضريبة مبيعات مؤقت له.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="4ce1a-108">حدد مبلغ ضريبة المبيعات والحساب في الإيصال.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="4ce1a-109">حدد اتجاه ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-109">Determine the sales tax direction</span></span>

<span data-ttu-id="4ce1a-110">تعتمد الطريقة التي يتم بها تحديد توجيه ضريبة المبيعات على نوع الحساب في الإيصال.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="4ce1a-111">يتم تحديد اتجاه ضريبة المبيعات بواسطة مجموعة من نوع الحساب وكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="4ce1a-112">فيما يلي تقسم الإمكانيات بشكل أكثر تفصيلا.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="4ce1a-113">نوع الحساب هو المشروع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-113">Account type is Project</span></span>

<span data-ttu-id="4ce1a-114">إذا كان الإيصال يحتوي على بند دفتر يومية يكون به نوع الحساب هو **المشروع**، فإن جميع بنود دفتر اليومية في الإيصال تطبق نفس اتجاه الضريبة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="4ce1a-115">يبين الرسم التوضيحي التالي القاعدة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-115">The following illustration shows the rule.</span></span> <span data-ttu-id="4ce1a-116">توضح النقاط التالية التوجيهات المحتملة للضريبة لحسابات المشروعات.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="4ce1a-117">•   إذا كان كود ضريبة المبيعات هو ضريبة المبيعات، فإن توجيه ضريبة المبيعات هو ضريبة الانتقاع.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="4ce1a-118">•   إذا كان كود ضريبة المبيعات هو ضريبة الإعفاء، فإن توجيه ضريبة المبيعات هو ‏‫مشتريات معفية من الضرائب‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="4ce1a-119">•   إذا كان كود ضريبة المبيعات هو ضريبة القيمة المضافة لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، فإن توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="4ce1a-120">•   إذا كان كود ضريبة المبيعات هو رسوم عكسية‬، فإن توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="4ce1a-121">وبخلاف ذلك، يكون توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة القبض‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="4ce1a-122">يوضح المخطط التالي القاعدة رسوميًا.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-122">The following diagram illustrates the rule graphically.</span></span>

![إمكانيات توجيه الضريبة لحسابات المشروعات](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="4ce1a-124">نوع الحساب هو المورد</span><span class="sxs-lookup"><span data-stu-id="4ce1a-124">Account type is Vendor</span></span>

<span data-ttu-id="4ce1a-125">إذا كان الإيصال يحتوي على بند دفتر يومية يكون به نوع الحساب هو **المورد**، فإن جميع بنود دفتر اليومية في الإيصال تطبق نفس اتجاه الضريبة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="4ce1a-126">توضح النقاط التالية التوجيهات المحتملة للضريبة لحسابات الموردين.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="4ce1a-127">•   إذا كان كود ضريبة المبيعات هو ضريبة الإعفاء، فإن توجيه ضريبة المبيعات هو ‏‫مشتريات معفية من الضرائب‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="4ce1a-128">•   إذا كان كود ضريبة المبيعات هو ضريبة القيمة المضافة لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، فإن توجيه ضريبة المبيعات هو ‏‫‏‫ضريبة المبيعات مستحقة القبض‬</span><span class="sxs-lookup"><span data-stu-id="4ce1a-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="4ce1a-129">•   إذا كان كود ضريبة المبيعات هو رسوم عكسية‬، فإن توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة القبض.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="4ce1a-130">وبخلاف ذلك، يكون توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="4ce1a-131">يوضح المخطط التالي القاعدة رسوميًا.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-131">The following diagram illustrates the rule graphically.</span></span>

![إمكانيات توجيه الضريبة لحسابات الموردين](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="4ce1a-133">نوع الحساب هو العميل</span><span class="sxs-lookup"><span data-stu-id="4ce1a-133">Account type is Customer</span></span>

<span data-ttu-id="4ce1a-134">إذا كان الإيصال يحتوي على بند دفتر يومية يكون به نوع الحساب هو **العميل**، فإن جميع بنود دفتر اليومية في الإيصال تطبق نفس اتجاه الضريبة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="4ce1a-135">توضح النقاط التالية التوجيهات المحتملة للضريبة لحسابات العملاء.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="4ce1a-136">•   إذا كان كود ضريبة المبيعات هو ضريبة المبيعات، فإن توجيه ضريبة المبيعات هو ضريبة الانتقاع.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="4ce1a-137">•   إذا كان كود ضريبة المبيعات هو ضريبة الإعفاء، فإن توجيه ضريبة المبيعات هو ‏‫مشتريات معفية من الضرائب‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="4ce1a-138">•   إذا كان كود ضريبة المبيعات هو ضريبة القيمة المضافة لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، فإن توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="4ce1a-139">•   إذا كان كود ضريبة المبيعات هو رسوم عكسية‬، فإن توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="4ce1a-140">وبخلاف ذلك، يكون توجيه ضريبة المبيعات هو ‏‫ضريبة المبيعات مستحقة القبض‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="4ce1a-141">يوضح المخطط التالي القاعدة رسوميًا.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-141">The following diagram illustrates the rule graphically.</span></span>

![إمكانيات توجيه الضريبة لحسابات العملاء](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="4ce1a-143">نوع حساب هو دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="4ce1a-143">Account type is Ledger</span></span>

<span data-ttu-id="4ce1a-144">يبين الرسم التوضيحي التالي القاعدة التي يتم تطبيقها عندما يكون للإيصال بنود دفتر يومية لا يكون فيها نوع الحساب غير **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="4ce1a-145">توضح النقاط التالية التوجيهات المحتملة للضريبة لحسابات دفترة الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="4ce1a-146">•   إذا كان كود ضريبة المبيعات هو ضريبة المبيعات، فإن توجيه ضريبة المبيعات هو ضريبة الانتقاع.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="4ce1a-147">•   إذا كان كود ضريبة المبيعات هو ضريبة الإعفاء، فإن توجيه ضريبة المبيعات هو ‏‫مشتريات معفية من الضرائب‬.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="4ce1a-148">أو، إذا كان مبلغ دفتر اليومية مدينًا (موجبًا)، فان توجيه ضريبة المبيعات هو ضريبة المبيعات مستحقه القبض؛ إذا كان مبلغ دفتر اليومية دائنًا (سالبًا)، فان توجيه ضريبة المبيعات هو ضريبة المبيعات مستحقه الدفع.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="4ce1a-149">يوضح المخطط التالي القاعدة رسوميًا.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-149">The following diagram illustrates the rule graphically.</span></span>

![إمكانيات توجيه الضريبة لحسابات دفترة الأستاذ](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="4ce1a-151">تجاوز اتجاه ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-151">Override the sales tax direction</span></span>

<span data-ttu-id="4ce1a-152">يمكنك تجاوز توجيه ضريبة المبيعات عندما يحتوي الإيصال على بنود يكون فيها نوع الحساب هو **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="4ce1a-153">انتقل إلى **دفترة الأستاذ العام \> ‏‫مخطط الحسابات‬ \> الحسابات \> الحسابات الرئيسية**، و حدد علامة التبويب السريعة‬ **‏‫تجاوزات الكيان القانوني‬**.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="4ce1a-154">تحديد مبلغ ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-154">Determine the sales tax amount</span></span>

<span data-ttu-id="4ce1a-155">يوضح هذا القسم كيفية حساب علامة المبلغ الخاص بضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-155">This section describes how the sales tax amount sign is calculated.</span></span>

![صفحة حركات ضرائب المبيعات](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="4ce1a-157">يعرض الجدول التالي القاعدة العامة لتحديد علامة مبالغ ضريبة المبيعات في جدول ضريبة المبيعات المؤقتة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="4ce1a-158">مبلغ بند دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4ce1a-158">Journal line amount</span></span> | <span data-ttu-id="4ce1a-159">توجيه ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-159">Sales tax direction</span></span>  | <span data-ttu-id="4ce1a-160">علامة مبلغ ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="4ce1a-161">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-161">Positive</span></span>            | <span data-ttu-id="4ce1a-162">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-162">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-163">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-163">Positive</span></span>              |
| <span data-ttu-id="4ce1a-164">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-164">Positive</span></span>            | <span data-ttu-id="4ce1a-165">ضريبة المبيعات مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-165">Sales Tax Payable</span></span>    | <span data-ttu-id="4ce1a-166">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-166">Negative</span></span>              |
| <span data-ttu-id="4ce1a-167">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-167">Negative</span></span>            | <span data-ttu-id="4ce1a-168">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-168">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-169">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-169">Negative</span></span>              |
| <span data-ttu-id="4ce1a-170">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-170">Negative</span></span>            | <span data-ttu-id="4ce1a-171">ضريبة المبيعات مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-171">Sales Tax Payable</span></span>    | <span data-ttu-id="4ce1a-172">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-172">Positive</span></span>              |

<span data-ttu-id="4ce1a-173">ثمة قاعدة خاصة للإيصالات تحتوي فقط على بنود **المشروع** أو **دفتر الأستاذ**، حيث يتم تحديد مجموعة ضريبة مبيعات أو مجموعة ضريبة مبيعات صنف في بند **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="4ce1a-174">يتم التحكم في هذه القاعدة من خلال تمكين ميزة حساب ضريبة المبيعات المستقلة لدفاتر اليومية العامة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="4ce1a-175">عند إيقاف تشغيل هذه الميزة، فإن مبلغ الضريبة لبند **دفتر الأستاذ** يستخدم توجيه ‏‫مدين/دائن لبند **المشروع**.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="4ce1a-176">عند تشغيل هذه الميزة، فإن مبلغ الضريبة لبند **دفتر الأستاذ** يستخدم توجيه ‏‫مدين/دائن الخاص به.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="4ce1a-177">تُظهر الجداول التالية القاعدة لكل سيناريو.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="4ce1a-178">**القاعد عند تشغيل الميزة**</span><span class="sxs-lookup"><span data-stu-id="4ce1a-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="4ce1a-179">مبلغ بند دفتر اليومية للمشروع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-179">Journal line amount of project</span></span> | <span data-ttu-id="4ce1a-180">توجيه ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-180">Sales tax direction</span></span>  | <span data-ttu-id="4ce1a-181">علامة مبلغ ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="4ce1a-182">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-182">Positive</span></span>                       | <span data-ttu-id="4ce1a-183">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-183">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-184">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-184">Positive</span></span>              |
| <span data-ttu-id="4ce1a-185">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-185">Negative</span></span>                       | <span data-ttu-id="4ce1a-186">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-186">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-187">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-187">Negative</span></span>              |

<span data-ttu-id="4ce1a-188">**القاعد عند إيقاف تشغيل الميزة**</span><span class="sxs-lookup"><span data-stu-id="4ce1a-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="4ce1a-189">مبلغ بند دفتر اليومية لدفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4ce1a-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="4ce1a-190">توجيه ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-190">Sales tax direction</span></span>  | <span data-ttu-id="4ce1a-191">علامة مبلغ ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="4ce1a-192">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-192">Positive</span></span>                       | <span data-ttu-id="4ce1a-193">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-193">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-194">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-194">Positive</span></span>              |
| <span data-ttu-id="4ce1a-195">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-195">Negative</span></span>                       | <span data-ttu-id="4ce1a-196">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-196">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-197">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="4ce1a-198">حدد مبلغ ضريبة المبيعات والحساب في الإيصال</span><span class="sxs-lookup"><span data-stu-id="4ce1a-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="4ce1a-199">عند قيامك بترحيل ضرائب المبيعات، يتم استرجاع الحساب الرئيسي من ملف تعريف مجموعه ترحيل دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="4ce1a-200">عندما تكون ضرائب المبيعات مستحقة القبض، يستخدم النظام حساب ضريبة المبيعات مستحقة القبض المحدد في ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="4ce1a-201">عندما تكون ضرائب المبيعات مستحقة الدفع، يستخدم النظام حساب ضريبة المبيعات مستحقة الدفع المحدد في ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="4ce1a-202">يوضح الجدول التالي القاعدة العامة.</span><span class="sxs-lookup"><span data-stu-id="4ce1a-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="4ce1a-203">توجيه ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-203">Sales tax direction</span></span>  | <span data-ttu-id="4ce1a-204">علامة مبلغ ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-204">Sales tax amount sign</span></span> | <span data-ttu-id="4ce1a-205">حساب ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="4ce1a-205">Sales tax account</span></span>      | <span data-ttu-id="4ce1a-206">مبلغ الإيصال</span><span class="sxs-lookup"><span data-stu-id="4ce1a-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="4ce1a-207">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-207">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-208">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-208">Positive</span></span>              | <span data-ttu-id="4ce1a-209">حسابات الضريبة مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-209">Tax Receivable Account</span></span> | <span data-ttu-id="4ce1a-210">موجب (مدين)</span><span class="sxs-lookup"><span data-stu-id="4ce1a-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="4ce1a-211">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-211">Sales Tax Receivable</span></span> | <span data-ttu-id="4ce1a-212">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-212">Negative</span></span>              | <span data-ttu-id="4ce1a-213">حسابات الضريبة مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="4ce1a-213">Tax Receivable Account</span></span> | <span data-ttu-id="4ce1a-214">سالب(دائن)</span><span class="sxs-lookup"><span data-stu-id="4ce1a-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="4ce1a-215">ضريبة المبيعات مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-215">Sales Tax Payable</span></span>    | <span data-ttu-id="4ce1a-216">موجب</span><span class="sxs-lookup"><span data-stu-id="4ce1a-216">Positive</span></span>              | <span data-ttu-id="4ce1a-217">حساب الضريبة مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-217">Tax Payable Account</span></span>    | <span data-ttu-id="4ce1a-218">سالب(دائن)</span><span class="sxs-lookup"><span data-stu-id="4ce1a-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="4ce1a-219">ضريبة المبيعات مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-219">Sales Tax Payable</span></span>    | <span data-ttu-id="4ce1a-220">سلبي</span><span class="sxs-lookup"><span data-stu-id="4ce1a-220">Negative</span></span>              | <span data-ttu-id="4ce1a-221">حساب الضريبة مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="4ce1a-221">Tax Payable Account</span></span>    | <span data-ttu-id="4ce1a-222">موجب (مدين)</span><span class="sxs-lookup"><span data-stu-id="4ce1a-222">Positive (Debit)</span></span>  |
