---
title: تكوين أنشطة موازية في سير عمل
description: لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11b541c3e159b2c38e4dd2fa9f2ad08e4c1e4500
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176318"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>تكوين أنشطة موازية في سير عمل

[!include [banner](../includes/banner.md)]

لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.

يتكون النشاط الموازي من فروع سير العمل التي يتم تشغيلها في نفس الوقت.

## <a name="name-a-parallel-activity"></a>تسمية نشاط موازٍ

اتبع الخطوات التالية لإدخال اسم للنشاط الموازي.

1. انقر بالزر الأيمن فوق النشاط الموازي، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.
2. في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
3. في حقل **الاسم**، أدخل اسمًا فريدًا للنشاط الموازي.
4. انقر فوق **إغلاق**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>تكوين فروع النشاط الموازي

اتبع هذه الخطوات لإضافة وتكوين فروع هذا النشاط الموازي.

1. انقر نقرًا مزدوجًا فوق النشاط الموازي لعرض فروع النشاط الموازي.
2. لإضافة فرع، اسحب عنصر **الفرع** من ناحية **عناصر سير العمل** إلى نقطة إدراج على لوحة الرسم. يظهر الرسم التوضيحي التالي نقطة إدراج.

    ![نقطة الإدراج](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > ليس لترتيب الفروع أي أهمية لأن جميع فروع النشاط الموازي تعمل في الوقت نفسه.

3. لتكوين كل فرع، راجع [تكوين فرع موازٍ](configure-parallel-branch-workflow.md).