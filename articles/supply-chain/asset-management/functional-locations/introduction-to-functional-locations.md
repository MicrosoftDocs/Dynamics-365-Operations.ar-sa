---
title: مقدمة إلى مواقع العمل
description: يوفر هذا الموضوع نظرة عامة حول مواقع العمل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d7d98ec5434d9cdc93276952035b559625be2bd
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783043"
---
# <a name="introduction-to-functional-locations"></a>مقدمة إلى مواقع العمل

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

يوفر هذا الموضوع نظرة عامة حول مواقع العمل في إدارة الأصول. مواقع العمل هي عناصر البنية التقنية، مثل الوحدات الوظيفية في النظام. يتم إنشاء مواقع العمل بشكل هرمي، وتقوم أنت بتثبيت الأصول عليها. يعتمد إعداد مواقع العمل في شركتك على متطلبات الشركة.

فيما يلي بعض الأمثلة حول كيفية استخدام مواقع العمل:

- **وظيفي** – يمكن أن تكون مواقع العمل موجهة نحو المستخدم ويتم استخدامها لإدارة الأصول التي لها سلوك مماثل.
- **متعلق بالعملية** - يمكن أن تكون مواقع العمل موجهة نحو سير العمل.
- **مكاني** – يمكن أن تمثل مواقع العمل مواقع جغرافية أو مواقع بناء.

تتم إدارة كل موقع عمل بشكل مستقل في إدارة الأصول. فيما يلي بعض الميزات المفيدة لمواقع العمل:

- إعداد مواصفات موقع العمل.
- إعداد متطلبات مواصفات الأصول.
- إعداد تسلسل الصيانة وذلك للصيانة الوقائية والتفاعلية.
- إدارة الأصول المثبتة.
- تعقب الطلبات النشطة وأوامر العمل المرتبطة بالأصول المثبتة.
- تعقب الأخطاء التي يتم تسجيلها على الأصول.
- متابعة تكاليف الصيانة على الأصول المرتبطة بموقع عمل في أي وقت من الأوقات.

توفر مواقع العمل إمكانية تعقب الأصول فيما يتعلق بالطلبات، وأوامر العمل، وتسجيلات الأخطاء، وتقييمات الحالة، وتسجيلات وقف الإنتاج، وتسجيلات عدادات الأصول.

> [!NOTE]
> حتى إذا تم تثبيت أصل على مواقع عمل مختلفة خلال مدة بقاءه، يمكن أن تكون التكاليف مرتبطة بكل موقع. وبعبارة أخرى، ترتبط تكاليف الأصول دائمًا بموقع العمل الذي تم تثبيت الأصل عليه في وقت معين.

مواقع العمل **ليست** مرنة. لذلك، بعد إعداد التدرج الهرمي لمواقع العمل، لا يمكنك نقل المواقع فيه. 

بعد إنشاء التدرج الهرمي لمواقع العمل، تكون الخطوة التالية هي تثبيت الأصول عليها. لمزيد من المعلومات، راجع [تثبيت الأصول على مواقع العمل](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>جميع مواقع العمل

حدد **إدارة الأصول** \> **عام** \> **مواقع العمل** \> **جميع مواقع العمل** لفتح صفحة قائمة **جميع مواقع العمل**. تُظهر هذه الصفحة جميع مواقع العمل وبعض المعلومات المتعلقة بكل منها. لعرض مواقع العمل النشطة فقط، حدد **مواقع العمل النشطة**. لعرض مواقع العمل التي ترتبط أنت بها كعامل، حدد **مواقع العمل النشطة الخاصة بي**. (يتم إعداد هذه العلاقة في صفحة **العاملون**. لمزيد من المعلومات، راجع [عاملو الصيانة ومجموعات عاملي الصيانة](../setup-for-objects/workers-and-worker-groups.md).)

في صفحة قائمة **جميع مواقع العمل**، حدد ارتباطًا في عمود **موقع العمل** لعرض تفاصيل السجل المحدد. لتحرير موقع العمل، حدد الزر **تحرير**. يُظهر عرض التفاصيل معلومات تفصيلية تتعلق بالموقع. كما يتضمن جزء **المعلومات ذات الصلة** على اليمين. يُظهر هذا الجزء التدرج الهرمي لمواقع العمل. ويمكنك توسيع جزء **المعلومات ذات الصلة** وطيه.

تم تنظيم الأزرار الموجودة في جزء الإجراءات على علامات تبويب. يصف الجدول التالي بإيجاز الأزرار المتعلقة بإدارة الأصول.

| اسم الزر                         | الوصف                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| تحرير                                | التبديل بين وضع التحرير ووضع العرض للصفحة.                                                                                         |
| القيمة الجديدة                                 | إنشاء موقع عمل جديد.                                                                                                            |
| حذف                              | حذف موقع العمل المحدد.                                                                                                     |
| إعادة تسمية                              | إعادة تسمية موقع العمل المحدد.                                                                                                     |
| نسخ بنية موقع عمل  | نسخ التدرج الهرمي لمواقع العمل.                                                                                                      |
| تثبيت الأصل                       | تثبيت أصل، بما في ذلك الأصول التابعة، على موقع العمل.                                                                        |
| استبدال الأصل                       | استبدال التدرج الهرمي للأصول بتدرج هرمي للأصول آخر في موقع العمل.                                                         |
| مراقبة التكاليف                        | افتح صفحة **مراقبة تكلفة موقع العمل**، حيث يمكنك إجراء حساب تكلفة لموقع العمل المحدد.                |
| مراقبة الساعة                        | افتح صفحة **مراقبة ساعة موقع العمل**، حيث يمكنك إجراء حساب تكلفة لموقع العمل المحدد.                |
| الأصول                              | افتح صفحة **كل الأصول**، حيث يمكنك عرض قائمة بالأصول المرتبطة بموقع العمل المحدد.                      |
| الطلبات                            | افتح صفحة **الطلبات النشطة**، حيث يمكنك عرض قائمة بالطلبات المرتبطة بموقع العمل المحدد.               |
| أوامر العمل                         | افتح صفحة **أوامر العمل النشطة**، حيث يمكنك عرض قائمة بأوامر العمل المرتبطة بموقع العمل المحدد.         |
| الأخطاء                              | افتح صفحة **أخطاء الأصول**، حيث يمكنك عرض قائمة بتسجيلات أخطاء الأصول المرتبطة بموقع العمل المحدد. |
| تحديث حالة موقع العمل    | تحديث مرحلة موقع العمل المحدد.                                                                                        |
| سجل حالة دورة الحياة                 | عرض سجل يُظهر مراحل موقع العمل المحدد.                                                                        |