---
title: تعقب العمولات في نقطة البيع (POS) باستخدام مجموعات المبيعات
description: وتعد ممارسة شائعة في البيع بالتجزئة لتعقب المبيعات بواسطة الموظفين الذين قاموا بأداء العمل من العميل- تقديم المساعدة، والبيع الإضافي والبيع التكميلي ومعالجة الحركة.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.industry: Retail
ms.openlocfilehash: 5a5cdf57d8c920b105e7f4a457b064cb2ceba242
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272785"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>تعقب العمولات في نقطة البيع (POS) باستخدام مجموعات المبيعات

[!include [banner](includes/banner.md)]

وتعد ممارسة شائعة في البيع بالتجزئة لتعقب المبيعات بواسطة الموظفين الذين قاموا بأداء العمل من العميل- تقديم المساعدة، والبيع الإضافي والبيع التكميلي ومعالجة الحركة.

يُعد تعقب المبيعات من قبل ممثل المبيعات هو إجراء لقياس قدرات موظفي المبيعات، في حين يتم قياس المبيعات من قبل الكاشير بالسرعة والكفاءة. في حين يتم عادةً تعقب المبيعات التي تتم من خلال ممثل المبيعات عادةُ باستخدام حساب العمولات أو غير ذلك من المكافآت التشجيعية.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>تكوين عامل ليكون مندوب مبيعات في نقطة البيع

عندما تتم إضافة عامل إلى مجموعة مبيعات، يصبح مؤهلًا للحصول على اعلمولة، ويمكن تعريفه كمندوب مبيعات في النظام. ولا يؤهل العامل غير موجود في مجموعة المبيعات للحصول على العمولة، ولن يتم إدراجه كمندوب مبيعات في تطبيق نقطة البيع. في نقطة البيع، يتم اشتقاق قائمة مندوبي المبيعات من كافة مجموعات المبيعات التي تحتوي على عامل واحد على الأقل يتم تعيينه للمتجر. يتم عرض القائمة في نقطة البيع كمجموعة من مُعرفات مجموعة المبيعات والاسم (المُعرف: الاسم). يمكن تعيين مجموعة مبيعات افتراضية للعاملين لدعم سيناريوهات يختار فيها بائع التجزئة تعيين مندوب مبيعات على خطوط نقطة البيع تلقائيًا. يمكن للمستخدمين الاختيار من أي مجموعة مبيعات يكون العامل عضوًا فيها.

## <a name="functionality-profile-settings"></a>إعدادات ملف تعريف الوظيفة

يوجد عدد من إعداد ملف تعريف الوظيفة لمتجر، والتي ستحدد التدفق والمعالجة في نقطة البيع التي تتضمن مندوبي المبيعات.

