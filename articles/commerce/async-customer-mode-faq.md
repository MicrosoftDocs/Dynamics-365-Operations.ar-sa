---
title: الأسئلة المتداولة حول وضع إنشاء العميل غير المتزامن
description: توفر هذه المقالة إجابات للأسئلة المتداولة حول وضع إنشاء العملاء غير المتزامن في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690192"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>الأسئلة المتداولة حول وضع إنشاء العميل غير المتزامن

[!include [banner](includes/banner.md)]

توفر هذه المقالة إجابات للأسئلة المتداولة حول وضع إنشاء العملاء غير المتزامن (غير المتزامن) في Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>لماذا لا يمكنني تمكين الميزة "تمكين تحرير العملاء في الوضع غير المتزامن" ؟

قبل تمكين **الميزة تمكين تحرير العملاء في الوضع** الغير متزامن ، يجب تمكين الميزات التالية:

- تحسينات في الأداء لأوامر العملاء ومعاملات العملاء
- تمكين إنشاء العملاء غير المتزامن المحسن
- تمكين الإنشاء غير المتزامن لعناوين العملاء

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>لماذا لا نزال نقوم برؤية استدعاءات خدمة الوقت الحقيقي التي تم اجراؤها علي Commerce headquarters بعد تمكين الميزة "تمكين تحرير العملاء في الوضع غير المتزامن" ؟

تحدث هذه المشكلة في حاله Commerce Data Exchange لم يتم تشغيل وظائف (CDX) لضمان مزامنة حالة الميزة وبيانات تعريف القناة الأخرى مع القناة. قبل إعادة محاولة السيناريو ، تأكد من تشغيل وظائف CDX التالية في Commerce headquarters:

- 1110 (التكوين العمومي)
- 1010 (العملاء)
- 1070 (تكوين القناة)

قد لا تظهر البيانات التي تم تخزينها مؤقتا في Commerce Scale Unit (CSU) علي الفور في Commerce headquarters بعد تشغيل وظائف CDX.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>لماذا لا تظهر Commerce headquarters الخاصة بإنشاء العملاء أو التحديثات من نقطه البيع (POS) أو قناه التجارة الكترونيه ؟

تأكد من تنفيذ الإجراءات التالية بالترتيب المذكور هنا.

1. قم بتشغيل CDX P-job في Commerce headquarters لضمان تخزين بيانات العميل غير المتزامنة في ملف **RETAILASYNCCUSTOMERV2**، **RETAILASYNCADDRESSV2** ، **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** و **RETAILASYNCCUSTOMERATTRIBUTEV2** الجداول.
1. تشغيل وظيفة مجموعه "مزامنة العملاء والقنوات **" في " Commerce headquarters"**. بعد تنفيذ مهمة المجموعة بنجاح ، يكون لكافة **السجلات التي تمت معالجتها بنجاح من الجداول المذكورة سابقا حقل OnlineOperationCompleted** معينا علي القيمة **1**.

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>كيف يمكنني معرفه أداره العملاء التي فشلت في الوضع غير المتزامن ، وكيف يمكنني اجراء التغييرات إذا كانت مطلوبه ؟

لعرض جميع عمليات الوضع غير المتزامن وحالة المزامنة الخاصة بها ، انتقل إلى Commerce headquarters **التجارة والتجزئة \> العملاء \> حالة مزامنة العميل**. لاجراء تغييرات ، قم بتحرير عمليه معينه ، وقم بتحديث الحقول ، وحدد **حفظ** ، ثم حدد **تزامن** لمزامنة التغييرات.

