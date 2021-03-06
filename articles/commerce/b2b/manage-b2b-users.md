---
title: إدارة مستخدمي شركاء الأعمال على مواقع ويب التجارة الإلكترونية بين الشركات B2B
description: يوضح هذا الموضوع كيف يمكن للمسؤولين إضافة مستخدمي شركاء العمل وتحريرهم وحذفهم من مواقع الويب الخاصة بالتجارة الإلكترونية بين الشركات (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96b76a08206b8c1bc5029acdfd385fda2870ca85
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035868"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>إدارة مستخدمي شركاء الأعمال على مواقع ويب التجارة الإلكترونية بين الشركات B2B

[!include [banner](../../includes/banner.md)]

يوضح هذا الموضوع كيف يمكن للمسؤولين إضافة مستخدمي شركاء العمل وتحريرهم وحذفهم من مواقع الويب الخاصة بالتجارة الإلكترونية بين الشركات (B2B).

تتطلب مواقع ويب التجارة الإلكترونية بين الشركات B2B أن تسجل المؤسسات لتصبح أطراف عمل. بعد قيام إحدى المؤسسات بإرسال تفاصيل التسجيل إلى موقع ويب التجارة الإلكترونية بين الشركات B2B، يتم الانتقال عبر عملية تأهيل. إذا تم تأهيل المؤسسة بنجاح، فإنه يتم ضمها كشريك عمل.

بعد أن يتم ضم المؤسسة كشريك عمل، يتم تعريف مستخدم المؤسسة الذي قام ببدء الطلب ليصبح شريك عمل كمستخدم مسؤول ويتم منحه امتيازات لضم مستخدمين إضافيين مخولين لموقع ويب التجارة الإلكترونية بين الشركات B2B. ويمكن لهؤلاء المستخدمين المخولين بعد ذلك تقديم الطلبات بالنيابة عن شريك العمل.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>تشغيل ميزة إمكانات التجارة الإلكترونية بين الشركات B2B في المركز الرئيسي لـ Commerce

تتيح ميزة إمكانات التجارة الإلكترونية بين الشركات B2B في المركز الرئيسي لـ Commerce للمؤسسات ضمن شركات الأعمال وتحديد المستخدمين المسؤلين. كما تتيح هذه الميزة للمسؤولين إمكانية إنشاء فرق ومستخدمي شركاء الأعمال وإدارتهم وتعيين أدوار محددة لهم. كما تتيح في النهاية لمستخدمي شركاء الأعمال إنشاء قوالب الأوامر واستخدام الأوامر الموجودة لإعادة ترتيب المنتجات.

لتشغيل ميزة إمكانات التجارة الإلكترونية بين الشركات B2B في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.

1. انتقل إلى **مساحات العمل \> إدارة الميزات**.
1. في علامة التبويب **الكل**، قم بإجراء تصفية على حقل **الوحدة النمطية** باستخدام مصطلح **البيع بالتجزئة والتجارة**.
1. ابحث عن وحدد الميزة التي يطلق عليها اسم **تمكين استخدام إمكانيات التجارة الإلكترونية بين الشركاتB2B**، ثم حدد **التمكين الآن**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>إنشاء تسلسل رقمي وإضافته إلى المحددات المشتركة لـ Commerce

وتُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركة التي تتطلب وجود هذه المعرفات. لمزيد من المعلومات حول التسلسلات الرقمية، راجع [نظرة عامة على التسلسلات الرقمية](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

لإنشاء تسلسل رقمي وإضافته إلى المعلمات المشتركة في Commerce في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المركز الرئيسي \> التسلسلات الرقمية \>**، وقم بإنشاء تسلسل رقمي.
1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المركز الرئيسي \> المعلمات \> المعلمات المشتركة في Commerce**، وأضف تسلسلا رقميًا جديدًا إلى مرجع  **معرف التدرج الهرمي للعميل**.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>إعداد مستخدم مسؤول لشريك عمل جديد

يمكن لشركاء العمل المحتملين بدء عملية ضم إلى موقع ويب التجارة الإلكترونيه بني الشركات B2B عن طريق إرسال طلب ضم من خلال ارتباط على الموقع. بعد أن يحدد مستخدم شريك العمل المحتمل الارتباط يمكنه توفير التفاصيل المطلوبة لعمليات الضم والتسجيل. بعد إرسال الطلب، تظهر صفحة تإكيد الإرسال. إذا تمت الموافقة على الإرسال، يصبح الطالب (أي، المستخدم الذي بدأ طلب الضم) هو المستخدم المسؤول لشريك العمل.

للموافقة على مستخدم مسؤول لشريك العمل وإعداده في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **تقنية معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.
1. قم بتشغيل وظيفة **P-0001** لسحب كافة طلبات ضم شريك العمل إلى المركز الرئيسي لـ Commerce.
1. بعد تشغيل وظيفة **P-0001** بنجاح، انتقل إلى **تقنية معلومات البيع بالتجزئة والتجارة \> العميل**، وقم بتشغيل وظيفة **مزامنة العملاء وشركاء الأعمال من وضع عدم المزامنة**. بعد تشغيل هذه المهمة بنجاح، يتم إنشاء طلبات ضم كسجلات عملاء متوقعين في المركز الرئيسي لـ Commerce. يتم تعيين حقل **معرف النوع** الخاص بهذه السجلات إلى **العميل المتوقع لـ B2B**.
1. انتقل إلى **العملاء \> كافة العملاء المتوقعين**، وافتح صفحة العملاء المتوقعون.
1. حدد سجل العميل المتوقع لشريك العمل الجديد لفتح صفحة تفاصيل العميل المتوقع.
1. في علامة التبويب **عام**، حدد **تحويل \> قبول/رفض** لاعتماد طلب الضم أو رفضه. عند ظهور رسالة تأكيد، أكد على أنك تريد متابعة العملية، والموافقة على الطلب. يتم بعد ذلك إرسال رسالة بريد إلكتروني إلى عنوان البريد إلكتروني الخاص بالطالب للتأكيد على أنه تم اعتماد مؤسسته كشريك عمل.

    بعد اعتماد الطلب ، يتم تعيين حقل **الحالة** الخاص بسجل العميل المتوقع إلى **معتمد**. بالاضافه إلى ذلك، يتم إنشاء سجلين عميلين جديدين في النظام: سجل عميل **من نوع مؤسسة** لمؤسسة شريك العمل وسجل عميل **من نوع شخص** للطالب. كما يتم إنشاء سجل التدرج الهرمي للعميل لشريك العمل أيضًا. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. انتقل إلى **تقنية معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**، وقم بتشغيل الوظيفة **1010** ( **العملاء**) لدفع سجلات العميل والتدرج الهرمي للعميل التي تم إنشاؤها حديثًا إلى قاعدة بيانات القناة.

بعد اعتماد الطلب، ومزامنة سجلات العميل والتسلسل الهرمي للعميل مع قاعدة بيانات القناة، يمكن للطالب تسجيل الدخول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B باستخدام عنوان البريد الإلكتروني الذي قام بتقديمه عند إرسال الطلب. يمكن للمستخدمين استخدام سير عمل التسجيل لتعريف كلمة المرور للحساب الخاص بهم.

## <a name="onboard-additional-business-partner-users"></a>ضم مستخدمين إضافيين كشركاء عمل

ويمكن للمستخدم المسؤول لشريك الأعمال ضم مستخدمين إضافيين كشركاء أعمال إلى موقع ويب التجارة الإلكترونية بين الشركات B2B كما هو مطلوب.

لضم مستخدمين إضافيين كشركاء أعمال إلى موقع ويب التجارة الإلكترونية بين الشركات B2B، اتبع الخطوات التالية.

1. سجل الدخول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B كمسؤول.
1. انتقل إلى **حسابي \> مستخدمو المؤسسة \> عرض التفاصيل**، وحدد **إضافة مستخدم**.
1. أدخل المعلومات المطلوبة ، ثم حدد **حفظ**. يتم تعيين حالة المستخدم الجديد إلى **معلقة**.

    بعد تشغيل المهمتين **P-0001** و **مزامنة العملاء وشركاء الأعمال من وضع عدم المزامنة**، يتم إنشاء سجل عميل من **نوع شخص** للمستخدم الجديد في المركز الرئيسي لـ Commerce. كما يرتبط سجل العميل هذا بسجل التدرج الهرمي للعميل الخاص بشريك العمل المرتبط. بالإضافة إلى ذلك، يتم إرسال رسالة بريد الكتروني إلى عنوان البريد الإلكتروني الخاص بالمستخدم الجديد لاعلامهم بأنه تمت إضافتهم كمستخدم لمؤسسة شريك الأعمال ويمكنهم الآن تسجيل الدخول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B.

1. قم بتشغيل الوظيفة **1010** (**العملاء**) لمزامنة مستخدم شريك العمل الجديد مع قاعدة بيانات القناة.

بعد مزامنة سجل العميل، يتم تعيين حالة المستخدم في موقع ويب التجارة الإلكترونية بين الشركات B2B إلى **نشط** ، ويمكن للمستخدم الجديد تسجيل الدخول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B باستخدام عنوان البريد الإلكتروني الخاص به. يمكن للمستخدمين استخدام سير عمل التسجيل لتعريف كلمة المرور للحساب الخاص بهم.

## <a name="edit-business-partner-user-details"></a>تحرير تفاصيل المستخدم الخاص بشريك العمل

لتحرير تفاصيل مستخدمي شركاء الأعمال، اتبع الخطوات التالية.

1. سجل الدخول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B كمسؤول.
1. انتقل إلى **حسابي \> مستخدمو المؤسسة \> عرض تفاصيل**، وحدد زر **تحرير** (رمز القلم)، وقم بإجراء التغييرات المطلوبة، ثم حدد **حفظ**. ويتم تطبيق هذه التغييرات فقط بعد تشغيل وظيفتي **P-0001**، **مزامنة العملاء وشركاء الأعمال من وضع عدم المزامنة**، و **1010** (**العملاء**).

## <a name="remove-a-business-partner-user"></a>إزالة مستخدم خاص بشريك أعمال

كما هو مطلوب، يمكن للمسؤول إزالة المستخدمين الموجودين في مؤسسة شريك العمل من قائمة المستخدمين الذين يمكنهم الوصول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B.

لإزالة مستخدم خاص بشريك العمل، اتبع الخطوات التالية.

1. سجل الدخول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B كمسؤول.
1. انتقل إلى **حسابي \> مستخدمو المؤسسة \> عرض التفاصيل**، وحدد زر **إزالة مستخدم** (الرمز "X"). عند ظهور رسالة تأكيد، قم بتأكيد رغبتك في إزالة المستخدم. ويتم تطبيق هذا التغيير فقط بعد تشغيل وظيفتي **P-0001**، **مزامنة العملاء وشركاء الأعمال من وضع عدم المزامنة**، و **1010** (**العملاء**).

> [!NOTE]
> عند إزالة مستخدم من قائمة المستخدمين الذين يمكنهم الوصول إلى موقع ويب التجارة الإلكترونية بين الشركات B2B، تتم إزالة سجل العميل المقابل من سجل التدرج الهرمي لعميل شريك الأعمال. ومع ذلك، لا يتم حذف سجل العميل نفسه من المركز الرئيسي لـ Commerce.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>ضم شريك أعمال والمستخدمين في المركز الرئيسي لـ Commerce

يمكن للمسؤولين ضم شركاء العمل والمستخدمين مباشرة في المركز الرئيسي لـ Commerce.

لضم شركاء العمل والمستخدمين في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. قم بإنشاء سجل عميل من **نوع مؤسسة** لمؤسسة شريك الأعمال.
1. قم بإنشاء سجل عميل من **نوع شخص** لمستخدمي شركاء الأعمال. تأكد من تحديد عنوان بريد إلكتروني رئيسي لكل عميل.
1. بالنسبة لكل سجل عميل من **نوع شخص** يجب تعيين كمستخدم مسؤول لمؤسسة شريك الأعمال في علامة التبويب السريعة **البيع بالتجزئة**، قم بتعيين خيار **مسؤول B2B** إلى **نعم**.
1. قم بإنشاء معرف التدرج الهرمي للعميل. في حقل **الاسم**، أدخل اسمًا.
1. في حقل **المؤسسة**، أدخل عميل مؤسسة شريك الأعمال.
1. حد **إضافة**، ثم حدد عميلاً في الحقل **الاسم**.
1. قم بتكرار هذه العملية لإضافة عملاء إضافيين إلى التدرج الهرمي.

## <a name="additional-information"></a>معلومات إضافية

- يمكن تكوين كافة المهام المذكورة في هذا الموضوع ليتم تشغيلها وفقًا لجدول بتنسيق دفعي. ومن المتوقع هو أن يقوم شركاء الأعمال بتكوين وظائف الدفعة كما هو مطلوب.
- حاليا، يمكن تعيين سجل مستخدم/عميل واحد فقط كمستخدم مسؤول، ولا يمكن تغيير هذا الدور إلا في المركز الرئيسي لـ Commerce. لا يوجد أي دعم لإمكانات الخدمة الذاتية التي تسمح لشركاء العمل بتعيين مسؤولين متعددين أو تغيير مسؤولين من مواقع ويب التجارة الإلكترونية بين الشركات B2B.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- على الرغم من أنه يمكن تحديد حدود الانفاق للمستخدمين، لكن لم يتم بعد تنفيذ فرض حدود الانفاق أثناء عملية إدخال الأمر.
- يعتمد كل منطق عمل والتحقق من خبرة المستخدم في موقع ويب التجارة الإلكترونية بين الشركات B2B على تكوين سجل العميل الذي يتم تعيينه للمستخدم في المركز الرئيسي لـ Commerce.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد موقع تجارة إلكترونية بين الشركات B2B](set-up-b2b-site.md)

[إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات B2B](org-model.md)

[تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات B2B](payment-method.md)

[تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات B2B](quantity-limits.md)

[نظرة عامة على التسلسل الرقمي](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]