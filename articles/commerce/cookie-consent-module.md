---
title: الوحدة النمطية للموافقة على ملف تعريف الارتباط
description: يتناول هذا الموضوع الوحدات النمطية للموافقة على ملف تعريف الارتباط ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 504232285267fb3663093a84a371e0040233ce23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993515"
---
# <a name="cookie-consent-module"></a>الوحدة النمطية للموافقة على ملف تعريف الارتباط

[!include [banner](includes/banner.md)]

يتناول هذا الموضوع الوحدات النمطية للموافقة على ملف تعريف الارتباط ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

تطالب الوحدة النمطية للموافقة على ملف تعريف الارتباط المستخدمين بتوفير موافقة صريحة على السماح بملفات تعريف الارتباط لأي ميزة أو وحدة نمطية تتعقب ملفات تعريف ارتباط المستعرض. تكون الموافقة مطلوبة في المرة الأولى التي يقوم فيها مستخدم موقع باستعراض موقع في جلسة عمل مستعرض جديدة. عند تلقي الموافقة، يتم تعقبها ولن تتم مطالبة مستخدم الموقع بإعطاء الموافقة مرة أخرى. لمزيد من المعلومات، راجع [التوافق مع ملف تعريف الارتباط](cookie-compliance.md).

إذا لم يتم استلام الموافقة على ملفات تعريف الارتباط من مستخدم الموقع، لن تظهر على الصفحة أي ميزات أو وحدات نمطية تتطلب الموافقة على ملفات تعريف الارتباط. على سبيل المثال، تتطلب الوحدة النمطية للسداد مع الخروج والوحدة النمطية للمشاركة الاجتماعية وميزة المتجر المفضل الموافقة على ملفات تعريف الارتباط ولن تظهر إذا لم يتم استلام موافقة مستخدم الموقع. 

يمكن تكوين الوحدة النمطية للموافقة على ملف تعريف الارتباط على جزء رأس الصفحة بحيث يمكن تنفيذها عند تحميل الصفحة. يجب أن تتضمن الوحدة النمطية للموافقة على ملف تعريف الارتباط رسالة واضحة تُعلم مستخدم الوقع عن استخدام ملفات تعريف الارتباط في الموقع ويجب أن توفر ارتباطًا غلى صفحة خصوصية الموقع.

يبين الرسم التوضيحي التالي مثالاً على رسالة الموافقة على ملفات تعريف الارتباط مع ارتباط إلى صفحة سياسة خصوصية الموقع يظهر على رأس صفحة الموقع.
![مثال عن وحدة نمطية للموافقة على ملف تعريف الارتباط](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>خصائص الوحدة النمطية للموافقة على ملف تعريف الارتباط

| اسم الخاصية             | قيمة                 | الوصف |
|---------------------------|-----------------------|-------------|
| نص منسق                  | نص منسق | تحديد اعلام نص منسق لمستخدمي الموقع يفيد بأن الموقع يستخدم ملفات تعريف ارتباط المستعرض وأنه يتعين على المستخدمين قبول استخدام ملفات تعريف الارتباط كي يعمل الموقع بشكل تام. |
| الارتباطات | URL | يمكن إضافة ارتباط واحد أو أكثر إلى صفحة خصوصية الموقع التي تصف أنواع ملفات تعريف الارتباط التي يتم تعقبها على الموقع. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>إضافة وحدة نمطية للموافقة على ملف تعريف الارتباط إلى صفحات الموقع

لإضافة وحدة نمطية للموافقة على ملف تعريف الارتباط لعدة صفحات في الموقع بكفاءة، يمكن إضافتها إلى جزء رأس الصفحة المشتركة. بعد إضافة جزء الرأس إلى جميع صفحات الموقع، سيظهر إعلام بالموافقة على ملفات تعريف الارتباط بشكل تلقائي في المرة الأولى التي ينتقل فيها المستخدم إلى أي صفحة في الموقع.

لمزيد من المعلومات حول أجزاء الرأس والوحدات النمطية، راجع [الوحدة النمطية للرأس](author-header-module.md).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول مكتبة الوحدات النمطية](starter-kit-overview.md)

[الوحدة النمطية للرؤوس](author-header-module.md) 

[توافق ملفات تعريف الارتباط](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]