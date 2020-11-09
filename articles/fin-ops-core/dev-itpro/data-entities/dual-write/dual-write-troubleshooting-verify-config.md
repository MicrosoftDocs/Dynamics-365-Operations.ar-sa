---
title: التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وCommon Data Service
description: يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Common Data Service.
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
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997220"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وCommon Data Service

[!include [banner](../../includes/banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service. على وجه التحديد، يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>التحقق من تكوين الكتابة الثنائية في تطبيق Finance and Operations

لتحديد ما إذا كانت الأخطاء التي تراها عند محاولة حفظ السجلات للتحديث تاتي من الكتابة الثنائية أو لا، تحقق أولاً من تكوين الكتابة الثنائية.

+ إذا كانت لديك امتيازات إدارية في تطبيق Finance and Operations، فانتقل إلى **مساحات العمل\> إدارة البيانات** ، وحدد تجانب **الكتابة الثنائية**. في حالة عرض تفاصيل البيئات المرتبطة وقائمة مخططات الكيانات قيد التشغيل، فإنه يتم تكوين الكتابة الثنائية.

    ![التحقق من اتصال تطبيق Finance and Operationsعندما يكون لديك امتيازات المسؤول](media/verify_fin_ops_1.png)

+ إذا لم يكن لديك امتيازات المسؤول، فستتلقى رسالة خطأ، *لا يمكن كتابة البيانات إلى كيان \<entity name\>*. في المثال الموجود في التوضيح التالي، لا يمكنك إنشاء سجل عميل في تطبيق Finance and Operations، لأنه يتم تكوين الكتابة الثنائية، ولكن لا توجد البيانات المرجعية لشروط الدفع ومجموعة العملاء في Common Data Service.

    ![التحقق من اتصال تطبيق Finance and Operationsعندما لا يكون لديك امتيازات المسؤول](media/verify_fin_ops_2.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في تطبيقات Finance and Operations، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>التحقق من تكوين الكتابة الثنائية في Common Data Service

عندما تقوم بإنشاء بيانات، إذا شاهدت حقل **الشركة** في صفحات في Common Data Service، ففنه يتم تكوين الكتابة الثنائية.

![التحقق من اتصال Common Data Service](media/verify_cds.png)

للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في Common Data Service، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).

للحصول على معلومات حول كيفية عرض تفاصيل الأخطاء في حالة مصادفة أي أخطاء اثناء إنشاء البيانات في Common Data Service، راجع [تمكين وعرض تسجيل تتبع المكونات الإضافية في Common Data Service لعرض تفاصيل الأخطاء](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
