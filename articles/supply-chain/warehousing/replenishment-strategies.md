---
title: استراتيجيات التزويد
description: يوفر هذا المقال معلومات حول استراتيجيات التزويد ويشرح كيفيه استخدام حقل استراتيجية التزويد في بنود قالب التزويد المطالبة بالموجه لتحديد كيفيه اجراء التزويد.
author: Mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1245d07436a9b57ee4f0402687e7a4367668cbfa
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336264"
---
# <a name="replenishment-strategies"></a>استراتيجيات التزويد

[!include [banner](../includes/banner.md)]

تتضمن القوالب التي تم تعريفها في صفحه **قوالب التزويد** بنود قالب تزويد طلب الموجه التي تتيح لك تحديد كيفيه القيام بالتزويد. يتضمن كل بند الآن حقل **استراتيجية التزويد**.

وتعتبر استراتيجية *الكمية لطلب الموجه* هي الاستراتيجية الافتراضية. انها استراتيجية التزويد التي تم استخدامها قبل مقدمه الحقل **استراتيجية التزويد**. ويستخدم توجيهات موقع التزويد للبحث عن مواقع يمكن تزويدها. ثم يتم تزويد هذه المواقع حتى تتم تغطيه الطلب.

وتقدم استراتيجية *الحد الأقصى لقدرة الموقع* بعض الوظائف الجديدة. ومثل استراتيجية *كمية طلب الموجة*، تستخدم هذه الاستراتيجية موجات مواقع التزويد للبحث عن مواقع يمكن تزويدها، ثم تزويد تلك المواقع إلى ان تتم تغطيه الطلب. يختلف ذلك عن استراتيجية *كميه طلب الموجه* وذلك بحيث يتم تزويد كافة المواقع التي تم تزويدها إلى الحد الأقصى للقدرة الخاصة بها ، كما هو محدد بواسطة حدود المخزون الخاصة بالموقع. تحاول استراتيجية *الحد الأقصى لقدرة الموقع* الذي يحاول إنشاء عمل لإحضار الكمية المطلوبة بالاضافه إلى الكمية الاضافيه لملء المواقع التي يتم تزويدها. ومع ذلك ، في بعض الحالات ، قد تفشل هذه المحاولة. علي سبيل المثال ، قد لا يكون لدي مواقع الكميات الكبيرة مخزون كاف لتغطيه الكمية الاضافيه. في هذه الحالات ، يكشف النظام عن الفشل ويحاول الاسترداد.

يعد "موسم الذروة" مثالا علي الموقف الذي يفضل استراتيجية *الحد الأقصى للقدرة الانتاجيه للموقع* لاستراتيجية  *كميه طلب الموجه*. واثناء الموسم في الذروة ، قد يتم بيع بعض الأصناف بحجم كبير. ولذلك ، قد ترغب في القيام بتزويد مواقع الانتقاء ذات الصلة بالقدر المستطاع ، لتقليل عدد معرفات العمل التي تم إنشاؤها لتزويدها.

> [!IMPORTANT]
> للاستفادة الكاملة من استراتيجية *الحد الأقصى لقدرة الإنتاج الخاصة بالموقع*، يجب أعاده تعريف حدود المخزون الخاصة بالمواقع ذات الصلة. وبخلاف ذلك ، تعمل هذه الاستراتيجية تماما مثل استراتيجية *الكمية الخاصة بطلب الموجه*.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>تشغيل التزويد إلى الحد الأقصى استنادا إلى ميزه حدود المخزون

قبل أن تتمكن من استخدام هذه الميزة ، يجب تشغيلها لنظامك. يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة. هناك، يتم إدراج الميزة بالطريقة التالية:

- **الوحدة:** *إدارة المستودعات*
- **اسم الميزة:** *تشغيل التزويد إلى الحد الأقصى استنادا إلى ميزه حدود المخزون*

## <a name="set-up-replenishment-strategies"></a>إعداد استراتيجيات التزويد

للوصول إلى القوالب، انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \>  قوالب التزويد**. في القسم **نظره عامه**، حدد أو أنشئ قالب تزويد طلبات الموجات حيث تم تعيين الحقل **نوع التزويد** إلى *طلب الموجه*. ثم قم بإعداد بنود قالب التزويد في قسم **تفاصيل قالب التزويد**. بالنسبة لكل بند، في الحقل **استراتيجية التزويد**، حدد استراتيجية التزويد التي ترغب في استخدامها.

![صفحة قوالب التزويد.](media/ReplenTempWaveDmdMaxLocCap.png "صفحة قوالب التزويد")

إذا لم يظهر عمود **استراتيجية التزويد** في الشبكة الموجودة في القسم **تفاصيل قالب التزويد**، فتاكد من انه تم تشغيل الميزة، وان قالب الاستعاضة المحدد يحتوي علي نوع التزويد *لطلب الموجه*.

