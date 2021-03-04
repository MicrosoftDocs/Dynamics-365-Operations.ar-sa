---
title: أخذ الأصناف المرتجعة عبر الفحص
description: أخذ الأصناف المرتجعة عبر الفحص.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421529"
---
# <a name="take-returned-items-through-inspection"></a>أخذ الأصناف المرتجعة عبر الفحص 

[!include [banner](../includes/banner.md)]


1.  ‏‫انقر فوق **‏‫إدارة المخزون‬** \> **دوري** \> **إدارة الجودة** \>‏‫ **أوامر إدخال مخزن الفحص**.

2.  تحديد موقع بند الأمر المطابق للصنف المرجع الجاري فحصه.

    > [!NOTE]
    > <P>يمكن أن يقترن أمر إدخال مخزن العزل برقم صنف وحيد فقط. إذا تم إرجاع 10 أصناف لديها أرقام صنف مختلفة في شحنة واحدة وتم إرسالها إلى أمر إدخال مخزن العزل، سيتم إنشاء 10 أوامر فردية لإدخال مخزن العزل.</P>

3.  بعد إجراء فحص الصنف، قم بالتحديد في الحقل **رمز الإرجاع** للإشارة إلى ما يجب عمله مع الصنف وكيفية التعامل مع الحركات المالية المتصلة. تشتمل الأمثلة على إرجاع الصنف إلى المخزن وإعادة تمويل العميل وتخريد الصنف وإرسال بديل إلى العميل أو إرجاع الصنف إلى العميل بدون ائتمان.
    
    > [!NOTE]
    > <P>إذا تعذر تعيين رمز الإرجاع نفسه إلى عدة أصناف مرجعة في مجموعة أرقام صنف واحد، فسينبغي عليك تقسيم أمر إدخال مخزن الفحص‬ (<STRONG>الوظائف</STRONG> &gt; <STRONG>تقسيم</STRONG>) لتعيين رمز إرجاع مختلف لكل مجموعة فرعية.</P>


4.  عند الانتهاء من الفحص، انقر فوق **‏‫الإبلاغ كمنته‬** لإصدار الأصناف المرجعة وإنشاء دفتر يومية الوصول لصنف. سيتولى الشخص أو القسم الذي يتسلم الأصناف معالجة دفتر اليومية للأصناف المراد إرجاعها إلى المخزن.
    
    –أو –
    
    قم بإنهاء أمر الإدخال ونقل الأصناف إلى المخزن مباشرةً باستخدام أحد وظائف **المخزون**.

5.  أغلق النموذج لحفظ التغييرات.

## <a name="see-also"></a>راجع أيضًا

[تحديد كيفية التخلص من الأصناف المرتجعة](specify-how-to-dispose-of-returned-items.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]