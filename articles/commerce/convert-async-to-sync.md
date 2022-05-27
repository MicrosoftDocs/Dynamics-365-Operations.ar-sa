---
title: تحويل عملاء غير متزامنين إلى عملاء متزامنين
description: يشرح هذا الموضوع كيفية تحويل العملاء غير المتزامنين إلى عملاء متزامنين في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691434"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>تحويل عملاء غير متزامنين إلى عملاء متزامنين

[!include [banner](includes/banner.md)]

يشرح هذا الموضوع كيفية تحويل العملاء غير المتزامنين إلى عملاء متزامنين في Microsoft Dynamics 365 Commerce.

لتحويل العملاء غير المتزامنين إلى عملاء متزامنين، اتبع هذه الخطوات.

1. في مركز Commerce الرئيسي، قم بتشغيل **وظيفة P** لإرسال العملاء غير المتزامنين إلى مركز Commerce الرئيسي.
1. قم بتشغيل وظيفة **مزامنة العملاء وشركاء الأعمال من وضع غير متزامن** لإنشاء معرفات حسابات العملاء. (تمت تسمية هذه الوظيفة سابقًا باسم **مزامنة العملاء وشركاء الاعمال من وضع غير متزامن**.)
1. قم بتشغيل الوظيفة **1010** لمزامنة معرفات حساب العملاء الجديدة إلى القنوات.

في حالة إشارة أحد الأوامر إلى عميل أو عنوان غير متزامن لم تتم مزامنته بعد إلى مركز Commerce الرئيسي، فستتم مزامنة العميل أو العنوان كجزء من وظيفة دفعة **أوامر المزامنة**. إذا كانت حركات الدفع نقدًا والاستلام فورًا‬‬‏‫ تشير إلى عميل أو عنوان غير متزامن، فستتم مزامنة العميل أو العنوان قبل ترحيل نهاية اليوم (EOD).

## <a name="additional-resources"></a>الموارد الإضافية

[إدارة العملاء في المتاجر](customer-mgmt-stores.md)

[وضع إنشاء عميل غير متزامن](async-customer-mode.md)

[سمات العميل](dev-itpro/customer-attributes.md)

[استبعاد البيانات دون اتصال](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
