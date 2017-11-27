---
title: "تكوين نشاط موازٍ في سير عمل"
description: "لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a913655b584aa23c2614903e6ede4f5826fec1fb
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>تكوين نشاط موازٍ في سير عمل

[!include[banner](../includes/banner.md)]


لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.

يتكون النشاط الموازي من فروع سير العمل التي يتم تشغيلها في نفس الوقت.

## <a name="name-a-parallel-activity"></a>تسمية نشاط موازٍ
اتبع الخطوات التالية لإدخال اسم للنشاط الموازي.
1.  انقر بالزر الأيمن فوق النشاط الموازي، ثم انقر فوق **خصائص** لفتح النموذج **خصائص**.
2.  في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
3.  في حقل **الاسم**، أدخل اسمًا فريدًا للنشاط الموازي.
4.  انقر فوق **إغلاق**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>تكوين فروع النشاط الموازي
اتبع هذه الخطوات لإضافة وتكوين فروع هذا النشاط الموازي.
1.  انقر نقرًا مزدوجًا فوق النشاط الموازي لعرض فروع النشاط الموازي.
2.  لإضافة فرع، اسحب عنصر **الفرع** من ناحية **عناصر سير العمل** إلى نقطة إدراج على لوحة الرسم. يظهر الرسم التوضيحية التالي نقطة إدراج.![نقطة الإدراج](./media/workflow_insertionpoint.gif)
    | **ملاحظة**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | ليس لترتيب الفروع أي أهمية لأن جميع فروع النشاط الموازي تعمل في الوقت نفسه. |

3.  لتكوين كل فرع، راجع [تكوين فرع موازٍ](configure-parallel-branch-workflow.md).






