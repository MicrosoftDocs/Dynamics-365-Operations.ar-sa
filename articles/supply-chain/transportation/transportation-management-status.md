---
title: حالات إدارة النقل
description: يوضح هذا الموضوع كيفيه إنشاء حاله نقل وتعيين هذه الحالة إلى حاله الناقل.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: fb0d98729046330037f96ab7e13a1bf897e35a1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233333"
---
# <a name="transportation-management-statuses"></a>حالات إدارة النقل

[!include [banner](../includes/banner.md)]

قم بإعداد أكواد السجل الرئيسي لحالات النقل لتفسير الأكواد المقدمة من شركات الشحن. يتيح لك ذلك امكانيه التكامل مع شركات الشحن لتقديم حاله. يمكن أن تساعدك حالة النقل التي تقدمها لرمز حالة رئيسية نقل على تعقب حالة التحميل أو شحن حاوية. يمكن تحديث حاله النقل الخاصة بالتحميل أو الشحن أو الحاوية فقط من خلال تكامل البيانات وليس يدويا من خلال واجهه المستخدم.

## <a name="create-a-transportation-status"></a>إنشاء حالة نقل

لإنشاء حال نقل، اتبع هذه الخطوات:

1. انتقل إلى **إدارة النقل \> إعداد \> السجلات الرئيسية لحالة النقل**.
1. حدد **جديد** لإنشاء السجل الرئيسي لحالة النقل.
1. في الحقل **السجل الرئيسي لحالة النقل**، أدخل كودًا فريدًا لحالة النقل.
1. في الحقل **نوع النقل**، حدد اما *شركه الشحن* أو *المركز* كنوع النقل.
1. ادخل الاسم وحاله النقل.
1. قم بإغلاق الصفحة.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>تعيين حاله النقل إلى حاله شركة النقل

لتعيين حاله النقل إلى حاله شركة النقل، اتبع الخطوات التالية:

1. انتقل إلى **إدارة النقل \> إعداد \> شركات النقل \> حالة النقل لشركة النقل**.
1. حدد **جديد** لتعيين رمز من شركة شحن إلى رمز حالة نقل رئيسية.
1. حدد معرف فريد لشركة الشحن وخدمة شركة النقل.
1. حدد رمز الحالة النقل التي تريد تعيينها إلى كود شركة الشحن المحددة.
1. أدخل الكود الخارجي المستخدمة بواسطة شركة الشحن.
1. قم بإغلاق الصفحة.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]