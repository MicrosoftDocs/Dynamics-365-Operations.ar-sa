---
title: إنشاء مستخدمي مدخل العميل وإدارتهم (يحتوي على فيديو)
description: يشرح هذا المقال كيفية إنشاء حسابات مستخدمي مدخل العميل وتعيين الأذونات لهم.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ec4f20daac39e1728ab46db159059e51a0cae0a6
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103759"
---
# <a name="create-and-manage-customer-portal-users"></a>إنشاء مستخدمي مدخل العميل وإدارتهم

[!include [banner](../includes/banner.md)]


في عملية التنفيذ الجاهزة، لا توجد أي طريقة تسمح للمستخدمين بالتسجيل ذاتيًا لمواقع الويب التي يتم إنشاؤها باستخدام مدخل العميل. لتسجيل الدخول إلى موقع ويب واستخدامه، يجب ان تتم دعوة المستخدمين بواسطة المسؤول. قامت Microsoft بحظر قدرة المستخدمين على التسجيل الذاتي بشكل متعمد.

قبل ان يتمكن المستخدم من استخدام موقع ويب، يجب إنشاء سجل جهة اتصال لذلك المستخدم. ويشير هذا السجل إلى حساب العميل والكيان القانوني الذي ينتمي اليه المستخدم. وتعتبر هذه المعلومات ضرورية لضمان إمكانية قيام المستخدم بإنشاء أوامر مبيعات وعرضها.

عندما يقوم المستخدم بالتسجيل الذاتي، يتم إنشاء سجلات جهات الاتصال لهم بشكل تلقائي. وبالتالي، لا يمكنك أن تتأكد من أن المستخدم يحدد مستخدم حساب العميل والكيان القانوني الصحيحين. من ناحية أخرى، تتيح عملية الدعوة للمسؤول إمكانية تعيين حساب العميل والكيان القانوني الصحيحين إلى سجل جهة الاتصال قبل إرسال الدعوة. إذا كنت تفكر في تخصيص الحل لتمكين المستخدمين من التسجيل ذاتيًا، احرص على مراعاة العواقب المحتملة.

## <a name="video"></a>الفيديو
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

