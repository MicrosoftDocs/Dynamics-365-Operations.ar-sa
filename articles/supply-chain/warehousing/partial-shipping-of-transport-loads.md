---
title: شحن جزئي لحمل النقل
description: يشرح هذا المقال كيفية شحن حمل جزئيًا وتأجيل تخطيط القدرة للحمل.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 09e35b8ee39b3635938f46e174e6ba98db7fa627
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907018"
---
# <a name="partial-shipment-of-a-transport-load"></a>شحن جزئي لحمل النقل

[!include[banner](../includes/banner.md)]

وبواسطة إعداد الشحن الجزئي للأحمال، يمكنك التعامل مع أحمال حيث لا يمكن تحديد القدرة حتى تتم إضافة جميع بنود المبيعات إلى حمل. ويمكن بعد ذلك إنهاء العملية عند معرفة عدد البالتات الفعلي. لذلك، يجب ألا تقرر البالتات التي سيتم تعيينها للنقل حتى لحظة تحميل عملية نقل فعلياً خارج المخزون المرحلي.

توفر هذه الميزة بديلاً لتطبيق بنية أكثر صارمةً، حيث يجب عليك تحديد البالتات التي سيتم تعيينها للنقل قبل انتقاء العمل أو إمكانية إنشاء عمل التحميل. وبدلاً من ذلك، يستطيع المستخدمون تكوين الأحمال الفردية لتأكيد شحن جزئي. يمكن بعد ذلك أن تحدث عمليات تحميل النقل لتلك الأحمال. ولذلك، يمكن قسم تخطيط النقل تحميل الأحمال دون الحاجة إلى مراعاة قدرة عمليات النقل الفردية.

في وقت التحميل، يستطيع العاملون تحديد حمل نقل جديد يمكن تحميل بالتة له. بدلاً من ذلك، يمكنهم تحديد حمل نقل موجود. يمكن تسجيل هذه البيانات عن طريق جهاز محمول. ولذلك، يستطيع عدد من عمال المستودع تحميل المخزون من نفس الأحمال أو أحمال مختلفة على نفس الشاحنة. يمكن بعد ذلك شحن الأحمال كليًا أو جزئيًا.

> [!NOTE] 
> لتحميل مخزون من حمل لحمل نقل محدد وشحن الحمل جزئيًا، يجب إنشاء عمل باستخدام فئة تحميل في قالب عمل. لا يمكن تحميل عمل انتقاء عادي من نوع **الانتقاء** إلى تحميل نقل مثل شاحنة.

## <a name="set-up-transport-loads-for-partial-shipment"></a>إعداد أحمال النقل للشحن الجزئي

يشتمل إعداد الشحن الجزئي للأحمال على الإجراءين التاليين.

### <a name="set-the-loading-strategy"></a>تعيين استراتيجية التحميل

يجب عليك تمكين التحميل الجزئي بتعيين استراتيجية التحميل. يمكنك تعيين استراتيجية التحميل بعد إنشاء تحميل.

1. حدد **إدارة المستودعات**\>**أحمال**\>**جميع الأحمال**.
2. حدد حملاً، ثم انقر فوق **عنوان**.
3. في حقل **استراتيجية التحميل**، حدد **شحن التحميل الجزئي المسموح به**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>إنشاء عنصر قائمة لتحميل أحمال النقل

يجب عليك إنشاء عنصر قائمة جديد يتيح نقل الأحمال المُراد تحميلها. يتيح لك حمل نقل تجميع خطوط العمل من حمل واحد أو أحمال متعددة. يمكن شحن كل شيء تمت إضافته إلى حمل النقل بعد ذلك باستخدام ماسح ضوئي جهاز محمول.

1. حدد **إدارة المستودعات** \> **الإعداد** \> **الجهاز المحمول** \> **عناصر الجهاز المحمول**.
2. حدد **جديد**، ثم في حقل **الوضع**، حدد **العمل**.
3. قم بتعيين خيار **استخدام العمل الموجود** إلى **نعم**.
4. في علامة التبويب **عام**، في حقل **موجه بواسطة**، حدد **تحميل النقل**.
5. لتمكين تأكيد الشحن على ماسح ضوئي جهاز محمول، في حقل **نوع تأكيد الشحن المسموح به**، حدد **حمل النقل**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>تأكيد شحن تحميل نقل من العميل

يتيح لك هذا الإعداد تأكيد تحميل نقل يحتوي على حمل كامل أو حمل محمل جزئيًا ليتم شحنه.

1. حدد **إدارة المستودعات**\>**الأحمال**\>**أحمال النقل**.
2. في "جزء الإجراءات"، في علامة التبويب **الشحن والاستلام‬**، في مجموعة **التأكيد**، حدد **نقل**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]