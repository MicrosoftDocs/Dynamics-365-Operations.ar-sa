---
title: جدولة أمر العمل في تاريخ ووقت محددين
description: يوضح هذا الموضوع كيفية جدولة أمر عمل في تاريخ ووقت محددين في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f818c4c3b669cc94e37cba1e3571c57b5c0dd1b
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887355"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>جدولة أمر العمل في تاريخ ووقت محددين

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

إذا كان من الضروري جدولة أحد أوامر العمل في تاريخ‏‎ *و*وقت محددين، فيمكنك تجاوز عمليه الجدولة القياسية في إدارة الأصول وإنشاء جدول معين لأمر العمل.

1. انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.

2. في قائمة أمر العمل، انقر فوق معرف أمر العمل في عمود **أمر العمل**.

3. انقر فوق **تحرير**.

4. على علامة التبويب السريعة **رأس أمر العمل**، أدخل تواريخ وأوقات البدء والانتهاء في الحقلين **البدء المتوقع** و**الانتهاء المتوقع**.

![الشكل 1](media/05-work-order-scheduling.png)

5. على علامة التبويب السريعة **عام**، انقر فوق **جدول** لاستخدام عملية الجدولة القياسية، أو انقر فوق **إرسال** لجدولة أمر العمل إلى عامل معين.

6. من أجل تجاوز حجوزات القدرة الإنتاجية الحالية لضمان جدولة أمر العمل في الفترة المتوقعة، قم بإجراء التحديدات كما هو موضح في الشكل أدناه في مربع الحوار **جدولة أمر العمل** > القسم **قدرة محدودة‬**. وهذا يعني أن عملية الجدولة ستتجاهل حجوزات القدرة الإنتاجية الحالية نظرًا لضرورة بدء أمر العمل في وقت البدء المتوقع.

![الشكل 2](media/06-work-order-scheduling.png)

7. انقر فوق **موافق** لبدء الجدولة.

8. إذا أدت عملية الجدولة إلى الحصول على حجوزات مزدوجة، فسترى رسالة على الشاشة، ويمكنك ضبط أوامر العمل ذات الصلة.

>[!NOTE]
>من أجل جدولة عامل صيانة لأمر العمل، يجب أن يكون عامل الصاينة هذا متوفرًا في وقت وتاريخ البدء المتوقعين. يتم إعداد توافر العاملين في [تقويم العمل](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 
