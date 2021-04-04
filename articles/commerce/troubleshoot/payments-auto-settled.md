---
title: تسوية المدفوعات تلقائيا قبل فوترة الأوامر أو شحنها
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عند تسوية الدفع في مدخل Adyen مباشرة بعد تقديم أمر ما، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585177"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>تسوية المدفوعات تلقائيا قبل فوترة الأوامر أو شحنها

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عند تسوية الدفع في مدخل Adyen مباشرة بعد تقديم أمر ما، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.

## <a name="description"></a>الوصف

بعد تقديم أحد الأوامر، تتم تسوية الدفع مباشرة في مدخل Adyen مباشرة، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.

## <a name="resolution"></a>الدقة

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>تكوين الالتقاط اليدوي لمدفوعات التجارة الإلكترونية في مدخل Adyen

لتكوين الالتقاط اليدوي لمدفوعات التجارة الإلكترونية في مدخل Adyen، اتبع الخطوات التالية.

1. سجل الدخول إلى مدخل Adyen.
1. في الركن الأيمن العلوي، حدد حساب التاجر الخاص بك لقناة التجارة الإلكترونية.
1. في جزء التنقل العلوي، حدد **الحساب**، ثم حدد **الإعدادات**.
1. في حقل **تأخير الالتقاط**، حدد **يدوي**.

    ![إعداد تأخير الالتقاط في مدخل Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>الموارد الإضافية

[التقاط مدفوعات Adyen](https://docs.adyen.com/point-of-sale/capturing-payments)

[موصل دفع Dynamics 365 لـ Adyen](../dev-itpro/adyen-connector.md)

[إعداد موصل دفع Adyen لـ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
