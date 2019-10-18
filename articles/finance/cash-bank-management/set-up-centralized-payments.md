---
title: إعداد الدفعات المركزية
description: ‏‫اتبع هذه الخطوات لإعداد معالجة المدفوعات في كيان قانوني واحد نيابة عن الكيانات القانونية الأخرى في مؤسستك.
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b47f819730ae221568e625a1b218e046927e41
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188178"
---
# <a name="set-up-centralized-payments"></a>إعداد الدفعات المركزية

[!include [banner](../includes/banner.md)]

‏‫اتبع هذه الخطوات لإعداد معالجة المدفوعات في كيان قانوني واحد نيابة عن الكيانات القانونية الأخرى في مؤسستك. وقبل البدء، يجب إكمال الإعداد التالي:‬

-   إنشاء كيانات قانونية.
-   إعداد معلمات دفتر الأستاذ العام ومخططات الحسابات.
-   إعداد معلمات الحسابات الدائنة ومعلمات الحسابات المدينة (اعتماداً على الوحدات التي تستخدم المدفوعات المركزية).
-   إعداد المحاسبة بين الشركات الشقيقة.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>إعداد تدرج هرمي مؤسسي للمدفوعات المركزية
يجب إعداد تدرج هرمي مؤسسي للمدفوعات المركزية. يتم استخدام التدرج الهرمي المؤسسي نفسه لمعالجة المدفوعات المركزية للمورد والعميل. **ملاحظة:** بالنسبة للمدفوعات المركزية، لا تهم بنية التدرج الهرمي. وسيتمكن أي كيان قانوني في التدرج الهرمي من معالجة المدفوعات نيابة عن أي كيان قانوني آخر في التدرج الهرمي. وفي صفحة **التدرجات الهرمية للمؤسسات**، يمكنك إنشاء تدرج هرمي للمؤسسات جديد. في حقل **الغرض**، يجب تحديد **المدفوعات المركزية‬**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>إعداد حساب بين الشركات الشقيقة للمدفوعات المركزية
عندما تتم تسوية حركات الدفع في الكيان القانوني الحالي باستخدام الفواتير في الكيانات القانونية الأخرى، يتم إنشاء حركات، مستحق حتى ومستحق من، مناسبة لكل كيان قانوني. ويجب تحديد الكيان القانوني الذي يتم به ترحيل الخصومات النقدية القابلة للتطبيق أو مبالغ ربح أو خسارة محققة. وقبل البدء في ذلك، حدد أي الكيانات القانونية التي ستستخدمها لمعالجة مدفوعات المورد والعميل. وإذا كان كيان قانوني واحد يعالج مدفوعات المورد ولكن هناك كيان قانوني آخر يعالج مدفوعات العميل، فيجب عليك التبديل إلى كل كيان قانوني. في صفحة **المحاسبة بين الشركات الشقيقة**، يمكنك تحديد سجل العلاقة بين الشركات الشقيقة لكيان قانوني سيقوم بمعالجة المدفوعات نيابةً عنه. 

في علامة التبويب ‬‏‫**‬‏‫المدفوعات المركزية‬‏‫**‬‏‫، يمكنك تحديد ما إذا كان يتم ترحيل الخصومات النقدية إلى الكيان القانوني الخاص بالدفع (أو حركة أخرى من شأنها تخفيض رصيد حساب المورد) أو الكيان القانوني الخاص بالفاتورة (أو حركة أخرى من شأنها زيادة رصيد حساب المورد).‬ ويعمل هذا التحديد مع حقل **إدارة الخصم النقدي** في صفحتي **معلمات الحسابات الدائنة** و**معلمات الحسابات المدينة**. بالنسبة لحالات الدفع بالزيادة والفروق النقدية، يتم استخدام الإعداد الموجود في كيان الدفع القانوني. وبالنسبة لحالات الدفع بالنقصان والفروق النقدية، يتم استخدام الإعداد الموجود في كيان إصدار الفواتير القانوني.

## <a name="map-vendor-accounts-across-legal-entities"></a>تعيين حسابات المورد عبر الكيانات القانونية
وفي حالة الدفع لمورد من إحدى الكيانات القانونية وكنت ترغب في تحديد الفواتير لذلك المورد في الكيانات القانونية الأخرى، يجب التأكد من أن جميع حسابات المورد المتناظرة في كل كيان قانوني تستخدم معّرف دفتر العناوين نفسه. وفي حالة استلام دفعة من عميل يدفع الفواتير في أكثر من كيان قانوني، يجب عليك التأكد من أن كافة حسابات العملاء المتناظرة في كل كيان قانوني تستخدم نفس معّرف دفتر العناوين.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>إعداد ترحيل ملفات التعريف للمدفوعات المركزية
عند إنشاء دفعة في كيان قانوني، تعمل على تسوية الفواتير في كيانات قانونية أخرى، يجب أن تكون معرفات ملفات تعريف الترحيل متشابهة في الكيانين القانونيين. وللمساعدة على ضمان إنشاء المدفوعات بشكل صحيح، في كل كيان قانوني للفاتورة، قم بإعداد ملف تعريف الترحيل مقابل لملفات تعريف الترحيل المستخدمة في كيان الدفع القانوني. ‏‫قم بالتبديل إلى الكيان القانوني الأول للفاتورة، ثم في صفحة **‬‏‫ملفات تعريف ترحيل المورد‬‏‫**، يمكنك إنشاء ملف تعريف ترحيل جديد أو تحرير ملف تعريف ترحيل موجود. ولا يلزم أن تتطابق التحديدات التي تقوم بها لملف تعريف الترحيل في الكيان القانوني للفاتورة مع إعداد ملف تعريف الترحيل في الكيان القانوني الخاص بالدفع.‬

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>إعداد طرق الدفع للمدفوعات المركزية
عند إنشاء دفعة في كيان قانوني، تعمل على تسوية الفواتير في كيانات قانونية أخرى، يجب أن تكون طريقة الدفع متشابهة في الكيانين القانونيين. وللمساعدة على ضمان إنشاء المدفوعات بشكل صحيح، في كل كيان قانوني للفاتورة، قم بإعداد طريقة دفع ‬مناسبة لطرق الدفع المستخدمة في كيان الدفع القانوني. وقم بالتبديل إلى الكيان القانوني الأول للفاتورة، ثم في صفحة **طرق الدفع**، يمكنك إنشاء طريقة جديدة للدفع أو تحرير طريقة دفع موجودة. لا يلزم أن تتطابق التحديدات، التي يتم إجراؤها على طريقة الدفع في كيان إصدار الفواتير القانوني، مع الطريقة التي تم بها إعداد طريقة الدفع في كيان الدفع القانوني.

## <a name="set-up-default-descriptions"></a>إعداد الأوصاف الافتراضية
يمكنك تحديد الأوصاف الافتراضية لإيصالات التسوية بين الشركات الشقيقة. يتم تضمين الوصف الافتراضي في الحركتين، مستحق حتى ومستحق من، أثناء عملية التسوية عبر الشركة. وفي صفحة **الأوصاف الافتراضية**، يمكنك إنشاء أوصاف جديدة لكلٍّ من **تسوية العميل بين الشركات الشقيقة** و**تسوية المورد بين الشركات الشقيقة** بتحديد اللغة ثم إدخال النص.


