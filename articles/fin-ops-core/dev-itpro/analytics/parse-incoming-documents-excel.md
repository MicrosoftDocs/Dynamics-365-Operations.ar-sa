---
title: توزيع المستندات الواردة بتنسيق Excel
description: يوفر هذا الموضوع معلومات حول تصميم تنسيقات التقارير الإلكترونية لتحليل المعلومات التي تحتوي عليها ملفات Microsoft Excel الواردة.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 6e27806d3b94eb485705cec539a4849b81fbba91
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685777"
---
# <a name="parse-incoming-documents-in-excel-format"></a>توزيع المستندات الواردة في تنسيق  Excel

[!include[banner](../includes/banner.md)]

يمكنك تصميم تنسيقات التقارير الإلكترونية لتحليل ملفات Microsoft Excel الواردة التي تمثل البيانات في مصنفات Microsoft Excel (ملفات بتنسيق XLSX). يمكنك بعد ذلك استخدام المحتوى من هذه الملفات لتحديث بيانات التطبيق. ويكون هذا مفيدًا في حالة:

- تصميم نموذج جديد وتنسيق، واختبارهم في وقت التشغيل. في هذه الحالة، سوف يقوم Excel بمحاكاة بيانات التطبيق الفعلية.
- إدارة بيانات تتجاوز تطبيقك في Excel وتريد استيراد هذه البيانات لإرسال تقرير مُحدد.

لمزيد من المعلومات حول هذه الميزة، قم بتشغيل دلائل المهام **التقارير الإلكترونية - استيراد بيانات من ملف Microsoft Excel (الجزء 1: تصميم التنسيق)** و **التقارير الإلكترونية - استيراد بيانات من ملف Microsoft Excel (الجزء 2: استيراد البيانات)** (أجزاء من عملية الأعمال 7.5.4.3 اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول (10677)). تتناول دلائل المهام هذه كيف يمكن نشر ملف Excel وارد باستخدام تنسيق ER لاستيراد معلومات من المستندات الواردة وتحديث بيانات التطبيق. يمكنك تحميل ملفات دليل المهام من [مركز تحميل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).

قم بتنزيل الملفات التالية لإكمال دلائل المهام المذكورة أعلاه.

| وصف المحتوى                         | ملف                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| ملف وارد بتنسيق XLSX- قالب    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| ملف وارد بتنسيق XLSX- بيانات نموذجية | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

إذا لم تقم بتشغيل دليل المهام التالي، [التقارير الإلكترونية - إنشاء التكوينات المطلوبة لاستيراد البيانات من ملف خارجي‬](./tasks/er-required-configurations-import-data.md) في تطبيق Finance and Operations، قم بتنزيل الملف التالي.

| وصف المحتوى    | ملف                                                            |
|------------------------|-----------------------------------------------------------------|
| تكوين نموذج تقارير إلكترونية | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
