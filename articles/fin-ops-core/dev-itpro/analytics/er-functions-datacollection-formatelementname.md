---
title: 'وظيفة FORMATELEMENTNAME ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني FORMATELEMENTNAME (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745623"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="d31a0-103">وظيفة FORMATELEMENTNAME ER</span><span class="sxs-lookup"><span data-stu-id="d31a0-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d31a0-104">تُرجع الوظيفة `FORMATELEMENTNAME` قيمة *السلسلة* التي تمثل اسم عنصر تنسيق التقارير الإلكترونية (ER) الحالي.</span><span class="sxs-lookup"><span data-stu-id="d31a0-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31a0-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d31a0-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="d31a0-106">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d31a0-106">Return values</span></span>

<span data-ttu-id="d31a0-107">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d31a0-107">*String*</span></span>

<span data-ttu-id="d31a0-108">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d31a0-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d31a0-109">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="d31a0-109">Usage notes</span></span>

<span data-ttu-id="d31a0-110">يُمكن استدعاء هذه الوظيفة في تعبيرات ER التي تم تكوينها لخصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER من مجموعة **النص** الموجودة الموجودة ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.</span><span class="sxs-lookup"><span data-stu-id="d31a0-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="d31a0-111">مثال</span><span class="sxs-lookup"><span data-stu-id="d31a0-111">Example</span></span>

<span data-ttu-id="d31a0-112">لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.</span><span class="sxs-lookup"><span data-stu-id="d31a0-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d31a0-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d31a0-113">Additional resources</span></span>

[<span data-ttu-id="d31a0-114">وظائف تجميع البيانات</span><span class="sxs-lookup"><span data-stu-id="d31a0-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
