---
title: الخطط استنادا إلى عروض الأسعار والأسعار
description: توضح هذه المقالة كيفيه اعداد التخطيط الرئيسي لوضع عروض الأسعار وطلبات عروض الأسعار (أسعار) عند إنشاء أوامر مخططه.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690069"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>خطة على أساس عروض الأسعار و RFQs

[!include [banner](../../includes/banner.md)]

تمثل عروض الأسعار وطلبات عروض الأسعار (أسعار) الأوامر المستقبلية أو حتى المحتملة. لذلك ، فمن المنطقي ان تراعيها اثناء التخطيط الرئيسي ، بحيث يمكن تخطيط الإدخال الإضافي استنادا إلى الأسعار الموجودة واحتمال ان يصبح كل عرض أسعار أمرا فعليا. توضح هذه المقالة كيفية إعداد التخطيط الرئيسي لمراعاة عروض الأسعار وطلبات عرض الأسعار عند إنشاء أوامر مخططة.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>قم باعداد التخطيط الرئيسي لأخذ عروض أسعار المبيعات و/أو الأسعار

استخدم الاجراء التالي لاعداد التخطيط الرئيسي لأخذ عروض أسعار المبيعات و/أو أسعار.

1. انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط \> الخطط الرئيسية**.
1. حدد خطة موجودة في جزء القائمة ، أو حدد **جديد** في جزء الإجراءات لإنشاء واحدة جديدة.
1. في علامة التبويب السريعة **عام**، اضبط الحقول التالية:

    - **تضمين عروض أسعار** المبيعات – يتم تعيين هذا الخيار علي *نعم* لمراعاه عروض أسعار المبيعات عند تشغيل الخطة الحالية. قم بتعيينها إلى *لا* لتجاهلها.
    - **الاحتمالية %** – تعيين الحد الأدنى لمستوي الثقة المطلوب لعرض الأسعار ليتم تضمينه في التخطيط الرئيسي. سيتضمن حساب التخطيط الرئيسي كافة عروض الأسعار التي تم إنشاؤها من فرص المبيعات التي لها النسبة المئوية لprobability هذه أو لاعلي. لتضمين كافة عروض الأسعار ، بما في ذلك عروض الأسعار التي ليس لها احتماليه معينه لها أو لا توجد إيه فرص مقترنة بها ، قم بتعيين هذا الحقل إلى *0* (صفر). لمزيد من المعلومات حول احتمالات عروض الأسعار ، راجع القسم التالي.
    - **تضمين طلبات الاقتباسات** - اضبط هذا الخيار على *نعم* للنظر في طلبات عروض الأسعار عند تشغيل الخطة الحالية. قم بتعيينها إلى *لا* لتجاهلها. إذا اخترت اعتبار أسعار ، سيقوم النظام بإنشاء أوامر شراء مخططه لها ، ولكن لن يقوم بتحديد المورد حتى يتم حل طلب عرض الأسعار. قد تؤثر أوامر الشراء المخططة التي تم إنشاؤها لأسعار علي كميات الأوامر المخططة الأخرى.

1. تابع اعداد الخطة الرئيسية بالطريقة المعتادة.

## <a name="assign-and-view-probabilities-for-quotations"></a>تعيين الاحتمالات لعروض الأسعار وعرضها

وكما ذكر في المقطع السابق ، ستراعي الخطة الرئيسية فقط عروض الأسعار التي تفي أو تتجاوز عتبه الاحتمال المحددة للخطة (في حاله تحديد العتبة). ومع ذلك ، لا يتم تعيين الاحتمالية مباشره علي كل عرض أسعار. وبدلا من ذلك ، فهي موروثه من الفرصة التي تم استخدامها لإنشاء عرض الأسعار. لذلك ، عروض الأسعار التي تم إنشاؤها مباشرة على **كل الاقتباسات** لن يتم تعيين احتمالية للصفحة أو فرصة مرتبطة بها ، ولن يتم أخذها في الاعتبار من خلال التخطيط الرئيسي (ما لم يكن **احتمالا %** الحقل مضبوط على *0* \[زيرو\]). للحصول علي احتمال معين له ، يجب ان يتم إنشاء عرض أسعار من فرصه.

