---
title: تحديث حالة كانبان
description: عندما يتم إفراغ كانبان عن طريق الخطأ أو يحتاج كانبان المستلم إلى الإفراغ، فإنك تحتاج إلى تحديث حالة كانبان.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831796"
---
# <a name="update-kanban-status"></a>تحديث حالة كانبان

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]