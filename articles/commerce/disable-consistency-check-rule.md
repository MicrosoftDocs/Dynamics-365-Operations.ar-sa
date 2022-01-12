---
title: تعطيل القواعد المستخدمة في عملية التحقق من صحة الحركات
description: يصف هذا الموضوع وظيفة تعطيل قواعد التحقق من صحة الحركات في Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919515"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>تعطيل القواعد المستخدمة في عملية التحقق من صحة الحركات

[!include [banner](../includes/banner.md)]

قد توجد سيناريوهات وعمليات فريدة لدى بائعي التجزئة. وبالتالي، لا تنطبق جميع القواعد المضمنة في عملية التحقق من صحة حركات التجارة على جميع بائعي التجزئة. ولاستيعاب الاختلافات، يقدم Microsoft Dynamics 365 Commerce وظيفة يمكن استخدامها لتعطيل القواعد غير القابلة للتطبيق.

لعرض قائمة بالقواعد المتوفرة في عملية التحقق من صحة الحركات في بيئتك، ولمعرفة حالة كل قاعدة، انتقل إلى **Retail وCommerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce** وحدد علامة التبويب **التحقق من صحة الحركات**. يتم استخدام كافة القواعد الممكّنة للتحقق من صحة الحركات أثناء عملية **التحقق من صحة حركات المتجر‬** ويجب تمريرها للحركات المطلوب تجميعها وترحيلها في كشف حساب الحركات.

بشكل افتراضي، تكون حالة كل قاعدة معينة إلى **ممكّن**. وبالتالي، تُستخدم جميع القواعد للتحقق من صحة الحركات قبل إمكانية سحبها إلى كشوف حسابات حركات التجارة. لتعطيل قاعدة، يمكنك تغيير حالتها إلى **معطّل**. لا تؤخذ القواعد المعطّلة في الاعتبار عندما يتم التحقق من صحة الحركات أثناء عملية **التحقق من صحة حركات المتجر**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
