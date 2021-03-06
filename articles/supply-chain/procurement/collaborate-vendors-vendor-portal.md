---
title: التعاون مع المورّدين باستخدام مدخل المورِّد‬
description: يشرح هذا الموضوع كيف يمكن لوكلاء الشراء استخدام مدخل المورّد للتعاون مع المورّدين الخارجيين أثناء عملية تأكيد أمر الشراء. تنطبق هذه المعلومات فقط على إصدارات Dynamics AX لشهري فبراير 2016 ومايو 2016.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aece4fd621be803abe5011e40785f6a3301924f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019093"
---
# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>التعاون مع المورّدين باستخدام مدخل المورِّد‬

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيف يمكن لوكلاء الشراء استخدام مدخل المورّد للتعاون مع المورّدين الخارجيين أثناء عملية تأكيد أمر الشراء. تنطبق هذه المعلومات فقط على إصدارات Dynamics AX لشهري فبراير 2016 ومايو 2016.

تنطبق المعلومات الواردة في هذا الموضوع فقط على إصدارات Dynamics AX لشهري فبراير 2016 ومايو 2016. لمزيد من المعلومات حول وظيفة تعاون الموردين الجديدة، راجع [تعاون الموردين مع موردين خارجيين‬‏‫](vendor-collaboration-work-external-vendors.md).  

يستهدف مدخل المورّد المورّدين الذين ليس لديهم تكامل التبادل الإلكتروني للبيانات (EDI) مع Microsoft Dynamics AX لتبادل معلومات أوامر الشراء. ويسمح المدخل لوكلاء الشراء بإرسال أمر شراء إلى المورّد، ثم تلقي استجابة "مؤكد" أو "مرفوض" مباشرةً في Dynamics AX.  

يمكن تكوين العملية بحيث يتم تأكيد الأمر من قِبل المورّد بشكل تلقائي. في هذه الحالة، يجب متابعة الأمر في بعض الأحيان فقط، عندما يتم رفض طلب، أو إذا تم تسجيل تأكيد المورّد كاستجابة ولكن لم يتم تحديث حالة أمر الشراء إلى **مؤكد** نتيجة حدوث مشكلة ما أثناء عملية التأكيد.

## <a name="po-confirmation-and-rejection"></a>تأكيد أمر الشراء ورفضه
يتم إعداد أوامر الشراء في Dynamics AX. إذا كان لديك أمر شراء بحالة من **معتمد**، سترسله إلى المورّد قبل إنشاء طلب تأكيد. وإذا كنت تريد لفت انتباه المورّد إلى أمر شراء جديد، فيمكنك أيضًا استخدام نظام إدارة الطباعة لإرسال أمر الشراء عن طريق البريد الإلكتروني. ويظهر أمر الشراء في مدخل المورّد، ويتضمن خيارًا يستطيع المورّد استخدامه لتأكيده أو رفضه. باستطاعة المورّد أيضًا إضافة تعليقات لتوصيل معلومات مثل التغييرات على أمر الشراء.  

في مدخل المورّد، يستطيع المورّد مشاهدة بنود الأمر. وتتضمن هذه البنود معلومات مثل رقم المنتج الخارجي وأبعاده ومعلومات عن السعر والكمية وتاريخ التسليم وعنوان التسليم. باستطاعة المورّد إنشاء تقرير يُظهر معلومات أمر الشراء، والسعر الإجمالي أيضًا. تظهر المصاريف المرتبطة بالمورّد إذا نقر المورّد فوق زر **المصاريف** في الرأس أو في البنود. ويمكن للموردين استيراد معلومات أمر الشراء في النظام الخاص بهم باستخدام وظيفة **تصدير إلى Excel**.  

يُظهر الجدول التبادل تبادل المعلومات النموذجي، استنادًا إلى كيفية استجابة المورّد عند إرسال أمر شراء للتأكيد:

