---
title: إنشاء ملف تعريف الوظائف عبر الإنترنت
description: يوضح هذا الموضوع كيفية إنشاء ملف تعريف وظائف على الإنترنت في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969966"
---
# <a name="create-an-online-functionality-profile"></a>إنشاء ملف تعريف الوظائف عبر الإنترنت


[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظره عامه حول اعداد ملف تعريف الوظائف عبر الإنترنت لـ Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

يوفر ملف تعريف الوظائف عبر الإنترنت الإعدادات المتنوعة المستخدمة للقنوات عبر الإنترنت. يجب ان تحدد كل قناه عبر الإنترنت ملف تعريف وظائف عبر الإنترنت.

## <a name="create-an-online-functionality-profile"></a>إنشاء ملف تعريف الوظائف عبر الإنترنت

يوضح الاجراء التالي كيفيه إنشاء ملف تعريف وظائف عبر الإنترنت من داخل تطبيق Commerce Headquarters.

1. في جزء التنقل، انتقل إلى **الوحدات \>إعداد القناة \> إعداد متجر على الإنترنت \> ملفات تعريف الوظائف**.
1. في جزء الإجراءات، حدد **جديد**.
1. في **ملف التعريف**، أدخل معرفًا لملف التعريف.
1. في حقل **الوصف**، ادخل قيمه ("ملف تعريف أعمال المغامرة" في صورة المثال أدناه).
1. في قسم **الوظائف**، قم بتعديل إعدادات **السلة** أو **عملاء RETAIL** أو **السحب**، حسب الحاجة.
1. في جزء الإجراءات، حدد **حفظ**.

تعرض الصورة التالية مثالاً لملف تعريف الوظائف على الإنترنت.
  
![مثال لملف تعريف الوظائف على الإنترنت](media/online-functionality-profile.png)

## <a name="functions"></a>الوظائف

- **تجميع المنتجات**: عند التمكين ، تسمح هذه الوظيفة لسله التسوق بتحديث الكمية التي تتم فيها أضافه نفس الصنف عده مرات.
- **السماح بالسحب بدون مدفوعات**: عند التمكين ، تعالج هذه الدالة السيناريو عندما تكون الأصناف المضافة إلى السلة ذات سعر 0.00 دولار.
- **إنشاء عميل في الوضع الغير متزامن**: يعد هذا اعداد قديم ينطبق علي قنوات التجارة الكترونيه للجهة الخارجية ولا يمكن تطبيقه علي موقع التجارة الكترونيه لـ Dynamics 365.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على القنوات](channels-overview.md)

[المتطلبات الأساسية‬ لإعداد قناة](channels-prerequisites.md)

[إعداد قناة عبر الإنترنت](channel-setup-online.md)

[إعداد قناة بيع بالتجزئة](channel-setup-retail.md)

[إعداد قناة مركز اتصال](channel-setup-callcenter.md)
