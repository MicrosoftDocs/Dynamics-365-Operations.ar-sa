---
title: ‏‫معرفات التسجيل
description: توفر هذه المقالة معلومات عن إعداد معرفات التسجيل واستخدامها.
author: kfend
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264824
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
ms.openlocfilehash: 380cb1d2b52d5d0debffdbe73183be2f5e783f21
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274540"
---
# <a name="registration-ids"></a>‏‫معرفات التسجيل

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات عن إعداد معرفات التسجيل واستخدامها.

يُستخدم لعرض البلدان والمناطق التي يوجد بها لوائح ومتطلبات مختلفة لتسجيل أرقام التسجيل الضريبي أو المُعرفات. توفر هذه المقالة نظرة عامة على الإعدادات المطلوبة ومعالجة أنواع التسجيل المدعومة للأطراف في البلدان الأوروبية/المناطق المختلفة. تحتوي كافة البلاد/المناطق على متطلباتها الخاصة لدعم الوظائف المختلفة المخصصة لهذه البلد المتعلقة بأرقات التسجيل التي تقدمها مكاتب الدولة المختلفة. تتضمن أمثلة أرقام التسجيل، رقم التأمين الاجتماعي (SSN) ورقم تعريف الضريبة (TIN)، ورقم تعريف ضريبة القيمة المضافة الأوروبي (EU VAT ID). توفر هذه الميزة إطار موحد لجميع البلدان في جميع المناطق مع مراعاة المتطلبات الخاصة بالبلد لبعض الدول الأوروبية. توضح الأقسام التالية التدفق العام للمعلومات المستخدمة لإعداد ومعالجة معرفات التسجيل.

## <a name="registration-type-creation"></a>إنشاء نوع التسجيل
وقبل أن تقوم بإدخال مُعرف التسجيل، يجب عليك إعداد أنواع التسجيل للأنواع المختلفة من أرقام التسجيل التي يخضع لها كل طرف. اذهب إلى صفحة **إدارة المؤسسة** &gt; **دفتر العناوين العمومي** &gt; **‎أنواع التسجيل** &gt; **أنواع التسجيل**، لإنشاء وإدارة أنواع التسجيل للموردين والعملاء، والعمال والكيانات القانونية في مختلف البلاد/المناطق.

|الحقل                 |‏‏الوصف      |
|------------------------------|----------------------------|                                                                           
| الاسم                | اسم نوع التسجيل. |                                                                           
| ‏‏الوصف         | وصف نوع التسجيل. |
| البلد/المنطقة      | المعرّف الفريد الخاص بالبلد/المنطقة.|
| هيئة الضرائب       | هيئة الضرائب المقترنة بنوع التسجيل.|
| مقصور على       | نوع القيد الذي ينطبق على نوع التسجيل الضريبي: بلا، شخص، المؤسسة.|
| التنسيق              | تنسيق التحقق من الصحة لنوع التسجيل.|
| يمكن تحديثه      | حدد إذا كان رقم التسجيل لنوع التسجيل يمكن تحديثه بعد إدخاله.|
| فريد              | حدد إذا كان رقم التسجيل لنوع التسجيل فريدًا. |
| رئيسي للبلد | إذا كان هناك طرف مقترن بعنوان واحد أو أكثر في دولة محددة، وكان مُعرف التسجيل صالحًا لجميع هذه العناوين، يجب عليك تحديد عنوان واحد كعنوان أساسي للدولة. يمكنك فقط تسجيل مُعرف واحد كمعرف أساسي. حدد إذا كان رقم التسجيل يمكن إدخاله فقط للأساسي لعنوان البلد. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>عيّن نوع تسجيل لفئة التسجيل
تُعد فئة التسجيل هي مُعرف تسجيل البلد/المنطقة المعتمد للاستخدام في البلد/المنطقة المحددة لأغراض الضرائب والجمارك وللأغراض الأخرى. تحدد هذه الفئة قواعد التحقق من الصحة لمُعرف تسجيل معين (ويشمل ذلك أرقام الفحص وغيرها)، وإدراج مُعرف التسجيل في تقارير مختلفة. استخدم صفحة **‎إدارة المؤسسة** &gt; **دفتر العناوين العمومي** &gt; **‎أنواع التسجيل** &gt; **‎فئات التسجيل** لتعيين نوع التسجيل لبلد معين لفئة التسجيل المدعومة.

