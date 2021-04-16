---
title: دالة Base64StringToContainer ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني Base64StringToContainer (ER).
author: NickSelin
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754364"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="600ca-103">دالة Base64StringToContainer ER</span><span class="sxs-lookup"><span data-stu-id="600ca-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="600ca-104">تقوم `BASE64STRINGTOCONTAINER` [دالة](er-formula-language.md#functions) بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *[الحاوية](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="600ca-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="600ca-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="600ca-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="600ca-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="600ca-106">Arguments</span></span>

<span data-ttu-id="600ca-107">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="600ca-107">`input`: *String*</span></span>

<span data-ttu-id="600ca-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="600ca-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="600ca-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="600ca-109">Return values</span></span>

<span data-ttu-id="600ca-110">*الحاوية*</span><span class="sxs-lookup"><span data-stu-id="600ca-110">*Container*</span></span>

<span data-ttu-id="600ca-111">القيمة الثنائية الناتجة بتنسيق الكائن الثنائي الكبير (BLOB).</span><span class="sxs-lookup"><span data-stu-id="600ca-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="600ca-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="600ca-112">Usage notes</span></span>

<span data-ttu-id="600ca-113">تم طرح استثناء "المعلمة غير صالحه" إذا كانت السلسلة المدخلة لا توفر مجموعه عناوين Base64 صحيحه لأنظمه ترميز ثنائيه النص الثنائية.</span><span class="sxs-lookup"><span data-stu-id="600ca-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="600ca-114">مثال</span><span class="sxs-lookup"><span data-stu-id="600ca-114">Example</span></span>

<span data-ttu-id="600ca-115">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="600ca-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="600ca-116">مصدر بيانات الجذر **DocuTypeGroupEnum** لنوع *Dynamics 365 for Operations/قائمه التعداد* الذي يشير إلى تعداد التطبيق **DocuTypeGroup**</span><span class="sxs-lookup"><span data-stu-id="600ca-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="600ca-117">مصدر بيانات **العميل** الجذر من النوع *Dynamics 365 for Operations/سجلات الجدول* الذي يُشير إلى جدول تطبيق **CustTable**.</span><span class="sxs-lookup"><span data-stu-id="600ca-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="600ca-118">مصدر بيانات **\#الوسائط** لنوع *الحقل المحسوب* الذي تم تكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="600ca-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="600ca-119">تتم اضافته كمصدر بيانات فرعي لمصدر بيانات **العميل**.</span><span class="sxs-lookup"><span data-stu-id="600ca-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="600ca-120">ويتضمن التعبير `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`</span><span class="sxs-lookup"><span data-stu-id="600ca-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="600ca-121">مصدر بيانات **\#MediaAsBase64String** لنوع *الحقل المحسوب* الذي تم تكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="600ca-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="600ca-122">تتم اضافته كمصدر بيانات فرعي لمصدر بيانات **العميل.'\#الوسائط'**.</span><span class="sxs-lookup"><span data-stu-id="600ca-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="600ca-123">ويتضمن التعبير `Customer.'#Media'.'getFileContentAsBase64String()'`</span><span class="sxs-lookup"><span data-stu-id="600ca-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="600ca-124">مصدر بيانات **\#BlobFomBase64** لنوع *الحقل المحسوب* الذي تم تكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="600ca-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="600ca-125">تتم اضافته كمصدر بيانات فرعي لمصدر بيانات **العميل.'\#الوسائط'**.</span><span class="sxs-lookup"><span data-stu-id="600ca-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="600ca-126">ويتضمن التعبير `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`</span><span class="sxs-lookup"><span data-stu-id="600ca-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="600ca-127">في هذا المثال، **\#MediaAsBase64String** بترميز المحتوي الثنائي لمرفق الوسائط الحالي كنص يمثل مجموعه Base64 من أنظمه ترميز ثنائيه النص.</span><span class="sxs-lookup"><span data-stu-id="600ca-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="600ca-128">ويقوم **\#BlobFomBase64** بفك ترميز سلسله Base64 وإرجاع قيمه ثنائيه في تنسيق BLOB.</span><span class="sxs-lookup"><span data-stu-id="600ca-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![مصادر البيانات النموذجية في صفحة مصمم تعيين النموذج](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="600ca-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="600ca-130">Additional resources</span></span>

[<span data-ttu-id="600ca-131">دالات الحاوية</span><span class="sxs-lookup"><span data-stu-id="600ca-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]