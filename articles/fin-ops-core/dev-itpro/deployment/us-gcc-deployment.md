---
title: Dynamics 365 Finance وSupply Chain Management وCommerce في سحابة القطاع الحكومي (GCC) الأمريكي
description: توضح هذه المقالة معلومات عن منتجات حكومة الولايات المتحدة في 365 Microsoft Dynamics التي يتم توفيرها للحكومة المؤهلة والكيانات الخاصة.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 41789d574cc7348dbf8a18db97da9c428da09602
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103927"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance وSupply Chain Management وCommerce في سحابة القطاع الحكومي (GCC) الأمريكي

[!include [banner](../includes/banner.md)]



حدد منتجات Microsoft Dynamics 365 United States (US) Government المتوفرة للكيانات الحكومية والخاصة المؤهلة. وتقتصر هذه الكيانات على الأنواع التالية:

- الكيانات الحكومية الفيدرالية الأمريكية وفي الولاية والمحلية والإقليمية
- الكيانات الخاصة التي تستخدم Dynamics 365 US Government لتوفير حلول للكيانات الحكومية أو للأعضاء المؤهلين في مجتمع السحابة
- إن الكيانات الخاصة التي لها بيانات عميل تخضع لقوانين الحكومية وDynamics 365 US Government العامة هي الخدمة المناسبة لتفي بالمتطلبات التنظيمية

لمزيد من المعلومات، راجع [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>‏‫الإعداد

لإكمال عملية الإلحاق الأولي لمشروع التنفيذ في Microsoft Dynamics Lifecycle Services (LCS)، اتبع التعليمات في [‏‫إعداد مشروع تنفيذ](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). ومع ذلك، لا تستخدم الارتباط لـ LCS العامة المتوفرة في تلك الإرشادات. بدلاً من ذلك، استخدم عنوان URL التالي لفتح LCS لـ سحابة القطاع الحكومي (GCC): <https://gov.lcs.microsoftdynamics.us>.

بعد اكتمال الإلحاق الأولي، اتبع الإرشادات الموجودة في [إلحاق المشروع](../lifecycle-services/project-onboarding.md). ومرة أخرى، استخدم [LCS لـ GCC](https://gov.lcs.microsoftdynamics.us) بدلاً من LCS العامة.

## <a name="environment-deployment"></a>توزيع البيئة

بعد إكمال عملية إعداد المشروع، يمكنك مراجعة القدرات الإضافية لـ LCS الموضحة في [Lifecycle Services (LCS) لعملاء تطبيقات التمويل والعمليات](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). ثم انتقل إلى توزيع البيئة.

- لتوزيع البيئات المدارة من قبل Microsoft بواسطة LCS، اتبع الإرشادات الموجودة في [Lifecycle Services (LCS) لعملاء تطبيقات التمويل والعمليات](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- للبيئات التي تستضيفها السحابة، راجع [نشر بيئات تطوير التوزيع والوصول](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). كما يجب إكمال عملية إلحاق Resource Manager للموصلات، كما تم وصفها في [إكمال عملية إلحاق في Azure Resource Manager لمشاريع Lifecycle Services الحكومية الأمريكية](arm-onbarding-us-goverment.md).

> [!NOTE]
> بالنسبة لمشاريع LCS الحكومية، يتم دعم الاشتراكات في Azure الخاصة بالحكومة من Azure فقط.

## <a name="features-that-arent-available"></a>الميزات غير المتوفرة

لن تتوفر بعض الميزات للتوزيع في GCC، أو لن تكون متوفرة للاستخدام مع Dynamics 365 في GCC. على سبيل المثال، لن تتوفر خدمات Azure DevOps في GCC. ومع ذلك، يمكن استخدام خدمات Azure DevOps المحلية أو خدمات Azure DevOps العامة. للحصول على معلومات مفصلة حول إتاحة الميزات، راجع [إتاحة ميزة الحكومة الأمريكية الخاصة بتطبيقات الأعمال](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>هل Dynamics 365 Finance وDynamics 365 Supply Chain Management مدعومان في GCC-High؟

الرقم Dynamics 365 Finance وDynamics 365 Supply Chain Management مدعومان فقط في GCC؟

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>هل يمكنني استخدام Azure DevOps مع Finance وSupply Chain Management في GCC؟

نعم، يمكنك استخدام خدمات Azure DevOps العامة إذا لم يكن لديك متطلبات لحل معتمد Federal Risk and Authorization Management Program (FEDRAMP). وبدلاً من ذلك، يمكنك استخدام خادم Azure DevOps.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>هل يمكنني توزيع بيئة تطوير من الطبقة 1 الخاصة بالبيئة المستضافة في السحابة على اشتراك Azure commercial؟

الرقم في [LCS لـ GCC](https://gov.lcs.microsoftdynamics.us)، فإنه يجب استخدام اشتراك Azure Government لتوزيع بيئة مستضافة في السحابة.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>ماذا يمكنني أن أفعل إذا كنت في حاجة إلى حزمة من مكتبة الأصول المشتركة، ولكنها غير متوفرة في LCS لـ GCC؟

يمكنك تنزيل الحزمة من مكتبة الأصول المشتركة في [LCS العامة](https://lcs.dynamics.com). وبدلاً من ذلك، يمكن أن يساعدك شريكك في تنزيل الحزمة.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>هل أداة ترقية الكود متوفرة في GCC؟

لا، أداة ترقية الكود غير متوفرة حاليًا في GCC. ومع ذلك، يمكنك إنشاء مشروع عميل متوقع في [LCS عامة](https://lcs.dynamics.com) واستخدام أداة ترقية الأكواد. لاحظ أنه لن تتمكن من توزيع البيئات في مشاريع العملاء المتوقعين.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>هل يمكن للشريك فتح بطاقة تذكرة نيابة عني؟

نعم. ومع ذلك، إذا كان شريكك يستخدم هوية ليست GCC، فإنه سيتم توجيه تذكرة الدعم إلى قائمة انتظار الدعم العام. نُوصي باستخدام استحقاق GCC الخاص بالعميل في LCS لفتح تذاكر الدعم.

## <a name="see-also"></a>راجع أيضًا

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [إتاحة ميزة الحكومة الأمريكية الخاصة بتطبيقات الأعمال](https://aka.ms/BAPFunctionalParity).
- [دليل مستخدم Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [نظرة عامة حول النشر عبر السحابة](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

