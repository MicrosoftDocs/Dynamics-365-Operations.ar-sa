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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240569"
---
# <a name="nf-e-custom-certificate-validation"></a>التحقق من صحة الشهادة NF-e مخصصة

[!include [banner](../includes/banner.md)]

عند تشغيل ميزه التحقق من صحة شهادة NF-e مخصصة، يسمح التحقق المخصص من الصحة بالاتصال بخدمات الويب. هذا الاتصال مطلوب لإرسال NF-e واستلام التخويل من SEFAZ.

يتم إصدار خاصيه **غرض مصادقه الخادم** من الشهادة V5 من قبل هيئه Brazilian Root Certificate Authority. يتم إيقاف تشغيل هذه الخاصية افتراضيا ويجب تمكينها يدويا. في بعض الحالات، يمكن لتحديث الشهادة التلقائي تبديل هذه الخاصية إلى لم يعد ممكنا. إذا حدث ذلك، فان اتصال TLS متأثر ولا يعد موثوقا به. وتتاثر القدرة علي إصدار NF-e في بيئات الإنتاج لولايات ميناس جريس (MG) وولايات بارانا (PR) أيضا.

يسمح هذا التحديث بحل بديل للتحقق من صحة الشهادة، مما يعني انه من الممكن تاسيس اتصال آمن.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]