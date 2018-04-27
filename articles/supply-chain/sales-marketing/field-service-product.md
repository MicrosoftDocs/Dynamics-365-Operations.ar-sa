---
title: "مزامنة المنتجات في Finance and Operations للمنتجات في Field Service"
description: "يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة منتجات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: ar-sa
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>مزامنة المنتجات في Finance and Operations للمنتجات في Field Service

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة منتجات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

يستند قالب **منتجات Field Service ‏(Fin and Ops إلى Field Service)** إلى قالب **المنتجات (Fin and Ops إلى Sales) - مباشر** من العميل المتوقع إلى نقد. للحصول على مزيد من المعلومات، راجع [المنتجات (Fin and Ops إلى Sales) - مباشر](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

يوضح هذا الموضوع فقط الاختلافات بين قالبي ** منتجات Field Service ‏(Fin and Ops إلى Field Service)** و**المنتجات (Fin and Ops إلى Sales) – مباشر**.

## <a name="templates-and-tasks"></a>القوالب والمهام

**اسم القالب في تكامل البيانات:**

- منتجات Field Service ‏(Fin and Ops إلى Field Service)

**اسم المهمة في مشروع تكامل البيانات:**

- المنتجات - المنتجات

يشتمل قالب **منتجات Field Service ‏(Fin and Ops إلى Field Service)** على تعيين واحد غير مضمن في قالب **المنتجات (Fin and Ops إلى Sales) - مباشر**. يضمن هذا التعيين أن يتم تعيين الحقل المطلوب والخاص بـ Field Service **نوع منتج الخدمة** بشكل صحيح.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

يتم استخدام تعيين القيمة التالية.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

في Finance and Operations، يتم حساب قيمة **نوع منتج Field Service** في كيان بيانات **منتجات قابلة للبيع تم إصدارها‬** كما يلي:

- **المخزون:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = صحيح
- **NonInventory:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = خطأ
- **الخدمة:** نوع المنتج = الخدمة

