---
title: تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel
description: يصف الموضوع كيفية تعديل تنسيق التقارير الإلكترونية (ER) الذي يستخدم لإنشاء مستندات الأعمال عن طريق إعادة تطبيق قالب Excel معدل.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f28760f42d16b6ffcd301f121e583542bce0fac0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559280"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel

[!include [banner](../includes/banner.md)]

يتم استخدام أداة إعداد التقارير الإلكترونية (ER) لإنشاء مستندات الأعمال بتنسيق إلكتروني. لإنشاء مستند عمل، يجب إنشاء تنسيق ER، وبعد ذلك استخدم مصمم ER لتحديد تخطيط مستند الأعمال وتحديد البيانات التي يجب تضمينها به. يمكنك بعد ذلك تشغيل تنسيق ER لإنشاء مستند الأعمال.

يمكن استخدام أداة إعداد التقارير الإلكترونية لإنشاء مستندات أعمال كملفات Microsoft Excel. ويمكنك استخدام مستند Excel كقالب لهذه المستندات. لتحديد تخطيط المستند في مصمم ER، يمكنك استيراد محتويات مستند Excel الذي تريد استخدامه كقالب في تنسيق ER المحدد. لمزيد من التفاصيل، وممارسة هذا السيناريو، يمكنك تشغيل دليل المهمة **‬‏‫تصميم تكوين لإنشاء التقارير بتنسيق OPENXML في ER‬‏‫** (جزء من العملية التجارية ‬‏‫‬‏‫7.5.4.3 اكتساب/تطوير مكونات الخدمات/الحلول الخاصة بتقنية المعلومات (10677)).

إذا قمت بتحرير المستند Excel الذي يتم استخدامه كقالب لمستند أعمال، تسمح لك وظيفة ER الجديدة بإعادة تطبيق القالب المحدث على تنسيق ER. يتم بعد ذلك تحديث تنسيق ER بحيث يلتزم بالقالب المحدث. للحصول على مزيد من التفاصيل حول هذه الوظيفة، قم بتشغيل دليل المهمة **تعديل تنسيق إعداد التقارير الإلكتروني من خلال إعادة تطبيق قالب Excel** (جزء من عملية الأعمال 7.5.5.3 اكتساب/تطوير مكونات خدمة تكنولوجيا المعلومات/الحلول(10683)). في خطوة دليل المهمة حيث تقوم باستيراد قالب تم تحديثه، استخدم القالب المعدل لملف Excel تقرير الدفع، SampleVendPaymWsReport2، كقالب.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]