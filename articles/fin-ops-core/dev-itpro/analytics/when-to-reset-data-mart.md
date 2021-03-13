---
title: متى يتم أعاده تعيين متجر البيانات
description: يسرد هذا الموضوع الحالات التي قد يتم تحسينها عن طريق أعاده تعيين متجر البيانات والظروف التي فيها أعاده تعيين متجر البيانات من المحتمل ان تساعدك.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093202"
---
# <a name="when-to-reset-a-data-mart"></a>متى يتم أعاده تعيين متجر البيانات

قد تستغرق عمليه أعاده تعيين متجر البيانات وقتا طويلا. استنادا إلى الحالات، قد لا يكون هذا الاجراء هو الحل المطلوب. يسرد هذا الموضوع الحالات التي قد يتم تحسينها عن طريق أعاده تعيين متجر البيانات والظروف التي فيها أعاده تعيين متجر البيانات من المحتمل ان تساعدك.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>متى تحتاج متجر أعاده تعيين البيانات؟
اطلع علي الاسئله التالية قبل أعاده تعيين متجر البيانات. الاجابه بنعم لأحد الاسئله أو أكثر قد يشير إلى ان مؤسستك يمكن ان تستفيد من أعاده تعيين متجر البيانات.

- تمت استعادة قاعدة بيانات التطبيق، ولكن لم تتم استعادة قاعدة بيانات متجر البيانات.
- تظهر بيانات غير صحيحه لفتره محاسبيه، وليست نتيجة لمشكله في تصميم التقرير.
- تظهر بيانات غير صحيحه لفتره محاسبيه ، ويتم سرد السجلات ضمن محاولات التكامل في صفحه **حاله التكامل** في مصمم التقرير (بدء تشغيل مصمم التقارير وتحديد **الادخالات > حاله التكامل**).
- لقد قمت بفتح حدث دعم وقام مهندس دعم بإرشادك لأعاده تعيين متجر البيانات كجزء من خطوه استكشاف الأخطاء وإصلاحها.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>عندما لا يكون من المناسب أعاده تعيين متجر البيانات؟
توجد بعض الحالات عندما لا نوصي باعاده تعيين متجر البيانات. تشمل هذه المهام ما يلي. 

- في اي وقت لا يتم سرد السبب في هذا الموضوع.
- مواجهه مشكلات في الأداء مقترنة بمزامنة البيانات. في هذه الحالة، قد لا تساعد أعاده تعيين متجر البيانات.
- إذا كان لديك نقش أعاده تعيين متكرر نتيجة لأي من الأسباب التالية: 
  - **البيانات المفقودة** - أولا، استبعاد مشاكل تصميم التقرير وإصدارات مزامنة البيانات، علي سبيل المثال، لاحظ انه لم يتم تشغيل خريطة الحقيقة نظرا لأنه قد تم نشر البيانات المفقودة.
  - **حاله التكامل العالق** - إذا كان التكامل بطيئا أو إذا كان عالقا، فان أعاده تعيين البيانات متجر هو أمر لا يمكن حل المشكلة.
  - **فشلت محاولات أعاده التعيين** - إذا تم اجراء عدد من المحاولات لإكمال عمليه أعاده تعيين، وكانت غير ناجحه بسبب البيانات المفقودة، فاننا نوصي بفتح حدث الدعم والعمل مع مهندس دعم لتحليل الموقف قبل محاولة أعاده تعيين متجر البيانات مره أخرى.
  - **السجلات القديمة** - السجلات التالفة بنفس الضرورة ضبط أعاده تعيين متجر البيانات بالضرورة. إذا كانت لديك مجموعه كبيره من البيانات، ستتطلب عمليه أعاده التعيين بعض الوقت ليتم تشغيلها، ولكنها من المحتمل ان تؤدي إلى تحسين.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>ما لا يقوم به متجر أعاده تعيين البيانات.  
- ستبدا عمليه أعاده التعيين فقط عند اكتمال المهام الموجودة. ويضمن ذلك عدم ادراج البيانات القديمة. في هذه المرحلة، قد تظهر لك رسالة مثل، "تعذرت معالجه البيانات متجر أعاده التعيين بسبب وجود مهمة نشطه. الرجاء المحاولة مره أخرى لاحقا."
- ستؤدي أعاده التعيين إلى تعطيل مهام التكامل وحذف كافة بيانات متجر البيانات. إعادة تمكين التكامل

> [!NOTE]
> تحدد النقاط التالية شيئين لأعاده تعيين متجر البيانات *لن* يفعلون. <br>
> - أعاده تعيين عدم مسح تصميمات التقرير. <br>
> - ولا يتم أعاده تعيين بيانات الشركة أو بيانات المستخدم الا إذا تم تحديدها.