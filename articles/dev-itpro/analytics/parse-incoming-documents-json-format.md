---
title: توزيع المستندات الواردة بتنسيق JSON
description: يوضح هذا الموضوع كيفية إعداد تنسيقات التقارير الإلكترونية (ER) لتحليل المستندات الواردة بتنسيق JavaScript Object Notation (JSON).
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703911"
---
# <a name="parse-incoming-documents-in-json-format"></a>توزيع المستندات الواردة بتنسيق JSON

[!include[banner](../includes/banner.md)]

يمكنك تصميم تنسيقات التقارير الإلكترونية (ER) لتحليل المستندات الإلكترونية الواردة التي تمثل البيانات في تنسيق نص والتي تستند إلى JavaScript( بمعنى آخر، ملفات بتنسيق JavaScript Object Notation \[JSON\]).

لمعرفة المزيد حول هذه الميزة، نزِّل الملفات الموجودة في الجدول التالي، ثم شغل "‏‫التقارير الإلكترونية - إنشاء تكوين تنسيق" لإنشاء تكوين لاستيراد البيانات من دليل مهام ملف JSON خارجي. يوضح دليل المهام هذا كيف يمكن استخدام تنسيق ER لتحليل ملف JSON وارد لتحديث بيانات التطبيق.

| المسمى الوظيفي                                  | اسم الملف |
|----------------------------------------|-----------|
| تنسيق تكوين ER                | [تنسيق لاستيراد trans_JSON.xml للموردين](https://go.microsoft.com/fwlink/?linkid=874111) |
| نموذج ملف وارد بتنسيق .csv | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>متطلبات

قبل إكمال "التقارير الإلكترونية - إنشاء تكوين تنسيق" لاستيراد بيانات من دليل مهام ملف JSON خارجي، يجب استيفاء المتطلب التالي:

- يمكن أن تكون عناصر الأصل في ملف JSON عناصر الكائن فقط.
- يجب أن تكون العناصر المتداخلة لأحد الكائنات عناصر خصائص، بحيث يتم إنشاء بنية JSON صالحة.
- يمكن أن تكون صفائف JSON عناصر متداخلة فقط من عناصر خصائص لأحد الكائنات.
- يمكن أن تحتوي صفائف JSON علي كائنات JSON فقط. لا يمكن أن تحتوي علي صفائف متداخلة وقيم سلسلة/رقمية مباشرة. سيتم تحليل العناصر في هذه الصفائف بالترتيب، كما تم تحديدها في التنسيق. سيتم التعامل مع إعدادات التعدد في كل كائن JSON.

وبالإضافة إلى ذلك، يجب إكمال [التقارير الإلكترونية - إنشاء التكوينات المطلوبة لاستيراد بيانات من ملف خارجي لدليل مهام إعداد التقارير الإلكترونية](tasks/er-required-configurations-import-data.md) إذا لم تكن قد قمت بإكماله بالفعل. نزِّل الملف التالي لإكمال دليل المهام.

| المسمى الوظيفي                  | اسم الملف |
|------------------------|-----------|
| تكوين نموذج تقارير إلكترونية | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |