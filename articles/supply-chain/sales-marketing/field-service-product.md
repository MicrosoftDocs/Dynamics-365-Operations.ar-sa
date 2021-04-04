---
title: مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d3dc21a39c9866d09e500e2f14ff810bac7d57fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261035"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

يستند قالب **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** إلى قالب **المنتجات (Supply Chain Management إلى Sales) - مباشر** من العميل المتوقع إلى النقدية. للحصول على مزيد من المعلومات، راجع [المنتجات (Supply Chain Management إلى Sales) - مباشر](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** و **المنتجات (Supply Chain Management إلى Sales) – مباشر**.

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات**

- منتجات Field Service ‏(Supply Chain Management إلى Field Service)

**اسم المهمة في مشروع تكامل البيانات**

- المنتجات - المنتجات

يتضمن قالب **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** تعيينًا غير مضمن في قالب **المنتجات (Supply Chain Management إلى Sales) - مباشر**. يضمن هذا التعيين أن يتم تعيين الحقل المطلوب والخاص بـ Field Service **نوع منتج الخدمة** بشكل صحيح.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

يتم استخدام تعيين القيمة التالية.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

في Supply Chain Management، يتم حساب قيمة **نوع منتج Field Service** في كيان بيانات **منتجات قابلة للبيع تم إصدارها‬** كما يلي:

- **المخزون:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = صحيح
- **NonInventory:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = خطأ
- **الخدمة:** نوع المنتج = الخدمة

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>منتجات Field Service ‏(Supply Chain Management إلى Field Service): المنتجات - المنتجات

[![تعيين القالب في تكامل البيانات](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]