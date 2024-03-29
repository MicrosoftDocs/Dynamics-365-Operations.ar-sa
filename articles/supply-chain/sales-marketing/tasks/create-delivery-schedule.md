---
title: إنشاء جدول تسليم
description: يُوضح هذا الإجراء كيفية إنشاء جدول تسليم لأمر مبيعات.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97dbbcc7173dcece9aea833551e8f985246bdbb2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578958"
---
# <a name="create-delivery-schedule"></a>إنشاء جدول تسليم

[!include [banner](../../includes/banner.md)]

يُوضح هذا الإجراء كيفية إنشاء جدول تسليم لأمر مبيعات. يتم استخدام جدول التسليم عندما يتم طلب كمية في أمر أو عرض أسعار بحيث يتم التسليم بواسطة شحنات متعددة. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.


## <a name="create-delivery-schedule"></a>إنشاء جدول تسليم
1. انتقل إلى "كافة أوامر المبيعات‬".
2. انقر فوق "جديد".
3. في الحقل "حساب العميل"، أدخل قيمة أو حددها.
4. انقر فوق موافق.
5. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
6. في الحقل "الكمية"، أدخل رقمًا أكبر من 1.
7. انقر فوق بند أمر المبيعات.
8. انقر فوق "جدول التسليم".
    * الصفحة "جدول التسليم" هي المكان حيث يمكنك تحديد عدد الشحنات التي سيتم تسليم الكمية الإجمالية لبند الأمر فيها إلى العميل.    
    * بشكل افتراضي، ينسخ النظام إجمالي الكمية وتفاصيل التسليم الأخرى لبند المبيعات الأصلي إلى البند الأول في جدول التسليم. في هذا المثال، سننشئ جدولاً لشحنتين، مع إزاحة تاريخ الشحنة الثانية بمقدار أسبوع عن الشحنة الأولى.  
9. في الحقل "الكمية"، أدخل رقمًا يشكل جزءًا من إجمالي الكمية.
10. انقر فوق جديد.
11. في الحقل "الكمية"، أدخل الكمية المتبقية.
12. في الحقل "تاريخ الشحن المطلوب"، أدخل تاريخًا يكون عبارة عن أسبوع واحد يسبق تاريخ بند التسليم الأول.
    * يتحكم الخياران على علامة التبويب السريعة "تحويل التكاليف‬" في الطريقة التي تريد بها توزيع التكاليف‬ عبر بنود جدول التسليم، حالما تم تعيينها إلى بند الأمر الأصلي. إذا قمت بتحديد "نسخ إجمالي المبالغ‬"، فسيتم نسخ مبلغ التكلفة نفسه إلى كل بند. يقوم الخيار "تخصيص لبنود التسليم‬" بتقسيم التكلفة بطريقة متساوية عبر بنود التسليم.  
    * يمكن تقسيم التكاليف الثابتة فقط، بينما سيستمر نسخ التكاليف المتغيرة إلى البنود.  
13. انقل المؤشر بعيدًا عن خط التسليم الثاني لتحديث الصفحة.
    * يمكنك تعقب إجمالي الكمية التي تم تخصيصها إلى بنود جدول التسليم بالنظر إلى حقلي الإجمالي والمتبقي. عندما تكون الكمية المتبقية صفر، فهذا يعني أن الكمية الكاملة من البند الأصلي تم تخصيصها للجدول.   
14. انقر فوق "موافق".
    * تم الآن نسخ جدول التسليم إلى بنود الأمر.   
    * تم تحويل بند الأمر الأصلي، المشار إليه كبند تجاري، إلى بند أمر بعمليات تسليم متعددة. تم وضع علامة عليه بواسطة أيقونة مميزة ويعمل كرأس لبنود التسليم.  
    * يشكّل البندين الجديدين، المشار إليهما ببنود التسليم، جدول تسليم واحدًا. ستتم معالجة الأمر في مقابل هذه البنود وليس البند الأصلي. إذا تمت طباعة مستندات، مثل إيصالات التأكيد أو قوائم الانتقاء أو إيصالات التعبئة أو الفواتير، فإن بنود التسليم وحدها ستظهر.   
    * بإمكان بنود التسليم أن تتضمن تواريخ تسليم وكميات وأوضاع تسليم وأبعاد تخزين مختلفة، مثل الموقع والمستودع. ومع ذلك، يجب أن تتطابق أبعاد المنتج دائمًا مع تلك الموجودة في البند التجاري ولا يمكن تغييرها.  
15. في الحقل "الكمية"، أدخل رقمًا أكبر من الرقم الحالي.
16. حدد البند التجاري لمعرفة تأثير إعادة حساب الكمية.
17. في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".
18. انقر فوق "ترحيل إيصال التعبئة".
19. وسّع مقطع "المحددات".
20. في الحقل "الكمية"، حدد "الكل".
    * لاحظ أنه سيتم إنشاء إيصال التعبئة لبندين من بنود جدول تسليم وليس بند الأمر الأصلي.  
21. حدد "نعم" في الحقل "طباعة إيصال التعبئة‬".
22. انقر فوق "موافق".
23. انقر فوق نعم.
24. قم بإغلاق الصفحة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]