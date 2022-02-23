---
title: التحقق من صحة الشهادة NF-e مخصصة
description: يوفر هذا الموضوع معلومات حول تمكين شهادة NF-e مخصصة واستخدامها.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439882"
---
# <a name="nf-e-custom-certificate-validation"></a>التحقق من صحة الشهادة NF-e مخصصة

[!include [banner](../includes/banner.md)]

عند تشغيل ميزه التحقق من صحة شهادة NF-e مخصصة، يسمح التحقق المخصص من الصحة بالاتصال بخدمات الويب. هذا الاتصال مطلوب لإرسال NF-e واستلام التخويل من SEFAZ.

يتم إصدار خاصيه **غرض مصادقه الخادم** من الشهادة V5 من قبل هيئه Brazilian Root Certificate Authority. يتم إيقاف تشغيل هذه الخاصية افتراضيا ويجب تمكينها يدويا. في بعض الحالات، يمكن لتحديث الشهادة التلقائي تبديل هذه الخاصية إلى لم يعد ممكنا. إذا حدث ذلك، فان اتصال TLS متأثر ولا يعد موثوقا به. وتتاثر القدرة علي إصدار NF-e في بيئات الإنتاج لولايات ميناس جريس (MG) وولايات بارانا (PR) أيضا.

يسمح هذا التحديث بحل بديل للتحقق من صحة الشهادة، مما يعني انه من الممكن تاسيس اتصال آمن.


