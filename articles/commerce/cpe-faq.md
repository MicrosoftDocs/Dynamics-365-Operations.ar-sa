---
title: الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce
description: يوفر هذا الموضوع إجابات للأسئلة الشائعة حول بيئة تقييم Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000965"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوفر هذا الموضوع إجابات للأسئلة الشائعة حول بيئة تقييم Microsoft Dynamics 365 Commerce.

**هل يمكن استخدام بيئة تقييم Commerce كواجهة للتجارة الإلكترونية للعملاء الذين يتولون حاليًا مسؤولية تنفيذ البيع بالتجزئة؟**

الرقم بيئة تقييم Commerce هي بيئة مخصصة للتقييم فقط. إذا كنت تحتاج إلى بيئة للعميل الذي يقوم بتنفيذ البيع بالتجزئة، اتصل بـ Microsoft.

**هل يمكن استخدام بيئة تقييم التجارة لتوفير ميزات التجارة الإلكترونية على رأس تطبيق/بيئة حالية تنفذ البيع بالتجزئة؟**

لا (غالبًا). لا تتوفر مكونات تقييم التجارة إلا للبيئات التي تطابق التكوينات المحددة في دليل التوفير والمتطلبات الأساسية. وبالإضافة إلى ذلك، لن تتوفر بيانات العرض التوضيحي الأساسي المطلوبة في البيئات التي تم نشرها بإصدار أولي أقدم من 10.0.8. 

**ما التكاليف التي ينطوي عليها نشر بيئة تقييم Commerce في Microsoft Azure عبر خدمات Microsoft Dynamics Lifecycle Services (LCS)؟**

ستتم استضافة بيئة Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce تقليدية للعرض التوضيحي للمقرات الرئيسية (جهاز ظاهري \[VM\]) في اشتراكك في Azure. يمكنك استخدام [حاسبة تسعير Azure](https://azure.microsoft.com/pricing/calculator/) لتقدير هذه التكلفة.

ستتوفر المكونات الأخرى مثل Commerce Scale Unit ومنشئ مواقع Commerce وموقع التجارة الإلكترونية كخدمة تأجير البرامج (SaaS) وستتم استضافتها بواسطة Microsoft.

**ما مناطق Azure الجغرافية المدعومة حاليًا لبيئة تقييم Commerce؟**

لا يمكن نشر بيئة تقييم Commerce إلا في جغرافيا أمريكا الشمالية.

**هل يوجد قرص ثابت ظاهري قابل للتنزيل (VHD) به خيار جهاز ظاهري (جهاز ظاهري) OneBox كامل؟**

تعتبر Dynamics 365 Commerce وCommerce Scale Unit بمثابة خدمة تأجير البرامج‬ (SaaS) ويجب استضافتها على السحابة.

**ما طول مدة استخدام بيئة تقييم Commerce؟**

تنطوي بيئة تقييم Commerce على حد زمني لمدة 30 يومًا من تاريخ توفير مكونات خدمة تأجير البرامج مثل Commerce Scale Unit ومنشئ مواقع Commerce وموقع التجارة الإلكترونية.

**هل يمكنني تمديد الحد الزمني لبيئة تقييم Commerce لدي؟**

يعد تمديد الحد الزمني استثناءًا للقاعدة ويتم اعتباره لكل حالة على حدة. ينبغي الاتصال بجهة اتصال شريك Microsoft للمساعدة.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على بيئة تقييم Dynamics 365 Commerce](cpe-overview.md)

[توفير بيئة تقييم Dynamics 365 Commerce](provisioning-guide.md)

[تكوين بيئة تقييم Dynamics 365 Commerce](cpe-post-provisioning.md)

[تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce](cpe-bopis.md)

[تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]