تم تضمين الفيديو [دعوة العملاء للتسجيل في مدخل العميل واستخدامه](https://youtu.be/drGUYHX9QIQ) (المبين أعلاه) في [قائمة تشغيل التمويل والعمليات](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) المتوفرة في YouTube.

## <a name="prerequisite-setup"></a>إعداد المتطلبات الأساسية

يتم تخزين جهات الاتصال في مداخل Power Apps كسجلات في جدول **جهات الاتصال** في Microsoft Dataverse ثم تقوم الكتابة المزدوجة بمزامنة هذه السجلات مع Microsoft Dynamics 365 Supply Chain Management كما هو مطلوب.

![الرسم التخطيطي للنظام لجهات اتصال مدخل العميل.](media/customer-portal-contacts.png "الرسم التخطيطي للنظام لجهات اتصال مدخل العميل")

قبل أن تبدأ دعوة عملاء جدد، تأكد من تمكين تعيين جدول **جهة الاتصال** في الكتابة المزدوجة.

## <a name="the-invitation-process"></a>عملية الدعوة

لدعوة جهة اتصال موجودة إلى مدخل العميل، اتبع الخطوات في [دعوه جهات الاتصال إلى مداخلك](/powerapps/maker/portals/configure/invite-contacts) في وثائق مداخل Power Apps.

قبل دعوة أحد العملاء للانضمام إلى مدخل العميل، تأكد من توفر [سجل جهة الاتصال](/powerapps/maker/portals/configure/configure-contacts) الخاص بالعميل واعمل على إعداده بالطريقة التالية:

1. عيّن حقل **الشركة** إلى الكيان القانوني الذي تريد أن ينتمي إليه العميل في Supply Chain Management.
2. عيّن حقل **رقم الحساب** إلى رقم حساب العميل الذي تريد أن يكون متوفرًا للمستخدم في Supply Chain Management.

بعد إنشاء جهة اتصال، من المفترض أن تتمكن من رؤيتها في Supply Chain Management.

لمزيد من المعلومات، راجع [تكوين جهة اتصال لاستخدامها في مدخل](/powerapps/maker/portals/configure/configure-contacts) في وثائق مداخل Power Apps.

## <a name="out-of-box-web-roles-and-table-permissions"></a>أدوار الويب الجاهزة وأذونات الجدول

يتم تعريف أدوار المستخدمين في مداخل Power Apps بواسطة [أدوار الويب](/powerapps/maker/portals/configure/create-web-roles) و[وأذونات الجدول](/powerapps/maker/portals/configure/assign-entity-permissions). يتم تعريف عدد قليل من الأدوار لمدخل العميل الجاهز. يمكنك إنشاء أدوار جديدة، ويمكنك تعديل أدوار موجودة أو إزالتها.

### <a name="out-of-box-web-roles"></a>أدوار الويب الجاهزة

يصف هذا القسم أدوار الويب التي يتم تقديمها مع مدخل العميل.

لمزيد من المعلومات حول كيفية تعديل أدوار المستخدمين الجاهزة، راجع [إنشاء أدوار الويب للمداخل](/powerapps/maker/portals/configure/create-web-roles) و[إضافة الأمان المستند إلى السجل باستخدام أذونات الجدول للمداخل](/powerapps/maker/portals/configure/assign-entity-permissions) في وثائق مداخل Power Apps.

#### <a name="administrator"></a>المسؤول

يقوم المسؤول بمراقبة موقع ويب وصيانته. سيقوم هذا الشخص بتزويد مدخل العميل وإعداده. يحافظ المسؤول على جواني تكنولوجيا المعلومات والأمان في المدخل، ويتأكد من أن شيء يعمل بطريقة سلسة. قد يقوم المسؤول أيضًا بتخصيص و/أو تغيير المدخل عن طريق إضافة وظائف جديدة وإنشاء أدوار جديدة والمزيد.

#### <a name="customer-representative"></a>ممثل العميل

يعمل ممثل العميل لصالح شركة العميل ويتولى مسؤلية إدارة الأوامر التي تضعها الشركة. بإمكان ممثل العميل رؤية كافة الأوامر التي تم وضعها للشركة والمستخدمين الذين قاموا بوضعها. علاوةً على ذلك، بإمكان ممثل العميل رؤية معلومات حول الحساب الإجمالي والذي يمكن لجهات الاتصال وضع أوامر بالنيابة عن هذا الحساب.

#### <a name="authorized-users"></a>المستخدمون المخولون

بإمكان المستخدمين المخولين وضع الأوامر وعرض حالة الأوامر التي قاموا بوضعها. ومع ذلك، لا يمكنهم عرض حالة الأوامر التي وضعها مستخدمون آخرون في شركتهم.

#### <a name="unauthorized-users"></a>المستخدمون غير المخولين

يتعذر على المستخدمين غير المخولين عرض أي بيانات. يمكنهم رؤية فقط المعلومات العامة، مثل البنود والشروط، وتفاصيل حول الشركة التي تقوم بتشغيل مدخل العميل.

#### <a name="example"></a>مثال

يعرض الجدول التالي أوامر المبيعات التي يمكن للمستخدمين في كل دور ويب الاطلاع عليها في النظام.

| أمر مبيعات | مسؤول | ممثل العميل للعميل&nbsp;X | المستخدم المخول: جين | المستخدم المخول: سام | المستخدم غير المخول: مايا |
|---|---|---|---|---|---|
| العميل&nbsp;X مقدم الأمر:&nbsp;جين | ‏‏نعم | ‏‏نعم | ‏‏نعم | لا | لا |
| العميل&nbsp;X مقدم الأمر:&nbsp;سام | ‏‏نعم | ‏‏نعم | لا | ‏‏نعم | لا |
| العميل&nbsp;Y مقدم الأمر:&nbsp;مايا | ‏‏نعم | لا | لا | لا | لا |

> [!NOTE]
> على الرغم من أن سام وجين هما من جهات الاتصال التي تعمل لصالح العميل X، إلا أنه لا يمكنهما رؤية سوى الأوامر التي قاما بوضعها ولا شيء آخر. وعلى الرغم من وجود أمر لمايا في النظام، إلا أنه لا يمكنها رؤية هذا الأمر في مدخل العميل، لأنها مستخدم غير مخول. (علاوةً على ذلك، يجب أن تكون قد وضعت الأمر عبر قناة أخرى غير مدخل العميل.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
