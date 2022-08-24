---
title: إنشاء موفري التكوين ووضع علامة نشط عليهم
description: تشرح هذه المقالة كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين.
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267802"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>إنشاء موفري التكوين ووضع علامة نشط عليهم

[!include [banner](../../includes/banner.md)]

تشرح هذه المقالة كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية. ستشير كل تكوينات التقارير الإلكترونية إلى الموفر على أنه مالك التكوين. في هذا المثال، ستقوم بإنشاء موفر تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كموفري تكوينات ER المشتركة بين جميع الشركات.

## <a name="create-a-provider"></a>إنشاء موفر
1. انتقل إلى **جزء التنقل** في الزاوية العلوية اليسرى وحدد **إدارة المؤسسة**.
2. انتقل إلى **مساحات العمل > إعداد التقارير الإلكترونية**.
3. انتقل إلى **الارتباطات ذات الصلة > موفري التكوين**.
4. حدد **جديد**.
    - يكون سجل الموفر فريدًا من حيث الاسم وعنوان URL. راجع محتويات هذه الصفحة وتجاوز هذا الإجراء في حال وجود سجل خاص بشركة Litware, Inc. (https://www.litware.com) الموجود بالفعل.  
5. في حقل الاسم، اكتب`Litware, Inc.`.
6. في حقل عنوان الإنترنت، اكتب `https://www.litware.com`.
7. حدد **حفظ**.
8. قم بإغلاق الصفحة.

## <a name="select-as-an-active-provider"></a>تحديد الموفر كموفر نشط
1. حدد الموفر Litware, Inc. .
2. حدد **تعيين كنشط**.

![صفحة مساحة عمل إعداد التقارير الإلكترونية.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
