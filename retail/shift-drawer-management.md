---
title: "إدارة الورديات وأدراج الأوراق النقدية‬"
description: "توضح هذه المقالة كيفية إعداد واستخدام نوعي ورديات نقاط البيع بالتجزئة: الورديات المستقلة والورديات المشتركة. يمكن استخدام الورديات المشتركة من قِبل عدة مستخدمين في أماكن متعددة، بينما يمكن استخدام الورديات المستقلة من قِبل عامل واحد فقط في كل مرة‬."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 09c7fce1fa83d6a8d6391db667b7260d2a199390
ms.lasthandoff: 03/31/2017


---

# <a name="shift-and-cash-drawer-management"></a>إدارة الورديات وأدراج الأوراق النقدية‬

[!include[banner](includes/banner.md)]


توضح هذه المقالة كيفية إعداد واستخدام نوعي ورديات نقاط البيع بالتجزئة: الورديات المستقلة والورديات المشتركة. يمكن استخدام الورديات المشتركة من قِبل عدة مستخدمين في أماكن متعددة، بينما يمكن استخدام الورديات المستقلة من قِبل عامل واحد فقط في كل مرة‬.

هناك نوعان من ورديات نقاط البيع بالتجزئة: الورديات المستقلة والورديات المشتركة. يمكن استخدام الورديات المستقلة من قِبل عامل واحد فقط في كل مرة. أما الورديات المشتركة فيمكن استخدامها من قِبل عدة مستخدمين في أماكن متعددة. وبالتالي، بإمكانها أن تنشئ بطريقة فعالة وردية واحدة لعدة عاملين في المتجر.

## <a name="standalone-shifts"></a>الورديات المستقلة
يتم استخدام الورديات المستقلة في سيناريو نقطة بيع تقليدية وثابتة، حيث تتم تسوية النقدية بشكل مستقل لكل آلة تسجيل المدفوعات النقدية في نقطة البيع. على سبيل المثال، في إعداد مخزن البقالة، يوجد عادة عدة آلات لتسجيل المدفوعات النقدية لنقاط البيع الثابتة، ويتم تعيين أمين صندوق لكل آلة. في هذه الحالة، تستخدم كل آلة تسجيل وردية مستقلة على الأرجح، ويتحمل أمين الصندوق مسؤولية درج النقدية أو النقد الفعلي في آلة تسجيل المدفوعات النقدية هذه. تضمّ الوردية المستقلة كل الأنشطة التي تتم على آلة التسجيل هذه أثناء وردية عمل أمين الصندوق. بإمكان الأنشطة أن تتضمن المبلغ الافتتاحي المودع في درج النقدية، وكافة عمليات إزالة النقدية وإضافتها عبر العمليات مثل الإيداعات البنكية والإدخال العائم‬ وإقرار الدفع في نهاية الوردية.

### <a name="set-up-a-stand-alone-shift"></a>إعداد وردية مستقلة

يتم تعيين الوردية المستقلة على مستوى درج الأوراق النقدية. يوضح هذا الإجراء كيفية إعداد وردية مستقلة على آلة تسجيل المدفوعات النقدية في نقطة البيع.

1.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **‎ملفات تعريف نقطة البيع** &gt; **ملفات تعريف الأجهزة**.
2.  حدد ملف تعريف الأجهزة الذي تريد استخدامه للوردية المستقلة.
3.  على علامة التبويب السريعة **الدرج‬**، تأكد من تعيين الخيار **درج الورديات المشتركة‬** إلى **لا**.
4.  انقر فوق **حفظ**.
5.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **السجلات**.
6.  حدد آلة التسجيل التي تحتاج إلى وردية مستقلة، ثم انقر فوق **تحرير**.
7.  في حقل **ملف تعريف الأجهزة**، حدد ملف تعريف الأجهزة الذي قمت بتحديده في الخطوة 2.
8.  انقر فوق **حفظ**.
9.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **تكنولوجيا معلومات البيع بالتجزئة** &gt; **جدول التوزيع**.
10. حدد جدول التوزيع **1090**، ثم انقر فوق **تشغيل الآن** لمزامنة التغييرات مع نقطة البيع.

### <a name="use-a-stand-alone-shift"></a>استخدام وردية مستقلة

1.  سجل الدخول إلى نقطة البيع.
2.  إذا لم يكن هناك أي وردية مفتوحة، فحدد **فتح وردية جديدة‬**.
3.  انتقل إلى عملية **إعلان مبلغ البدء‬**، وحدد المبلغ النقدي الذي تمت إضافته إلى درج النقدية لبدء يوم العمل.
4.  نفّذ بعض الحركات.
5.  في نهاية اليوم، حدد **إعلان طريقة الدفع‬** للإعلان عن المبلغ النقدي المتبقي في درج الأوراق النقدية.
6.  أدخل المبلغ النقدي، ثم انقر فوق **حفظ** لحفظ إقرار الدفع.
7.  حدد **إقفال الوردية** لإقفال الوردية.

