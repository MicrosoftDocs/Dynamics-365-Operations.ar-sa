---
title: تثبيت مدخل العميل وإعداده وتحديثه
description: يوفر هذا الموضوع تفاصيل الترخيص وتعليمات حول إعداد مدخل العميل.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fa95995320a0f81c040eeebe6fd796200fbff13f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255027"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>تثبيت مدخل العميل وإعداده وتحديثه

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>متطلبات الترخيص

لتطبيق موقع العميل، يجب أن تتوفر لديك التراخيص التالية:

- **مداخل Power Apps** – هذا الترخيص مطلوب لاستضافة مدخل العميل. يتم ترخيص المداخل استنادًا إلى الاستخدام. لمزيد من المعلومات، راجع [متطلبات ترخيص مداخل Power Apps](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **الكتابة المزدوجة** - يجب أن تتوفر لديك التراخيص اللازمة لتمكين الكتابة المزدوجة لجداول Supply Chain Management. لمزيد من المعلومات، راجع [متطلبات النظام للكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>التبعيات على الكتابة المزدوجة ومداخل Power Apps

يعتمد مدخل العميل على مداخل Power Apps والكتابة المزدوجة، كما هو مبين في الشكل التوضيحي التالي.

![تبعيات مدخل العميل](media/customer-portal-elements.png "تبعيات مدخل العميل")

بعكس الميزات الأخرى من Supply Chain Management، يقيم قالب مدخل العميل في مداخل Power Apps. وبالتالي، يتحدد مدخل العميل بالوظيفة والقدرات التي توفرها مداخل وجداول Power Apps في الكتابة المزدوجة.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>الإعداد المطلوب لتمكين مدخل العميل

بعد أن تتأكد من امتلاك التراخيص المطلوبة، يمكنك إعداد الكتابة المزدوجة كما ورد في [إرشادات المزامنة الأولية للكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

تأكد من تمكين تعيينات الجداول التالية في الكتابة المزدوجة:

- رأس أمر المبيعات
- تفاصيل أمر المبيعات
- الحسابات
- جهات الاتصال
- المنتجات

بعد اكتمال هذا الإعداد، يمكنك تزويد قالب مدخل العميل.

## <a name="provision-the-customer-portal"></a>تزويد مدخل العميل

قبل البدء، تأكد من إكمال [الإعداد المطلوب](#required-setup). ثم اتبع الخطوات التالية لتزويد مدخل العميل.

1. انتقل إلى [make.powerapps.com](https://make.powerapps.com/).
2. تأكد من استخدام البيئة حيث قمت بتمكين الكتابة المزدوجة.
3. من علامة التبويب **إنشاء**، قم بالتمرير لأسفل إلى القسم **بدء من القالب**، وحدد القالب المسمى **مدخل العميل**.
4. اتبع الإرشادات التي تظهر على الشاشة.

بعد اكتمال التزويد، يمكنك الوصول إلى مدخل العميل في قسم **تطبيقاتك** في **الصفحة الرئيسية**.

> [!NOTE]
> إذا لم يكن حل الكتابة المزدوجة مثبتًا في البيئة التي تعمل فيها، فستتلقى رسالة خطأ، ولن يتم تزويد مدخل العميل.

## <a name="update-the-customer-portal"></a>تحديث مدخل العميل

قد تُضاف وظائف إضافية إلى مدخل العميل لاحقًا. ستظهر تلقائيًا في بيئتك التغييرات التي تجريها Microsoft على مكون الحل الأساسية. ومع ذلك، فإن موقع الويب الذي تم تزويده في بيئتك لن يعكس التغييرات التي يتم إدخالها على بيانات التكوين. سيتعين عليك تطبيق هذه التغييرات يدويًا عن طريق الحصول على التعليمات البرمجية من القالب الجديد ودمجه مع موقع ويب الذي تم تزويده.

## <a name="additional-resources"></a>الموارد الإضافية

لمعرفة كيفية إعداد مدخل العميل وتخصيصه، يجب البدء بمراجعة الوثائق التالية للتقنيات الأساسية:

- [وثائق مداخل Power Apps](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [وثائق الكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

لإدارة المداخل بطريقة فعالة، يجب فهم مداخل Power Apps ودورة حياة Microsoft Dataverse. لمزيد من المعلومات، راجع الموارد التالية:

- [حول دورة حياة المدخل](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [ترقية مدخل](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [ترحيل تكوين المدخل](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [إدارة دورة حياة الحل: تطبيقات Dynamics 365 for Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]