| نوع الاستجابة                                                                                                  | النتيجة                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| يؤكد المورّد لأمر. يتم تكوين النظام لتأكيد أوامر الشراء تلقائيًا عندما يرسل المورّد تأكيدًا.    | يتم تحديث حالة الأمر إلى **مؤكد**. إذا منع شيء ما تحديث الأمر، فستبقى مع ذلك استجابة المورّد مسجلة على أن الأمر **مؤكد**، ولكن حالة أمر الشراء تبقى **قيد المراجعة الخارجية**.                                                                       |
| يؤكد المورّد لأمر. لم يتم تكوين النظام لتأكيد أوامر الشراء تلقائيًا عندما يرسل المورّد تأكيدًا. | يتم تسجيل استجابة المورّد على أن الأمر **مؤكد**، ولكن حالة أمر الشراء تبقى **قيد المراجعة الخارجية**.                                                                                                                                                                                      |
| المورد يرفض لأمر.                                                                                     | يتم تسجيل استجابة المورّد على أن الأمر **مرفوض**، ولكن حالة أمر الشراء تبقى **قيد المراجعة الخارجية**. يتم تلقي الرفض مع السبب واقتراح للتغيير، مثل تاريخ تسليم بديل. يمكنك تحديث أمر الشراء ثم إرسال إصدار جديد للتأكيد. |

## <a name="changes-to-a-po"></a>تغييرات على أمر شراء
عند الحاجة إلى تغيير أمر شراء تم تأكيده بالفعل، يمكنك إرسال أمر شراء جديد إلى المورّد عبر مدخل المورّد. سيتضمن أمر الشراء الجديد لاحقة إصدار تشير إلى أنه إصدار معدّل من أمر شراء تم إرساله في وقت سابق. يسمح موقع المورّد للمورّدين بتعقب محفوظات كل أمر. سيبقى إصدار أمر الشراء الذي تم تأكيده في السابق في قائمة أوامر الشراء حتى يتم تأكيد أمر الشراء الجديد.  

عندما تقوم بإلغاء أمر شراء، تتغير الحالة مرة أخرى إلى **معتمد**. يجب عليك إعادة إرسال أمر الشراء إلى المورّد عبر مدخل المورّد، بحيث يتمكن المورّد من تأكيد الإلغاء أو رفضه. بعد تأكيد الإلغاء، يظهر أمر الشراء في قائمة المورّد الخاصة بأوامر الشراء التي تم تأكيدها على أنها **ملغاة**.

## <a name="versions-status-transitions-and-change-management"></a>الإصدارات وانتقالات الحالة وإدارة التغييرات
عند إرسال أمر شراء إلى المورّد، يتم تسجيله في النظام كإصدار محدد من أمر الشراء وتتغير الحالة من **معتمد** إلى **قيد المراجعة الخارجية‬**. إذا تغيّر أمر الشراء فيما بعد، فسيتم إنشاء إصدار جديد من أمر الشراء، وتتغيّر الحالة من جديد إلى **معتمد** (أو **مسودة**, إذا تم تشغيل إدارة التغييرات).  

يُظهر الجدول التالي مثالاً على التغييرات في الحالة والإصدار التي قد يمر بها أمر الشراء.

| الإجراء                                                   | الحالة والإصدار                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| يتم إنشاء الإصدار الأولى لأمر الشراء في Dynamics AX. | الحالة هي **معتمد**.                                                                           |
| يتم إرسال أمر الشراء إلى مدخل المورّد.                     | يتم تسجيل إصدار في مدخل المورّد وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.    |
| ستجري بعض التغييرات المطلوبة من قِبل المورّد.  | تتغير الحالة مرة أخرى إلى **معتمد**.                                                            |
| سترسل الإصدار الجديد من أمر الشراء إلى موقع المورّد. | يتم تسجيل إصدار جديد في مدخل المورّد وتتغير الحالة إلى **قيد المراجعة الخارجية‬**. |
| يوافق المورّد على الإصدار الجديد من أمر الشراء.           | تتغير الحالة إلى **مؤكد**.                                                                |

لمشاهدة إصدارات أمر الشراء التي تم إرسالها إلى المورّد واستجابات المورّد، انقر فوق **دفاتر اليومية** &gt; **طلبات التأكيد** من أمر الشراء.  

ستظهر الأوامر التي تم إرسالها إلى المورّد للحصول على استجابة وحالتها **قيد المراجعة الخارجية** إما في قائمة **تم إرسال أوامر الشراء إلى المورِّد، في انتظار الرد** أو قائمة **تم إرسال أوامر الشراء إلى مدخل المورِّد، الاستجابة تتطلب إجراءً‬**. عندما تغيّر أمرًا تم إرساله إلى المورّد، بحيث تتغير الحالة مرة أخرى إلى **معتمد**، فلن يظهر الأمر من جديد في هذه القوائم. لمعرفة ما إذا كان المورّد قد استجاب في وقت سابق للأمر، انقر فوق **دفاتر اليومية** &gt; **طلبات التأكيد**.  