### <a name="create-a-quotation-from-an-opportunity"></a>إنشاء اقتباس من فرصة

استخدم الاجراء التالي لتعيين احتماليه إلى فرصه ثم قم بإنشاء عرض أسعار من تلك الفرصة.

1. انتقل إلى **المبيعات والتسويق \> العلاقات \> فرص \> كافة العملاء**.
1. حدد فرصة موجودة ، أو حدد **جديد** في جزء الإجراءات لإنشاء واحدة جديدة.
1. قم بملء الصفحة الفرصة لتعريف الفرصة بالشكل الذي تريده. تاكد من تعيين الحقل **الاحتمالية** إلى القيمة المناسبة. ستقوم فقط الخطط الرئيسية التي تم اعدادها للبحث عن احتمالات هذه القيمة أو اعلي بالتفكير في عروض الأسعار التي تم إنشاؤها من هذه الفرصة.
1. في جزء الإجراءات، حدد **حفظ**.
1. في جزء الإجراءات ، ضمن علامة التبويب **الفرصة** ، في المجموعة **جديد** ، حدد **عرض أسعار** المبيعات أو **عرض أسعار** المشروع ، وفقا لنوع عرض الأسعار الذي ترغب في إنشائه.
1. في مربع الحوار **إنشاء الاقتباس** ، في مربع الحوار ، قم بتعيين الحقول كما تريد ، ثم حدد **موافق**.
1. يتم إنشاء عرض أسعار جديد وفتحه. في البنود **FastTab** ، استخدم شريط الاداات لأضافه بنود المبيعات أو بنود المشروع كما هو مطلوب لتحديد محتوي عرض الأسعار.
1. في جزء الإجراءات، حدد **حفظ**. ثم أغلق الاقتباس.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>عرض الاحتمال الذي تم تعيينه لعرض الأسعار

والطريقة الوحيدة لعرض الاحتمالية التي تم تعيينها إلى عرض الأسعار هي فتح الفرصة التي تم استخدامها لإنشاء عرض الأسعار هذا ، كما هو موضح في الاجراء التالي.

1. انتقل إلى **المبيعات والتسويق \> عروض أسعار المبيعات \> جميع عروض الأسعار**.
1. إذا لم يكن العمود معرف **الفرصة** معروضا (تم إخفاؤه في تثبيت افتراضي) ، فاتبع الخطوات التالية لإظهاره بشكل مؤقت. (بدلا من ذلك ، للاحتفاظ بال **العمود معرف** الفرصة متوفر ، قم بإنشاء [ طريقه عرض ](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json)محفوظه تتضمنه.)

    1. حدد مع الاستمرار (أو انقر بزر الماوس الأيمن) في الشبكة ، ثم حدد **إدراج الأعمدة**.
    1. في مربع الحوار **ادراج أعمده** ، ابحث عن الصف الذي تم تعيين حقل **الحقل** إلى *الفرصة* فيه ، ثم حدد خانه الاختيار **تحديد** لهذا الصف.
    1. حدد **تحديث** لأضافه العمود المحدد إلى صفحه كافة عروض **الأسعار**.

1. في الشبكة ، ابحث عن الصف الخاص بعرض الأسعار المرتبط. ثم في **العمود معرف** الفرصة ، حدد قيمه لهذا الصف.

    > [!NOTE]
    > إذا كنت تبحث عن عرض أسعار مشروع ، فقد يتعين عليك تحديد راس العمود نوع **عرض الأسعار** ومسح عامل التصفية الخاص به. في التثبيت الافتراضي ، يتم تعيين عامل التصفية هذا بحيث يتم عرض عروض أسعار المبيعات فقط.

1. يتم فتح الفرصة ذات الصلة. يمكنك الآن عرض قيمه الاحتمالية **وتحريرها** كما هو مطلوب.