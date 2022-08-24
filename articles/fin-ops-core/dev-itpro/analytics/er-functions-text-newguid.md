---
title: وظيفة NEWGUID ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية NEWGUID‏ (ER).
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274761"
---
# <a name="newguid-er-function"></a>وظيفة NEWGUID ER

[!include [banner](../includes/banner.md)]

`NEWGUID`تقوم الدالة بإنشاء معرف فريد عمومي جديد (GUID) وإرجاعه كقيمه *[GUID](er-formula-supported-data-types-primitive.md#guid)*.

## <a name="syntax"></a>بناء الجملة

```vb
NEWGUID ()
```

## <a name="return-values"></a>إرجاع القيم

*GUID*

قيمة GUID الناتجة.

## <a name="example"></a>مثال

`NEWGUID()`تقوم دائما بإرجاع *قيمه معرف فريد عمومي (GUID)* جديده ، مثل **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
