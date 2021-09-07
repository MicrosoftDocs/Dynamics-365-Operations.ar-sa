---
title: التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وDataverse
description: يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 074cfd5dc2d2877e83e7e65a8b2178ed954a288e
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416671"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وDataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse. على وجه التحديد، يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>التحقق من تكوين الكتابة الثنائية في تطبيق Finance and Operations

لتحديد ما إذا كانت الأخطاء التي تراها عند محاولة حفظ الصفوف للتحديث تاتي من الكتابة الثنائية أو لا، تحقق أولاً من تكوين الكتابة الثنائية.

+ إذا كانت لديك امتيازات إدارية في تطبيق Finance and Operations، فانتقل إلى **مساحات العمل\> إدارة البيانات**، وحدد تجانب **الكتابة الثنائية**. في حالة عرض تفاصيل البيئات المرتبطة وقائمة مخططات الجداول قيد التشغيل، فإنه يتم تكوين الكتابة الثنائية.

    ![التحقق من اتصال تطبيق Finance and Operations عندما يكون لديك امتيازات المسؤول.](media/verify_fin_ops_1.png)

+ إذا لم يكن لديك امتيازات المسؤول، فستتلقى رسالة خطأ، *لا يمكن كتابة البيانات إلى كيان \<entity name\>*. في المثال الموجود في التوضيح التالي، لا يمكنك إنشاء صف عميل في تطبيق Finance and Operations، لأنه يتم تكوين الكتابة الثنائية، ولكن لا توجد البيانات المرجعية لشروط الدفع ومجموعة العملاء في Dataverse.

    ![التحقق من اتصال تطبيق Finance and Operationsعندما لا يكون لديك امتيازات المسؤول.](media/verify_fin_ops_2.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في تطبيقات Finance and Operations، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>التحقق من تكوين الكتابة الثنائية في Dataverse

عندما تقوم بإنشاء بيانات، إذا شاهدت عمود **الشركة** في صفحات في Dataverse، فإنه يتم تكوين الكتابة الثنائية.

![التحقق من اتصال Dataverse.](media/verify_cds.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في Dataverse، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

للحصول على معلومات حول كيفية عرض تفاصيل الأخطاء في حالة مصادفة أي أخطاء اثناء إنشاء البيانات في Dataverse، راجع [تمكين وعرض تسجيل تتبع المكونات الإضافية في Dataverse لعرض تفاصيل الأخطاء](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]