**ملاحظة:** تتوفر عمليات أخرى أثناء الوردية، وهذا يتوقف على العمليات التجارية الموجودة. يمكن استخدام العمليات **إيداع بالخزين** و**إيداع بنكي** و**إزالة طريقة الدفع‬** لإزالة الأموال من درج النقدية خلال النهار أو قبل إقفال الوردية. في حال وجود نقص في النقد درج النقدية، فيمكن استخدام العملية **إدخال عائم** لإضافة نقد إلى درج النقدية.

## <a name="shared-shifts"></a>الورديات المشتركة
يتم استخدام الوردية المشتركة في بيئة يتشارك فيها الكثير من أمناء الصناديق درج أوراق نقدية أو مجموعة من أدراج الأوراق النقدية طيلة يوم العمل. يتم استخدام الوردي المشتركة عادةً في بيئات نقاط البيع المتنقلة. في البيئات المتنقلة، لا يتم تعيين كل أمين صندوق إلى درج واحد للأوراق النقدية ولا يكون مسؤولاً عن مثل هذا الدرج. بدلاً من ذلك، يجب أن يكون أمناء الصناديق كلهم قادرين على استخدام طريقة دفع للمبيعات وإضافة النقد إلى درج أوراق النقدية الأقرب إليهم. في هذا السيناريو، يتم تضمين أدراج الأوراق النقدية المشتركة بين أمناء الصناديق في وردية مشتركة. ويتم تضمين كافة أدراج الأوراق النقدية في وردية مشتركة للوردية نفسها لغرض يتعلق بالأنشطة المرتبطة بإدارة النقدية لهذه الوردية. وبالتالي، يجب أن يشمل مبلغ البدء للوردية مجموع جميع المبالغ النقدية في كافة أدراج الأوراق النقدية التي تم تضمينها في الوردية المشتركة. وبطريقة مماثلة، سيكون إقرار الدفع عبارة عن مجموع جميع المبالغ النقدية في كافة أدراج الأوراق النقدية التي تم تضمينها في الوردية المشتركة. **ملاحظة:** يمكن فتح وردية مشتركة واحدة فقط في كل مرة في كل متجر. ويمكن استخدام الورديات المشتركة والورديات المستقلة في المتجر نفسه.

### <a name="set-up-a-shared-shift"></a>إعداد وردية مشتركة

1.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **‎ملفات تعريف نقطة البيع** &gt; **ملفات تعريف الأجهزة**.
2.  حدد ملف تعريف الأجهزة الذي تريد استخدامه للوردية المشتركة.
3.  على علامة التبويب السريعة **الدرج‬**، عيّن الخيار **درج الورديات المشتركة‬** إلى **نعم**.
4.  انقر فوق **حفظ**.
5.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **السجلات**.
6.  حدد آلة التسجيل التي تحتاج إلى وردية مشتركة، ثم انقر فوق **تحرير**.
7.  في حقل **ملف تعريف الأجهزة**، حدد ملف تعريف الأجهزة الذي قمت بتحديده في الخطوة 2.
8.  انقر فوق **حفظ**.
9.  انقر فوق **البيع بالتجزئة والتجارة** &gt; **تكنولوجيا معلومات البيع بالتجزئة** &gt; **جدول التوزيع**.
10. حدد جدول التوزيع **1090**، ثم انقر فوق **تشغيل الآن** لمزامنة التغييرات مع نقطة البيع.

### <a name="use-a-shared-shift"></a>استخدام وردية مشتركة

1.  سجل الدخول إلى نقطة البيع.
2.  إذا لم يتم حتى الآن توصيل نقطة البيع بمحطة أجهزة، فحدد **عملية غير مرتبطة بالدرج‬**، ثم حدد العملية **تحديد محطة الأجهزة‬** لتنشيط محطة الأجهزة للوردية المشتركة. يجب تنفيذ هذه الخطوة فقط في المرة الأولى التي تُضاف فيها آلة تسجيل المدفوعات النقدية إلى بيئة وردية مشتركة.
3.  سجل خروجك من نقطة البيع، ثم سجل دخولك مرة أخرى.
4.  حدد **إنشاء وردية جديدة**.
5.  حدد **إعلان مبلغ البدء**.
6.  أدخل مبلغ البدء لكل أدراج الأوراق النقدية في المتجر التي تشكل جزءًا من الوردية المشتركة، ثم انقر فوق **حفظ**.
    -   لإضافة جزء من مبلغ البدء إلى كل درج أوراق نقدية لاحق، استخدم العملية **تحديد محطة الأجهزة **لتنشيط محطة الأجهزة.
    -   لإضافة درج نقدية إلى درج أوراق نقدية معين، استخدم عملية **فتح الدرج**.
    -   تابع حتى تحصل كافة أدراج الأوراق النقدية في الوردية المشتركة على حصتها من مبلغ البدء.

7.  في نهاية اليوم، افتح كل درج من أدراج الأوراق النقدية، واعمل على إخراج النقد منه.
8.  بعد إخراج النقد من درج الأوراق النقدية الأخير، يمكنك تعداد الأوراق النقدية في كل أدراج الأوراق النقدية.
9.  استخدم عملية **إعلان طريقة الدفع‬** للإعلان عن إجمالي المبلغ النقدي من كافة أدراج الأوراق النقدية المضمنة في الوردية المشتركة.
10. استخدم عملية **إقفال الوردية** لإقفال الوردية المشتركة.




