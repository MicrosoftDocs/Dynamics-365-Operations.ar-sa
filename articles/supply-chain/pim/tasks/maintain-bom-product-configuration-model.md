---
title: الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج
description: يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcdf4b735587b76b7f761f59c56da1ca358a2e37
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421226"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج

[!include [banner](../../includes/banner.md)]

يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود. يتم استخدام نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF لإنشاء هذا الإجراء.


## <a name="add-a-bom-line"></a>إضافة بند قائمة مكونات الصنف
1. انقر فوق "تعريف نموذج متغير المنتج"ز
2. انقر فوق "نماذج تكوين المنتجات".
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد مكبر الصوت المتطور لهذا الإجراء.  
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. قم بتوسيع القسم "قائمة مكونات الصنف".
6. وانقر فوق إضافة.
7. في حقل "الاسم"، اكتب قيمة.
8. في وصف الحقل، اكتب قيمة.
9. انقر فوق "حفظ".

## <a name="add-bom-line-details"></a>إضافة تفاصيل بنود قائمة مكونات الصنف
1. انقر فوق "تفاصيل بنود قائمة مكونات الصنف".
2. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
    * على سبيل المثال، يمكنك تحديد الصنف M0055.  
    * لكل خاصية بند قائمة مكونات الصنف، يمكنك تحديد إذا كانت الخاصية سيُحدد لها قيمة ثابتة أو يتم تعيينها إلى سمة.  
3. حدد خانة الاختيار "تعيين".
4. حدد "نعم" في الحقل "حساب".
    * يضمن تعيين "خاصية الحساب" على "نعم" إدراج بند قائمة مكونات الصنف في حسابات التكلفة.  
5. انقر فوق علامة التبويب "إعداد".
6. حدد خانة الاختيار "تعيين".
7. في حقل الكمية، أدخل رقمًا.
    * يحدد الحقل "الكمية" كمية الصنف التي سيتم تضمينها في قائمة مكونات الصنف. قد يكون هذا مرشحًا واضحًا لتعيين سمة.  
8. انقر فوق علامة التبويب "البُعد".
    * تحقق مما إذا كان أي من أبعاد المنتج نشطًا ويجب أن يكون ذا قيمة أو سمة معينة في هذه الحالة.  
9. انقر فوق "موافق".

