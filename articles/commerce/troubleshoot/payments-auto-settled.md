---
title: تسوية المدفوعات تلقائيا قبل فوترة الأوامر أو شحنها
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عند تسوية الدفع في مدخل Adyen مباشرة بعد تقديم أمر ما، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282697"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>تسوية المدفوعات تلقائيا قبل فوترة الأوامر أو شحنها

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد عند تسوية الدفع في مدخل Adyen مباشرة بعد تقديم أمر ما، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.

## <a name="description"></a>الوصف

بعد تقديم أحد الأوامر، تتم تسوية الدفع مباشرة في مدخل Adyen مباشرة، حتى وإن لم يكن قد تمت فوترة أمر المبيعات أو شحنه.

## <a name="resolution"></a>الدقة

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>تكوين الالتقاط اليدوي لمدفوعات التجارة الإلكترونية في مدخل Adyen

لتكوين الالتقاط اليدوي لمدفوعات التجارة الإلكترونية في مدخل Adyen، اتبع الخطوات التالية.

1. سجل الدخول إلى مدخل Adyen.
1. في الركن الأيمن العلوي، حدد حساب التاجر الخاص بك لقناة التجارة الإلكترونية.
1. في جزء التنقل العلوي، حدد **الحساب**، ثم حدد **الإعدادات**.
1. في حقل **تأخير الالتقاط**، حدد **يدوي**.

    ![إعداد تأخير الالتقاط في مدخل Adyen.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>الموارد الإضافية

[التقاط مدفوعات Adyen](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector لـ Adyen](../dev-itpro/adyen-connector.md)

[إعداد موصل دفع Adyen لـ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
