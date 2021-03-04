---
title: تعقب مصادر المرشحين في Attract
description: يوفر هذا الموضوع معلومات حول تعقب المصدر لملفات تعريف المرشحين واستمارات التقديم الخاصة بهم.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460197"
---
# <a name="track-candidate-sources-in-attract"></a>تعقب مصادر المرشحين في Attract

[!include [banner](includes/banner.md)]

> [!NOTE] 
> تتوفر الوظيفة المذكورة في هذا الموضوع كجزء من إصدار مراجعة المعاينة. المحتوى والوظيفة عرضة للتغيير. لاستخدام هذه الميزة، اطلب من مسؤول تمكينها باستخدام **إعدادات المسؤول** في Attract. سيوفر إصدار مستقبلي لك تقارير تعقب المصدر. للحصول على مزيد من المعلومات، راجع [الوصول إلى ميزات المعاينة في Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

عندما يقدم المرشحون طلبات الحصول على الوظيفة، يقوم Attract بشكل تلقائي بتعقب استمارات تقديم هؤلاء المرشحين، ويوفر لك معلومات قيّمة لمساعدتك في توجيه الجهود التي تبذلها في مجال التعيين. بإمكان مسؤولي التعيين ومدراء التوظيف أيضًا تحديد مصدر استمارة التقديم أثناء إضافة مرشح إلى مجموعة وظائف أو مجموعة مواهب.‬

يمكنك عرض مصدر استمارة التقديم في نشاط استمارة التقديم ضمن علامة التبويب **النشاط**، وكذلك الأمر في سجل التوظيف ضمن **ملف التعريف** في مجموعات المواهب.= يمكنك العثور على مصدر ملف تعريف المرشح في تفاصيل المرشح ضمن علامة التبويب **ملف التعريف** في مجموعات استمارات التقديم والمواهب.

> [!NOTE] 
> يمكنك العثور على قوالب العملية في [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>المصادر المكوّنة مسبقًا

تحتوي قائمة المصادر الافتراضية على مصادر استمارات التقديم الشائعة. تتضمن بعض أنواع المصادر، مثل **لوحة الوظائف** و **الشبكة الاجتماعية** تفاصيل مصادر إضافية. على سبيل المثال، تتضمن **الشبكة الاجتماعية** Facebook وTwitter. يسمح لك نوع المصدر **إحالة‬** بتحديد موظف داخلي كمحيل. تتضمن قائمة المصادر الافتراضية المصادر التالية المعرفة مسبقًا:

-   موقع وظائف Attract

-   الوكالة

-   معرض الوظائف

-   تسويق الشركة

-   المؤتمرات والمعارض التجارية

-   النقابات المهنية

-   لوحة الوظيفة

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   المجلات والمنشورات

-   الشبكة الاجتماعية

    -   Facebook

    -   Twitter

-   التوظيف في الجامعة

-   LinkedIn

-   الإعلانات المبوبة

-   إحالة

-   مُضاف من قِبل مسؤول التعيين

-   ‏‏غير ذلك

## <a name="customize-the-source-list"></a>تخصيص قائمة المصادر 

يمكنك توسيع قائمة المصادر بحيث تتضمن مصادر استمارات تقديم إضافية. لتخصيص هذه القائمة، اتبع الإرشادات الموجودة في [توسيع مجموعات الخيارات في Attract‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). حرر الكيان **TalentSource‎** بحيث يتضمن مصادر إضافية. 

لتجنب التأثير السلبي على واجهة المستخدم (UI)، لا تعمل على تحرير أو حذف قيم تعداد (وليس أسماء) **TalentCategory** لما يلي:

- **إحالة**
- **LinkedIn**
- **‏‏غير ذلك**

بدلاً من ذلك، يمكنك توسيع تعداد **TalentSource** لإضافة أنواع أخرى من المصادر.


[!INCLUDE[footer-include](../includes/footer-banner.md)]