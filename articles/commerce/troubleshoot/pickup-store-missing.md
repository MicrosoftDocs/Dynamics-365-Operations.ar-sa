---
title: لا يظهر متجر البيع بالتجزئة في قائمة المتاجر المطلوب الانتهاء منها
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور متجر البيع بالتجزئة في قائمة المتاجر التي يمكن انتقاء الأصناف منها.
author: Reza-Assadi
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
ms.openlocfilehash: 9974b3e10bbdcd2e8a8723a3be4b70401bb9e546
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801593"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>لا يظهر متجر البيع بالتجزئة في قائمة المتاجر المطلوب الانتهاء منها

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور متجر البيع بالتجزئة في قائمة المتاجر التي يمكن انتقاء الأصناف منها.

## <a name="description"></a>الوصف

لا يظهر متجر البيع بالتجزئة في قائمة المتاجر التي يمكن انتقاء الأصناف منها.

## <a name="resolution"></a>الدقة

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>تكوين خط الطول وخط العرض لعنوان المتجر في المركز الرئيسي لـ Commerce

لتكوين خط الطول وخط العرض لعنوان المتجر في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> القنوات \> المتاجر \> جميع المتاجر**.
1. ابحث عن المتجر الذي ترغب في ظهوره بين خيارات الانتقاء في موقع التجارة الإلكترونية. قم بتدوين قيمة **رقم وحدة التشغيل** الخاصة به.
1. انتقل إلى **إدارة المؤسسة \> المؤسسات \> وحدات التشغيل**.
1. ابحث عن رقم وحدة التشغيل الذي قمت بالإشارة إليه سابقًا، ثم حدد وحدة التشغيل في نتائج البحث.
1. في علامة التبويب السريعة **العناوين**، حدد **المزيد من الخيارات**، ثم حدد **متقدم**.
1. في علامة التبويب السريعة **عام**، تأكد من أن حقلي **خط الطول** و **خط العرض** تعيينهما بشكل صحيح. كجزء من هذه الخطوة، تأكد من تحديد القيم بشكل صحيح كأرقام موجبة أو سالبة.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>تكوين مجموعات الاستيفاء في المركز الرئيسي لـ Commerce

لتكوين مجموعات الاستيفاء في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.
1. حدد المتجر على الإنترنت المراد تكوينه.
1. في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **تعيين مجموعة الاستيفاء**.
1. في صفحة **تعيين مجموعة الاستيفاء**، حدد مجموعة الاستيفاء الخاصة بالمتجر على الإنترنت.
1. تحت **الإعداد**، تأكد من تكوين مخزن البيع بالتجزئة بشكل صحيح لمجموعة الاستيفاء.

## <a name="additional-resources"></a>الموارد الإضافية 

[إنشاء وحدة تشغيل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[إعداد قناة على الإنترنت](../channel-setup-online.md)
