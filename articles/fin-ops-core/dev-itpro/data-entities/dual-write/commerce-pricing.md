---
title: استخدام محرك التسعير لـ Dynamics 365 Commerce مع Dynamics 365 Sales
description: يصف هذا الموضوع كيفية استخدام محرك التسعير في Microsoft Dynamics 365 Commerce لإنشاء عروض أسعار المبيعات في Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 364cc5adf0358ffa952750149ad31d62cbd35e87
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751424"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>استخدام محرك التسعير لـ Dynamics 365 Commerce مع Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع كيفية استخدام محرك التسعير في Microsoft Dynamics 365 Commerce لإنشاء عروض أسعار المبيعات في Dynamics 365 Sales.

يدعم محرك التسعير في Dynamics 365 Commerce معظم سيناريوهات التسعير من الشركات إلى المستهلك (B2C)، مثل التسعير على مستوى المتجر، والتسعير المستند إلى الانتماء والقائم على الولاء، وخصومات المزيج والمطابقة، وخصومات الكمية، وخصومات الحد الأدنى. يستخدم محرك التسعير قواعد معقدة لتحديد أفضل سعر لعرض أسعار أو أمر معين.

عند استخدام [الكتابة الثنائية](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)، تتوفر لديك ثلاثه خيارات لاحتياجات التسعير الخاصة بك. يمكنك استخدام التسعير الثابت الذي يأتي من قائمة الأسعار في Dynamics 365 Sales أو محرك التسعير في Dynamics 365 Supply Chain Management أو محرك التسعير في Dynamics 365 Commerce. من بين هذه الخيارات، يعد محرك التسعير التجاري الأنسب لسيناريوهات العمل إلى المستهلك.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>استخدام محرك التسعير التجاري في Sales

> [!NOTE]
> حاليًا، يمكن استخدام محرك التسعير التجاري فقط لإنشاء عروض الأسعار في Sales. تكامل أمر المبيعات مع محرك التسعير التجاري غير متاح بعد.

عندما يبدأ المستخدمون عرض أسعار في Sales، ينسخ إطار عمل الكتابة المزدوجة تفاصيل عرض الأسعار إلى Commerce. يتم نسخ أي تغييرات على بنود عروض الأسعار الحالية أو أي بنود عروض أسعار مضافة حديثًا في Sales إلى Commerce. عندما يرغب المستخدمون في استخدام محرك التسعير التجاري لتسعير عرض الأسعار، يمكنهم تحديد **عرض أسعار السعر** لتحديث أسعار عرض الأسعار، بناءً على محرك التسعير التجاري. يتم تحديث الأسعار تلقائيًا في كل من Sales وCommerce.

## <a name="prerequisites"></a>المتطلبات الأساسية

- قبل أن تتمكن من استخدام محرك تسعير Commerce في Sales، يجب عليك اتباع الخطوات الواردة في [العميل المتوقع إلى النقدية في الكتابة المزدوجة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).
- يجب عليك إيقاف تشغيل تقييم الاتفاقية التجارية للإدخال اليدوي باتباع الخطوات التالية:

    1. في بيئة Commerce، انتقل إلى **الحسابات المدينة\> إعداد \>معلمات الحسابات المدينة**.
    1. في علامة التبويب **الأسعار**، في علامة التبويب السريع **سياسات تقييم الاتفاقية التجارية**، قم بإلغاء تحديد خانة الاختيار **الإدخال اليدوي**.

## <a name="additional-resources"></a>الموارد الإضافية

[العميل المتوقع إلى النقدية في الكتابة المزدوجة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]