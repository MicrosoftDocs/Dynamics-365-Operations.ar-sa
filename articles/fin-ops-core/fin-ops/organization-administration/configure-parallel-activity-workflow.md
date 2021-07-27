---
title: تكوين أنشطة موازية في سير عمل
description: لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0bc97f401ad9e097248dfd5afb0baa8edbb6b3c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350660"
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

    ![نقطة الإدراج.](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > ليس لترتيب الفروع أي أهمية لأن جميع فروع النشاط الموازي تعمل في الوقت نفسه.

3. لتكوين كل فرع، راجع [تكوين أفرع موازية في سير عمل](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]