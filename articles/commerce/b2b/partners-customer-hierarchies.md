---
title: إدارة شركاء الأعمال B2B باستخدام التدرجات الهرمية للعملاء
description: يوضح هذا المقال كيفية استخدام التدرجات الهرمية للعلماء لإدارة شركاء الأعمال لمواقع ويب التجارة الإلكترونية بين الشركات (B2B) في Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ddd02045b5df3ce20160a4feaa23339475823d3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864971"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>إدارة شركاء الأعمال B2B باستخدام التدرجات الهرمية للعملاء

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية استخدام التدرجات الهرمية للعلماء لإدارة شركاء الأعمال لمواقع ويب التجارة الإلكترونية بين الشركات (B2B) في Microsoft Dynamics 365 Commerce.

في Commerce headquarters، يُستخدم كيان *التدرج الهرمي للعميل* لتمثيل المؤسسات الشريكة للأعمال التي ستستخدم موقعك على الويب للتجارة الإلكترونية بين الشركات (B2B). قبل أن تتمكن من بدء استخدام التدرجات الهرمية للعملاء لإدارة شركاء الأعمال، يجب عليك تمكين إمكانات التجارة الإلكترونية B2B في Commerce Headquarters ثم تحديد تسلسل رقمي للتدرج الهرمي للعميل.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>تشغيل ميزة التجارة الإلكترونية B2B في Commerce Headquarters

لاستخدام قدرات التجارة الإلكترونية B2B، يجب أولاً تمكين ميزة **تمكين استخدام إمكانيات التجارة الإلكترونية B2B** في Commerce Headquarters.

1. انتقل إلى **مساحات العمل \> إدارة الميزات**.
1. في علامة التبويب **الكل**، استخدم مربع التصفية للبحث عن **الوحدة النمطية: Retail وCommerce**.
1. ابحث عن الميزة **تمكين استخدام إمكانيات التجارة الإلكترونية B2B**، وحددها، ثم حدد **التمكين الآن** في الزاوية السفلية اليسرى.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>تحديد تسلسل رقمي للتدرج الهرمي للعميل

وتُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركة التي تتطلب وجود هذه المعرفات. يجب تحديد تسلسل رقمي يتم استخدامه لإنشاء معرف للتدرج الهرمي للعميل. لمزيد من المعلومات حول التسلسلات الرقمية، راجع [نظرة عامة على التسلسلات الرقمية](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

لتحديد تسلسل رقمي للتدرج الهرمي للعميل في Commerce Headquarters، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> التسلسلات الرقمية \> التسلسلات الرقمية**.
1. قم بإنشاء تسلسل رقمي جديد، أو حدد تسلسلاً رقميًا موجودًا لإعادة استخدامه.
1. انتقل إلى **Retail and Commerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce المشتركة**.
1. في علامة التبويب **التسلسلات الرقمية**، أضف التسلسل الرقمي الذي أنشأته أو حددته سابقًا لمرجع **معرف التدرج الهرمي للعميل**.

![التسلسل الرقمي المضاف إلى مرجع معرف التدرج الهرمي للعميل.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>كيفية عمل عملية الموافقة

وعندما يطلب شريك أعمال الانضمام إلى موقع تجارة إلكترونية B2B، يحفظ النظام الطلب على أنه *عميل متوقع*. بإمكان مسؤول Commerce Headquarters مثل مدير عمليات البيع بالتجزئة الموافقة على طلبات الشركاء أو رفضها. لمزيد من المعلومات حول كيفية إدارة طلبات شركاء الاعمال والموافقات على العملاء المتوقعين، راجع [إدارة مستخدمي شركاء الأعمال على مواقع ويب التجارة الإلكترونية بين الشركات B2B‬](manage-b2b-users.md).

عند الموافقة على عميل متوقع، يقوم النظام بإنشاء سجلين جديدين للعميل:

- سجل عميل من النوع **مؤسسة** يمثل المؤسسة المطلوبة لتصبح شريك أعمال.
- سجل عميل من النوع **شخصية** يمثل الشخص الذي أرسل الطلب.

علاوة على ذلك، يتم إنشاء سجل تدرج هرمي جديد للعملاء في **Retail وCommerce \> العملاء \> التدرجات الهرمية للعملاء**. يتضمن سجل التدرج الهرمي للعميل هذا الخصائص التالية:

- **معرف التدرج الهرمي للعميل** - معرف فريد للتدرج الهرمي للعميل. يستخدم هذا المعرف التسلسل الرقمي الذي حددته في المعلمات المشتركة في Commerce.
- **الاسم** – اسم المؤسسة الخاصة بشريك الأعمل، كما هو محدد في طلب الانضمام. هذا الحقل قابل للتحرير.
- **الغرض** – يتم تعيين هذه الخاصية على القيمة المحددة مسبقًا **مؤسسة B2B**.
- **المؤسسة** – معرف العميل الخاص بمؤسسة شريط الأعمال.

يُضاف الشخص الذي قام بتقديم طلب الإلحاق إلى علامة التبويب السريعة **التدرج الهرمي** ودور **المسؤول** المعين له. عندما يضيف المسؤول المزيد من المستخدمين إلى مؤسسة شركاء الأعمال في موقع B2B، يتم إنشاء سجل عميل جديد لكل مستخدم. وتتم أيضًا إضافة سجل العميل إلى سجل التدرج الهرمي للعميل المناسب لشريك الأعمال ويتم تعيين دور **المستخدم** له.

### <a name="examples"></a>أمثلة

أرسل شخص يسمى سام جي. طلب إلحاق بالنيابة عن مؤسسة Microsoft. بعد الموافقة على الطلب، تم إنشاء حسابين جديدين للعميل: أحدها حساب من النوع **شخصية** لسام جي وحساب من النوع **مؤسسة** لشركة Microsoft.

كما يوضح المثال في الرسم التوضيحي التالي، يتم أيضًا إنشاء سجل تدرج هرمي جديد للعميل. يحمل هذا السجل الاسم نفسه للمؤسسة (**Microsoft**)، وتم تعيين دور **المسؤول** إلى سام جي. كمسؤول، بصفته المسؤول، يضيف سام جي. أي مستخدمين آخرين من Microsoft لموقع B2B إلى هذا التدرج الهرمي ويعين **المستخدم** لهم. في هذا المثال، تمت إضافة سوش آر. كمستخدم.

![مثال عن سجل تدرج هرمي للعميل.](../media/CustomerHierarchy2.png)

لتحديد ما إذا كان العميل مقترنًا بتدرج هرمي للعميل، افتح سجل العميل. كما يوضح المثال في الشكل التوضيحي التالي، يبيّن حقل **معرف التدرج الهرمي للعميل** في القسم **B2B** على علامة التبويب السريعة **البيع بالتجزئة** ما إذا كان العميل جزءًا من التدرج الهرمي للعميل، ويشير الخيار **مسؤول B2B** إلى ما إذا كان العميل مسؤول ذلك التدرج الهرمي.

![مثال عن قسم B2B علي علامة التبويب السريعة "البيع بالتجزئة" لسجل العميل، حيث يتم ربط العميل بالتدرج الهرمي وتحديده كمسؤول.](../media/CustomerHierarchyMapping2.png)

في معظم الحالات، يجب أن تتطابق قيم الخصائص لكافة سجلات العملاء في التدرج الهرمي. على سبيل المثال، نظرًا لأن كافة مستخدمي شريك الأعمال يجب أن يحصلو على أسعار مماثلة للمنتجات، فيجب أن تتطابق مجموعات الأسعار والتكوينات المقترنة بها. ومع ذلك، لا يفرض النظام هذا التناسق. لذلك، فإن يكون مستخدمو المركز الرئيسي لـ Commerce المتعلقون مسؤولين عن ضمان مطابقة قيم الخصائص والتكوينات لكافة العملاء في تدرج هرمي المُعطى.

بإمكان مستخدمي Commerce Headquarters فحص قيم الخصائص لكافة سجلات العملاء في التدرج الهرمي من طريقة عرض جنبًا إلى جنب. كما يوضح المثال في الشكل التوضيحي التالي، يمكنك استخدام الخيار **عام** في القائمة المنسدلة على علامة التبويب السريعة **التدرج الهرمي**، ثم تحديد أي قسم في سجل العميل لإظهار الخصائص ذات الصلة. بإمكان المستخدمين عرض قيم الخصائص وتحريرها مباشرة في طريقة العرض هذه. لنسخ كافة القيم من سجل العميل المسؤول إلى كافة المستخدمين، حدد **تجاوز** على علامة التبويب السريعة **التدرج الهرمي**.

![مثال عن سجل التدرج الهرمي للعميل، يُظهر الزر "تجاوز" والخيار في القائمة المنسدلة.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
