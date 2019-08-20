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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a3e0d00d674af913953d7fd01183b0289c20d3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844080"
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

