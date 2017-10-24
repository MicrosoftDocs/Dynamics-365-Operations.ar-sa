---
title: "إعداد أمر رسمي لخصم سيبا مباشر"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="e8378-102">إعداد أمر رسمي لخصم سيبا مباشر</span><span class="sxs-lookup"><span data-stu-id="e8378-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="e8378-103">يتيح الخصم المباشر لمنطقة دفع يورو واحدة (SEPA) جمع أموال من الحساب البنكي للعميل، شريطة منح أمر رسمي مُوقَع من العميل إلى الدائن.</span><span class="sxs-lookup"><span data-stu-id="e8378-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="e8378-104">ويوقع العميل أمرًا رسميًا يأذن فيه للدائن بجمع الدفع ويوجه بنك العميل لدفع التحصيل.</span><span class="sxs-lookup"><span data-stu-id="e8378-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="e8378-105">تم تنظيم هذا الموضوع لعرض عملية إعداد الأوامر الرسمية لخصم سيبا المباشر.‬</span><span class="sxs-lookup"><span data-stu-id="e8378-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8378-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="e8378-106">Prerequisites</span></span>
<span data-ttu-id="e8378-107">يعرض الجدول التالي المتطلبات الأساسية التي يجب أن تكون موجودة قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="e8378-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="e8378-108">‏‏الفئة</span><span class="sxs-lookup"><span data-stu-id="e8378-108">Category</span></span>       | <span data-ttu-id="e8378-109">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="e8378-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8378-110">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="e8378-110">Country/region</span></span> | <span data-ttu-id="e8378-111">يجب أن يكون العنوان الرئيسي للكيان القانوني في البلدان/المناطق التالية: النمسا، أو بلجيكا، أو ألمانيا، أو إسبانيا، أو فرنسا، أو إيطاليا، أو هولندا.</span><span class="sxs-lookup"><span data-stu-id="e8378-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="e8378-112">‏‫إعداد تسلسل رقمي للأوامر الرسمية للخصم المباشر‬   ‏‫يجب أن يكون لكل أمر رسمي لخصم مباشر رقم فريد.‬</span><span class="sxs-lookup"><span data-stu-id="e8378-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="e8378-113">استخدم صفحة **المسلسلات الرقمية** لإنشاء تسلسل رقمي للأوامر الرسمية للخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="e8378-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="e8378-114">سيتم استخدام هذا المعرف لتعيين التسلسل الرقمي نظام الأمر الرسمي للخصم المباشر في صفحة **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="e8378-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="e8378-115">‏‫إعداد معلمات حسابات مدينة ‏‫للأوامر الرسمية للخصم المباشر‬    ‏‫استخدم صفحة **معلمات الحسابات المدينة‬‏‫** لإعداد معلمات للأوامر الرسمية للخصم المباشر.‬</span><span class="sxs-lookup"><span data-stu-id="e8378-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="e8378-116">‏‫ولإعداد المعلمات، في علامة التبويب **الخصم المباشر**، قم بتغيير المعلمات الافتراضية كما تريد.</span><span class="sxs-lookup"><span data-stu-id="e8378-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="e8378-117">وفي الخطوة التالية، في علامة التبويب **‬‏‫المسلسلات الرقمية**‬‏‫، قم بتحديث **معرف الأمر الرسمي للخصم المباشر** باستخدام المسلسل الرقمي الذي تقوم بإعداده مسبقاً.‬</span><span class="sxs-lookup"><span data-stu-id="e8378-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="e8378-118">‏‫إعداد طريقة دفع للأوامر الرسمية الخصم المباشر‬    ‏‫يجب إعداد طريقة دفع للأوامر الرسمية للخصم المباشر.‬</span><span class="sxs-lookup"><span data-stu-id="e8378-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="e8378-119">يمكنك استخدام طريقة الدفع هذه للاستعلام عن الفواتير لإنشاء مدفوعات الدائن المباشرة لها.</span><span class="sxs-lookup"><span data-stu-id="e8378-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="e8378-120">واستخدم صفحة **طرق الدفع** لإعداد طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="e8378-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="e8378-121">ولإعداد طريقة الدفع للأوامر الرسمية للخصم المباشر، يجب عليك اتباع هذه الخطوات الإضافية لطريقة الدفع:</span><span class="sxs-lookup"><span data-stu-id="e8378-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="e8378-122">في حقل **نوع الدفع**، حدد **الدفع الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="e8378-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="e8378-123">اختياري: إذا كنت تتوقع كل من العملاء أن يكون لديهم عدة أوامر رسمية، في الحقل **الفترة‬**، حدد **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="e8378-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="e8378-124">ويتم إنشاء دفعة منفصلة لكل فاتورة، وستستخدم كل دفعة الأمر الرسمي المحدد للفاتورة.‬</span><span class="sxs-lookup"><span data-stu-id="e8378-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="e8378-125">وحدد خيار **الأمر الرسمي مطلوب** لإنشاء المدفوعات باستخدام الأوامر الرسمية للخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="e8378-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="e8378-126">يتوفر خيار **الأمر الرسمي مطلوب** فقط إذا قمت بتحديد **الدفع الإلكتروني** في حقل **نوع الدفع**.</span><span class="sxs-lookup"><span data-stu-id="e8378-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="e8378-127">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e8378-127">See Also</span></span>

[<span data-ttu-id="e8378-128">نظرة عامة على الخصم المباشر</span><span class="sxs-lookup"><span data-stu-id="e8378-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="e8378-129">إنشاء تفويض خصم مباشر لعميل</span><span class="sxs-lookup"><span data-stu-id="e8378-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


