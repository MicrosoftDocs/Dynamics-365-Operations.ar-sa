---
title: ترحيل دفتر يومية وصول المنتجات المرتجعة
description: ترحيل دفتر يومية وصول المنتجات المرتجعة.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14619069c0e984060f67fc4536b311c6802bfec7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214288"
---
# <a name="post-arrival-journal-for-returned-products"></a>ترحيل دفتر يومية وصول المنتجات المرتجعة 

[!include [banner](../includes/banner.md)]


لمعالجة إرجاع، يجب أولاً التحقق من كمية الإرجاع وتحديث حقل الكمية في دفتر يومية وصول الأصناف. وبعد ذلك، حدد كود ترتيب أو قم بالإشارة إلى أنه يجب فحص أصناف الإرجاع. بعد استكمال هذه الخطوات، يمكنك ترحيل دفتر يومية وصول الصنف الخاص بأمر الإرجاع.

1.  انقر فوق **إدارة المخزون** \> **دوري** \> **نظرة عامة على الوصول**.

2.  في عامل التصفية **اسم الإعداد**، حدد **أمر الإرجاع**.

3.  إذا كانت قائمة عمليات الاستلام طويلة، فاستخدم الحقول الموجودة في المنطقة **النطاق** لتصغير القائمة.

4.  حدد بند أمر الإرجاع المراد ترحيله، وحدد مربع **محدد للوصول‬** الخاص به، ثم انقر فوق **بدء الوصول**.

5.  انقر فوق **دفاتر يومية** \> **إظهار عمليات الوصول من عمليات الاستلام** لفتح النموذج **دفتر يومية الموقع**.
    

    > [!TIP]
    > <P>لعرض معلومات مفصلة، حدد دفتر يومية، ثم انقر فوق <STRONG>البنود</STRONG>.</P>


6.  قم بإجراء أية تحديثات ضرورية، ثم انقر فوق **ترحيل**.

بعد ترحيل دفتر اليومية، يتم تسجيل الأصناف المرتجعة في المخزون، ويشير النموذج **أوامر الإرجاع** إلى وصول الأصناف إلى المستودع.

## <a name="see-also"></a>راجع أيضًا

[دفتر يومية الموقع (نموذج)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]