---
title: الضمانات على الأصول وأنواع الأصول
description: يشرح هذا الموضوع كيفية إعداد الضمانات على الأصول وأنواع الأصول في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874591"
---
# <a name="warranty-on-assets-and-asset-types"></a>الضمان على الأصول وأنواع الأصول

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


يشرح هذا الموضوع كيفية إعداد الضمانات على الأصول وأنواع الأصول في إدارة الأصول.

## <a name="set-up-a-warranty-on-an-asset-type"></a>إعداد ضمان على نوع أصل

1. حدد **إدارة الأصول** \> **الإعداد** \> **أنواع الأصول** \> **أنواع الأصول**.
2. في الجزء الأيمن، حدد نوع الأصل لإرفاق اتفاقية ضمان المورّد به، ثم حدد **الإعدادات الافتراضية لنوع الأصل**.
3. على علامة التبويب السريعة **عام**، في حقل **ضمان المورّد**، حدد الاتفاقية.

## <a name="set-up-a-warranty-on-an-asset"></a>إعداد ضمان على أصل

1. حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **كل الأصول‏‎**.
2. حدد الأصل، ثم حدد **تحرير**.
3. على علامة التبويب السريعة **المورّد** في قسم **ضمان المورّد**، في حقل **المورّد**، حدد اتفاقية الضمان.
4. في الحقلين **بدء الضمان** و**انتهاء الضمان**، حدد تاريخي البدء والانتهاء.

    > [!IMPORTANT]
    > إذا تم تحديد تاريخ في حقل **بدء الضمان** على أمر عملي، يصبح الضمان صالحًا لأمر العمل في ذلك التاريخ. عند إنشاء أمر عمل، يتم تعيين حقل **بدء الضمان** بشكل تلقائي إلى تاريخ الإنشاء. ومع ذلك، يمكنك تغيير التاريخ بحيث يتوافق مع تاريخ بدء اتفاقية الضمان، على سبيل المثال.
    >
    > ![الشكل 1](media/02-warranty.png)

> [!NOTE]
> إذا أنشأت أمر عمل لأصل يغطيه ضمان المورّد، وفي حال وجود تاريخ بدء متوقع لأمر العمل خلال فترة الضمان، ستتلقى إشعارًا حول اتفاقية الضمان. يمكنك عندئذٍ إلغاء أمر العمل، كما هو مطلوب.
