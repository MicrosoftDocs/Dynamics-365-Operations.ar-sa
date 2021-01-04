---
title: إنشاء موفري التكوين ووضع علامة نشط عليهم
description: يشرح هذا الموضوع كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fb9f5be8571974237154ea704c93b8666c539a7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681987"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>إنشاء موفري التكوين ووضع علامة نشط عليهم

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية. ستشير كل تكوينات التقارير الإلكترونية إلى الموفر على أنه مالك التكوين. في هذا المثال، ستقوم بإنشاء موفر تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كموفري تكوينات ER المشتركة بين جميع الشركات.

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

![صفحة مساحة عمل إعداد التقارير الإلكترونية](../media/GER-Task-ActiveProvider-1.png)
