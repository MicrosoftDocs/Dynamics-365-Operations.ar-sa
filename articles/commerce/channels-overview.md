---
title: نظرة عامة على القنوات
description: يقدم هذا الموضوع نظرة عامة على القنوات في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409852"
---
# <a name="channels-overview"></a>نظرة عامة على القنوات


[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على القنوات في Microsoft Dynamics 365 Commerce. وهو يتضمن معلومات حول المهام التي يجب إتمامها قبل وبعد إعداد كل قناة.

## <a name="types-of-channels"></a>أنواع القنوات

يدعم Dynamics 365 Commerce ثلاثة أنواع مختلفة من القنوات: البيع بالتجزئة ومركز الاتصال والقنوات عبر الإنترنت.

### <a name="retail-channels"></a>قنوات البيع بالتجزئة

تمثل قنوات البيع بالتجزئة المتاجر القياسية التقليدية. بإمكان كل متجر أن يتضمن سجلات نقاط بيع (POS) بالإضافة إلى حسابات إيرادات ومصروفات خاصة به بالإضافة إلى فريق عمل خاص به أيضًا. 

### <a name="call-center-channels"></a>قنوات مراكز الاتصال

تمثل قنوات مراكز الاتصال أوامر مراكز الاتصال وإدارة العملاء.

### <a name="online-channels"></a>قنوات على الإنترنت

تمثل القنوات عبر الإنترنت متاجر التجارة الإلكترونية عبر الإنترنت. عن إنشاء قناة عبر الإنترنت، يجب إنشاء موقع باستخدام أداة منشئ الموقع من Microsoft Dynamics 365 Commerce أو حل تجارة إلكترونية خارجي آخر.

## <a name="channel-setup-basics"></a>أساسيات إعداد القناة

يتم تنفيذ إعداد القناة في أداة Commerce. تتوفر لدى كل قناة طرق دفع ومجموعات أسعار وتدرجات هرمية للمنتجات ومجموعات متنوعة ومجموعات من المنتجات خاصة بها. وبعد إنشاء قناة، يمكنك تعيين المنتجات التي ترغب أن تتضمنها هذه القناة وتبيعها. تتوفر مجموعة فريدة من الميزات التي تحتاج إلى تكوينها لكل نوع قناة. على سبيل المثال، تحتاج قناة بيع بالتجزئة إلى موظفين وسجلات وعملاء معينين لها. بعد إنشاء قناة جديدة، يجب تعيينها إلى تدرج هرمي للمؤسسات.

## <a name="channel-setup-prerequisites"></a>المتطلبات الأساسية‬ لإعداد قناة

قبل إعداد قناة، يجب عليك إكمال بعض المهام المطلوبة استنادًا إلى نوع القناة. لمزيد من المعلومات، راجع [المتطلبات الأساسية‬ لإعداد قناة‬](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>إعداد قناة

بعد إكمال المهام المطلوبة، استخدم الارتباطات التالية للحصل على مزيد من إرشادات الإعداد:

- [إعداد قناة بيع بالتجزئة](channel-setup-retail.md)
- [إعداد قناة مركز اتصال](channel-setup-callcenter.md)
- [إعداد قناة عبر الإنترنت](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>الموارد الإضافية

[المتطلبات الأساسية‬ لإعداد قناة](channels-prerequisites.md)

[إعداد قناة بيع بالتجزئة](channel-setup-retail.md)
    
[إعداد قناة عبر الإنترنت](channel-setup-online.md)

[إعداد قناة مركز اتصال](channel-setup-callcenter.md)

[إعداد التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]