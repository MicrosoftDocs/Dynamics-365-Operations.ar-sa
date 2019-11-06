---
title: تعطيل القواعد في مدقق تناسق حركة البيع بالتجزئة
description: يصف هذا الموضوع وظيفة تعطيل قواعد مدقق تناسق حركة البيع بالتجزئة في Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586287"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>تعطيل القواعد في مدقق تناسق حركة البيع بالتجزئة 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

قد توجد سيناريوهات وعمليات فريدة لدى بائعي التجزئة. وبالتالي، لا تنطبق جميع القواعد المضمنة بشكل افتراضي في مدقق تناسق حركة البيع بالتجزئة على جميع بائعي التجزئة. ولاستيعاب الاختلافات، يقدم Microsoft Dynamics 365 Retail وظيفة يمكن استخدامها لتعطيل القواعد غير القابلة للتطبيق.

لعرض قائمة بالقواعد المتوفرة في مدقق تناسق حركة البيع بالتجزئة في بيئتك، وللاطلاع على حالة كل قاعدة، انتقل إلى **البيع بالتجزئة \> إعداد المراكز الرئيسية \> المعلمات \> معلمات البيع بالتجزئة‬**، وحدد علامة التبويب **التحقق من صحة الحركات‬**.

بشكل افتراضي، تكون حالة كل قاعدة معينة إلى **ممكّن**. وبالتالي، تُستخدم جميع القواعد للتحقق من صحة حركات البيع بالتجزئة قبل سحبها إلى كشوف حسابات البيع بالتجزئة. لتعطيل قاعدة، يمكنك تغيير حالتها إلى **معطّل**. لا تؤخذ القواعد المعطّلة في الاعتبار عندما يتم التحقق من صحة الحركات أثناء عملية حساب كشف الحساب.

لتجاوز عملية التحقق من الصحة بكاملها، بصرف النظر عما إذا كانت القواعد ممكّنة، انتقل إلى **البيع بالتجزئة \> إعداد المراكز الرئيسية \> المعلمات \> معلمات البيع بالتجزئة**، ثم على علامة التبويب **التحقق من صحة الحركات‬**، قم بتعيين الخيار **تعطيل مدقق التوافق لحركات البيع بالتجزئة‬** إلى **نعم**. بعد تعيين هذا الخيار إلى **لا**، لا يمكن إعادته إلى **لا** من واجهه المستخدم.
