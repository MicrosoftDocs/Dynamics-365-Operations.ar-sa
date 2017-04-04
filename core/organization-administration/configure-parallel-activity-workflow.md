---
title: "تكوين نشاط مواز في سير عمل"
description: "لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>تكوين نشاط مواز في سير عمل

لتكوين نشاط موازٍ، أكمل الإجراءات التالية في محرر سير العمل.

يتكون النشاط الموازي من فروع سير العمل التي يتم تشغيلها في نفس الوقت.

## <a name="name-a-parallel-activity"></a>تسمية نشاط موازٍ
اتبع الخطوات التالية لإدخال اسم للنشاط الموازي.
1.  انقر بالزر الأيمن النشاط الموازي ومن ثم انقر فوق **خصائص** لفتح **خصائص** النموذج.
2.  في الجزء الأيمن، انقر فوق **الإعدادات الأساسية‬**.
3.  في حقل **الاسم**، أدخل اسمًا فريدًا للنشاط الموازي.
4.  انقر فوق **إغلاق**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>تكوين فروع النشاط الموازي
اتبع هذه الخطوات لإضافة وتكوين فروع هذا النشاط الموازي.
1.  انقر نقرًا مزدوجًا فوق النشاط الموازي لعرض فروع النشاط الموازي.
2.  لإضافة فرع، اسحب عنصر **الفرع** من ناحية **عناصر سير العمل** إلى نقطة إدراج على لوحة الرسم. يظهر الرسم التوضيحية التالي نقطة إدراج.![نقطة الإدراج](./media/workflow_insertionpoint.gif)
    | **ملاحظة **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | ليس لترتيب الفروع أي أهمية لأن جميع فروع النشاط الموازي تعمل في الوقت نفسه. |

3.  لتكوين كل فرع، راجع [تكوين فرع موازٍ](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).




