---
title: المتطلبات الأساسية‬ لإعداد قناة
description: يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002279"
---
# <a name="channel-setup-prerequisites"></a>المتطلبات الأساسية‬ لإعداد قناة


[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على المتطلبات الأساسية لإعداد القناة في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

قبل أن تتمكن من إنشاء قناة Dynamics 365 Commerce، يجب إكمال العديد من المهام الأساسية. يتم تنظيم القوائم التالية للمهام الأساسية حسب نوع القناة.

> [!NOTE]
> لا تزال بعض الوثائق قيد الكتابة، وسيتم تحديث الارتباطات عند نشر محتوى جديد.

## <a name="initialization"></a>بدء

- [تهيئة البيانات الأولية](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>المتطلبات الأساسية العمومية لكل أنواع القنوات

- [تعريف بنية الكيان القانوني وتكوينها](channels-legal-entities.md) 
- [تكوين التدرج الهرمي للمؤسسات](channels-org-hierarchies.md)
- [إعداد مستودع](channels-setup-warehouse.md)
- [تكوين ضريبة المبيعات](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [إعداد ملف تعريف إخطار البريد الإلكتروني](email-notification-profiles.md)
- [إعداد التسلسلات الرقمية](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [إعداد عميل ودفتر عناوين افتراضيين](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>المتطلبات الأساسية‬ لقناة البيع بالتجزئة

- [أكواد المعلومات ومجموعات أكواد المعلومات](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [إعداد ملف تعريف وظائف البيع بالتجزئة](retail-functionality-profile.md)
- [إعداد دفتر عناوين للموظفين](new-address-book.md)
- [إعداد تخطيط الشاشة](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [إعداد محطة أجهزة](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>المتطلبات الأساسية لقناة مركز الاتصال

- محددات مركز الاتصال
- طرق استرداد مبالغ مراكز الاتصال
- أنواع الإيجار
- خدمات الدفع
- أكواد تعليق الأمر

## <a name="online-channel-prerequisites"></a>المتطلبات الأساسية‬ لقناة عبر الإنترنت

- [إنشاء ملف تعريف الوظائف عبر الإنترنت](online-functionality-profile.md)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على القنوات](channels-overview.md)

[نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[إعداد التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md)

[إنشاء كيانات قانونية](channels-legal-entities.md)

[إعداد قناة بيع بالتجزئة](channel-setup-retail.md)
    
[إعداد قناة عبر الإنترنت](channel-setup-online.md)
