---
title: التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وDataverse
description: يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 361d6555b60e02832c337b6f416b2b3627b6d365
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129297"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وDataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse. على وجه التحديد، يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>التحقق من تكوين الكتابة الثنائية في تطبيق Finance and Operations

لتحديد ما إذا كانت الأخطاء التي تراها عند محاولة حفظ الصفوف للتحديث تاتي من الكتابة الثنائية أو لا، تحقق أولاً من تكوين الكتابة الثنائية.

+ إذا كانت لديك امتيازات إدارية في تطبيق Finance and Operations، فانتقل إلى **مساحات العمل\> إدارة البيانات**، وحدد تجانب **الكتابة الثنائية**. في حالة عرض تفاصيل البيئات المرتبطة وقائمة مخططات الجداول قيد التشغيل، فإنه يتم تكوين الكتابة الثنائية.

    ![التحقق من اتصال تطبيق Finance and Operationsعندما يكون لديك امتيازات المسؤول](media/verify_fin_ops_1.png)

+ إذا لم يكن لديك امتيازات المسؤول، فستتلقى رسالة خطأ، *لا يمكن كتابة البيانات إلى كيان \<entity name\>*. في المثال الموجود في التوضيح التالي، لا يمكنك إنشاء صف عميل في تطبيق Finance and Operations، لأنه يتم تكوين الكتابة الثنائية، ولكن لا توجد البيانات المرجعية لشروط الدفع ومجموعة العملاء في Dataverse.

    ![التحقق من اتصال تطبيق Finance and Operationsعندما لا يكون لديك امتيازات المسؤول](media/verify_fin_ops_2.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في تطبيقات Finance and Operations، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>التحقق من تكوين الكتابة الثنائية في Dataverse

عندما تقوم بإنشاء بيانات، إذا شاهدت عمود **الشركة** في صفحات في Dataverse، فإنه يتم تكوين الكتابة الثنائية.

![التحقق من اتصال Dataverse](media/verify_cds.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في Dataverse، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

للحصول على معلومات حول كيفية عرض تفاصيل الأخطاء في حالة مصادفة أي أخطاء اثناء إنشاء البيانات في Dataverse، راجع [تمكين وعرض تسجيل تتبع المكونات الإضافية في Dataverse لعرض تفاصيل الأخطاء](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]