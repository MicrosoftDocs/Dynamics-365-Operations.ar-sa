---
title: التغيير الأساسي في حسابات ضرائب ICMS-DIF للمنتجات من المورّدين في ولايات أخرى
description: توفر هذه المقالة تكوين الحسابات لنوع ضريبة ICMS-DIF عند استلام مستند مالي في ولاية ريو غراندي دو سول (RS) أو ساو باولو (SP) البرازيلية.
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218638"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>تغيير الأساس (قاعدة مزدوجة) في حسابات ضريبة ICMS-DIF للمنتجات من الموردين في الولايات الأخرى

توضح هذه المقالة تكوين الحسابات لنوع الضريبة **ICMS-DIF** عند استلام مستند مالي في ولاية ريو غراندي دو سول (RS) أو ساو باولو (SP) البرازيلية.

وفقًا للتعريف الوارد في قانون الولاية ، يجب أن تتبع Imposto sobre Circulação de Mercadorias e Serviços (ICMS) التي يتم تحصيلها هذه القاعدة:

*ICMS التي يجب تحصيلها* = ([(*مبلغ العملية* – *ICMS من المصدر*) ÷ (1 – *ICMS داخلي %*)] × *ICMS داخلي %*) – *مبلغ ICMS من المصدر*

## <a name="example"></a>مثال

تتلقى شركة برازيلية في ولاية RS مستندًا ماليًا لعملية شراء من مورّد في ولاية SP. يجب على الشركة تحصيل النسبة المئوية للفرق في ICMS بين ولاية RS‏ (18 بالمئة) وولاية SP ‏(12 بالمئة). ومع ذلك، يجب حساب الأساس وفقًا للقاعدة السابقة.

- **مبلغ العملية:** 1,000.00 ريال برازيلي (ريال برازيلي 1,000.00)
- **ICMS بين الولايات:** 120.00ريال برازيلي
- **نسبة ICMS في ولاية RS:** 18 بالمئة
- **ICMS المطلوب تحصيلها في ولاية RS:** (\[(1,000 – 120) ÷ (1 – 0.18)\] × 0.18 ) – 120 = R$ 73.17 

## <a name="resolution"></a>القرار

لحساب ICMS التفاضلي (ICMS-DIF) وفقًا لقواعد ولاية RS، يجب عليك إعداد أكواد ضرائب المبيعات ومجموعة ضرائب المبيعات بالطريقة التالية:

1. قم بإنشاء كود ضريبة مبيعات لاستلام ICMS بنسبة 12 بالمئة (للولاية الأخرى). يتم استخدام هذا الكود لتسجيل مبلغ الضريبة المستحقة من المورّد.
2. قم بإنشاء كود ضريبة مبيعات لتحصيل ICMS-DIF. يجب أن يكون لكود ضريبة المبيعات هذا نسبة مئوية تبلغ 18 بالمائة (لولايتك) لتحديد الفرق بين 18 بالمئة و 12 بالمئة. عيّن نوع الضريبة إلى **ICMS-DIF**. يجب تحديد كود ضريبة المبيعات هذا بالطريقة التالية في معلمات الحساب:

    - في حقل **الأصل**، حدد **النسبة المئوية لإجمالي المبلغ‬**
    - في حقل **‏‫القاعدة الهامشية‬** حدد **‏‫المبلغ الصافي لكل بند‬**.
    - حدد كود الضرائب بحيث يكون له قيمة مالية من **3**. بهذه الطريقة ، سيتم إنشاء حركة التعديل تلقائيًا عند تمكين الوحدة النمطية **الدفاتر المالية**.
    - في تكوين مجموعة ضرائب المبيعات، حدد الخيار **ضريبة الانتفاع** لكود ضريبة المبيعات **ICMS-DIF**.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>استخدم معدل ضريبة دلتا في تكوين أكواد ضريبة المبيعات ICMS-DIF ثنائية القاعدة

عند استخدام الإعدادات الموصوفة سابقًا ، سيتم حساب كود ضريبة المبيعات **ICMS-DIF** في القاعدة المزدوجة. ومع ذلك ، يصبح معدل الضريبة الاسمي 18 بالمائة ، وهو ما يختلف عن معدل 6 بالمائة في القاعدة الأساسية البسيطة. يتسبب هذا الاختلاف في حدوث مشكلات عدم تناسق في المستندات المالية وإعداد التقارير الضريبية. اعتبارًا من الإصدار 10.0.29 لـ Microsoft Dynamics 365 Finance version 10.0.29, يمكنك تمكين ميزة **(البرازيل) تكوين معدل ضريبة دلتا في رمز ضريبة ICMS-DIF للحالة الأساسية المزدوجة** في **‏‫إدارة الميزات** لإزالة عدم الاتساق.

- بالإضافة إلى إكمال الخطوات الواردة في القسم السابق ، حدد **ICMS 12** كود ضريبة المبيعات في **ضريبة المبيعات في حقل ضريبة المبيعات‬** .
- قم بتعيين معدل الضريبة لرمز ضريبة المبيعات **ICMS-DIF** على 18 بالمائة. سيعرض الحقل **النسبة المئوية / المبلغ** معدل الضريبة الاسمي على أنه 6 بالمائة.

> [!NOTE]
> يجب تعيين رموز ضريبة المبيعات **ICMS-DIF** و **ICMS 12** في نفس مجموعة ضريبة المبيعات.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>تغيير الأساس (قاعدة مزدوجة) في حسابات ضريبة ICMS-DIF للمنتجات إلى المستهلكين من غير دافعي الضرائب (DIFAL) في الولايات الأخرى

تمكين ميزة **(البرازيل) الحساب المزدوج الأساسي لـ ICMS-DIFAL في معاملات المبيعات** في **إدارة الميزات** لدعم تغيير أساس ICMS-DIF بشأن التداول للمستهلكين غير دافعي الضرائب من دولة أخرى. يصبح نموذج رمز ضريبة المبيعات ICMS-DIF ساريًا في أوامر المبيعات وحركات الفاتورة ذات النص الحر.

تمكين ميزة **(البرازيل) الحساب ثنائي القاعدة لـ ICMS-DIFAL لحالات IPI** في **إدارة الميزات** لدعم السيناريوهات حيث يكون التداول مع المستهلكين من غير دافعي الضرائب من دولة أخرى مسؤولاً أيضًا عن Imposto sobre Produtos Industrializados (IPI). سيتم التعرف على مبلغ الضريبة الخاص برمز ضريبة المبيعات IPI وتطبيقه في قاعدة ضريبة ICMS-DIFAL.

- في رأس أمر المبيعات أو الفاتورة ذات النص الحر ، في علامة التبويب السريعة **المعلومات المالية** يجب تعيين خيار **المستخدم النهائي** على **نعم**.
- في رأس أمر الشراء أو فاتورة المورد ، في علامة التبويب السريعة **المعلومات المالية** يجب تعيين خيار **الاستخدام والاستهلاك** على **نعم**.
