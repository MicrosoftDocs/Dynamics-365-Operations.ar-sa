---
title: جعل محدد دليل الحسابات فريدًا
description: يشرح هذا الموضوع تعذر الحصول على المحدد نفسه لدليل الحسابات وقيم الأبعاد. يجب عليك تغيير قيم المحددات بعد الترقية.
author: panolte
ms.date: 03/30/2018
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
ms.openlocfilehash: 5887eb2fb6a5849058981b93b3ae39be3f75a5e6ae0a8da15170ecb81792553a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719808"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>جعل محدد دليل الحسابات فريدًا

[!include [banner](../includes/banner.md)]

في Microsoft Dynamics AX 2012، يمكنك استخدام المحدد نفسه لدليل الحسابات وقيم الأبعاد. في الإصدارات الحالية من Finance and Operations، لا يمكنك الحصول على المحدد نفسه لدليل الحسابات وقيم الأبعاد. في حالة وجود محدد مكرر، يمكنك تغييره بعد الترقية. 

هذه الميزة متاحة في الإصدارات التالية:
- الإصدار 8.0 من Finance and Operations
- Finance and Operations، الإصدار 7.1، KB 4094701 لا يمكن إدخال الأبعاد المالية عندما تحتوي قيم الأبعاد على محدد دليل الحسابات
- Finance and Operations الإصدار 7.2، KB 4092967 لا يمكن اختيار مشروع فرعي كالبُعد مثلاً عندما يحتوي تنسيق مشروع فرعي على محدد أبعاد

## <a name="update-delimiter"></a>تحديث المحدد
في حالة وجود تعارض في "دليل الحسابات"، يمكن تغيير محدد دليل الحسابات وتنسيق معرف المشروع/المشروع الفرعي. لا يمكن تغيير أي محددات أبعاد أخرى. 
- يمكنك تغيير محدد دليل الحسابات بعد الترقية في **محددات دفتر الأستاذ العام** > **دليل الحسابات والأبعاد** > **تغيير محدد**. 
- إذا كان التعارض فقط في تنسيق معرف المشروع/المشروع الفرعي، يمكنك تغيير هذه القيمة في **محددات المحاسبة وإدارة المشروع** > **عام** > **تعديل تنسيق المشروع الفرعي**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>كيفية تحديد ما إذا كانت البيئة الخاصة بك تتطلب محددات محدَّثة 
في حالة حدوث تعارض بين المحددات الموجودة في البيئة الخاصة بك التي تمت ترقيتها، تواجه عدم استقرار عند إدخال قيم في عنصر تحكم الإدخال المقسَّم أو عنصر تحكم إدخال الأبعاد. ويعني هذا أنك ستحتاج دائمًا إلى استخدام عمليات بحث أو قائمة منبثقة عند إدخال مجموعات الحسابات والأبعاد.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]