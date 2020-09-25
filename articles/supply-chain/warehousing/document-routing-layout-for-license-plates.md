---
title: تخطيط توجيه المستند لتسميات لوحات الترخيص
description: يوضح هذا الموضوع كيفية استخدام أساليب التنسيق لطباعة القيم على التسميات.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 9af077022ab0759534d2c1da5f39997712e6a354
ms.sourcegitcommit: 965fa733be068dc37f482d02ebbcd77f2c3d0a45
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763445"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="93f44-103">تخطيط توجيه المستند لتسميات لوحات الترخيص</span><span class="sxs-lookup"><span data-stu-id="93f44-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93f44-104">يحدد تخطيط توجيه المستندات تخطيط تسميات لوحات الترخيص والبيانات التي تتم طباعتها عليها.</span><span class="sxs-lookup"><span data-stu-id="93f44-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="93f44-105">يتم تكوين نقاط مشغل الطباعة عند إعداد عناصر قائمة الجهاز المحمول وقوالب العمل.</span><span class="sxs-lookup"><span data-stu-id="93f44-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="93f44-106">في السيناريو النموذجي، يقوم موظفو الاستلام في المستودع بطباعة تسميات لوحة الترخيص مباشرة بعد تسجيل محتويات ألواح التحميل التي تصل إلى منطقة الاستلام.</span><span class="sxs-lookup"><span data-stu-id="93f44-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="93f44-107">يتم تطبيق التسميات الفعلية على ألواح التحميل.</span><span class="sxs-lookup"><span data-stu-id="93f44-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="93f44-108">ويمكن استخدامها بعد ذلك للتحقق من الصحة كجزء من عملية التخزين التي تتبع وعمليات الانتقاء الخارجية والمستقبلية.</span><span class="sxs-lookup"><span data-stu-id="93f44-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="93f44-109">يمكنك طباعة التسميات المعقدة جدًا، شريطة أن يتمكن جهاز الطباعة من ترجمة النص الذي يتم إرساله إليه.</span><span class="sxs-lookup"><span data-stu-id="93f44-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="93f44-110">على سبيل المثال، قد يشبه تخطيط لغة برمجة Zebra الذي يحتوي على كود شريطي المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="93f44-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="93f44-111">كجزء من عملية طباعة التسمية، سيتم استبدال النص `$LicensePlateId$` الموجود في هذا المثال بقيمة بيانات.</span><span class="sxs-lookup"><span data-stu-id="93f44-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="93f44-112">لمشاهدة القيم التي ستتم طباعتها، انتقل إلى **إدارة المستودعات \> ‏‫الاستعلامات والتقارير‬ \> تسميات لوحات الترخيص**.</span><span class="sxs-lookup"><span data-stu-id="93f44-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="93f44-113">يمكن أن تساعدك العديد من أدوات إنشاء التسميات المتوفرة بشكل كبير على تنسيق النص الخاص بتخطيط التسمية.</span><span class="sxs-lookup"><span data-stu-id="93f44-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="93f44-114">وتدعم العديد من هذه الأدوات تنسيق `$FieldName$`.</span><span class="sxs-lookup"><span data-stu-id="93f44-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="93f44-115">بالإضافة إلى ذلك، يستخدم Microsoft Dynamics 365 Supply Chain Management منطق تنسيق خاص كجزء من تعيين الحقل لتخطيط توجيه المستند.</span><span class="sxs-lookup"><span data-stu-id="93f44-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="93f44-116">تنسيقات الأرقام المخصصة</span><span class="sxs-lookup"><span data-stu-id="93f44-116">Custom number formats</span></span>

<span data-ttu-id="93f44-117">يمكنك تخصيص تنسيق قيم الحقول الرقمية التي تتم طباعتها باستخدام الأكواد التي لها التنسيق التالي.</span><span class="sxs-lookup"><span data-stu-id="93f44-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="93f44-118">فيما يلي شرح هذا التنسيق:</span><span class="sxs-lookup"><span data-stu-id="93f44-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="93f44-119">`FieldName` هو اسم حقل البيانات (مثل **الكمية**).</span><span class="sxs-lookup"><span data-stu-id="93f44-119">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="93f44-120">`FormatString` يحدد كيفية طباعة البيانات.</span><span class="sxs-lookup"><span data-stu-id="93f44-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="93f44-121">تبين الأمثلة التالية كيف يمكنك تخصيص حقل كمية العمل (**الكمية**):</span><span class="sxs-lookup"><span data-stu-id="93f44-121">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="93f44-122">لإظهار أربعة خانات دائمًا (باستخدام الأصفار كعناصر نائبة)، استخدم `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="93f44-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="93f44-123">على سبيل المثال، إذا كانت الكمية 10، فسوف تُظهر التسمية "0010".</span><span class="sxs-lookup"><span data-stu-id="93f44-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="93f44-124">لإظهار منزلتين عشريتين دائمًا، استخدم `$Qty:0.00$`</span><span class="sxs-lookup"><span data-stu-id="93f44-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="93f44-125">على سبيل المثال، إذا كانت الكمية 10، فسوف تُظهر التسمية "10.00".</span><span class="sxs-lookup"><span data-stu-id="93f44-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="93f44-126">للحصول على قائمة كاملة بالسلاسل المتوفرة لتنسيق الأرقام، راجع [سلاسل التنسيق الرقمي المخصصة](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="93f44-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="93f44-127">تنسيقات السلاسل المخصصة</span><span class="sxs-lookup"><span data-stu-id="93f44-127">Custom string formats</span></span>

