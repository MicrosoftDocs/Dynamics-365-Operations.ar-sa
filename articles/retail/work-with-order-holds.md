---
title: "تعليقات الأمر"
description: "يصف هذا الموضوع تعليقات الأوامر باستخدام Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a>تعليقات الأمر

[!INCLUDE [banner](includes/banner.md)]

يصف هذا الموضوع تعليقات الأوامر باستخدام Dynamics 365 for Retail.

يمكن وضع أمر قيد الانتظار لأسباب مختلفة. على سبيل المثال، قد تضع أمر قيد الانتظار حتى يمكن التحقق من أسلوب الدفع أو عنوان عميل أو حتى يقوم مدير بمراجعة حد الائتمان الخاص بالعميل. أثناء عملية المبيعات، هناك أوقات يجب عندها وضع أوامر المبيعات قيد الانتظار. على سبيل المثال، قد يتم وضع أمر المبيعات قيد الانتظار بسبب مشاكل في دفع عميل، بسبب احتيال مشكوك فيه أو لأنه يجب على المدير مراجعة الأمر. عندما يتم وضع أمر المبيعات قيد الانتظار، يتم تعيين رمز تعليق لأمر إلى أمر المبيعات للإشارة إلى سبب التعليق. يتم تكوين رموز تعليق أمر المبيعات في **المبيعات والتسويق** &gt; **الإعداد** &gt; **أوامر المبيعات** &gt; **رموز تعليقات الأمر**. ويمكن وضع أمر مبيعات قيد الانتظار يدوياً في وقت إنشاء الأمر أو لاحقًا. بالإضافة إلى ذلك، يمكن وضع أمر قيد الانتظار تلقائياً، وفقًا لقواعد الاحتيال. وأثناء وضع أمر مبيعات قيد الانتظار، قد تحتاج إلى تحديثه بمزيد من المعلومات. وبدلاً من ذلك، قد تحتاج إلى التحقق من أمر المبيعات عند مواصلة العمل فيه. ويمكنك سحب أمر مبيعات، وإدراجه مرة أخرى، وحتى تجاوز سحب مستخدم آخر باستخدام منضدة تعليق الأوامر (**البيع بالتجزئة** &gt; **العملاء‏‎** &gt; **تعليقات الأمر**). عندما يكون أمر ما جاهز للاكتمال، يجب إزالة الوضع قيد الانتظار قبل إتمام عملية الأمر.




