---
title: شحن أوامر من متجر آخر باستخدام ميزة إرسال شحنة
description: يصف هذا الموضوع ميزة إرسال شحنة.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 088f55e5605c99f69852b4d6811b5c5504f267a2
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019452"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>شحن أوامر من متجر آخر باستخدام ميزة إرسال شحنة

[!include [banner](includes/banner.md)]

باستخدام ميزة إرسال الشحنة في Retail، يمكن تقديم طلبات العملاء في متجر وشحنها من متجر العملاء.

فأوامر العميل في نقطة البيع (POS) تدعم العديد من خيارات التنفيذ. تتضمن بعض أمثلة خيارات التنفيذ ما يلي:

- الاستلام من المتجر نفسه بتاريخ مختلف.
- الاستلام من متجر آخر بنفس التاريخ أو بتاريخ مختلف.
- الشحن من مستودع الشحن الافتراضي المُعين للمتجر والتسليم في تاريخ محدد.

تستخدم ميزة إرسال الشحنة هذه عمليات نقاط البيع التالية: شحن جميع المنتجات وشحن المنتجات المحددة. يسمح هذا لموظف المتجر بتحديد موقع "الشحن من" الذي يمكن تلبية الأمر أو سطر الأمر منه. بشكل افتراضي، موقع "الشحن من" هو مستودع الشحن المقترن بالمتجر. ومع ذلك، يمكن لموظف المتجر تغيير هذا الموقع وتحديد أي متجر يكون محددًا في مجموعة محدد مواقع المتاجر المُعينة للمتجر.

وتبقى إمكانية تحديد عناوين "الشحن إلى" دون تغيير.

تستند طرق الشحن التي يمكن استخدامها لتنفيذ سطر الأمر إلى تكوين أوضاع التسليم الصالحة للمنتجات والعناوين. ونظرًا لأن القواعد الخاصة بأوضاع التسليم الصالحة يتم الاحتفاظ بها في إدارة البيع بالتجزئة فقط، يقوم عميل نقطة البيع باتصال في الوقت الفعلي لمعرفة أوضاع التسليم الصالحة لبند شحن.
