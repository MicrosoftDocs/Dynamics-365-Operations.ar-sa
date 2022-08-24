---
title: فحص جودة البضائع
description: يصف هذا المقال كيفية معالجة أوامر الجودة.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219023"
---
# <a name="inspect-the-quality-of-goods"></a>فحص جودة البضائع

[!include [banner](../../includes/banner.md)]

يصف هذا المقال كيفية معالجة أوامر الجودة. عادة ما يتم إجراء عمليات فحص الجودة بواسطة موظف الجودة.

الموارد البشرية [بيانات العرض التوضيحي](../../../fin-ops-core/fin-ops/get-started/demo-data.md) القياسية، يمكنك استخدامها لإكمال الإجراءات في هذا المقال. لاستخدام بيانات العرض التوضيحي، حدد الكيان القانوني *USMF* قبل البدء. يجب عليك بعد ذلك تأكيد أمر الشراء *000016* وترحيل إيصال استلام المنتجات. يتم إنشاء أمر الجودة تلقائيًا.

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
