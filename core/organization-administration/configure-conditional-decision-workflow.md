---
title: "تكوين قرار شرطي في سير عمل‬"
description: "استخدم الإجراء التالي لتكوين خصائص قرار شرطي."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c21c8e33ab3a88e1b93ca81d6f0770f1c77fe139
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>تكوين قرار شرطي في سير عمل‬

[!include[banner](../includes/banner.md)]


استخدم الإجراء التالي لتكوين خصائص قرار شرطي.

القرار المشروط هو نقطة يتفرع عندها سير العمل إلى فرعين. لتكوين قرار شرطي، في محرر سير العمل، انقر بزر الماوس الأيمن فوق القرار الشرطي، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.

## <a name="name-a-decision"></a>تسمية قرار
اتبع الخطوات التالية لإدخال اسم للقرار الشرطي.
1.  في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
2.  في حقل **الاسم**، أدخل اسمًا فريدًا للقرار الشرطي.

## <a name="set-conditions"></a> تعيين الشروط
يحدد النظام العلامة التجارية التي يجب استخدامها عن طريق تقييم المستند المرسل لتحديد ما إذا كان يستوفي شروطًا معينة.
1.  في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
2.  انقر فوق **إضافة شرط**.
3.  يتيح إمكانية إدخال شرط.
4.  أدخل الشروط الإضافية، إذا كانت مطلوبة.
5.  للتأكد من تكوين الشروط التي قمت بإدخالها بشكل صحيح، أكمل الخطوات التالية:
    1.  انقر فوق **اختبار** لفتح النموذج **اختبار حالة سير العمل**.
    2.  حدد سجلاً في المنطقة **‏‏التحقق من الشرط** من النموذج.
    3.  انقر فوق **اختبار**. سيقوم النظام بتقييم السجل لمعرفة ما إذا كان يستوفي الشروط التي قمت بتحديدها أم لا.
    4.  انقر فوق **موافق** أو **إلغاء الأمر** للعودة إلى النموذج **خصائص**.






