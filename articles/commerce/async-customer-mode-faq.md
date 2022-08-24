---
title: الأسئلة المتداولة حول وضع إنشاء العميل غير المتزامن
description: توفر هذه المقالة إجابات للأسئلة المتداولة حول وضع إنشاء العملاء غير المتزامن في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229864"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>الأسئلة المتداولة حول وضع إنشاء العميل غير المتزامن

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

توفر هذه المقالة إجابات للأسئلة المتداولة حول وضع إنشاء العملاء غير المتزامن (غير المتزامن) في Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>لماذا لا يمكنني تمكين الميزة "تمكين تحرير العملاء في الوضع غير المتزامن" ؟

قبل تمكين **الميزة تمكين تحرير العملاء في الوضع** الغير متزامن ، يجب تمكين الميزات التالية:

- تحسينات في الأداء لأوامر العملاء ومعاملات العملاء
- تمكين إنشاء العملاء غير المتزامن المحسن
- تمكين الإنشاء غير المتزامن لعناوين العملاء

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>لماذا لا نزال نقوم برؤية استدعاءات خدمة الوقت الحقيقي التي تم اجراؤها علي Commerce headquarters بعد تمكين الميزة "تمكين تحرير العملاء في الوضع غير المتزامن" ؟

تحدث هذه المشكلة في حاله Commerce Data Exchange عدم تشغيل مهام (CDX) لضمان مزامنة حالة الميزة وبيانات تعريف القنوات الأخرى مع القناة. قبل أعاده محاولة السيناريو ، تأكد من تشغيل مهام CDX التالية في Commerce headquarters:

- 1110 (التكوين العمومي)
- 1010 (العملاء)
- 1070 (تكوين القناة)

قد لا تظهر البيانات التي تم تخزينها مؤقتا في Commerce Scale Unit (CSU) علي الفور في Commerce headquarters بعد تشغيل وظائف CDX.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>لماذا لا تظهر Commerce headquarters الخاصة بإنشاء العملاء أو التحديثات من نقطه البيع (POS) أو قناه التجارة الكترونيه ؟

تأكد من اجراء الإجراءات التالية بالترتيب الواردة به هنا.

1. قم بتشغيل CDX P-job في Commerce headquarters للتأكد من أن بيانات العميل غير المتزامنة المخزنة في **RETAILASYNCCUSTOMERV2**، **RETAILASYNCADDRESSV2**، **RETAILASYNCCUSTOMERCONTACT**، **RETAILASYNCCUSTOMERAFFILIATION**، و **RETAILASYNCCUSTOMERATTRIBUTEV2** الجداول متوفرة في Commerce headquarters.
1. تشغيل وظيفة مجموعه "مزامنة العملاء والقنوات **" في " Commerce headquarters"**. بعد تنفيذ مهمة المجموعة بنجاح ، يكون لكافة **السجلات التي تمت معالجتها بنجاح من الجداول المذكورة سابقا حقل OnlineOperationCompleted** معينا علي القيمة **1**.
