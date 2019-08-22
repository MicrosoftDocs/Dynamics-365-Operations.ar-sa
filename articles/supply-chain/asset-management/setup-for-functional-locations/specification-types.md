---
title: أنواع سمات الصيانة
description: يشرح هذا الموضوع كيفية إنشاء أنواع السمات في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783034"
---
# <a name="maintenance-attribute-types"></a>أنواع سمات الصيانة

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

يشرح هذا الموضوع كيفية إنشاء أنواع السمات في إدارة الأصول. يتم استخدام السمات لوصف خصائص العناصر المختلفة. يمكن إعداد سمات على العناصر التالية:

- [أنواع مواقع العمل](../setup-for-functional-locations/functional-location-types.md)
- [مواقع العمل](../functional-locations/create-functional-locations.md)
- [أنواع الأصول](../setup-for-objects/object-types.md)
- الأصول

تختلف السمات التي يمكنك إعدادها، استنادًا إلى العنصر. على سبيل المثال، يمكنك إعداد سمات التكوين والحجم الفعلي للموقع فيما يتعلق بموقع عمل. فيما يتعلق بنوع أصل أو أصل، يمكنك إعداد سمات لحجم المحرك واستهلاك الطاقة والحد الأقصى لسعة التحميل في ظروف مختلفة.

## <a name="create-attribute-types"></a>إنشاء أنواع سمات

يمكنك إنشاء أنواع سمات خاصة بك. بالإضافة إلى ذلك، يمكنك نقل أبعاد المنتج من Microsoft Dynamics 365 for Finance and Operations إلى صفحة **أنواع السمات**.

1. حدد **إدارة الأصول** \> **الإعداد** \> **أنواع السمات**.
2. في المرة الأولى التي تقوم فيها بإعداد أنواع السمات، حدد **إنشاء أبعاد المنتج** لنقل أبعاد منتج Finance and Operations القياسية تلقائيًا.
3. حدد **جديد** لإنشاء نوع سمة جديدة.
4. في الحقل **نوع السمة**، أدخل اسمًا لنوع السمة.
5. في الحقل **الوصف**، أدخل وصفًا.
6. في حقل **الوحدة**،، حدد وحدة السمات ذات الصلة، حسب الاقتضاء.
7. في حقل **نوع البيانات**، حدد نوع بيانات للوحدة.
8. إذا حددت **سلسلة** كنوع البيانات، فاتبع الخطوات التالية لإنشاء قيم لنوع السمة:

    1. حدد نوع السمة، ثم حدد **القيم**.
    2. في حقل **قيم السمة**، حدد **جديد**.
    3. في الحقل **نوع السمة**، حدد نوع سمة (البُعد).
    4. في حقل **القيمة**، أدخل قيمة ذات صلة.
    5. في الحقل **الوصف**، أدخل وصفًا.
    6. قم بحفظ السجل.
    7. عد إلى صفحة **أنواع السمات**.

9. قم بحفظ السجل.

    يعرض حقل **أنواع مواقع العمل** عدد مواقع العمل التي تستخدم نوع السمة. يعرض حقل **أنواع الأصول** أنواع الأصول التي تستخدمها.