لا يتعيّن على المورّدين تأكيد أمر الشراء في مدخل المورّد. يمكنهم أيضًا إرسال رسالة بريد إلكتروني أو التبليغ عن موافقتهم على أمر الشراء عبر قنوات أخرى. يمكنك عندئذٍ تأكيد الأمر يدويًا في Dynamics AX. في هذه الحالة، تتلقى تحذيرًا يفيد بأنه قد تم تأكيد الأمر حتى لو لم يكن هناك استجابة من المورّد. يظهر أمر الشراء عندئذٍ في محفوظات التأكيد في مدخل المورّد كأمر مؤكد مفتوح ليس لديه أية استجابات. علاوةً على ذلك، لن يتوفر للمورّد خيار تأكيد أمر الشراء أو رفضه.  

**ملاحظة:** يكون إصدار أمر الشراء المتوفر لعمليات أخرى في Dynamics AX الإصدار الأحدث دائمًا، حتى لو لم يكن مسجلاً بعد.

### <a name="change-management"></a>إدارة التغييرات

إذا قمت بتشغيل إدارة التغييرات لأمر شراء، فسيمر أمر الشراء عبر سير عمل الموافقة للوصول إلى الحالة **معتمد**. ولا تظهر هذه العملية للمورد.  

عند تشغيل إدارة التغييرات لأمر شراء، يتم تسجيل الإصدار عندما تتم الموافقة على أمر الشراء، وليس عندما يتم إرسال أمر الشراء إلى المورّد أو تأكيده.  

يُظهر الجدول التالي مثالاً على التغييرات في الحالة والإصدار التي قد يمر بها أمر الشراء عند تشغيل إدارة التغييرات.


|                                                    الإجراء                                                     |                                                                                                                                                                                                                      الحالة والإصدار                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           يتم إنشاء الإصدار الأولى لأمر الشراء في Dynamics AX.                            |                                                                                                                                                                                                            الحالة هي <strong>مسودة</strong>.                                                                                                                                                                                                             |
| يتم إرسال أمر الشراء إلى عملية الموافقة. (هذه عملية داخلية لا يتدخل فيها المورد.) |                                                                                                                        تتغيّر الحالة من <strong>مسودة‬</strong> إلى <strong>قيد المراجعة‬</strong> إلى <strong>اعتماد</strong> إذا لم يتم رفض أمر الشراء أثناء عملية الموافقة. يتم تسجيل أمر الشراء المعتمد كإصدار.                                                                                                                        |
|                                      يتم إرسال أمر الشراء إلى مدخل المورّد                                      |                                                                                                                                                                      يتم تسجيل الإصدار في مدخل المورّد وتتغير الحالة إلى <strong>قيد المراجعة الخارجية‬</strong>.                                                                                                                                                                       |
|                            ستجري بعض التغييرات المطلوبة من قِبل المورّد.                            |                                                                                                                                                                                                    تتغير الحالة مرة أخرى إلى <strong>مسودة</strong>.                                                                                                                                                                                                     |
|                              يتم إرسال أمر الشراء إلى عملية الموافقة مرة أخرى.                               | تتغيّر الحالة من <strong>مسودة‬</strong> إلى <strong>قيد المراجعة‬</strong> إلى <strong>اعتماد</strong> إذا لم يتم رفض أمر الشراء أثناء عملية الموافقة. بدلاً من ذلك، يمكن تكوين النظام بحيث لا تحتاج تغييرات محددة في الحقل إلى إعادة الموافقة. وفي هذه الحالة، تتغير الحالة إلى <strong>مسودة</strong> أولاً، ثم يتم تحديثها بشكل تلقائي إلى <strong>معتمد</strong>. يتم تسجيل أمر الشراء المعتمد كإصدار جديد. |
|                           سترسل الإصدار الجديد من أمر الشراء إلى موقع المورّد.                            |                                                                                                                                                                    يتم تسجيل الإصدار الجديد في مدخل المورّد وتتغير الحالة إلى <strong>قيد المراجعة الخارجية‬</strong>.                                                                                                                                                                     |
|                                يوافق المورّد على الإصدار الجديد من أمر الشراء.                                 |                                                                                                                                                     تتغير الحالة إلى <strong>مؤكد</strong>، إما تلقائياً أو عندما تتلقى الاستجابة من المورّد ثم تؤكد أمر الشراء.                                                                                                                                                     |

<a name="additional-resources"></a>الموارد الإضافية
--------

[أمان مستخدم مدخل المورّد على الإنترنت‬](configure-security-vendor-portal-users.md)

[مساحة عمل فوترة تعاون المورد](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]