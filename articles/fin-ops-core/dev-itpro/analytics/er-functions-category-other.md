---
title: قائمة وظائف التقارير الإلكترونية في فئة خاصة بمجال الأعمال
description: يوفر هذا الموضوع معلومات حول الوظائف الخاصة بجهات الأعمال المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f7612e83d9f30281e2b1a783275365459e67a40
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686113"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a><span data-ttu-id="42cc3-103">قائمة وظائف التقارير الإلكترونية في فئة خاصة بمجال الأعمال</span><span class="sxs-lookup"><span data-stu-id="42cc3-103">List of ER functions in the business domain–specific category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42cc3-104">يمكن استخدام الوظائف الخاصة بمجال في التقارير الكترونيه (ER) لتنفيذ العمليات الحسابية وطلبات الوصول إلى البيانات الخاصة بتنفيذ Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="42cc3-104">Electronic reporting (ER) domain-specific functions can be used to perform calculations and data access requests that are specific to the implementation of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="42cc3-105">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="42cc3-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="42cc3-106">قائمة الوظائف المدعومة</span><span class="sxs-lookup"><span data-stu-id="42cc3-106">List of supported functions</span></span>

| <span data-ttu-id="42cc3-107">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="42cc3-107">Function</span></span>| <span data-ttu-id="42cc3-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="42cc3-108">Description</span></span> |
|---------|-------------|
| [<span data-ttu-id="42cc3-109">CH_Bank_Mod_10</span><span class="sxs-lookup"><span data-stu-id="42cc3-109">CH_Bank_Mod_10</span></span>](er-functions-other-chbankmode10.md) | <span data-ttu-id="42cc3-110">تُرجع هذه الوظيفة قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD10، بناءً على أرقام رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-110">This function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="42cc3-111">CN_GBT_AdditionalDimensionID</span><span class="sxs-lookup"><span data-stu-id="42cc3-111">CN_GBT_AdditionalDimensionID</span></span>](er-functions-other-cngbtadditionaldimensionid.md) | <span data-ttu-id="42cc3-112">تُرجع هذه الوظيفة قيمة *سلسلة* تمثل مُعرف بعد مالي واحد مأخوذ من السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-112">This function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="42cc3-113">تعرض السلسلة المُحددة كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-113">The specified string presents all dimensions as a comma-separated list of IDs.</span></span> |
| [<span data-ttu-id="42cc3-114">ConvertCurrency</span><span class="sxs-lookup"><span data-stu-id="42cc3-114">ConvertCurrency</span></span>](er-functions-other-convertcurrency.md) | <span data-ttu-id="42cc3-115">تُرجع هذه الوظيفة قيمة *حقيقية* تمثل نتيجة تحويل المبلغ المالي المحدد من العملة المصدر المحددة إلى العملة الهدف المحددة باستخدام إعدادات الشركة المُحددة في التاريخ المُحدد.</span><span class="sxs-lookup"><span data-stu-id="42cc3-115">This function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span> |
| [<span data-ttu-id="42cc3-116">CurCredRef</span><span class="sxs-lookup"><span data-stu-id="42cc3-116">CurCredRef</span></span>](er-functions-other-curcredref.md) | <span data-ttu-id="42cc3-117">تُرجع هذه الوظيفة قيمة *سلسلة* تُمثل مرجع دائن، بناءً على أرقام رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-117">This function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="42cc3-118">FA_Balance</span><span class="sxs-lookup"><span data-stu-id="42cc3-118">FA_Balance</span></span>](er-functions-other-fabalance.md) | <span data-ttu-id="42cc3-119">تُرجع هذه الوظيفة قيمة *حاوية (سجل)* تتكون من بيانات لرصيد الأصل الثابت لعنصر الأصل الثابت المُحدد وكود نموذج القيمة وسنة إعداد التقرير وتاريخ إعداد التقرير.</span><span class="sxs-lookup"><span data-stu-id="42cc3-119">This function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span> |
| [<span data-ttu-id="42cc3-120">FA_Sum</span><span class="sxs-lookup"><span data-stu-id="42cc3-120">FA_Sum</span></span>](er-functions-other-fasum.md) | <span data-ttu-id="42cc3-121">تُرجع هذه الوظيفة قيمة *حاوية (سجل)* تتكون من بيانات لمبالغ الأصول الثابتة لعنصر الأصل الثابت المُحدد وكود نموذج القيمة والفترات المرتبطة بالتواريخ.</span><span class="sxs-lookup"><span data-stu-id="42cc3-121">This function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span> |
| [<span data-ttu-id="42cc3-122">GetCurrentCompany</span><span class="sxs-lookup"><span data-stu-id="42cc3-122">GetCurrentCompany</span></span>](er-functions-other-getcurrentcompany.md) | <span data-ttu-id="42cc3-123">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل كود الكيان القانوني (الشركة) الذي يقوم مستخدم بتسجيل الدخول فيه حاليًا.</span><span class="sxs-lookup"><span data-stu-id="42cc3-123">This function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span> |
| [<span data-ttu-id="42cc3-124">ISOCredRef</span><span class="sxs-lookup"><span data-stu-id="42cc3-124">ISOCredRef</span></span>](er-functions-other-isocredref.md) | <span data-ttu-id="42cc3-125">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل مرجع دائن المنطقة العالمية للمواصفات (ISO)، استنادًا إلى الخامات الرقمية والرموز الأبجدية في رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-125">This function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span> |
| [<span data-ttu-id="42cc3-126">IsValidCharacterISO7064</span><span class="sxs-lookup"><span data-stu-id="42cc3-126">IsValidCharacterISO7064</span></span>](er-functions-other-isvalidchariso7064.md) | <span data-ttu-id="42cc3-127">تُرجع هذه الوظيفة قيمة *منطقية* **TRUE** إذا كانت السلسلة المُحددة تمثل رقم حساب مصرفي دولي (IBAN) صالح.</span><span class="sxs-lookup"><span data-stu-id="42cc3-127">This function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="42cc3-128">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="42cc3-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="42cc3-129">Mod_97</span><span class="sxs-lookup"><span data-stu-id="42cc3-129">Mod_97</span></span>](er-functions-other-mod97.md) | <span data-ttu-id="42cc3-130">تُرجع هذه الوظيفة قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD97، بناءً على أرقام رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-130">This function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span> |
| [<span data-ttu-id="42cc3-131">NumSeqValue</span><span class="sxs-lookup"><span data-stu-id="42cc3-131">NumSeqValue</span></span>](er-functions-other-numseqvalue.md) | <span data-ttu-id="42cc3-132">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل القيمة الجديدة التي تم إنشاؤها للتسلسل الرقمي، استنادًا إلى التسلسل الرقمي المُحدد والنطاق ومُعرف النطاق.</span><span class="sxs-lookup"><span data-stu-id="42cc3-132">This function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="42cc3-133">يساوي مُعرف النطاق كود الشركة الذي يتم توفيره بواسطة السياق الذي يتم تشغيل تنسيق إعداد التقارير الإلكترونية ضمنه.</span><span class="sxs-lookup"><span data-stu-id="42cc3-133">The scope ID equals the company code that is supplied by the context that the ER format is run under.</span></span> |
| [<span data-ttu-id="42cc3-134">RoundAmount</span><span class="sxs-lookup"><span data-stu-id="42cc3-134">RoundAmount</span></span>](er-functions-other-roundamount.md) | <span data-ttu-id="42cc3-135">تُرجع هذه الوظيفة قيمة *حقيقة* تمثل نتيجة تقريب المبلغ المُحدد إلى الرقم المُحدد من منازل عشرية وفقًا لقاعدة التقريب المُحددة.</span><span class="sxs-lookup"><span data-stu-id="42cc3-135">This function returns a *Real* value that represents the result of rounding the specified amount to the specified number of decimal places according to the specified rounding rule.</span></span> |
| [<span data-ttu-id="42cc3-136">TableName2ID</span><span class="sxs-lookup"><span data-stu-id="42cc3-136">TableName2ID</span></span>](er-functions-other-tablename2id.md) | <span data-ttu-id="42cc3-137">تُرجع هذه الوظيفة تمثيل رقمي لمُعرف الجدول لاسم الجدول المُحدد كقيمة *عدد صحيح*.</span><span class="sxs-lookup"><span data-stu-id="42cc3-137">This function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="42cc3-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="42cc3-138">Additional resources</span></span>

[<span data-ttu-id="42cc3-139">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="42cc3-139">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="42cc3-140">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="42cc3-140">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="42cc3-141">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="42cc3-141">Electronic reporting formula language</span></span>](er-formula-language.md)
