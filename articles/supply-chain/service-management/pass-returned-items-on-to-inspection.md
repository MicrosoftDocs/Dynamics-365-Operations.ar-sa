---
title: "تمرير الأصناف المرتجعة إلى الفحص"
description: "عند تسجيل صنف مرتجع، فحدد أنه ينبغي إرسال صنف للفحص قبل إرجاعه إلى المخزون أو التخلص منه بطريقة أخرى."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4a60e6635e3bb1723ced7aba1a71135116b53272
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---


# <a name="pass-returned-items-on-to-inspection"></a>تمرير الأصناف المرتجعة إلى الفحص 

[!include [banner](../includes/banner.md)]


عند تسجيل صنف مرتجع، فربما تحدد أنه ينبغي إرسال صنف للفحص قبل إرجاعه إلى المخزون أو التخلص منه بطريقة أخرى.

1.  انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **وصول الصنف‬**.
    
    \-أو-
    
    انقر فوق **إدارة المخزون** \> **دفتر اليومية** \> **وصول الصنف‬** \> **مدخلات الإنتاج**.

2.  في نموذج **دفتر يومية الموقع**، سجل استلام صنف كما هو معتاد. 
    

    > [!NOTE]
    > <P>للحصول على مزيد من المعلومات حول تسجيل استلام الأصناف المرتجعة، راجع <A href="register-the-receipt-of-returned-items.md">تسجيل استلام الأصناف المرتجعة</A></P>



3.  في علامة تبويب **قيم افتراضية**، في منطقة **وضع المعالجة**، حدد خانة **إدارة العزل**.

سوف يؤدي هذا إلى مطالبة النظام بإنشاء أمر إدخال مخزن الفحص، وسوف يستجيب الشخص أو القسم الذي يجري عمليات الفحص لهذا الأمر باستخدام النموذج **أمر العزل**.

## <a name="see-also"></a>راجع أيضًا

[أخذ الأصناف المرتجعة عبر الفحص](take-returned-items-through-inspection.md)

[تحديد كيفية التخلص من الأصناف المرتجعة](specify-how-to-dispose-of-returned-items.md)