<table>
<thead>
<tr>
<th>ملف التعريف</th>
<th>‏‏الوصف</th>
</tr>
</thead>
<tbody>
<tr>
<td>افتراضي للصراف عند التوافر</td>
<td>إذا تم تمكين هذا الخيار، سوف تقوم نقطة البيع بملء بنود الحركة تلقائيًا باستخدام مجموعة المبيعات الافتراضية للكاشير الحالي. إذا لم يكن للكاشير مجموعة مبيعات افتراضية محددة، فلن يتم تعيين القيمة. لا يزال بإمكان المستخدم تعيين مجموعة المبيعات باستخدام آزرار شريط أوامر نقطة البيع.</td>
</tr>
<tr>
<td>المطالبة بمندوب المبيعات</td>
<td>تتوفر لدى هذا الخيار ثلاث قيم ممكنة:
<ul>
<li><strong>لا</strong> – إذا تم تحديد هذا الخيار، فلن تتم مطالبة المستخدم بتحديد مجموعة مبيعات. ومن الممكن تعيين القيمة باستخدام مجموعات المبيعات الافتراضية للكاشير أو يدويًا باستخدام زر في شبكة أزرار نقطة البيع.</li>
<li><strong>بداية الحركة</strong> - إذا تم تحديد هذا الخيار، ولم يتم تمكين <strong>افتراضي للكاشير</strong>، أو لم يكن للكاشير الحالي مجموعة مبيعات افتراضية، فسوف تتم مطالبة المستخدم بتحديد مجموعة مبيعات في بداية كل حركة. وبتحديد مجموعة مبيعات من هذه المطالبة من شأنه أن يُعيّن جميع الأسطر التالية لمجموعات المبيعات المحددة تلقائيًا. لا يزال بإمكان المستخدم تعيين مجموعة المبيعات باستخدام آزرار شريط أوامر نقطة البيع.</li>
<li><strong>لكل بند</strong> - إذا تم تحديد هذا الخيار، ولم يتم تمكين <strong>افتراضي للكاشير</strong>، أو لم يكن للكاشير الحالي مجموعة مبيعات افتراضية، فسوف تتم مطالبة المستخدم بتحديد مجموعة مبيعات بعد إضافة كل سطر. لا يزال بإمكان المستخدم تعيين مجموعة المبيعات باستخدام آزرار شريط أوامر نقطة البيع.</li>
</ul>
</td>
</tr>
<tr>
<td>مطلوب</td>
<td>ينطبق هذا الخيار فقط عندما يتم تكوين نقاط البيع للمطالبة بمندوب مبيعات. في حالة التمكين، فسوف يكون المستخدم مطالبًا باختيار مجموعة مبيعات قبل المتابعة والاستمرار. وبخلاف ذلك، سوف يكون المستخدم مطالبًا، ولكنه يمكنه الإلغاء والاستمرار دون إجراء تحديد. بعد إضافة السطر، لا يزال بإمكان المستخدم الذي لدية الأذونات الكافية إزالة مجموعة المبيعات من السطر. لا يتم فرض "طلب مندوب مبيعات" في هذه الحالة.</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>عرض معلومات مندوب المبيعات على شاشة حركات نقطة البيع

يمكن تكون تخطيط شاشة حركة نقطع البيع والمحتويات باستخدام مصمم تخطيط الشاشة، وتعيين تخطيطات الشاشة إلى المخازن أو السجلات أو العمال. يمكن إضافة حقل **مندوب المبيعات** في علامة تبويب "البنود" في جزء الإيصال.  سيؤدي ذلك إلى عرض مُعرف مجموعة المبيعات المحددة لكل بند على شاشة الحركة.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>إضافة عمليات مندوب المبيعات إلى شبكة أزرار نقطة البيع

تسمح نقطة البيع للمستخدمين بتكوين شبكات آزرار، والتي يتم تضمينها في تخطيطات الشاشة لتوفير الوصول إلى عمليات نقطة البيع. يمكن تعيين نقاط البيع التالية لأزرار شبكة الأزرار المتعلقة بمندوبي المبيعات.

| العملية                                 | ‏‏الوصف |
|-------------------------------------------|-------------|
| تعيين مندوب مبيعات في بند          | تعرض عملية نقطة البيع قائمة بمجموعات المبيعات المؤهلة (المُعرف: الاسم) للمتجر. سيؤدي تحديد مجموعة مبيعات من هذه القائمة إلى تعيين القيمة على بند الحركة الحالية. |
| مسح مندوب مبيعات في بند        | تزيل عملية نقطة البيع هذه قيمة مجموعة المبيعات الحالية من سطر الحركة الحالي. |
| تعيين مندوب مبيعات في الحركة   | تعرض عملية نقطة البيع قائمة بمجموعات المبيعات المؤهلة (المُعرف: الاسم) للمتجر. سيؤدي تحديد مجموعة مبيعات من هذه القائمة إلى تعيين القيمة الافتراضية في الحركة الحالية. سوف يتم تعيين أي سطور موجودة بدون مجموعة مبيعات فضلًا عن أي سطور مضافة فيما بعد. |
| مسح مندوب مبيعات في الحركة | تزيل عملية نقطة البيع هذه قيمة مجموعة المبيعات الحالية الافتراضية من الحركة الحالية. ولا يؤثر هذا على أي سطور موجودة بالفعل في الحركة. |

## <a name="calculating-commissions"></a>حساب العمولات

يتم حساب العمولة للعمال في مجموعات مبيعات محددة في وقت ترحيل كشف الحساب أو ترحيل أمر التوريد. يُحدد مبلغ العمولة استنادًا إلى حصة عمولة العامل، على النحو المحدد في مجموعة المبيعات وإعدادات حساب العمولة المقترنة للعميل و/أو المنتجات على الحركة.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
