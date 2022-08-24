---
title: التحقق من صحة الشهادة NF-e مخصصة
description: توفر هذه المقالة معلومات عن تمكين شهادة NF-e مخصصة واستخدامها.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288533"
---
# <a name="nf-e-custom-certificate-validation"></a>التحقق من صحة الشهادة NF-e مخصصة

[!include [banner](../includes/banner.md)]

خاصية **غرض مصادقة الخادم** من الشهادات الصادرة من المرجع المصدق الجذر البرازيلي إيقاف افتراضيا ويجب تمكين يدويا. في بعض الحالات، يمكن لتحديث الشهادة التلقائي تبديل هذه الخاصية إلى لم يعد ممكنا. إذا حدث ذلك، فان اتصال TLS متأثر ولا يعد موثوقا به. وتتاثر القدرة علي نموذج المستند المالي الإلكتروني في البرازيل رقم 55 (NF-e) في بيئات التشغيل لولايات ميناس جريس (MG) وولايات بارانا (PR) أيضا.

لتمكين الإصلاح **للتحقق من صحة الشهادة المخصصة NF-e** ، انتقل إلى **إدارة الميزة**. تسمح هذه الميزة بحل بديل للتحقق من صحة شهادة V5 و V10 وتسمح باتصال موثوق به مع خدمات الويب ، وهو أمر مطلوب للإرسال الآمن ل NF-e واستلام التفويض من SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
