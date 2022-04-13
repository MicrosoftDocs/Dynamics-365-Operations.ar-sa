---
title: 'دليل: تعديل التنبؤ بالطلب يدويًا'
description: يوضح هذا الموضوع كيفية تعديل التنبؤ لصنف ما.
author: t-benebo
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e5030bf97bee8dc475f22473ecc87e900298b6f
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469357"
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