<span data-ttu-id="93f44-128">يمكنك إزالة الأحرف الأولي من سلسلة باستخدام الحقل التالي وكود التنسيق التالي.</span><span class="sxs-lookup"><span data-stu-id="93f44-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="93f44-129">هنا، يُعيّن `#` عدد الأحرف التي سيتم تخطيها.</span><span class="sxs-lookup"><span data-stu-id="93f44-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="93f44-130">على سبيل المثال، لطباعة رقم لوحة الترخيص التسلسلي لكود حاوية الشحن (SSCC) الذي لا يتضمن الحرفين الأولين، استخدم `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="93f44-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="93f44-131">في هذه الحالة، ستتم طباعة رقم لوح الترخيص 0011111111111222221 بالشكل "11111111111222221".</span><span class="sxs-lookup"><span data-stu-id="93f44-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="93f44-132">تنسيقات التاريخ/الوقت المخصصة</span><span class="sxs-lookup"><span data-stu-id="93f44-132">Custom date/time formats</span></span>

<span data-ttu-id="93f44-133">يُظهر المثال التالي كيف يمكنك التحكم في التنسيق المستخدم لطباعة التواريخ.</span><span class="sxs-lookup"><span data-stu-id="93f44-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="93f44-134">في هذا المثال، ستتم طباعة التاريخ 30 أبريل 2020 بالشكل "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="93f44-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="93f44-135">للحصول على قائمة كاملة بتنسيقات التاريخ/الوقت، راجع [سلاسل تنسيق الوقت والتاريخ المخصصة](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="93f44-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="93f44-136">طباعة سطور منفردة من بيانات متعددة السطور</span><span class="sxs-lookup"><span data-stu-id="93f44-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="93f44-137">إذا كان حقل البيانات يحتوي على أسطر متعددة (أي أسطر مفصولة بفواصل الأسطر)، فإنه يمكن طباعة سطر واحد باستخدام التنسيق التالي.</span><span class="sxs-lookup"><span data-stu-id="93f44-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="93f44-138">هنا، `#` هو رقم السطر الذي تريد طباعته.</span><span class="sxs-lookup"><span data-stu-id="93f44-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="93f44-139">(استخدم القيمة 1 للسطر الأول.)</span><span class="sxs-lookup"><span data-stu-id="93f44-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="93f44-140">على سبيل المثال، يحتوي النظام لديك على حقل `AdditionalAddress` الذي يقوم بتخزين العنوان متعدد الأسطر التالي:</span><span class="sxs-lookup"><span data-stu-id="93f44-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="93f44-141">.Contoso Inc</span><span class="sxs-lookup"><span data-stu-id="93f44-141">Contoso Inc.</span></span>  
<span data-ttu-id="93f44-142">123 اسم الشارع</span><span class="sxs-lookup"><span data-stu-id="93f44-142">123 Street Name</span></span>  
<span data-ttu-id="93f44-143">مدينة، ولاية</span><span class="sxs-lookup"><span data-stu-id="93f44-143">Some City, Some State</span></span>

<span data-ttu-id="93f44-144">يمكنك طباعة هذا العنوان، سطر واحد في كل مرة، باستخدام الرموز التالية.</span><span class="sxs-lookup"><span data-stu-id="93f44-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="93f44-145">الرمز</span><span class="sxs-lookup"><span data-stu-id="93f44-145">Code</span></span> | <span data-ttu-id="93f44-146">النص المطبوع</span><span class="sxs-lookup"><span data-stu-id="93f44-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="93f44-147">.Contoso Inc</span><span class="sxs-lookup"><span data-stu-id="93f44-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="93f44-148">123 اسم الشارع</span><span class="sxs-lookup"><span data-stu-id="93f44-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="93f44-149">مدينة، ولاية</span><span class="sxs-lookup"><span data-stu-id="93f44-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="93f44-150">طباعة وتنسيق من أسلوب عرض</span><span class="sxs-lookup"><span data-stu-id="93f44-150">Print and format from a display method</span></span>

<span data-ttu-id="93f44-151">يمكنك الطباعة من أسلوب عرض باستخدام التنسيق التالي.</span><span class="sxs-lookup"><span data-stu-id="93f44-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="93f44-152">يمكنك جمع هذا التنسيق مع أنواع أخرى تم وصفها سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="93f44-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="93f44-153">على سبيل المثال، لديك أسلوب عرض يسمى `DisplayListOfItemsNumbers()`، وتريد طباعة رقم العنصر الأول لهذا الأسلوب.</span><span class="sxs-lookup"><span data-stu-id="93f44-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="93f44-154">في هذه الحالة، يمكنك استخدام الرمز التالي.</span><span class="sxs-lookup"><span data-stu-id="93f44-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="93f44-155">مزيد من المعلومات حول كيفية طباعة التسميات</span><span class="sxs-lookup"><span data-stu-id="93f44-155">More information about how to print labels</span></span>

<span data-ttu-id="93f44-156">لمزيد من المعلومات حول كيفية إعداد التسميات وطباعتها، راجع [تمكين طباعة تسمية لوح الترخيص](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="93f44-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
