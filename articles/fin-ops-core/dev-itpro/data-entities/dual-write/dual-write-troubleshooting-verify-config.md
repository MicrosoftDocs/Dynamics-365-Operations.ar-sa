---
title: تحقق من تكوين الكتابة المزدوجة في تطبيقات التمويل والعمليات وDataverse
description: توضح هذه المقالة كيفية تحديد ما إذا كان قد تم تكوين الكتابة المزدوجة في تطبيقات التمويل والعمليات وفي Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289379"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>تحقق من تكوين الكتابة المزدوجة في تطبيقات التمويل والعمليات وDataverse

[!include [banner](../../includes/banner.md)]





توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها في تكامل الكتابة المزدوجة بين تطبيقات التمويل والعمليات وDataverse. على وجه التحديد، يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة المزدوجة في تطبيقات التمويل والعمليات وفي Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>تحقق من تكوين الكتابة المزدوجة في تطبيقات التمويل والعمليات

لتحديد ما إذا كانت الأخطاء التي تراها عند محاولة حفظ الصفوف للتحديث تاتي من الكتابة الثنائية أو لا، تحقق أولاً من تكوين الكتابة الثنائية.

+ إذا كانت لديك امتيازات إدارية في تطبيق التمويل والعمليات، فانتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد الإطار المتجانب **الكتابة المزدوجة**. في حالة عرض تفاصيل البيئات المرتبطة وقائمة مخططات الجداول قيد التشغيل، فإنه يتم تكوين الكتابة الثنائية.

    ![التحقق من اتصال تطبيق التمويل والعمليات عندما يكون لديك امتيازات المسؤول.](media/verify_fin_ops_1.png)

+ إذا لم يكن لديك امتيازات المسؤول، فستتلقى رسالة خطأ، *لا يمكن كتابة البيانات إلى كيان \<entity name\>*. في المثال الموجود في التوضيح التالي، لا يمكنك إنشاء صف عميل في تطبيق التمويل والعمليات، بسبب تكوين الكتابة المزدوجة، ولكن البيانات المرجعية لشروط الدفع ومجموعة العملاء غير موجودة في Dataverse.

    ![التحقق من اتصال تطبيق التمويل والعمليات عندما لا يكون لديك امتيازات المسؤول.](media/verify_fin_ops_2.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في تطبيقات التمويل والعمليات، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>التحقق من تكوين الكتابة الثنائية في Dataverse

عندما تقوم بإنشاء بيانات، إذا شاهدت عمود **الشركة** في صفحات في Dataverse، فإنه يتم تكوين الكتابة الثنائية.

![التحقق من اتصال Dataverse.](media/verify_cds.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في Dataverse، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

للحصول على معلومات حول كيفية عرض تفاصيل الأخطاء في حالة مصادفة أي أخطاء اثناء إنشاء البيانات في Dataverse، راجع [تمكين وعرض تسجيل تتبع المكونات الإضافية في Dataverse لعرض تفاصيل الأخطاء](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
