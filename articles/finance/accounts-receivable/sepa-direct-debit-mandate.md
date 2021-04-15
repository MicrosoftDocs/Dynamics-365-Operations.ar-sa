---
title: إعداد تفويض الخصم المباشر عن طريق سيبا‬
description: يتيح الخصم المباشر لمنطقة دفع يورو واحدة (SEPA) جمع أموال من الحساب البنكي للعميل، شريطة منح أمر رسمي مُوقَع من العميل إلى الدائن.
author: ShivamPandey-msft
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb167798a1c721d9f0e81f5e33e2989259037e9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817187"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="ac0c3-103">إعداد تفويض الخصم المباشر عن طريق سيبا‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac0c3-104">يتيح الخصم المباشر لمنطقة دفع يورو واحدة (SEPA) جمع أموال من الحساب البنكي للعميل، شريطة منح أمر رسمي مُوقَع من العميل إلى الدائن.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="ac0c3-105">ويوقع العميل أمرًا رسميًا يأذن فيه للدائن بجمع الدفع ويوجه بنك العميل لدفع التحصيل.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="ac0c3-106">تم تنظيم هذا الموضوع لعرض عملية إعداد الأوامر الرسمية لخصم سيبا المباشر.‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac0c3-107">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ac0c3-107">Prerequisites</span></span>
<span data-ttu-id="ac0c3-108">يعرض الجدول التالي المتطلبات الأساسية التي يجب أن تكون موجودة قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="ac0c3-109">‏‏الفئة</span><span class="sxs-lookup"><span data-stu-id="ac0c3-109">Category</span></span>       | <span data-ttu-id="ac0c3-110">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="ac0c3-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0c3-111">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="ac0c3-111">Country/region</span></span> | <span data-ttu-id="ac0c3-112">يجب أن يكون العنوان الرئيسي للكيان القانوني في البلدان/المناطق التالية: النمسا، أو بلجيكا، أو ألمانيا، أو إسبانيا، أو فرنسا، أو إيطاليا، أو هولندا.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="ac0c3-113">‏‫إعداد تسلسل رقمي للأوامر الرسمية للخصم المباشر‬   ‏‫يجب أن يكون لكل أمر رسمي لخصم مباشر رقم فريد.‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="ac0c3-114">استخدم صفحة **المسلسلات الرقمية** لإنشاء تسلسل رقمي للأوامر الرسمية للخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="ac0c3-115">سيتم استخدام هذا المعرف لتعيين التسلسل الرقمي نظام الأمر الرسمي للخصم المباشر في صفحة **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="ac0c3-116">‏‫إعداد معلمات حسابات مدينة ‏‫للأوامر الرسمية للخصم المباشر‬    ‏‫استخدم صفحة **معلمات الحسابات المدينة‬‏‫** لإعداد معلمات للأوامر الرسمية للخصم المباشر.‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="ac0c3-117">‏‫ولإعداد المعلمات، في علامة التبويب **الخصم المباشر**، قم بتغيير المعلمات الافتراضية كما تريد.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="ac0c3-118">وفي الخطوة التالية، في علامة التبويب **‬‏‫المسلسلات الرقمية**‬‏‫، قم بتحديث **معرف الأمر الرسمي للخصم المباشر** باستخدام المسلسل الرقمي الذي تقوم بإعداده مسبقاً.‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="ac0c3-119">‏‫إعداد طريقة دفع للأوامر الرسمية الخصم المباشر‬    ‏‫يجب إعداد طريقة دفع للأوامر الرسمية للخصم المباشر.‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="ac0c3-120">يمكنك استخدام طريقة الدفع هذه للاستعلام عن الفواتير لإنشاء مدفوعات الدائن المباشرة لها.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="ac0c3-121">واستخدم صفحة **طرق الدفع** لإعداد طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="ac0c3-122">ولإعداد طريقة الدفع للأوامر الرسمية للخصم المباشر، يجب عليك اتباع هذه الخطوات الإضافية لطريقة الدفع:</span><span class="sxs-lookup"><span data-stu-id="ac0c3-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="ac0c3-123">في حقل **نوع الدفع**، حدد **الدفع الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="ac0c3-124">اختياري: إذا كنت تتوقع كل من العملاء أن يكون لديهم عدة أوامر رسمية، في الحقل **الفترة‬**، حدد **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="ac0c3-125">ويتم إنشاء دفعة منفصلة لكل فاتورة، وستستخدم كل دفعة الأمر الرسمي المحدد للفاتورة.‬</span><span class="sxs-lookup"><span data-stu-id="ac0c3-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="ac0c3-126">وحدد خيار **الأمر الرسمي مطلوب** لإنشاء المدفوعات باستخدام الأوامر الرسمية للخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="ac0c3-127">يتوفر خيار **الأمر الرسمي مطلوب** فقط إذا قمت بتحديد **الدفع الإلكتروني** في حقل **نوع الدفع**.</span><span class="sxs-lookup"><span data-stu-id="ac0c3-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="ac0c3-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ac0c3-128">Additional resources</span></span>

[<span data-ttu-id="ac0c3-129">نظرة عامة على دين سيبا المباشر</span><span class="sxs-lookup"><span data-stu-id="ac0c3-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="ac0c3-130">إنشاء تفويض خصم مباشر لعميل</span><span class="sxs-lookup"><span data-stu-id="ac0c3-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]