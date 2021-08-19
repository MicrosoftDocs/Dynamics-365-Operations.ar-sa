---
title: حفظ دلائل المهام في LCS وإعادة تشغيلها
description: يتناول هذا المقال كيفية حفظ أدلة المهام إلى Microsoft Dynamics Lifecycle Services (LCS) ثم إعادة تشغيلها.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8cf6338e17c9d4f0f50e5c36291ce4f81800f76951e873f2e0cf435cc3cc97e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713068"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>حفظ دلائل المهام في LCS وإعادة تشغيلها

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**تفاصيل البيئة** 

Microsoft Dynamics 365 Human Resources، الذي تم نشره عبر Microsoft Dynamics Lifecycle Services (LCS)

**إصدار**

يرغب العميل في حفظ تسجيلات مهام جديدة لمشروع LCS، ثم يُعيد تشغيل أدلة المهام المحفوظة.

**الدقة**

اتبع هذه الخطوات لحفظ تسجل المهام إلى LCS.

1. تسجيل الدخول إلى LCS، وتحديد المشروع.
2. حدد تجانب **أداة تكوين عمليات الأعمال**.
3. عرض الصفحة في "تجربة عارض العمليات التجارية (BPM) المُحدّثة."
4. حدد مكتبة، ثم حدد **نسخ**.
5. أدخل اسمًا لنموذج أداة تكوين عمليات الأعمال (BPM).
6. تسجيل الدخول إلى Human Resources من LCS.
7. في حقل **بحث**، أدخل **تعليمات**. تم فتح تعليمات Lifecycle Services.
8. حدد زر **تحديث** لتكوين تعليمات Lifecycle Services.

    يجب أن تظهر مكتبة عارض العمليات التجارية (BPM) الخاص بك، ويجب أن يكون نشطًا.

9. قم بإغلاق الصفحة.
10. إنشاء تسجيل مهام.
11. عند الانتهاء، حدد **حفظ إلى Lifecycle Services**.

    ![حفظ إلى Lifecycle Services.](media/task-guides.png)

12. حدد مكتبة عارض العمليات التجارية (BPM) وعقدة لحفظ تسجيل المهمة للعقدة.

اتبع هذه الخطوات لإعادة تشغيل دليل المهام من LCS.

1. بدء مسجل المهام.
2. حدد **فتح من LCS**.
3. حدد المكتبة وعقدة عارض العمليات التجارية التي تحتوي على دليل مهام محفوظ.
4. فتح دليل المهام.


[!INCLUDE[footer-include](../includes/footer-banner.md)]