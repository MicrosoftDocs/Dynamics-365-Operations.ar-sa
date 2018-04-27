---
title: "يجب أن يكون محدد دليل الحسابات فريدًا"
description: "في Dynamics 365 for Finance and Operations، لا يمكنك الحصول على نفس المحدد لدليل الحسابات وقيم الأبعاد. يجب عليك تغيير قيم المحددات بعد الترقية."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a>يجب أن يكون محدد دليل الحسابات فريدًا

[!INCLUDE [banner](../includes/banner.md)]

في Microsoft Dynamics AX 2012، يمكنك استخدام نفس المحدد لدليل الحسابات وقيم الأبعاد. في Dynamics 365 for Finance and Operations، لا يمكنك الحصول على نفس المحدد لدليل الحسابات وقيم الأبعاد. في حالة وجود محدد مكرر، يمكنك تغييره بعد الترقية. 

تتوفر هذه الميزة في:
- Dynamics 365 for Finance and Operations، الإصدار 8.0
- في Dynamics 365 for Finance and Operations الإصدار 7.1، لا يمكن لقاعدة المعارف KB 4094701 إدخال الأبعاد المالية عندما تحتوي قيم الأبعاد على محدد دليل الحسابات
- في Dynamics 365 for Finance and Operations الإصدار 7.2، لا يمكن لقاعدة المعارف 4092967 اختيار مشروع فرعي مثل بُعد عندما يحتوي تنسيق مشروع فرعي على محدد أبعاد

## <a name="update-delimiter"></a>تحديث المحدد
في حالة وجود تعارض في "دليل الحسابات"، يمكن تغيير محدد دليل الحسابات وتنسيق معرف المشروع/المشروع الفرعي. لا يمكن تغيير أي محددات أبعاد أخرى. 
- يمكنك تغيير محدد دليل الحسابات بعد الترقية إلى Finance and Operations في **محددات دفتر الأستاذ العام** > **دليل الحسابات والأبعاد** > **تغيير محدد**. 
- إذا كان التعارض فقط في تنسيق معرف المشروع/المشروع الفرعي، يمكنك تغيير هذه القيمة في **محددات المحاسبة وإدارة المشروع** > **عام** > **تعديل تنسيق المشروع الفرعي**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>كيفية تحديد ما إذا كانت البيئة الخاصة بك تتطلب محددات محدَّثة 
في حالة حدوث تعارض بين المحددات الموجودة في البيئة الخاصة بك التي تمت ترقيتها، تواجه عدم استقرار عند إدخال قيم في عنصر تحكم الإدخال المقسَّم أو عنصر تحكم إدخال الأبعاد. ويعني هذا أنك ستحتاج دائمًا إلى استخدام عمليات بحث أو قائمة منبثقة عند إدخال مجموعات الحسابات والأبعاد.

