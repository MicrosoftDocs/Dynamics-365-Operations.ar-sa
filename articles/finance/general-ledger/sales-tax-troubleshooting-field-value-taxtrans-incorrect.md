---
title: قيمه الحقل غير صحيحة في TaxTrans
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء قيم الحقول غير الصحيحة وإصلاحها في TaxTrans.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947588"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="e0035-103">قيمه الحقل غير صحيحة في TaxTrans</span><span class="sxs-lookup"><span data-stu-id="e0035-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0035-104">إذا كانت قيمة حقل في **TaxTrans** غير صحيحة، استخدم المعلومات الواردة في هذا الموضوع لمحاولة حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="e0035-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="e0035-105">نظرة عامة على القيم</span><span class="sxs-lookup"><span data-stu-id="e0035-105">Overview of values</span></span>
<span data-ttu-id="e0035-106">تعرض القائمة التالية مدى تشابه مجموعات بيانات **TaxTrans**، و **TaxUncommitted**، و **TmpTaxWorkTrans**، ولكنها مختلفة في العمل.</span><span class="sxs-lookup"><span data-stu-id="e0035-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="e0035-107">**TaxTrans** هي النتيجة النهائية لحركة الضريبة المُرحلة التي استمرت في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="e0035-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="e0035-108">**TaxUncommitted** هي نتيجة الضريبة الوسيطة المحسوبة الموجودة في قاعدة البيانات (إن وجدت)، والتي سيتم استخدامها لاحقًا في النشر.</span><span class="sxs-lookup"><span data-stu-id="e0035-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="e0035-109">**TmpTaxWorkTrans** هي نتيجة الضريبة المحسوبة المؤقتة في الجدول الموجود في الذاكرة (نوع الجدول = InMemory).</span><span class="sxs-lookup"><span data-stu-id="e0035-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="e0035-110">إذا وجدت السبب الجذري لعمود **TaxTrans**، لقد وجدت أيضًا السبب الجذري لعمود **TaxUncommitted** أو **TmpTaxWorkTrans** غير الصحيح.</span><span class="sxs-lookup"><span data-stu-id="e0035-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="e0035-111">هذا بسبب نسخ الأعمدة الثلاثة من بعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="e0035-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="e0035-112">وعادة ما يتم أثناء حساب الضريبة إنشاء **TmpTaxWorkTrans**، ثم إنشاء **TaxUncommitted** إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="e0035-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="e0035-113">أثناء ترحيل الضريبة، تم إنشاء **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="e0035-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="e0035-114">إضافة نقاط التوقف</span><span class="sxs-lookup"><span data-stu-id="e0035-114">Add breakpoints</span></span>
<span data-ttu-id="e0035-115">لإضافة نقاط توقف، أكمل الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="e0035-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="e0035-116">أضف الامتدادات ونقاط التوقف في *insert()* و *update()* في الامتدادات كما هو موضح أدناه.</span><span class="sxs-lookup"><span data-stu-id="e0035-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="e0035-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="e0035-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="e0035-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="e0035-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="e0035-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="e0035-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="e0035-120">بدلاً من ذلك، يمكنك إضافة نقاط توقف مباشرة عند عدم تضمين **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="e0035-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="e0035-121">*TaxTrans.insert()*، *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="e0035-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="e0035-122">*TmpTaxWorkTrans.insert()*، *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="e0035-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="e0035-123">إعادة الإنتاج والتصحيح</span><span class="sxs-lookup"><span data-stu-id="e0035-123">Reproduce and debug</span></span>

<span data-ttu-id="e0035-124">بعد تعيين نقاط التوقف، يكون كل تغيير في استمرارية البيانات مرئيًا أثناء تصحيح الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="e0035-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="e0035-125">للعثور على السبب الجذري لعمود غير صحيح لـ **TaxTrans** أو **TaxUncommitted** أو **TmpTaxWorkTrans**، راجع ولاحظ العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="e0035-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="e0035-126">آخر نقطة توقف حيث يكون العمود صحيحًا.</span><span class="sxs-lookup"><span data-stu-id="e0035-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="e0035-127">نقطة الإيقاف الأولى حيث يكون العمود غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="e0035-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="e0035-128">ماذا يحدث بين هاتين النقطتين.</span><span class="sxs-lookup"><span data-stu-id="e0035-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="e0035-129">حدد ما إذا كان التخصيص موجودًا</span><span class="sxs-lookup"><span data-stu-id="e0035-129">Determine whether customization exists</span></span>
<span data-ttu-id="e0035-130">إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تتمكن من حل المشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="e0035-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="e0035-131">إذا لم يكن هناك تخصيص، فاتصل بدعم Microsoft للحصول على المساعدة.</span><span class="sxs-lookup"><span data-stu-id="e0035-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