| الحقل            | ‏‏الوصف|
|-----------------------|----------------|
| نوع التسجيل     | نوع التسجيل في البلد/المنطقة المعينة.|
| مقصور على         | نوع القيد الذي ينطبق على نوع التسجيل الضريبي: بلا، شخص، المؤسسة.|
| فئة التسجيل | معرف التسجيلات الفريد المعتمد للاستخدام في البلد. تظهر القائمة الكاملة للفئات المعتمدة لاحقًا في هذه المقالة. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>إدخال مُعرفات التسجيل لسجلات دفتر العناوين العمومي

يحتوي دفتر العناوين العمومي (GAB) على معلومات العنوان الموحد للعملاء والموردين، وجهات الاتصال، وعلاقات العمل والكيانات القانونية. لمزيد من المعلومات، انظر [نظرة عامة حول دفتر العناوين العمومي](../../fin-ops-core/fin-ops/organization-administration/overview-global-address-book.md). يمكن أن تحتوي سجلات الطرف التي يتم تخزينها في دفتر العناوين العمومي على سجل عناوين واحد أو أكثر. يتم استخدام هذه العناوين لأغراضٍ مختلفة، مثل الفوترة أو التسليم. يمكنك إعداد معرفات تسجيل لمعلومات العنان الخاصة بالعملاء والموردين والعمال والكيانات القانونية. قم بالبحث عن سجل الطرف (الكيان القانوني أو المورد أو العميل أو العامل) الذي تريد إدخال المُعرف المسجل فيه، ثم انقر فوق **"مُعرفات التسجيل"** الموجودة في النماذج المتعلقة بالطرف أو الكيان القانوني، أو المورد أو العميل أو العامل لفتح صفحة **إدارة العناوين**. في علامة تبويب **تسجيل الضريبة**، انقر فوق **إضافة**، ثم أدخل المعلومات التالية حول مُعرف التسجيل.


|الحقل                |‏‏الوصف                                                |
|---------------------|-----------------------------------------------------------|
| نوع التسجيل   | نوع التسجيل في البلد/المنطقة المحددة.     |
| رقم التسجيل | معرف التسجيل الطرف.                                |
| ‏‏الوصف         | وصف رقم التسجيل.               |
| قسم             | المعلومات الإضافية المتعلقة برقم التسجيل. |
| جهة الإصدار      | الهيئة التي قامت بإصدار رقم التسجيل.        |
| تاريخ الإصدار         | تاريخ الإصدار لرقم التسجيل.              |
| فعالة           | تاريخ السريان لرقم التسجيل.           |
| انتهاء الصلاحية          | تاريخ انتهاء الصلاحية لرقم التسجيل.          |

> [!NOTE]
> يمكن تحديد رقم الإعفاء الضريبي للكيان القانوني، أو المورد أو العميل من مُعرفات التسجيل المرتبطة بمُعرف ضريبة القيمة المضافية والمدخلة للطرف.

## <a name="search-for-records-by-registration-id"></a>البحث عن السجلات حسب معرف التسجيل
البحث عن سجلات الطرف استناداً إلى مُعرف التسجيل المتوفر على النماذج المتعلقة بالطرف أو الكيان القانوني أو المورد أو العميل أو العامل. انقر فوق **البحث بمعرف التسجيل** لفتح صفحة **معايير البحث بمعرف التسجيل**. تحديد معايير البحث، ثم انقر فوق **بحث**. سوف يعرض النظام السجلات المحددة من دفتر العناوين العمومي والأنواع المقترنة بها من سجل الطرف.

