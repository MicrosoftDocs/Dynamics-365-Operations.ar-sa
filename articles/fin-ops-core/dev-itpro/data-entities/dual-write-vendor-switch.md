---
title: التبديل بين تصميمات الموردين
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772354"
---
# <a name="switch-between-vendor-designs"></a>التبديل بين تصميمات الموردين

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>تدفق بيانات المورّد 

إذا كنت تستخدم تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت عزل معلومات المورّد عن العملاء، فاستخدم تصميم المورّد الأساسي هذا.  

![تدفق المورد الأساسي](media/dual-write-switch-1.png)
 
إذا كنت تستخدم تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت متابعة استخدام كيان **الحساب** لتخزين معلومات المورّدين، فاستخدم تصميم المورّد الموسع هذا. في هذا التصميم، يتم تخزين معلومات المورد الموسعة مثل حالة انتظار المورد وملف تعريف المورد في كيان **الموردين** في Common Data Service. 

![تدفق المورّد الموسّع](media/dual-write-switch-2.png)
 
اتبع الخطوات المذكورة أدناه لاستخدام تصميم المورد الموسع: 
 
1. تحتوي حزمة حل **SupplyChainCommon** على قوالب عملية سير العمل كما هو موضح في الصورة التالية.
    > [!div class="mx-imgBorder"]
    > ![قوالب عمليات سير العمل](media/dual-write-switch-3.png)
2. أنشئ عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل: 
    1. أنشئ عملية سير عمل جديدة لكيان **المورد** باستخدام قالب عملية سير عمل **إنشاء الموردين في كيان الحساب** وانقر فوق **موافق**. يعالج سير العمل هذا سيناريو إنشاء المورد لكيان **الحساب**.
        > [!div class="mx-imgBorder"]
        > ![إنشاء موردين في كيان الحساب](media/dual-write-switch-4.png)
    2. أنشئ عملية سير عمل جديدة لكيان **المورد** باستخدام قالب عملية سير عمل **تحديث كيان الحسابات** وانقر فوق **موافق**. يعالج سير العمل هذا سيناريو تحديث المورد لكيان **الحساب**. 
        > [!div class="mx-imgBorder"]
        > ![تحديث كيان الحسابات](media/dual-write-switch-5.png)
    3. أنشئ عمليات سير عمل جديدة من القوالب التي تم إنشاؤها في كيان **الحسابات**. 
        > [!div class="mx-imgBorder"]
        > ![إنشاء موردين في كيان الموردين](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![تحديث كيان الموردين](media/dual-write-switch-7.png)
    4. يمكنك تكوين مهام سير العمل بمثابه الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك. 
        > [!div class="mx-imgBorder"]
        > ![التحويل إلى سير عمل في الخلفية](media/dual-write-switch-8.png)
    5. قم بتنشيط مهام سير العمل التي قمت بإنشائها في كياني **الحساب** و**المورد** لبدء استخدام كيان **الحساب** في Customer Engagement لتخزين معلومات المورد. 
 
