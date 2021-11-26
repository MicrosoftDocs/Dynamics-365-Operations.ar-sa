---
title: نقل ملفات NF-e XML كمرفقات
description: يشرح هذا الموضوع كيفية نقل ملفات NF-e XML من قاعدة بيانات Microsoft Dynamics 365 Finance أو Dynamics 365 Supply Chain Management أو جعلها متاحة كمرفقات بدلاً من ذلك..
author: gionoder
ms.date: 11/11/2021
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
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799439"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>نقل ملفات NF-e XML كمرفقات

[!include [banner](../includes/banner.md)] 


عند إصدار المستندات المالية الإلكترونية (NF-e)، يتم إنشاء ملفات XML وتخزينها في Microsoft Dynamics 365 Finance وقواعد بيانات Dynamics 365 Supply Chain Management. في الترجمة البرازيلية، يمكنك استخدام ميزة **نقل NF-e XML كمرفق** لتحرير مساحة قاعدة البيانات التي تستهلك ملفات XML تلك.

بالنسبة إلى نطاق تاريخ محدد وإنشاء مالي، تنقل الميزة ملفات NF-e XML من قاعدة بيانات Finance أو Supply Chain Management إلى مخزن Blob من اشتراك Azure. تجعل هذه الحركة الملفات متاحة كمرفقات فقط. بعد أن يتم نقل ملفات XML بنجاح إلى تخزين Blob، يتم حذف الملفات الأصلية من قاعدة البيانات Finance أو Supply Chain Management. لذلك، يتم تحرير مساحة قاعدة البيانات التي استخدمتها تلك الملفات.

اتبع هذه الخطوات لتمكين ميزة **نقل NF-e XML كمرفق**.

1. في Finance أو Supply Chain Management، افتح مساحة عمل **إدارة الميزات**.
2. في علامة التبويب **الكل**، ابحث عن وحدد ميزة **نقل NF-e XML كمرفق**.
3. حدد **تمكين الآن**.

اتبع هذه الخطوات لنقل ملفات NF-e XML كمرفقات.

1. انتقل إلى **الحسابات المدينة** \> **المستندات المالية** \> **المستندات المالية الإلكترونية** \> **نقل NF-e XML كمرفقات**.
2. في حقلي **من التاريخ** و **إلى التاريخ**، حدد تاريخي البدء والانتهاء.
3. في حقل **معرف المؤسسة المالية**، حدد قيمة.
4. حدد **موافق**.

> [!IMPORTANT]
> هذه العملية غير قابلة للعكس. بعد نقل ملفات NF-e XML، يمكن للمستخدمين عرضها فقط عن طريق تحديد **المرفقات** في الجزء العلوي من صفحة **المستند المالي**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
