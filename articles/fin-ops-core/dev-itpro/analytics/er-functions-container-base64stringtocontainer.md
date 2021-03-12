---
title: دالة Base64StringToContainer ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني Base64StringToContainer (ER).
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739053"
---
# <a name="base64stringtocontainer-er-function"></a>دالة Base64StringToContainer ER

[!include [banner](../includes/banner.md)]

تقوم `BASE64STRINGTOCONTAINER` [دالة](er-formula-language.md#functions) بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *[الحاوية](er-functions-category-container.md)*.

## <a name="syntax"></a>بناء الجملة

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>الوسائط

`input`: *السلسلة*

المسار الصالح لمصدر البيانات من نوع *السلسلة*.

## <a name="return-values"></a>إرجاع القيم

*الحاوية*

القيمة الثنائية الناتجة بتنسيق الكائن الثنائي الكبير (BLOB).

## <a name="usage-notes"></a>ملاحظات الاستخدام

تم طرح استثناء "المعلمة غير صالحه" إذا كانت السلسلة المدخلة لا توفر مجموعه عناوين Base64 صحيحه لأنظمه ترميز ثنائيه النص الثنائية.

## <a name="example"></a>مثال

أنت تحدد مصادر البيانات التالية في تعيين نموذج:

- مصدر بيانات الجذر **DocuTypeGroupEnum** لنوع *Dynamics 365 for Operations/قائمه التعداد* الذي يشير إلى تعداد التطبيق **DocuTypeGroup**
- مصدر بيانات **العميل** الجذر من النوع *Dynamics 365 for Operations/سجلات الجدول* الذي يُشير إلى جدول تطبيق **CustTable**.
- مصدر بيانات **\#الوسائط** لنوع *الحقل المحسوب* الذي تم تكوينه بالطريقة التالية:

    - تتم اضافته كمصدر بيانات فرعي لمصدر بيانات **العميل**.
    - ويتضمن التعبير `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`

- مصدر بيانات **\#MediaAsBase64String** لنوع *الحقل المحسوب* الذي تم تكوينه بالطريقة التالية:

    - تتم اضافته كمصدر بيانات فرعي لمصدر بيانات **العميل.'\#الوسائط'**.
    - ويتضمن التعبير `Customer.'#Media'.'getFileContentAsBase64String()'`

- مصدر بيانات **\#BlobFomBase64** لنوع *الحقل المحسوب* الذي تم تكوينه بالطريقة التالية:

    - تتم اضافته كمصدر بيانات فرعي لمصدر بيانات **العميل.'\#الوسائط'**.
    - ويتضمن التعبير `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`

في هذا المثال، **\#MediaAsBase64String** بترميز المحتوي الثنائي لمرفق الوسائط الحالي كنص يمثل مجموعه Base64 من أنظمه ترميز ثنائيه النص. ويقوم **\#BlobFomBase64** بفك ترميز سلسله Base64 وإرجاع قيمه ثنائيه في تنسيق BLOB.

![مصادر البيانات النموذجية في صفحة مصمم تعيين النموذج](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>الموارد الإضافية

[دالات الحاوية](er-functions-category-container.md)
