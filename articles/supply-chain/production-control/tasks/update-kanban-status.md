---
title: تحديث حالة كانبان
description: عندما يتم إفراغ كانبان عن طريق الخطأ أو يحتاج كانبان المستلم إلى الإفراغ، فإنك تحتاج إلى تحديث حالة كانبان.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d069414829518c8c952a0e7a74cd0ae4f24c450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "346262"
---
# <a name="update-kanban-status"></a>تحديث حالة كانبان

[!include [task guide banner](../../includes/task-guide-banner.md)]

عندما يتم إفراغ كانبان عن طريق الخطأ أو يحتاج كانبان المستلم إلى الإفراغ، فإنك تحتاج إلى تحديث حالة كانبان. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص لمشرف المتجر.


## <a name="find-the-kanban"></a>قم بإيجاد الكانبان.
1. انتقل إلى التحكم بالإنتاج > كانبان > عمليات كانبان.
2. افتح عامل تصفية عمود وحدة معالجة المواد.
3. انقر فوق "مسح".
    * هذا يعيد تعيين عوامل التصفية.  
4. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية بالحقل "رقم البطاقة" باستخدام القيمة "000149".

## <a name="change-emptied-status-to-received-status"></a>تغيير حالة "مفرغة" إلى حالة "مستلمة"
1. انقر فوق "عكس وحدة معالجة مواد فارغة".
2. انقر فوق "موافق".
    * لاحظ أن حالة وحدة معالجة المواد هي "مستلم".  

## <a name="change-received-status-to-emptied-status"></a>تغيير حالة "مستلمة" إلى حالة "مفرغة"
1. انقر فوق "كانبان فارغة".
2. في القائمة، قم بوضع علامة للصف المحدد.
    * لاحظ أن حالة وحدة معالجة المواد هي "مفرغ".  

