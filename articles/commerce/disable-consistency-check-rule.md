---
title: تعطيل القواعد في مدقق تناسق حركة البيع بالتجزئة
description: يصف هذا الموضوع وظيفة تعطيل قواعد مدقق تناسق الحركة في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 37209f1c1de19335f5f9fa6636ab55dd8b2fccc1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458376"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>تعطيل القواعد في مدقق تناسق حركة البيع بالتجزئة 

[!include [banner](../includes/banner.md)]

قد توجد سيناريوهات وعمليات فريدة لدى بائعي التجزئة. وبالتالي، لا تنطبق جميع القواعد المضمنة بشكل افتراضي في مدقق تناسق حركة التجارة على جميع بائعي التجزئة. ولاستيعاب الاختلافات، يقدم Microsoft Dynamics 365 Commerce وظيفة يمكن استخدامها لتعطيل القواعد غير القابلة للتطبيق.

لعرض قائمة بالقواعد المتوفرة في مدقق تناسق الحركة في بيئتك، وللاطلاع على حالة كل قاعدة، انتقل إلى **Retail and Commerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce**، وحدد علامة التبويب **التحقق من صحة الحركات‬**.

بشكل افتراضي، تكون حالة كل قاعدة معينة إلى **ممكّن**. وبالتالي، تُستخدم جميع القواعد للتحقق من صحة الحركات قبل سحبها إلى كشوف حسابات التجارة. لتعطيل قاعدة، يمكنك تغيير حالتها إلى **معطّل**. لا تؤخذ القواعد المعطّلة في الاعتبار عندما يتم التحقق من صحة الحركات أثناء عملية حساب كشف الحساب.

لتجاوز عملية التحقق من الصحة بكاملها، بصرف النظر عما إذا كانت القواعد ممكّنة، انتقل إلى **Retail and Commerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce**، ثم في علامة التبويب **التحقق من صحة الحركات‬**، قم بتعيين الخيار **تعطيل مدقق التوافق لحركات Commerce** إلى **نعم**. بعد تعيين هذا الخيار إلى **لا**، لا يمكن إعادته إلى **لا** من واجهه المستخدم.
