---
title: وظيفة QRCODE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني QRCODE (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916742"
---
# <span data-ttu-id="cf076-103"><a name="QRCODE">وظيفة QRCODE ER</a></span><span class="sxs-lookup"><span data-stu-id="cf076-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf076-104">تقوم الوظيفة `QRCODE` بإرجاع قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR)  للسلسلة المُحددة بالتنسيق الثنائي. </span><span class="sxs-lookup"><span data-stu-id="cf076-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf076-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="cf076-105">Syntax</span></span>

```
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="cf076-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="cf076-106">Arguments</span></span>

<span data-ttu-id="cf076-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="cf076-107">`text`: *String*</span></span>

<span data-ttu-id="cf076-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="cf076-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="cf076-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="cf076-109">Return values</span></span>

<span data-ttu-id="cf076-110">*الحاوية*</span><span class="sxs-lookup"><span data-stu-id="cf076-110">*Container*</span></span>

<span data-ttu-id="cf076-111">الدفق الثنائي الناتج.</span><span class="sxs-lookup"><span data-stu-id="cf076-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="cf076-112">مثال</span><span class="sxs-lookup"><span data-stu-id="cf076-112">Example</span></span>

<span data-ttu-id="cf076-113">يُمكنك تكوين تنسيق التقارير الإلكترونية (ER) لإنشاء مستند صادر في تنسيق Microsoft Office (مصنفات Excel أو مستندات Word) باستخدام قالب مُعرف مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="cf076-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="cf076-114">قد يحتوي هذا القالب على كائن **صورة** (مصنف Excel) أو (مستند Word) **عنصر تحكم محتوى صورة** كعنصر نائب لصورة كود QR.</span><span class="sxs-lookup"><span data-stu-id="cf076-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="cf076-115">تحتاج إلى إضافة تنسيق ER مكون عنصر **خلية** والذي سوف يتم استخدامه لملء نائب العنصر هذا.</span><span class="sxs-lookup"><span data-stu-id="cf076-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="cf076-116">لتحديد المعلومات التي سوف يتم تخزينها في رمز QR، تحتاج إلى تعريف لربط عنصر **الخلية** هذا.</span><span class="sxs-lookup"><span data-stu-id="cf076-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="cf076-117">على سبيل المثال، يمكنك تكوين هذا الرابط على أنه يحتوي على التعبير التالي:</span><span class="sxs-lookup"><span data-stu-id="cf076-117">For example, you can configure such binding as containing the following expression:</span></span>

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="cf076-118">عندما تقوم بتشغيل تنسيق ER المُكون، فسوف يتم استخدام قيمة نص الحقل **LabelText** من مصدر البيانات **model.ListOfShelfLabels** لإنشاء صورة كود QR. </span><span class="sxs-lookup"><span data-stu-id="cf076-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="cf076-119">سوف تحل هذه الصورة محل عنصر نائب صورة كود QR في قالب المستند المستخدم لإنشاء مستند صادر.</span><span class="sxs-lookup"><span data-stu-id="cf076-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="cf076-120">عندما يتم مسح هذه الصورة من المستند الذي تم إنشاؤه ضوئيًا، تقوم بإرجاع النص الذي تم أخذه من حقل **LableText** من مصدر البيانات **model.ListOfShelfLabels**. </span><span class="sxs-lookup"><span data-stu-id="cf076-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="cf076-121">للمزيد من المعلومات، راجع [تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="cf076-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf076-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cf076-122">Additional resources</span></span>

[<span data-ttu-id="cf076-123">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="cf076-123">Text functions</span></span>](er-functions-category-text.md)