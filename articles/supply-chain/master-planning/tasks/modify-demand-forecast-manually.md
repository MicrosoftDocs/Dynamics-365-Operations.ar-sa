---
title: 'دليل: تعديل التنبؤ بالطلب يدويًا'
description: يوضح هذا الموضوع كيفية تعديل التنبؤ لصنف ما.
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224000"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>دليل: تعديل التنبؤ بالطلب يدويًا

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية تعديل التنبؤ لصنف ما. هذا الإجراء مخصص لمخطط الإنتاج‬.

## <a name="modify-the-forecast-for-a-selected-item"></a>تعديل التنبؤ لصنف محدد

لتعديل التنبؤ لصنف محدد

1. انتقل إلى **الوحدات النمطية \> إدارة معلومات المنتج \> المنتجات \> المنتجات الصادرة**.
1. في القائمة، قم بالبحث عن السجل المطلوب وحدده. حدد الصنف الذي تريد تعديل التنبؤ الخاص به.
1. في جزء الإجراءات، افتح علامة التبويب **الخطة**، ثم حدد **التنبؤ بالطلب**.
1. في القائمة، حدد صفًا. إذا لم يكن هناك أي بنود تنبؤ، فيمكنك إنشاء بند جديد بالنقر فوق **جديد** في جزء الإجراءات.  
1. في الحقل **كمية المبيعات**، أدخل رقمًا موجبًا. يمثل هذا الرقم الكمية المتوقعة للصنف. سيظهر خطأ إذا قمت بإدخال رقم سالب.
1. قم بملء الحقول الأخرى، حسب الحاجة.
1. في جزء الإجراءات، حدد **حفظ**.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>تعديل التنبؤ لصنف واحد أو أكثر باستخدام Microsoft Excel:

لتعديل التنبؤ لصنف واحد أو أكثر باستخدام Microsoft Excel:

1. قم بأحد الإجراءين التاليين:
    - افتح صفحة **التنبؤ بالطلب** لأي صنف كما ورد في القسم السابق.
    - انتقل إلى **التخطيط الرئيسي \> تنبؤ‬ \> إدخال التنبؤ اليدوي \> بنود التنبؤ بالطلب**.
1. في جزء الإجراءات، حدد **فتح في Microsoft Office \> إدخالات التنبؤ بالطلب**.
1. حدد موقع تنزيل، ثم احفظه، ثم افتح الملف الذي تم تنزيله في Excel.
1. إذا شاهدت تحذيرًا، فاختر **تمكين التحرير**.
1. في Excel، سجل دخولك إلى Supply Chain Management باستخدام جزء المهام في Microsoft Dynamics. يجب عليك تسجيل الدخول مع تمكين الخيار **الاستمرار في تسجيل الدخول** ويجب عليك الوثوق بتطبيق اتصال البيانات.
1. يعرض جدول بيانات Excel الآن كافة بنود التنبؤ بالطلب الحالي لشركتك.  يمكنك إضافة بنود التنبؤ بالطلب وحذفها وتحريرها وفق الحاجة.
1. حدد **نشر** على جزء المهام في Microsoft Dynamics لتحميل تغييراتك من جديد إلى Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
