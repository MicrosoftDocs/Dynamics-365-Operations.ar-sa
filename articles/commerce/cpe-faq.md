---
title: الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce
description: يوفر هذا الموضوع إجابات للأسئلة الشائعة حول بيئة تقييم Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343548"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>الأسئلة المتداولة حول بيئة تقييم Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوفر هذا الموضوع إجابات للأسئلة الشائعة حول بيئة تقييم Microsoft Dynamics 365 Commerce.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>هل يمكن استخدام بيئة تقييم Commerce كواجهة للتجارة الإلكترونية للعملاء الذين يتولون حاليًا مسؤولية تنفيذ البيع بالتجزئة؟

الرقم بيئة تقييم Commerce هي بيئة مخصصة للتقييم فقط. إذا كنت تحتاج إلى بيئة للعميل الذي يقوم بتنفيذ البيع بالتجزئة، اتصل بـ Microsoft.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>هل يمكن استخدام بيئة تقييم التجارة لتوفير ميزات التجارة الإلكترونية على رأس تطبيق/بيئة حالية تنفذ البيع بالتجزئة؟

لا (غالبًا). لا تتوفر مكونات تقييم التجارة إلا للبيئات التي تطابق التكوينات المحددة في دليل التوفير والمتطلبات الأساسية. وبالإضافة إلى ذلك، لن تتوفر بيانات العرض التوضيحي الأساسي المطلوبة في البيئات التي تم نشرها بإصدار أولي أقدم من 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>ما التكاليف التي ينطوي عليها نشر بيئة تقييم Commerce في Microsoft Azure عبر Microsoft Dynamics Lifecycle Services (LCS)؟

ستتم استضافة بيئة Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce تقليدية للعرض التوضيحي للمقرات الرئيسية (جهاز ظاهري \[VM\]) في اشتراكك في Azure. يمكنك استخدام [حاسبة تسعير Azure](https://azure.microsoft.com/pricing/calculator/) لتقدير هذه التكلفة.

ستتوفر المكونات الأخرى مثل Commerce Scale Unit ومنشئ مواقع Commerce وموقع التجارة الإلكترونية كخدمة تأجير البرامج (SaaS) وستتم استضافتها بواسطة Microsoft.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>ما مناطق Azure الجغرافية المدعومة حاليًا لبيئة تقييم Commerce؟

لا يمكن نشر بيئة تقييم Commerce إلا في جغرافيا أمريكا الشمالية.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>هل يوجد قرص ثابت ظاهري قابل للتنزيل (VHD) به خيار جهاز ظاهري (جهاز ظاهري) OneBox كامل؟

تعتبر Dynamics 365 Commerce وCommerce Scale Unit بمثابة خدمة تأجير البرامج‬ (SaaS) ويجب استضافتها على السحابة.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>ما طول مدة استخدام بيئة تقييم Commerce؟

تنطوي بيئة تقييم Commerce على حد زمني لمدة 30 يومًا من تاريخ توفير مكونات خدمة تأجير البرامج مثل Commerce Scale Unit ومنشئ مواقع Commerce وموقع التجارة الإلكترونية.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>هل يمكنني تمديد الحد الزمني لبيئة تقييم Commerce لدي؟

يعد تمديد الحد الزمني استثناءًا للقاعدة ويتم اعتباره لكل حالة على حدة. ينبغي الاتصال بجهة اتصال شريك Microsoft للمساعدة.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على بيئة تقييم Dynamics 365 Commerce](cpe-overview.md)

[توفير بيئة تقييم Dynamics 365 Commerce](provisioning-guide.md)

[تكوين بيئة تقييم Dynamics 365 Commerce](cpe-post-provisioning.md)

[تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce](cpe-bopis.md)

[تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
