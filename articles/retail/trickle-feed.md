---
title: إنشاء أوامر تستند إلى التغذية المستمرة لحركات متجر البيع بالتجزئة
description: يصف هذا الموضوع إنشاء أوامر تستند إلى التغذية المستمرة لحركات متجر البيع بالتجزئة في Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80233a73dbffc7380503cf03703758b187824c2a
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622656"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>إنشاء أوامر تستند إلى التغذية المستمرة لحركات متاجر البيع بالتجزئة (معاينة عامة)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

في الإصدار 10.0.4 من Dynamics 365 Retail والإصدارات السابقة، يعتبر ترحيل كشوف حسابات البيع بالتجزئة عمليه نهاية اليوم ويتم ترحيل جميع الحركات في الدفاتر في نهاية اليوم. عندئذٍ، يجب معالجة الحركات الكبيرة في غضون فاصل زمني محدد، مما يؤدي في بعض الأحيان إلى نشوء حالات فشل في ترحيل حمل العمل والتأمين وكشوف الحسابات. ويتعذر أيضًا على بائعي التجزئة التعرف على الإيرادات والمدفوعات في دفاترهم خلال اليوم.

مع المعاينة العامة لوظيفة إنشاء أوامر تستند إلى التغذية المستمرة التي تم تقديمها في الإصدار 10.0.5 من Retail، تتم معالجة الحركات خلال اليوم، في حين تتم معالجة التسوية المالية لطرق الدفع والحركات الأخرى لإدارة النقدية في نهاية اليوم. تقوم هذه الوظيفة بتقسيم حمل عمل إنشاء أوامر المبيعات والفواتير والمدفوعات خلال اليوم، مما يوفر أداء أفضل والقدرة على التعرف على الإيرادات والمدفوعات في الدفاتر في وقت قريب من الحقيقي‬. 


## <a name="how-to-use-trickle-feed-based-posting"></a>كيفية استخدام الترحيل الذي يستند إلى التغذية المستمرة
  
1. لتمكين الترحيل الذي يستند إلى التغذية المستمرة‬ لحركات البيع بالتجزئة، انتقل إلى **إدارة النظام > الإعداد > تكوين الترخيص** وعطّل المفتاح **كشوف البيع بالتجزئة‬**.

2. على الصفحة نفسها، قم بتمكين مفتاح ترخيص **كشوف البيع بالتجزئة (تغذية مستمرة) – معاينة**. عند تمكين هذا المفتاح، تأكد من عدم وجود كشوف حسابات معلّقة تنتظر ترحيلها. 

> [!Important]
> قبل تمكين **كشوف البيع بالتجزئة (تغذية مستمرة) – معاينة**، تأكد من عدم وجود كشوف حسابات معلّقة تنتظر ترحيلها.

3. سيتم تقسيم مستند كشف الحساب الحالي إلى نوعين مختلفين: كشف الحركات والقائمة المالية.

      - سيقوم كشف الحركات بانتقاء جميع حركات البيع بالتجزئة غير المرحّلة والتي تم التحقق من صحتها، وينشئ دفاتر يومية لأوامر المبيعات وفواتير المبيعات والمدفوعات والخصومات، وحركات الإيرادات والمصروفات وفق الوتيرة التي تريد تكوينها. يجب تكوين هذه العملية كي تعمل وفق تكرار عالٍ بحيث يتم إنشاء المستندات عند تحميل حركات البيع بالتجزئة إلى Retail Headquarters عبر وظيفة P. مع كشف الحركات الذي ينشئ أوامر المبيعات وفواتير المبيعات، لا حاجة حقيقية لتكوين الوظيفة الدُفعية **ترحيل المخزون**. ومع ذلك، يمكنك مع ذلك استخدامه لتلبية احتياجات عمل معينة قد تكون لديك.  
      
     - تم تصميم القائمة المالية بحيث يتم إنشاؤها في نهاية اليوم وهي تدعم فقط أسلوب الإقفال **وردية**. سوف تقتصر هذه القائمة على التسوية المالية وستنشئ فقط دفاتر اليومية لمبالغ الفروقات بين المبلغ المحسوب ومبلغ الحركة لمختلف طريق الدفع، بالإضافة إلى دفاتر اليومية لحركات إدارة النقدية الأخرى.   

4. لحساب كشف الحركات، انقر فوق **البيع بالتجزئة > تكنولوجيا معلومات البيع بالتجزئة‬ > ترحيل نقطة البيع > حساب كشوف الحركات على دُفعات**. لترحيل كشف الحركات على دُفعات، انقر فوق **البيع بالتجزئة > تكنولوجيا معلومات البيع بالتجزئة‬ > ترحيل نقطة البيع > ترحيل كشوف الحركات على دُفعات**.

5. لحساب القائمة المالية، انقر فوق **البيع بالتجزئة > تكنولوجيا معلومات البيع بالتجزئة‬ > ترحيل نقطة البيع > حساب القوائم المالية على دُفعات**. لترحيل القوائم المالية على دُفعات، انقر فوق **البيع بالتجزئة > تكنولوجيا معلومات البيع بالتجزئة‬ > ترحيل نقطة البيع > ترحيل القوائم المالية على دُفعات**.

> [!NOTE]
> تمت إزالة عناصر القائمة **البيع بالتجزئة > تكنولوجيا معلومات البيع بالتجزئة > ترحيل نقطة البيع > حساب الكشوف على دُفعات‬** و**البيع بالتجزئة > تكنولوجيا معلومات البيع بالتجزئة > ترحيل نقطة البيع > ترحيل الكشوف على دُفعات‬** مع هذه الميزة.

كطريقة بديلة، يمكن إنشاء أنواع كشوف الحسابات والقوائم المالية يدويًا. انتقل إلى **البيع بالتجزئة > القنوات > متاجر‏‎ البيع بالتجزئة** وانقر فوق **كشوف البيع بالتجزئة‬**. انقر فوق **جديد**، ثم اختر نوع الكشف الذي ترغب في إنشائه. ستعرض الحقول في صفحة **كشوف البيع بالتجزئة‬** والإجراءات تحت **مجموعة كشوف الحسابات** في الصفحة البيانات والإجراءات ذات الصلة استنادًا إلى نوع الكشف المحدد.