---
title: مشكلات في تسوية البيانات لتقرير Z
description: يوضح هذا المقال أن المستخدمين قد يكون لهم تجربة في تسوية البيانات الخاصة بتقرير Z في "Commerce headquarters". كما يوضح الأسباب الجذرية المحتملة والحلول التي يمكن أن تساعد في منع التواجدات المستقبلية.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832112"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>مشكلات في تسوية البيانات لتقرير Z

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة مصادفة مشكلات في تسوية البيانات الخاصة بتقرير Z في Microsoft Dynamics 365 Commerce headquarters. وإنه يصف المشكلات التي قد يواجهها المستخدمون مع تسوية البيانات والأسباب الجذرية المحتملة والحلول التي يمكن أن تساعد في منع التواجدات المستقبلية.

## <a name="description"></a>‏‏الوصف‬

- يوجد عدم تطابق بين المبالغ التي يتم عرضها في تقرير Z والإجماليات التي يتم عرضها في الكشف المحسوب.
- تحتوي الحركة الموجودة في headquarters على عدد غير صحيح من أصناف البند، أو يوجد عدم تطابق بين إجمالي البند وإجمالي الحركة.
- عدد الحركات التي تظهر في وردية في headquarters أقل من عدد الحركات في تقرير Z.
- فشل ترحيل كشف الحساب لأحد الأسباب السابقة.

### <a name="root-cause"></a>السبب الأساسي

إن السبب الجذري الأكثر شيوعًا لأعراض العرض الموضحة سابقًا هو إنشاء معرفات المعاملات المكررة في قاعدة بيانات القناة. يمكن إنشاء معرفات الحركة المكررة للأسباب التالية:

- يتم تلف تخزين قاعدة البيانات المحلية لنقطة البيع الحديثة (MPOS).
- تحتوي MPOS على بعض الحركات في الوضع "غير متصل"، ويتم إعادة تنشيطها باستخدام حساب له حق الوصول إلى قاعدة البيانات غير المتصلة.
- توجد مشكلة في التخصيص المرتبط بإنشاء معرفات الحركات.

## <a name="resolution"></a>القرار

عادةً، يعتمد Commerce على تسلسل رقمي لإنشاء معرفات الحركات التسلسلية. إذا لم يتمكن النظام من تحديد التسلسل الرقمي الذي تم استخدامه لأي سبب من الأسباب، فإنه يتم إنشاء معرف حركة مكرر. 

لإصلاح مشكلة معرف الحركة المكررة، قم بإنشاء تذكرة دعم للتحقق مما إذا كان يمكن إصلاح بيانات الحركة أم لا. في بعض الحالات، على سبيل المثال عند عدم وجود فقدان للبيانات في headquarters، فلن يكون إصلاح البيانات ممكنًا أو مطلوبًا.

للمساعدة في منع حدوث هذه المشكلة في المستقبل، فإنه يجب تمكين الميزة **‬‏‫تمكين معرف الحركة الجديد لتجنب تكرار معرفات الحركات** في headquarters. تم تقديم هذه الميزة في Commerce، الإصدار 10.0.19. وإنها تساعد على منع إنشاء معرفات الحركات التسلسلية من خلال التأكد من إنشاء معرف حركة فريد لكل حركة. لمزيد من المعلومات حول هذه الميزة، راجع [منع معرفات حركات مكررة‬](../channel-setup-retail.md#ensure-unique-transaction-ids).