---
title: المتطلبات الأساسية‬ لإعداد قناة
description: يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800509"
---
# <a name="channel-setup-prerequisites"></a>المتطلبات الأساسية لإعداد القناة

[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.

قبل أن تتمكن من إنشاء قناة Dynamics 365 Commerce، يجب إكمال العديد من المهام الأساسية. يتم تنظيم القوائم التالية للمهام الأساسية حسب نوع القناة.

> [!NOTE]
> لا تزال بعض الوثائق قيد الكتابة، وسيتم تحديث الارتباطات عند نشر محتوى جديد.

## <a name="initialization"></a>بدء

- [تهيئة البيانات الأولية](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>المتطلبات الأساسية العمومية لكل أنواع القنوات

- [تعريف بنية الكيان القانوني وتكوينها](channels-legal-entities.md) 
- [تكوين التدرج الهرمي للمؤسسات](channels-org-hierarchies.md)
- [إعداد مستودع](channels-setup-warehouse.md)
- [تكوين ضريبة المبيعات](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [إعداد ملف تعريف إخطار البريد الإلكتروني](email-notification-profiles.md)
- [إعداد التسلسلات الرقمية](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [إعداد عميل ودفتر عناوين افتراضيين](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>المتطلبات الأساسية‬ لقناة البيع بالتجزئة

- [أكواد المعلومات ومجموعات أكواد المعلومات](info-codes-retail.md)
- [إعداد ملف تعريف وظائف البيع بالتجزئة](retail-functionality-profile.md)
- [إعداد دفتر عناوين للموظفين](new-address-book.md)
- [إعداد تخطيط الشاشة](pos-screen-layouts.md)
- [إعداد محطة أجهزة](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>المتطلبات الأساسية لقناة مركز الاتصال

- محددات مركز الاتصال
- [طريقة أمر مركز الاتصال ودفع المبلغ المسترد](work-with-payments.md)
- [أوضاع تسليم مركز الاتصال والمصاريف](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>المتطلبات الأساسية لقناة على الإنترنت

- [إنشاء ملف تعريف وظائف على الإنترنت](online-functionality-profile.md)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على القنوات](channels-overview.md)

[نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[إعداد التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md)

[إنشاء كيانات قانونية](channels-legal-entities.md)

[إعداد قناة بيع بالتجزئة](channel-setup-retail.md)
    
[إعداد قناة عبر الإنترنت](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