> [!NOTE]
> وتعتبر استراتيجية *الكمية لطلب الموجه* هي الاستراتيجية الافتراضية. التالي ، يجب عليك فقط تحديث بنود قالب التزويد حيث تريد استخدام استراتيجية *الحد الأقصى لقدرة الموقع* بدلا من ذلك.

## <a name="example-scenarios"></a>سيناريوهات مقدمة كمثال

### <a name="example-1"></a>مثال1

بالنسبة لهذا المثال ، يوجد فقط قالب تزويد واحد يحتوي علي بند قالب تزويد واحد فقط.

تقوم بإنشاء أمر مبيعات لعدد 130 قطعة للصنف A0001. قبل إصدار الأمر إلى المستودع ، يتم إعداد المستودع بالطريقة التالية:

- يوجد موقع كبير واحد فقط يتضمن 500 قطعة من المخزون الفعلي المتاح.
- توجد ثلاث مواقع انتقاء، ويكون لكل منها حد مخزون يصل إلى 100قطعة. (تذكر ان حدود المخزون مطلوبه لاستراتيجية *الحد الاقصي للقدرة علي الموقع*.)
- ستكون مواقع تخزين التزويد هي نفسها مواقع انتقاء المبيعات.
- وحده التزويد هي صندوق (1 صندوق = 20 قطعة).

وفي وقت الطلب ، يكون المخزون التالي متوافرا في مواقع انتقاء المبيعات:

- **انتقاء 001:** عدد 20 قطعة (صندوق واحد)
- **انتقاء-002:** عدد 0 قطعة
- **انتقاء-003:** عدد 0 قطعة

بشكل مبدئي ، يتم تعيين استراتيجية التزويد علي *كميه الطلب الموجه*.

بعد إصدار أمر المبيعات إلى المستودع ، وتشغيل معالجه الموجه للموجه ، ستحصل علي عمل التزويد التالي:

- **عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.
- **عمل التزويد 2:** انتقاء 2 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.

يمكنك الحصول علي معرفي عمل التزويد نظرا لأنه يجب تزويد الموقعين ، ولا يتم دعم العديد من الوضعين.

إذا قمت بتعيين استراتيجية التزويد إلى *الحد الأقصى لقدرة الموقع* بدلا من ذلك ، ستحصل علي عمل التزويد التالي:

- **عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.
- **عمل التزويد 2:** انتقاء 5 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.

[![مثال 1.](media/ReplenTemp_example_1.png "مثال1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>مثال2

يوضح هذا المثال ما يحدث عندما لا يحتوي موقع الكميات الكبيرة علي مخزون كافي لتغطيه الكمية الاضافيه. يستخدم السيناريو نفسه مثل المثال 1، ولكن موقع الكمية الكبيرة يحتوي علي 160قطعة (8 صناديق).

تقوم استراتيجية *الكمية الخاصة بطلب الموجه* بإنشاء نفس العمل الذي كانت عليه في المثال 1.

ومع ذلك ، نظرا لان استراتيجية *الحد الأقصى لقدره الموقع* تحاول إنشاء معرفات العمل كما كانت في المثال 1، قد تفشل العملية. وفي هذه المرحلة ، يحاول النظام الاسترداد.

اعتمادا علي إعداد **السماح بالتقسيم** علي موجات المواقع الخاصة بانتقاء التزويد ، فانه يمكن للنتيجتين:

- إذا تم تعيين الخيار **السماح بالتقسيم** إلى *نعم*، يتم إنشاء عمل التزويد التالي:

    - **عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.
    - **عمل التزويد 2:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.

- إذا تم تعيين الخيار **السماح بالتقسيم** إلى *لا*، يتم إنشاء عمل التزويد التالي:

    - **عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.
    - **عمل التزويد 2:** انتقاء 2 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.

تختلف النتائج بسبب المعلومات المتاحة عند إنشاء العمل. عند تعيين **السماح بالتقسيم** إلى *نعم* في موجهات المواقع الخاصة بانتقاء التزويد، فأنت تعرف انك قمت بالاداره للعثور علي 160 قطعة. التالي ، يمكنك إنشاء عمل لهذه الكمية. ومع ذلك ، عندما يكون الخيار **السماح بالتقسيم** معينا إلى *لا*، فانك لا تعرف بوجود 160 قطعة. ونظرا لان الكمية الزائدة التي قمت بتحديدها للتزويد كانت 3 صناديق، فانك تقوم بإسقاط الكمية الاضافيه ومحاولة الكمية الاصليه مره أخرى.

[![مثال 2.](media/ReplenTemp_example_2.png "مثال2")](media/ReplenTemp_example_2_large.png)

التالي ، للحصول علي الحد الأقصى من الكمية للمواقع التي تمت تزويدها، يجب تعيين الخيار **السماح بالتقسيم** إلى *نعم* في موجات المواقع الخاصة بانتقاء التزويد.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]