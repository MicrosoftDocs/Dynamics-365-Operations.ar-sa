---
title: فحص جودة البضائع
description: يصف هذا الموضوع كيفية معالجة أوامر الجودة.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956124"
---
# <a name="inspect-the-quality-of-goods"></a>فحص جودة البضائع

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع كيفية معالجة أوامر الجودة. عادة ما يتم إجراء عمليات فحص الجودة بواسطة موظف الجودة.

إذا تم تثبيت بيانات العرض التوضيحي القياسية، يمكنك استخدامها لإكمال الإجراءات في هذا الموضوع. لاستخدام بيانات العرض التوضيحي، حدد الكيان القانوني *USMF* قبل البدء. يجب عليك بعد ذلك تأكيد أمر الشراء *000016* وترحيل إيصال استلام المنتجات. يتم إنشاء أمر الجودة تلقائيًا.

## <a name="step-1-select-a-quality-order"></a>الخطوة 1: تحديد أمر جودة

لتحديد أمر جودة، اتبع هذه الخطوات.

1. انتقل إلى‬ **‏‫إدارة المخزون \> المهام الدورية‬ \> إدارة الجودة \> أوامر الجودة**.
1. حدد أمر الجودة الذي تم إنشاؤه قبل بدء هذا الإجراء.

## <a name="step-2-record-test-results"></a>الخطوة 2: تسجيل نتائج الاختبار

لتسجيل نتائج الاختبار، اتبع الخطوات التالية.

1. حدد **النتائج**.
1. حدد **تحرير**.
1. في الحقل **كمية النتائج‬**، أدخل رقمًا.
1. في حقل **النتيجة**، حدد السجل المطلوب. في هذا المثال، تستند النتيجة إلى ناتج محدد مسبقًا. عادة، سوف تسجل نتيجة اختبار أكثر تحديدًا، مثل الحجم أو البعد الآخر.
1. حدد **حفظ**.
1. قم بإغلاق الصفحة.

## <a name="step-3-validate-the-quality-order"></a>الخطوة 3: التحقق من صحة أمر الجودة

للتحقق من صحة أمر الجودة، اتبع هذه الخطوات.

1. حدد **التحقق من الصحة**.
1. في حقل **تم التحقق بواسطة**، حدد المستخدم الذي يقوم بالفحص.
1. حدد **تحديد**.
1. حدد **موافق**.
1. قم بإغلاق الصفحة.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
