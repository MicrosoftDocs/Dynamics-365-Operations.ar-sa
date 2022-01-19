---
title: نصائح رؤية المخزون
description: يوفر هذا الموضوع تلميحات قليله يجب وضعها في الاعتبار عند اعداد الوظيفة الاضافيه لرؤية المخزون واستخدامها.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1f6ade36ac184a3c8bf790fc0d899ea01d90c8d2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952405"
---
# <a name="inventory-visibility-tips"></a>نصائح رؤية المخزون

[!include [banner](../includes/banner.md)]

فيما يلي بعض النصائح التي يجب مراعاتها عند إعداد الوظيفة الإضافية رؤية المخزون واستخدامها:

- في الوقت الحالي، لا تدعم الوظيفة الاضافيه لرؤية المخزون إلا بيئات Microsoft Dataverse التي تم إنشاؤها باستخدام Microsoft Dynamics Lifecycle Services (LCS). إذا تم إنشاء بيئة Dataverse الخاصة بك بطريقة أخرى (على سبيل المثال، باستخدام مركز إدارة Power Apps)، وإذا كانت مرتبطة ببيئة Dynamics 365 Supply Chain Management الخاصة بك، فيجب عليك أولاً الاتصال بالمخزون رؤية فريق المنتج لإصلاح مشكلة التعيين. يمكنك الاتصال بالفريق على [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). سيخبرك الفريق عندما تكون بيئتك جاهزة لك لتثبيت رؤية المخزون.
- إذا كان لديك أكثر من بيئة LCS، فقم بإنشاء تطبيق Azure Active Directory (Azure AD) مختلف لكل بيئة. في حالة استخدام نفس معرف التطبيق ومعرف المستاجر لتثبيت الوظيفة الإضافية لرؤية المخزون لبيئات مختلفة، ستحدث مشكلة في الرمز المميز للبيئات الأقدم. سيكون المثيل الأخير فقط للوظيفة الاضافيه لرؤية المخزون التي تم تثبيتها صالحا.
- لا يتم دعم رؤية المخزون حاليا للبيئات المستضافة في السحابة. إنه مدعوم فقط لبيئات المستوى 2+.
- تدعم واجهه برمجه التطبيقات (API) حاليا الاستعلام حتى 100 صنفا فرديا حسب قيمة `ProductID`. يمكن أيضًا تحديد قيم `SiteID` و`LocationID` المتعددة في كل استعلام. ويتم تحديد الحد الأقصى على أنه `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- يمكن لواجهة برمجة التطبيقات المجمعة إرجاع 512 سجلاً كحد أقصى لكل طلب.
- مصدر بيانات `fno` محجوز لـ Supply Chain Management. إذا كانت الوظيفة الاضافيه لرؤية المخزون متكاملة مع بيئة Supply Chain Management، فاننا نوصي بعدم حذف التكوينات المرتبطة بـ `fno` في [مصدر البيانات](inventory-visibility-configuration.md#data-source-configuration).
- لا يمكن لرؤية المخزون تغيير أية بيانات لمصدر البيانات `fno`. يكون تدفق البيانات باتجاه واحد، مما يعني أنه يجب الحصول على كافة تغييرات الكمية لمصدر البيانات `fno` من بيئة Supply Chain Management. لذلك، لا يمكنك استخدام واجهة برمجة التطبيقات (API) لإرسال التغيير المتاح أو طلبات الحجز الخاصة بمصدر البيانات `fno`.
- إذا قمت بإضافة قياس أو أكثر من القياسات الجديدة إلى بيئة Supply Chain Management، فيجب أيضًا إضافتها في رؤية المخزون. ومع ذلك، يجب أن تأتي كافة تغييرات الكمية للمقاييس الجديدة من بيئة Supply Chain Management.
- يتكون [تكوين القسم](inventory-visibility-configuration.md#partition-configuration) حاليًا من بعدين أساسيين (`SiteId` و`LocationId`) اللذين يشيران إلى كيفية توزيع البيانات. يمكن للعمليات التي تتم تحت نفس القسم تقديم أداء أعلى بتكلفة أقل. يتضمن الحل تكوين هذا القسم بشكل افتراضي. لذلك، *لا يتعين عليك تحديده بنفسك*. لا تقم بتخصيص تكوين القسم الافتراضي. إذا قمت بحذفه أو تغييره، فمن المحتمل ان تتسبب في حدوث خطا غير متوقع.
- يجب عدم تعريف الأبعاد الأساسية التي تم تعريفها في تكوين القسم في [تكوين التدرج الهرمي لفهرس المنتجات](inventory-visibility-configuration.md#index-configuration).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
