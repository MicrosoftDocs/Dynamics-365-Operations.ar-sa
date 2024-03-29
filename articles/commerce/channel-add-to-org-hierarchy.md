---
title: إضافة قناة إلى التدرج الهرمي للمؤسسة
description: يصف هذا المقال كيفية إضافة قناة إلى التدرج الهرمي لمؤسسة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278587"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>إضافة قناة إلى التدرج الهرمي للمؤسسة


[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية إضافة قناة إلى التدرج الهرمي لمؤسسة في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

يجب أن تقترن القنوات بتدرج هرمي أو أكثر للمؤسسة. قبل إنشاء القنوات، يجب أن تؤكد إعداد التدرجات الهرمية لمؤسستك.  

راجع [التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md) لمزيد من التفاصيل حول كيفيه إنشاء التدرجات الهرمية للمؤسسات.

## <a name="select-a-hierarchy"></a>تحديد تدرج هرمي

لتحديد تدرج هرمي، اتبع هذه الخطوات.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد القناة \> التدرجات الهرمية للمؤسسات**.
1. من القائمة، حدد التدرج الهرمي للمؤسسات الذي ستضيف القناة إليه.
1. في جزء الاجراءات، حدد **عرض** لعرض تفاصيل التدرج الهرمي.

تظهر الصورة التالية تفاصيل التدرج الهرمي للمؤسسات للتدرج الهرمي المحدد.

![تفاصيل التدرج الهرمي للمؤسسات للتدرج الهرمي المحدد.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>إضافة قناه إلى عقدة التدرج الهرمي

لإضافة قناه إلى عقدة التدرج الهرمي، اتبع هذه الخطوات.

1. في جزء الإجراءات، حدد **تحرير**.
1. حدد عقدة التدرج الهرمي التي ترغب في إضافة القناة اليها، ثم حدد **قناة البيع بالتجزئة** من القائمة المنسدلة **ادراج قناة**. 
1. حدد القناة التي تريد اضافتها، ثم حدد الزر **موافق**.
1. في جزء الإجراءات، حدد **حفظ**.
1. في جزء الإجراءات، حدد **نشر** وأدخل **تاريخ سريان** في الماضي كي يدخل هذا الاجراء حيز التنفيذ على الفور.

تظهر الصورة التالية كيفية تحديد قناة لإضافتها إلى عقدة التدرج الهرمي.

![تحديد قناة لإضافتها إلى عقدة التدرج الهرمي.](media/channel-add-to-org-hierarchy-2.png)

تظهر الصورة التالية تدرجًا هرميًا أضيفت إليه قنوات متنوعة.

![تدرج هرمي أضيفت إليه قنوات متعددة.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظره عامة حول القنوات](channels-overview.md)

[المتطلبات الأساسية لإعداد القناة](channels-prerequisites.md)

[نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[تخطيط التدرج الهرمي للمؤسسات](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md)

[إعداد قناة بيع بالتجزئة](channel-setup-retail.md)
    
[إعداد قناة عبر الإنترنت](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
