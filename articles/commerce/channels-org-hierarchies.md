---
title: إعداد التدرجات الهرمية للمؤسسات
description: يصف هذا الموضوع كيفية إعداد التدرجات الهرمية للمؤسسات في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 490d466c10cfe0640f8fbcf8fe2298536e499d9b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477962"
---
# <a name="set-up-organization-hierarchies"></a>إعداد التدرجات الهرمية للمؤسسات

[!include [banner](includes/banner.md)]

يصف هذا الموضوع كيفية إعداد التدرجات الهرمية للمؤسسات في Microsoft Dynamics 365 Commerce.

قبل إنشاء القنوات، يجب أن تتأكد من إعداد التدرجات الهرمية لمؤسستك.

يمكنك استخدام التدرجات الهرمية المؤسسية لعرض عملك وإنشاء تقارير متعلقة به من منظورات متعددة. على سبيل المثال، يمكنك إعداد تدرج هرمي للتقارير الضريبية أو القانونية. ثم يمكنك إعداد تدرج هرمي آخر لإنشاء تقارير خاصة بالمعلومات المالية غير المطلوبة قانونيًا، ولكنها مستخدمة من أجل الإنشاء الداخلي للتقارير.

قبل إنشاء تدرج هرمي للمؤسسات، يتعين عليك إنشاء مؤسسات. لمزيد من المعلومات، راجع [إنشاء كيانات قانونية](channels-legal-entities.md) أو [إنشاء وحدات تشغيل](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


لمزيد من المعلومات، راجع الموضوعات التالية.
- [نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [تخطيط التدرج الهرمي للمؤسسات](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [إنشاء تدرج هرمي لمؤسسة](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>إنشاء تدرج هرمي مؤسسي

لإنشاء تدرج هرمي للمؤسسات، اتبع الخطوات التالية.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> التدرجات الهرمية للمؤسسات**.
1. في جزء الإجراءات، حدد **جديد**.
1. في حقل **الاسم**، أدخل قيمة.
1. في قسم **الغرض**، حدد **تعيين غرض‬**.
1. في القائمة، قم بالبحث عن السجل المطلوب وحدده. حدد غرضًا للتعيين إلى التدرج الهرمي للمؤسسات الخاصة بك.
1. في قسم **التدرجات الهرمية المعينة‬**، حدد **إضافة**.
1. في القائمة، قم بوضع علامة للصف المحدد. ابحث عن التدرج الهرمي الذي قمت بإنشائه.
1. حدد **موافق**.

تعرض الصورة التالية مثالاً لتدرد هرمي للمؤسسات تم إنشاؤها لمجموعة متاجر "Adventure Works".

![مثال لتدرج هرمي للمؤسسات](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>إضافة مؤسسات إلى تدرج هرمي

لإضافة مؤسسات إلى تدرج هرمي، اتبع هذه الخطوات.

1. في القائمة، قم بالبحث عن السجل المطلوب وحدده. قم بتحديد التدرج الهرمي.
1. في جزء الإجراءات، حدد **عرض**.
1. قم بإضافة المؤسسات، حسب الحاجة.
1. لإضافة مؤسسة، حدد **تحرير** ثم حدد **إدراج**. عند الانتهاء من إجراء التغييرات، يمكنك حفظ مسودة ونشر التغييرات.

تعرض الصورة التالية كيانًا قانونيًا تمت إضافته إلى جذر التدرج الهرمي مع أربع مراكز تكلفة مضافة لقنوات "مركز التسوق" و "المنفذ" و "عبر الإنترنت" و "مركز الاتصال". بعد ذلك، يمكن إضافة مركز اتصال وقنوات عبر الإنترنت لكل واحد منها.

![مثال لمصمم التدرج الهرمي](media/hierarchy-designer.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[تخطيط التدرج الهرمي للمؤسسات](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[إنشاء كيانات قانونية](channels-legal-entities.md)

[إنشاء وحدات تشغيل](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[نظرة عامة على القنوات](channels-overview.md)

[المتطلبات الأساسية‬ لإعداد قناة](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
