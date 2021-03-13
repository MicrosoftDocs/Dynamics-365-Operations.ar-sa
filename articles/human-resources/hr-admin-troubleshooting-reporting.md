---
title: خيارات إعداد التقارير
description: يتناول هذا المقال كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Microsoft Dynamics 365 Human Resources أو إنشاء تقارير جديدة.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111308"
---
# <a name="reporting-options"></a>خيارات إعداد التقارير

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**تفاصيل البيئة**

تنطبق هذه المشكلة على كافة البيئات.

**العَرَضْ**

يُريد العميل تخصيص تقارير Dynamics 365 Human Resources أو إنشاء تقارير جديدة.

**إصدار**

يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.

**الحل**

- يمكن الإبلاغ عن بيانات Human Resources التي تتدفق إلى Dataverse عبر موصل Power Apps Dataverse إلى Power BI Desktop. لاحظ أن Dataverse تحتوي على مجموعة فرعية من بيانات Human Resources. لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .
- يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Human Resources. يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.
- يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Human Resources من خلال تكامل Microsoft Office.

**حل طويل الأجل**

ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Dataverse.
