---
title: "توزيع المستندات الواردة في Microsoft Excel"
description: "يوفر هذا الموضوع معلومات حول تنسيقات تصميم إعداد التقارير الإلكترونية (ER) لتوزيع المعلومات الواردة في ملفات Microsoft Excel الواردة."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a>توزيع مستندات Microsoft Excel الواردة

[!include[banner](../includes/banner.md)]

يمكنك تصميم الإلكتروني تقارير تنسيقات إعداد التقارير الإلكترونية (ER) Excel لتوزيع ملفات Microsoft Excel الواردة التي تمثل البيانات في مصنفات Microsoft Excel (الملفات بتنسيق XLSX). يمكنك بعد ذلك استخدام المحتوى من هذه الملفات لتحديث بيانات التطبيق. ويكون هذا مفيدًا في حالة:

-   تصميم نموذج جديد وتنسيق، واختبارهم في وقت التشغيل. في هذه الحالة، سوف يقوم Excel بمحاكاة بيانات التطبيق الفعلية.
-   إدارة بيانات تتجاوز تطبيقك في Excel وتريد استيراد هذه البيانات لإرسال تقرير مُحدد.

لمزيد من المعلومات حول هذه الميزة، قم بتشغيل دليل المهام **استيراد بيانات ER من ملف Microsoft Excel (الجزء الأول: تصميم التنسيق)** و **استيراد بيانات ER من ملف Microsoft Excel (الجزء 2: استيراد البيانات)** (الأجزاء من 7.5.4.3 الحصول على/تطوير مكونات خدمة/حل تكنولوجيا المعلومات (10677) العملية التجارية). تتناول دلائل المهام هذه كيف يمكن نشر ملف Excel وارد باستخدام تنسيق ER لاستيراد معلومات من المستندات الواردة وتحديث بيانات التطبيق. يمكنك تحميل ملفات دليل المهام من [مركز تحميل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).

قم بتنزيل الملفات التالية لإكمال دلائل المهام المذكورة أعلاه.

| وصف المحتوى                        | ملف                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| ملف وارد بتنسيق XLSX- قالب   | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)  |
| ملف وارد بتنسيق XLSX- بيانات نموذجية| [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

إذا لم تقم بتشغيل دليل المهام التالي بعد، [‏‫التقارير الإلكترونية - إنشاء التكوينات المطلوبة لاستيراد البيانات من ملف خارجي‬](./tasks/er-required-configurations-import-data.md) في تطبيق Dynamics 365 for Finance and Operation الحالي، قم بتنزيل الملف التالي.

| وصف المحتوى                        | ملف                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| تكوين نموذج تقارير إلكترونية                     | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266)            |


