---
title: التبديل بين تصميمات المورّدين
description: يصف هذا الموضوع كيفية التبديل بين تكامل بيانات البائع وبين تطبيقات Finance and Operations و Common Data Service.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902715"
---
# <a name="switch-between-vendor-designs"></a>التبديل بين تصميمات المورّدين

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>تدفق بيانات المورّد 

إذا كنت تستخدم تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت عزل معلومات المورّد عن العملاء، فاستخدم تصميم المورّد الأساسي هذا.  

![تدفق المورد الأساسي](media/dual-write-vendor-data-flow.png)
 
إذا كنت تستخدم تطبيقات Dynamics 365 الأخرى لإدارة المورّدين، وأردت متابعة استخدام كيان **الحساب** لتخزين معلومات المورّدين، فاستخدم تصميم المورّد الموسع هذا. في هذا التصميم، يتم تخزين معلومات المورد الموسعة مثل حالة انتظار المورد وملف تعريف المورد في كيان **الموردين** في Common Data Service. 

![تدفق المورّد الموسّع](media/dual-write-vendor-detail.jpg)
 
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
    5. قم بتنشيط عمليات سير العمل التي قمت بإنشائها في كياني **الحساب** و **المورد** لبدء استخدام كيان **الحساب** لتخزين معلومات المورد. 
 
