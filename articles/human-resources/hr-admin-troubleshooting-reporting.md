---
title: خيارات إعداد التقارير
description: يتناول هذا المقال كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Microsoft Dynamics 365 Human Resources أو إنشاء تقارير جديدة.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431005"
---
# <a name="reporting-options"></a>خيارات إعداد التقارير

**تفاصيل البيئة**

تنطبق هذه المشكلة على كافة البيئات.

**العَرَضْ**

يُريد العميل تخصيص تقارير Dynamics 365 Human Resources أو إنشاء تقارير جديدة.

**إصدار**

يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.

**الحل**

- يمكن الإبلاغ عن بيانات Human Resources التي تتدفق إلى Common Data Service عبر موصل Power Apps Common Data Service إلى Power BI Desktop. لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Human Resources. لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .
- يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Human Resources. يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.
- يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Human Resources من خلال تكامل Microsoft Office.

**حل طويل الأجل**

ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.
