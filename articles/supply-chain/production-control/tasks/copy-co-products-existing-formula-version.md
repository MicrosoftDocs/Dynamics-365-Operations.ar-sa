---
title: نسخ المنتجات المساعدة من إصدار معادلة موجودة
description: يوضح هذا الإجراء كيفية نسخ المنتجات المساعدة أو المنتجات الثانوية من إصدار معادلة حالية إلى إصدار معادلة مختلفة لمنتج صادر.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b70ccbdac2061baf3896ecbd9449da3c38842a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421096"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>نسخ المنتجات المساعدة من إصدار معادلة موجودة

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية نسخ المنتجات المساعدة أو المنتجات الثانوية من إصدار معادلة حالية إلى إصدار معادلة مختلفة لمنتج صادر. إنه شرط مسبق أن يوجد إصدار معادلة واحدة على الأقل مقترنة بالمنتجات المساعدة. يتم استخدام شركة بيانات العرض التوضيحي USP2 لإنشاء هذا الإجراء.


## <a name="find-a-released-product"></a>البحث عن منتج صادر
1. انتقل إلى "المنتجات الصادرة‬".
2. انقر فوق "إظهار عوامل التصفية".
    * أنت على وشك إضافة نوع إنتاج الحقل في مربع حوار "عامل التصفية".  
3. انقر فوق حقل "إضافة عامل تصفية" لإضافة نوع إنتاج الحقل.
    * في الخطوة التالية، إنك بحاجة إلى إدخال معادلة في حقل نوع الإنتاج قبل تحديد "تطبيق" يدويًا. وهذا يعمل على تعيين عامل التصفية على قائمة المنتجات الصادرة.  
4. أدخل المعادلة في حقل "نوع الإنتاج" يدويًا.
5. انقر فوق تطبيق.

## <a name="select-a-released-product"></a>حدد المنتج الصادر
1. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
2. انقر على إصدارات المعادلة.
    * في جزء "الإجراءات الهندسية"، انقر فوق "إصدارات المعادلة".  

## <a name="copy-co-products"></a>نسخ منتجات مساعدة
1. في جزء "الإجراءات"، انقر فوق "إصدار المعادلة".
2. انقر فوق "‏‫المنتجات المساعدة‬".
3. انقر فوق نسخ.
4. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
5. في حقل "إصدار المعادلة"، أدخل قيمة أو حددها.
6. انقر فوق "موافق".
7. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]