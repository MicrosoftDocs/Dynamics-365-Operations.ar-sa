---
title: جعل محدد دليل الحسابات فريدًا
description: يشرح هذا الموضوع تعذر الحصول على المحدد نفسه لدليل الحسابات وقيم الأبعاد. يجب عليك تغيير قيم المحددات بعد الترقية.
author: panolte
ms.date: 09/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: a19dc8926df0efeac242e2e42ac37fdad91df9f8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500493"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>جعل محدد دليل الحسابات فريدًا

[!include [banner](../includes/banner.md)]

في Microsoft Dynamics AX 2012، يمكنك استخدام المحدد نفسه لدليل الحسابات وقيم الأبعاد. في الإصدارات الحالية من Finance and Operations، لا يمكنك الحصول على المحدد نفسه لدليل الحسابات وقيم الأبعاد. في حالة وجود محدد مكرر، يمكنك تغييره بعد الترقية. 

## <a name="update-delimiter"></a>تحديث المحدد
في حالة وجود تعارض في "دليل الحسابات"، يمكن تغيير محدد دليل الحسابات وتنسيق معرف المشروع/المشروع الفرعي. لا يمكن تغيير أي محددات أبعاد أخرى. 
- يمكنك تغيير محدد دليل الحسابات بعد الترقية في **محددات دفتر الأستاذ العام** > **دليل الحسابات والأبعاد** > **تغيير محدد**. 
- إذا كان التعارض فقط في تنسيق معرف المشروع/المشروع الفرعي، يمكنك تغيير هذه القيمة في **محددات المحاسبة وإدارة المشروع** > **عام** > **تعديل تنسيق المشروع الفرعي**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>كيفية تحديد ما إذا كانت البيئة الخاصة بك تتطلب محددات محدَّثة 
في حالة حدوث تعارض بين المحددات الموجودة في البيئة الخاصة بك التي تمت ترقيتها، تواجه عدم استقرار عند إدخال قيم في عنصر تحكم الإدخال المقسَّم أو عنصر تحكم إدخال الأبعاد. ويعني هذا أنك ستحتاج دائمًا إلى استخدام عمليات بحث أو قائمة منبثقة عند إدخال مجموعات الحسابات والأبعاد.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
