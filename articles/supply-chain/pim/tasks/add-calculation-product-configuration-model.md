--- 
title: "إضافة عملية حسابية إلى نموذج تكوين منتج"
description: "يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>إضافة عملية حسابية إلى نموذج تكوين منتج

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إضافة عملية حساب جديدة إلى نموذج تكوين منتج. ويُظهر كيف يمكنك إنشاء تعبير منطقي باستخدام العامل "لو" لتعيين ارتفاع مكبر الصوت إلى 10 لمكبرات الصوت البيضاء و15 لألوان الكابينات الأخرى. يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.


## <a name="add-a-calculation"></a>إضافة عملية حساب

## <a name="create-calculation-expression"></a>إنشاء عملية تعبير حساب
1. انقر فوق "تحرير التعبير".
2. في الحقل "ConstraintBody"، أدخل "If[CabinetFinish=="White", 10, 15]".
3. انقر فوق "التحقق من الصحة‬".
4. انقر فوق "إغلاق".
5. انقر فوق "موافق".


