---
title: خيارات إعداد التقارير في Talent
description: يتناول هذا الموضوع كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Dynamics 365 Talent أو إنشاء تقارير جديدة.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897938"
---
# <a name="reporting-options-in-talent"></a>خيارات إعداد التقارير في Talent

**تفاصيل البيئة**

تنطبق هذه المشكلة على كافة البيئات.

**العَرَضْ**

يُريد العميل تخصيص تقارير Dynamics 365 Talent أو إنشاء تقارير جديدة.

**إصدار**

يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.

**الحل**

- يمكن الإبلاغ عن بيانات Core HR التي تتدفق إلى Common Data Service عبر موصل Power AppsCommon Data Service إلى Power BI Desktop. لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Core HR. لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير Power BI ولوحات معلومات Power Apps باستخدام Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) .
- يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Talent. يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.
- يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Talent من خلال تكامل Microsoft Office.

**حل طويل الأجل**

ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.