## <a name="supported-registration-categories"></a>فئات التسجيل المدعومة
يسرد الجدول التالي أنواع التسجيل المدعومة. إذا اعتدت على حقول Microsoft Dynamics AX 2012 لمُعرفات التسجيل، فهذا الجدول يعين أيضًا هذه الحقول إلى فئات تسجيل Dynamics 365 Finance.

| فئة تسجيل في Finance         |البلد/المنطقة  | حقل/شرط Dynamics AX 2012|
|---------------------------------------------------------------|---------------------|---------------------------------|
| معرف ضريبة القيمة المضافة                                                        | جميع بلدان الاتحاد الأوروبي|  رقم الإعفاء الضريبي (مُعرف الضريبة للنوع التشريعي في AX 2012 R3)|
| معرف الشركة (COID)                                          | جمهورية التشيك، إستونيا، المجر، لاتفيا، لتوانيا، بولندا، روسيا | رقم الشرك (EnterpriseNumber) رقم التسجيل (RegNum\_W) رقم التسجيل (RegNum\_W) رقم التسجيل (RegNum\_W) رقم التسجيل (RegNum\_W) كود الشركة (EnterpriseCode) رقم التسجيل (RegNum\_W) المُعرف الفريد (المُعرف الفريد للنوع التشريعي في AX 2012 R3) |
| معرف الفرع                                                     | بلجيكا            | رقم الفرع (BranchNumber)|
| Značka Spisová (رقم التسجيل، جهة الإصدار، القسم) | جمهورية التشيك     | إدخال رقم (CommercialRegisterInsetNumber) يتم الاحتفاظ به في السجل التجاري (CommercialRegister) قسم السجل التجاري (CommercialRegisterSection)|
| معرف عميل الجمارك                                           | فنلندا | رقم عميل الجمارك (CustomsCustomerNumber\_FI)|
| INN                                                           | روسيا الاتحادية| INN (النوع التشريعي INN في AX 2012 R3)|
| RRC                                                           | روسيا الاتحادية| RRC (النوع التشريعي RRC في AX 2012 R3)|
| OKDP                                                          | روسيا الاتحادية| OKDP (النوع التشريعي OKDP في AX 2012 R3)|
| OKPO                                                          | روسيا الاتحادية| OKPO (النوع التشريعي OKPO في AX 2012 R3)|
| RCOAD                                                         | روسيا الاتحادية| RCOAD (النوع التشريعي RCOAD في AX 2012 R3)|
| OGRN                                                          | روسيا الاتحادية| OGRN (النوع التشريعي OGRN في AX 2012 R3) |
| SNILS                                                         | روسيا الاتحادية| SNILS (النوع التشريعي SNILS في AX 2012 R3)|
| CIFTS                                                         | روسيا الاتحادية| CIFTS (النوع التشريعي CIFTS في AX 2012 R3)|
| جواز السفر                                                      | أسبانيا             | جواز السفر|
| مستند تعريف رسمي                              | إسبانيا             | مستند تعريف رسمي|
| الشهادة الإقامة                                         | إسبانيا             | الشهادة الإقامة|
| مستند تعريف آخر                                 | إسبانيا             | مستند تعريف آخر|
| غير مدرج في التعداد                                                  | أسبانيا             | غير متوفر في AX 2012 R3|


للمزيد من المعلومات حول معالجة معرفات التسجيل، بما في ذلك المتطلبات الأساسية اللازمة، انظر تسجيلات المهام التالية لمُعرف ضريبة القيمة المضافية في Lifecycle Services.

-   إعداد معرف ضريبة قيمة مضافة صالح
-   تسجيل معرف ضريبة القيمة المضافة للمورّد
-    البحث عن طرف باستخدام معرف ضريبة القيمة المضافة






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
