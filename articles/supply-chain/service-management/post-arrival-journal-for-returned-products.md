---
title: ترحيل دفتر يومية وصول المنتجات المرتجعة
description: ترحيل دفتر يومية وصول المنتجات المرتجعة.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63659288ab8551e458f6e92a5045c72441ff68cc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743269"
---
# <a name="post-arrival-journal-for-returned-products"></a>ترحيل دفتر يومية وصول المنتجات المرتجعة 

[!include [banner](../includes/banner.md)]


لمعالجة إرجاع، يجب أولاً التحقق من كمية الإرجاع وتحديث حقل الكمية في دفتر يومية وصول الأصناف. وبعد ذلك، حدد كود ترتيب أو قم بالإشارة إلى أنه يجب فحص أصناف الإرجاع. بعد استكمال هذه الخطوات، يمكنك ترحيل دفتر يومية وصول الصنف الخاص بأمر الإرجاع.

1.  انقر فوق **إدارة المخزون** \> **دوري** \> **نظرة عامة على الوصول**.

2.  في عامل التصفية**اسم الإعداد**، حدد **أمر الإرجاع**.

3.  إذا كانت قائمة عمليات الاستلام طويلة، فاستخدم الحقول الموجودة في المنطقة **النطاق** لتصغير القائمة.

4.  حدد بند أمر الإرجاع المراد ترحيله، وحدد مربع **محدد للوصول‬** الخاص به، ثم انقر فوق **بدء الوصول**.

5.  انقر فوق **دفاتر يومية** \> **إظهار عمليات الوصول من عمليات الاستلام** لفتح النموذج **دفتر يومية الموقع**.
    

    > [!TIP]
    > <P>لعرض معلومات مفصلة، حدد دفتر يومية، ثم انقر فوق <STRONG>البنود</STRONG>.</P>


6.  قم بإجراء أية تحديثات ضرورية، ثم انقر فوق **ترحيل**.

بعد ترحيل دفتر اليومية، يتم تسجيل الأصناف المرتجعة في المخزون، ويشير النموذج **أوامر الإرجاع** إلى وصول الأصناف إلى المستودع.

## <a name="see-also"></a>راجع أيضًا

[دفتر يومية الموقع (نموذج)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))

  


