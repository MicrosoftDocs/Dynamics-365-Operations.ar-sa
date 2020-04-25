---
title: دورة حياة أمر الدُفعة من الإنشاء حتى بدء التشغيل
description: يأخذك هذا الإجراء من خلال الجزء الأول من دورة حياة أمر الدفعة.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16b55726fdb9ab15e74a9f752cac972b80a98de2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210975"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>دورة حياة أمر الدُفعة من الإنشاء حتى بدء التشغيل

[!include [banner](../../includes/banner.md)]

يأخذك هذا الإجراء من خلال الجزء الأول من دورة حياة أمر الدفعة.

من الإنشاء وتقدير التكلفة، ثم عبر جدولة وظيفة الإنتاج إلى البدء الفعلي لأمر الدفعة.



شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. 



المتطلبات المسبقة لتشغيل الإجراء بواسطة مجموعة بيانات أخرى هي منتج صادر مع معادلة نشطة وإصدار المسار.


## <a name="create-a-batch-order"></a>إنشاء أمر دفعة
1. انتقل إلى "كافة أوامر الإنتاج".
2. انقر فوق أمر دُفعة جديد.
3. في الحقل "رقم الصنف"، أدخل قيمة أو حددها.
4. انقر فوق إنشاء.
5. استخدم "عامل التصفية السريع" لتصفية حقل "الإنتاج" باستخدام القيمة ''b".

## <a name="view-production-formula-and-expected-co-products"></a>عرض معادلة الإنتاج والمنتجات المساعدة المتوقعة
1. في جزء "الإجراءات"، انقر فوق "أمر إنتاج".
2. انقر فوق المعادلة.
3. قم بإغلاق الصفحة.
4. انقر فوق "‏‫المنتجات المساعدة‬".
5. قم بإغلاق الصفحة.

## <a name="estimate-the-batch-order"></a>تقدير أمر الدُفعة
1. انقر فوق "تقدير".
2. انقر فوق "موافق".
3. في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".
4. انقر فوق "عرض تفاصيل الحساب"ز
5. قم بإغلاق الصفحة.

## <a name="release-the-batch-order"></a>إصدار أمر الدُفعة
1. في جزء "الإجراءات"، انقر فوق "أمر إنتاج".
2. انقر فوق "إصدار".
3. انقر فوق "موافق".

## <a name="schedule-production-jobs"></a>جدولة وظائف الإنتاج
1. في جزء الإجراءات، انقر فوق "جدول".
2. انقر فوق "جدولة الوظائف".
3. حدد "لا" في حقل "القدرة المحدودة‬".
4. حدد "لا" في حقل "المواد المحدودة‬".
5. انقر فوق موافق.
6. في جزء "الإجراءات"، انقر فوق "أمر إنتاج".
7. انقر فوق كافة الوظائف.
8. قم بإغلاق الصفحة.

## <a name="start-the-batch-order"></a>بدء تشغيل أمر الدفعة
1. انقر فوق "بدء".
2. انقر فوق علامة التبويب "عام".
3. حدد "لا" في حقل ترحيل قائمة الانتقاء الآن.
4. انقر فوق "موافق".
5. في جزء "الإجراءات"، انقر فوق "عرض".
6. انقر فوق "قائمة الانتقاء".
7. في القائمة، انقر فوق الارتباط في الصف المحدد.
8. قم بإغلاق الصفحة.
9. قم بإغلاق الصفحة.
10. انقر فوق "بطاقة المسار".
11. في القائمة، انقر فوق الارتباط في الصف المحدد.
12. قم بإغلاق الصفحة.
13. قم بإغلاق الصفحة.

