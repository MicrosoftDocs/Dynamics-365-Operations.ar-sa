---
title: تضمين وزن وحجم الحاوية على الحمولة
description: يصف هذا الموضوع كيفية إعداد وتطبيق وظيفة تضمين وزن وحجم الحاوية على الحمولات‬.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8fb40a0fe1606b856f58f5bc517c7f1aff85e4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977503"
---
# <a name="include-container-weight-and-volume-on-load"></a>تضمين وزن وحجم الحاوية على الحمولة

[!include [banner](../includes/banner.md)]

توفر وظيفة تضمين وزن وحجم الحاوية على الحمولة تمثيلًا واضحًا لإجمالي وزن وحجم الحاويات التي سيتم تحميلها.

تحتوي الحمولة على شحنة واحدة أو شحنات متعددة، وتحتوي هذه الشحنات على أصناف مميزة تنتمي إلى أمر مبيعات واحد أو أوامر مبيعات متعددة. يتم تخزين الأصناف داخل حاوية، ويتم تحميل الحاويات على حمولة. وباستطاعة الأصناف الموجودة خارج الحاوية أن تكون هي أيضًا جزءًا من الحمولة. استنادًا إلى هذه الشروط، يقوم النظام بحساب قيم الوزن والحجم على الحمولة من خلال أخذ حجم ووزن الحاويات والأصناف في الاعتبار.

إذا لم تكن القيم المحسوبة دقيقة، فيمكنك ضبطها عن طريق إدخال القيم الفعلية للوزن والحجم على الحمولة. يتم استخدام قيم الوزن والحجم في عمليات إدارة النقل. على سبيل المثال، يتم استخدام القيم الموجودة في لوحة عمل مسار الأسعار‬، حيث تساعد في تحديد سعر ومسار الحمولات، ويتم استخدامها أيضًا لطرق دفع النقل وتسجيل دخول السائق.

## <a name="where-it-applies"></a>أين يتم التطبيق

تنطبق وظيفة تضمين وزن وحجم الحاوية على حمولة في عمليات إدارة النقل، مثل لوحة عمل مسار الأسعار‬ وطرق دفع النقل وتسجيل دخول السائق.‬

## <a name="how-it-is-set-up"></a>كيف يتم إعدادها

يتم حساب عدد الحاويات التي يجب اخذها في الاعتبار لحمولة ما استنادًا إلى وزن وحجم الحاوية وإلى النسبة المئوية المستخدمة من الحاوية.

-   لتعيين الوزن والحجم لحاوية، انقر فوق **إدارة المستودعات** \> **الإعداد** \> **الحاويات** \> **أنواع الحاويات**.

-   لتعيين النسبة المئوية لاستخدام الحاوية، انقر فوق **إدارة المستودعات** \> **الإعداد** \> **الحاويات‏‎** \> **مجموعات الحاويات**، ثم أدخل قيمة في حقل **النسبة المئوية لاستخدام الحاوية‬**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]