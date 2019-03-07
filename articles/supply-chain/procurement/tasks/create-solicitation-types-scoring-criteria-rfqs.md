---
title: إنشاء أنواع طلبات ومعايير تسجيل النقاط‬ لطلبات عروض الأسعار
description: يوضح هذا الدليل كيفية إنشاء نوع طلب وربطه بأسلوب تسجيل النقاط.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14fd7d0bfa17427883f97c5e0a72044016d4965e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "344606"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>إنشاء أنواع طلبات ومعايير تسجيل النقاط‬ لطلبات عروض الأسعار

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الدليل كيفية إنشاء نوع طلب وربطه بأسلوب تسجيل النقاط. ويُظهر أيضًا كيفية استخدام نوع الطلب على طلب عرض أسعار (RFQ) الذي يعيّن عندئذٍ أسلوب تسجيل النقاط الافتراضي. يقوم عادةً مدير المشتريات بتنفيذ هذه المهام. يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك. يجب أن يكون لديك أسلوب تسجيل نقاط قبل البدء.


## <a name="create-a-solicitation-type"></a>إنشاء نوع طلب
1. انتقل إلى التدبير وتحديد الموارد > إعداد > طلب عرض أسعار > نوع الطلب.
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في حقل "أسلوب تسجيل النقاط"، حدد أسلوب تسجيل النقاط الذي تريد استخدامه لنوع الطلب هذا.
6. انقر فوق "حفظ".
7. قم بإغلاق الصفحة.

## <a name="use-the-solicitation-type"></a>استخدام نوع الطلب
1. انتقل إلى التدبير وتحديد الموارد > طلبات عروض الأسعار‬ > كل طلبات عروض الأسعار‬.
2. انقر فوق "جديد".
3. في الحقل "نوع الطلب"، حدد نوع الطلب الذي قمت بإنشائه للتوّ. 
    *   
4. انقر فوق "موافق".
5. انقر فوق "معايير تسجيل النقاط".
    * معايير تسجيل النقاط التي تظهر هي تلك المعايير الخاصة بأسلوب تسجيل النقاط المقترن بنوع الطلب. يمكنك اختيار إضافة معايير أو حذفها في هذه الصفحة. من الممكن أيضًا إضافة معايير جديدة عن طريق نسخها من أساليب أخرى لتسجيل النقاط.  
6. انقر فوق "نسخ المعايير".
7. في الحقل "أسلوب تسجيل النقاط"، أدخل قيمة أو حددها.
8. انقر فوق "موافق".
9. قم بإغلاق الصفحة.

