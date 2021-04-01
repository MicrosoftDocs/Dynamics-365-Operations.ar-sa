---
title: تكوين وتشغيل وظيفة لترحيل البيانات
description: يتناول هذا الإجراء تكوين الوظيفة الدفعية المتكررة وتشغيلها لترحيل كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1401d51491205731843abe6e2278f798c5c979
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232727"
---
# <a name="configure-and-run-job-to-post-statements"></a>تكوين وتشغيل وظيفة لترحيل البيانات

[!include [banner](../includes/banner.md)]

يتناول هذا الإجراء تكوين الوظيفة الدفعية المتكررة وتشغيلها لترحيل كشوف الحسابات لمتجر محدد أو مجموعة من المتاجر. ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.

1. انتقل إلى كل مساحات العمل > .. > ماليات المتاجر.
2. انقر فوق "ترحيل الكشوف على دُفعات".
    * حدد تدرجًا هرميًا تنظيميًا ثم في شجرة عُقد المؤسسة‬، حدد عقدة أو مخزنًا فرديًا. حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.  
    * انقر فوق السهم لإضافة التحديد الخاص بك.  
3. انقر فوق علامة التبويب "تشغيل في الخلفية". ![تشغيل في الخلفية](../dev-itpro/media/runbackground.png "تشغيل في الخلفية") 
4. حدد خانة الاختيار "معالجة الدُفعة" أو قم بإلغاء تحديدها.
![معالجة الدُفعات](../dev-itpro/media/batchprocessing.png "معالجة الدفعات والتكرار") 
5. انقر فوق "تكرار".
6. في الحقل "تاريخ البدء"، أدخل تاريخًا.
7. في حقل "‏‫وقت البدء"، أدخل الوقت.
    * اختر ما إذا أردت إنهاء التكرار بعد عدد معين من عمليات التشغيل، في تاريخ محدد، أو أبدًا. ثم اختر الخيارات المختلفة لتحديد عدد المرات التي تريد فيها تشغيل الوظيفة.  
8. انقر فوق موافق.
9. انقر فوق موافق.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]