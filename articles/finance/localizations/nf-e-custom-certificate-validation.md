---
title: التحقق من صحة الشهادة NF-e مخصصة
description: يوفر هذا الموضوع معلومات حول تمكين شهادة NF-e مخصصة واستخدامها.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755581"
---
# <a name="nf-e-custom-certificate-validation"></a>التحقق من صحة الشهادة NF-e مخصصة

[!include [banner](../includes/banner.md)]

خاصية **غرض مصادقة الخادم** من الشهادات الصادرة من المرجع المصدق الجذر البرازيلي إيقاف افتراضيا ويجب تمكين يدويا. في بعض الحالات، يمكن لتحديث الشهادة التلقائي تبديل هذه الخاصية إلى لم يعد ممكنا. إذا حدث ذلك، فان اتصال TLS متأثر ولا يعد موثوقا به. وتتاثر القدرة علي نموذج المستند المالي الإلكتروني في البرازيل رقم 55 (NF-e) في بيئات التشغيل لولايات ميناس جريس (MG) وولايات بارانا (PR) أيضا.

لتمكين الإصلاح **للتحقق من صحة الشهادة المخصصة NF-e** ، انتقل إلى **إدارة الميزة**. تسمح هذه الميزة بحل بديل للتحقق من صحة شهادة V5 و V10 وتسمح باتصال موثوق به مع خدمات الويب ، وهو أمر مطلوب للإرسال الآمن ل NF-e واستلام التفويض من SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
