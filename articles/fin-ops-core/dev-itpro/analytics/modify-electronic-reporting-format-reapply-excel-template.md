---
title: تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel
description: توضح المقالة كيفية تعديل تنسيق التقارير الإلكترونية (ER) الذي يُستخدم لإنشاء مستندات الأعمال عن طريق إعادة تطبيق قالب Excel معدل.
author: NickSelin
ms.date: 05/18/2022
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
ms.openlocfilehash: 50b115448bc89bba7e9abeb8062d03d31a163b64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906720"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel

[!include [banner](../includes/banner.md)]

يتم استخدام أداة إعداد التقارير الإلكترونية (ER) لإنشاء مستندات الأعمال بتنسيق إلكتروني. لإنشاء مستند عمل، يجب إنشاء تنسيق ER، وبعد ذلك استخدم مصمم ER لتحديد تخطيط مستند الأعمال وتحديد البيانات التي يجب تضمينها به. يمكنك بعد ذلك تشغيل تنسيق ER لإنشاء مستند الأعمال.

يمكن استخدام أداة إعداد التقارير الإلكترونية لإنشاء مستندات أعمال كملفات Microsoft Excel. ويمكنك استخدام مستند Excel كقالب لهذه المستندات. لتحديد تخطيط المستند في مصمم ER، يمكنك استيراد محتويات مستند Excel الذي تريد استخدامه كقالب في تنسيق ER المحدد. لمزيد من التفاصيل، وممارسة هذا السيناريو، يمكنك تشغيل دليل المهمة **‬‏‫تصميم تكوين لإنشاء التقارير بتنسيق OPENXML في ER‬‏‫** (جزء من العملية التجارية ‬‏‫‬‏‫7.5.4.3 اكتساب/تطوير مكونات الخدمات/الحلول الخاصة بتقنية المعلومات (10677)). في خطوة دليل المهام حيث تقوم باستيراد قالب Excel، استخدم القالب الأولي لملف Excel الخاص بتقرير الدفع، [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

إذا قمت بتحرير المستند Excel الذي يتم استخدامه كقالب لمستند أعمال، تسمح لك وظيفة ER الجديدة بإعادة تطبيق القالب المحدث على تنسيق ER. يتم بعد ذلك تحديث تنسيق ER بحيث يلتزم بالقالب المحدث. للحصول على مزيد من التفاصيل حول هذه الوظيفة، قم بتشغيل دليل المهمة **تعديل تنسيق إعداد التقارير الإلكتروني من خلال إعادة تطبيق قالب Excel** (جزء من عملية الأعمال 7.5.5.3 اكتساب/تطوير مكونات خدمة تكنولوجيا المعلومات/الحلول(10683)). في خطوة دليل المهام حيث تقوم باستيراد نموذج محدث، استخدم القالب المعدل لملف Excel الخاص بتقرير الدفع، [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>الموارد الإضافية

[تحديث قالب](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
