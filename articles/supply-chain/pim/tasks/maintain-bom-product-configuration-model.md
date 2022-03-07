---
title: الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج
description: يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577278"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج

[!include [banner](../../includes/banner.md)]

يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود. يتم استخدام نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF لإنشاء هذا الإجراء.

## <a name="add-a-bom-line"></a>إضافة بند قائمة مكونات الصنف

1. انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.
1. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد مكبر الصوت المتطور لهذا الإجراء.  
1. في القائمة، حدد الارتباط في الصف المحدد.
1. قم بتوسيع قسم **بنود قائمة مكونات الصنف**.
1. حدد **إضافة**.
1. في الحقل **الاسم**، اكتب قيمة.
1. في حقل **الوصف**، اكتب قيمة.
1. حدد **حفظ**.

## <a name="add-bom-line-details"></a>إضافة تفاصيل بنود قائمة مكونات الصنف

1. حدد **تفاصيل بند قائمة مكونات الصنف**.
2. في الحقل **رقم الصنف**، أدخل قيمة أو حددها.
    * على سبيل المثال، يمكنك تحديد الصنف M0055.  
    * لكل خاصية بند قائمة مكونات الصنف، يمكنك تحديد إذا كانت الخاصية سيُحدد لها قيمة ثابتة أو يتم تعيينها إلى سمة.  
3. حدد خانة الاختيار **تعيين**.
4. حدد *نعم* في حقل **الحساب**.
    * يضمن تعيين خاصية **الحساب** إلى *نعم* إدراج بند قائمة مكونات الصنف في حسابات التكلفة.  
5. حدد علامة التبويب **الإعداد**.
6. حدد خانة الاختيار **تعيين**.
7. في الحقل **الكمية**، أدخل رقمًا.
    * يحدد الحقل "الكمية" كمية الصنف التي سيتم تضمينها في قائمة مكونات الصنف. قد يكون هذا مرشحًا واضحًا لتعيين سمة.  
8. حدد علامة التبويب **بُعد**.
    * تحقق مما إذا كان أي من أبعاد المنتج نشطًا ويجب أن يكون ذا قيمة أو سمة معينة في هذه الحالة.  
9. حدد **موافق**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]